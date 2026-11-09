# AGENTS.md

## Mục tiêu

Dự án cần luôn hướng tới giao diện hiện đại, sáng, cân đối và sản phẩm-ready. Khi xây dựng hoặc chỉnh sửa UI, hãy kết hợp các nguyên tắc làm việc nghiêm ngặt từ `impeccable` và triết lý thiết kế hệ thống từ `ui-ux-pro-max-skill`:

- Tập trung vào trải nghiệm người dùng thật sự tốt.
- Ưu tiên sự rõ ràng, dễ đọc, dễ dùng, và khả năng mở rộng.
- Không tạo ra các mockup "AI slop" quá lố, quá rối, hoặc thiếu nhịp điệu.
- Luôn giữ phong cách hiện đại nhưng không lỗi thời.

## 1) Design System & Styling

### Chế độ màu

- Dùng Light Theme làm chuẩn, ưu tiên nền sáng và không quá tối.
- Sử dụng palette trung tính và dịu: trắng, xám nhạt, slate, pastel blue/green/amber.
- Tránh nền quá tối, màu quá gắt, gradient phẳng và nhợt nhạt không có mục đích.
- Nếu cần accent, hãy dùng màu tinh tế và có độ tương phản hợp lý.

### Tailwind / HTML5

- Dùng HTML5 semantic elements (`header`, `main`, `section`, `article`, `nav`, `footer`, `button`, `form`, `label`...)
- Dùng Tailwind CSS làm phương pháp styling chính.
- Ưu tiên class rõ ràng, gọn, không dư thừa.
- Giữ code dễ đọc, có cấu trúc rõ, không lạm dụng class dài vô nghĩa.

### Card, border và shadow

- Dùng `border-slate-100` làm viền thẻ siêu mảnh, rất nhẹ và tinh tế.
- Dùng `bg-white/80`, `backdrop-blur-sm` hoặc `backdrop-blur-xl` cho layer glass nhẹ nhưng không quá mờ.
- Soft shadows phải dịu, có chiều sâu vừa phải: `shadow-sm`, `shadow-[0_10px_30px_rgba(15,23,42,0.06)]`, hoặc tương đương.
- Không dùng shadow quá đậm, shadow quá màu, hoặc box-shadow quá mạnh làm phá nhịp.
- Tất cả card, panel, modal, dropdown nên có border và nền trung tính để giữ kiểu đồng bộ.

### Typography & spacing

- Ưu tiên hierarchy rõ ràng: heading lớn, body vừa, label nhỏ và có độ chênh rõ.
- Dùng spacing theo hệ thống hợp lý, tránh khoảng cách vô lý hoặc thô.
- Không để khoảng cách bị thiếu cân đối giữa các block, section hoặc component.
- Đảm bảo text và UI element luôn tạo cảm giác “thở” mà không rỗng.

## 2) Layout Structure

### Bento Grid

- Dùng Bento Grid làm cấu trúc chính cho dashboard, landing page và các section dữ liệu.
- Thiết kế các card có kích thước không đều để tạo nhịp bất đối xứng nhưng vẫn cân bằng.
- Chia layout thành các nhóm có trọng tâm rõ ràng: card lớn, card vừa, card nhỏ.
- Không làm layout quá đều hoặc quá giống grid cơ bản nhàm chán.

### Hero section

- Hero phải có yếu tố nổi (floating elements) và nền có vòng tròn đồng tâm, tạo cảm giác có chiều sâu và tinh tế.
- Sử dụng background decorative có các vòng tròn, gradient rất nhẹ, hoặc pseudo-element bằng Tailwind.
- Các floating element có thể là badge, stat card, icon chip, mini chart, form snippet, hoặc current KPI card.
- Hero không được quá bừa, không được chồng quá nhiều element gây rối mắt.

### Layout mindset

- Cân bằng giữa content và whitespace.
- Tạo điểm nhấn bằng hierarchy, không nhồi nhét quá nhiều thông tin cùng lúc.
- Mỗi section nên giải quyết 1 mục tiêu rõ ràng: thông tin, hành động, hoặc chứng minh giá trị.

## 3) Code Quality

### Tailwind writing guidelines

- Code Tailwind nên gọn gàng, rõ ràng, dễ đọc.
- Không dùng class thừa hoặc class lặp vô nghĩa.
- Prefer utility composition over repeated custom CSS.
- Dùng class theo nhóm logic: layout → spacing → color → border → shadow → interaction.
- Chỉ tạo custom CSS khi thật sự cần thiết; nếu có, hãy giữ tối thiểu.

### Responsive

- Thiết kế ưu tiên Mobile-first.
- Tối ưu trải nghiệm ở màn hình nhỏ trước, sau đó mở rộng cho Desktop.
- Không để layout bị vỡ ở mobile vì sử dụng grid quá cứng hoặc spacing quá lớn.
- Khi cần, dùng breakpoint hợp lý: `sm:`, `md:`, `lg:`, `xl:`.

### Maintainability

- Tách component rõ ràng, có tên rõ nghĩa, không chồng logic UI và logic nghiệp vụ.
- Dùng cấu trúc component dễ mở rộng và tái sử dụng.
- Không hardcode vô tội vạ. Tránh Magic Number nếu có thể.
- Tạo code sạch, dễ sửa, dễ review.

## 4) UX / Product quality

- Ưu tiên khả năng đọc và hiểu ngay lập tức.
- Mỗi action phải rõ ràng, không gây nhầm lẫn.
- Tương tác phải mượt, không quá nhiều hiệu ứng gây phân tâm.
- Nền, chữ, button, badge phải có độ tương phản hợp lý để người dùng không mệt mắt.
- Sử dụng motion nhẹ nhàng, không quá ồn.

## 5) Anti-patterns và nguyên tắc “No AI Slop”

- Không dùng kiểu thiết kế lỗi thời như quá nhiều gradient neon, shadows nặng, layout nặng màu, card quá lạ hình dạng, hoặc typography quá cực đoan.
- Không dùng màu sắc quá gắt hoặc quá nhiều màu sắc không đồng bộ.
- Không dùng spacing không cân đối: quá dày, quá thấp, hoặc chồng chéo không có logic.
- Không thiết kế theo kiểu “càng nhiều càng tốt” — phải có ẩn nhịp, sự tập trung và nhường chỗ cho nội dung chính.
- Tránh các layout quá “AI-generated” và thiếu cảm giác thực tế, thẩm mỹ, và tính sử dụng.
- Mọi thiết kế phải có mục đích rõ ràng: phục vụ thông tin, hành động, hoặc sự tin cậy.

## 6) Example Tailwind patterns

### Card chuẩn

```html
<article class="rounded-[28px] border border-slate-100 bg-white/80 p-5 shadow-[0_12px_32px_rgba(15,23,42,0.06)] backdrop-blur-sm sm:p-6">
  <div class="flex items-center justify-between">
    <div>
      <p class="text-xs font-medium uppercase tracking-[0.12em] text-slate-500">Overview</p>
      <h3 class="mt-2 text-xl font-semibold text-slate-900">Smart Finance</h3>
    </div>
    <span class="rounded-full border border-slate-200 bg-slate-50 px-2.5 py-1 text-xs font-medium text-slate-600">
      Live
    </span>
  </div>
</article>
```

### Hero với floating elements

```html
<section class="relative overflow-hidden rounded-[32px] border border-slate-100 bg-white/80 shadow-[0_18px_40px_rgba(15,23,42,0.06)] backdrop-blur-sm">
  <div class="absolute inset-0 flex items-center justify-center">
    <div class="h-72 w-72 rounded-full border border-slate-200/80"></div>
    <div class="absolute h-96 w-96 rounded-full border border-slate-100"></div>
  </div>

  <div class="relative grid gap-8 px-5 py-8 sm:px-8 lg:grid-cols-[1.2fr_0.8fr] lg:px-12 lg:py-12">
    <div>
      <span class="inline-flex rounded-full border border-slate-200 bg-slate-50 px-3 py-1 text-xs font-medium text-slate-600">
        Smart Planning
      </span>
      <h1 class="mt-5 max-w-xl text-4xl font-semibold tracking-tight text-slate-900 sm:text-5xl">
        Control your money with clarity.
      </h1>
      <p class="mt-4 max-w-lg text-base text-slate-600">
        Personal finance dashboard that keeps spending, saving, and goals in one calm view.
      </p>
    </div>

    <div class="relative flex justify-center lg:justify-end">
      <div class="w-full max-w-sm rounded-2xl border border-slate-100 bg-white p-4 shadow-sm">
        <div class="flex items-center justify-between">
          <span class="text-sm text-slate-500">Balance</span>
          <span class="rounded-full bg-emerald-50 px-2 py-1 text-xs font-medium text-emerald-600">+12.4%</span>
        </div>
        <div class="mt-4 text-3xl font-semibold text-slate-900">$24,860</div>
      </div>
    </div>
  </div>
</section>
```

## 7) Decision rules cho mọi thay đổi UI

Khi làm việc với giao diện, hãy tuân theo thứ tự ưu tiên sau:

1. Dễ đọc trước.
2. Rõ ràng trước.
3. Dễ dùng trước.
4. Đẹp nhưng không quá lố.
5. Đồng bộ hệ thống trước khi tối ưu chi tiết.

Nếu một thiết kế không thể vừa đủ đẹp, đủ rõ, đủ cân đối, và đủ chuyên nghiệp, thì không nên ship.

## 8) Kết luận

Mọi UI trong dự án phải có cảm giác:

- Sáng
- Chắc chắn
- Mạnh mẽ nhưng không quá khô
- Hiện đại nhưng không kiểu cách
- Thẩm mỹ nhưng không phức tạp
- Tinh tế, rõ ràng, và đáng tin cậy

Đây là tiêu chuẩn bắt buộc cho mọi module, section, component, dashboard view, landing page và trải nghiệm tương tác của dự án.
