# Thửa đất Tây Ninh – MCP

Kết nối trợ lý AI (Claude, ChatGPT, Cursor…) với dữ liệu thửa đất tại Tây Ninh trên [BumiAtlas](https://bumiatlas.com) qua Model Context Protocol (MCP).

- Tra cứu thửa đất theo số tờ bản đồ và số thửa như ghi trên sổ đỏ, sổ hồng (*"tờ 7 thửa 171, Phường 1, Tân An"*), theo mã thửa đất hoặc theo tọa độ
- Mục đích sử dụng đất (ODT đất ở đô thị, ONT đất ở nông thôn, LUC đất chuyên trồng lúa, CLN đất trồng cây lâu năm…), diện tích ghi nhận và diện tích theo ranh thửa
- Địa chỉ theo đơn vị hành chính mới (từ 1/7/2025) và địa chỉ cũ (phường, xã, quận, huyện) như trên giấy chứng nhận cấp trước đó; tìm bằng tên cũ hay tên mới, có dấu hoặc không dấu
- Ảnh vệ tinh hoặc bản đồ của thửa đất và các thửa xung quanh, mỗi thửa ghi số thửa

Từ 1/7/2025, tỉnh Tây Ninh gồm cả tỉnh Long An cũ; dữ liệu phủ cả hai.

Dữ liệu là những gì các cổng thông tin công bố, nên chưa có đủ mọi thửa đất. Không có tên chủ sở hữu, số giấy chứng nhận hay giá đất.

## Kết nối

```
https://bumiatlas.com/mcp/tayninh
```

Thêm địa chỉ này làm custom connector (trình kết nối tùy chỉnh) trong Claude, ChatGPT, Cursor hoặc ứng dụng khác hỗ trợ MCP, rồi đăng nhập bằng Google. Không cần API key. Hướng dẫn chi tiết: [bumiatlas.com/mcp-docs/tayninh](https://bumiatlas.com/mcp-docs/tayninh).

Tên công cụ bằng tiếng Anh, nhưng trợ lý vẫn trả lời bằng tiếng Việt. Đây là bộ công cụ Việt Nam của BumiAtlas, nên cũng tra cứu được thửa đất ở các tỉnh, thành khác.

## Công cụ

| Công cụ | Chức năng |
|---|---|
| `VN_parcel_search` | Tìm thửa đất theo mã thửa, theo số tờ và số thửa kèm địa danh, hoặc theo tọa độ `vĩ độ, kinh độ` |
| `VN_parcel_get` | Chi tiết một thửa: mục đích sử dụng, diện tích, địa chỉ mới và cũ, các khu quy hoạch phủ lên thửa; ranh thửa dạng GeoJSON |
| `VN_parcel_image` | Ảnh vệ tinh hoặc bản đồ quanh một thửa hay một điểm; các thửa trong khung hình được viền và ghi số thửa |
| `VN_zoning_get` | Khu quy hoạch tại một điểm (TP. Hồ Chí Minh và Đà Nẵng): cấp quy hoạch, chức năng sử dụng đất, mật độ xây dựng, hệ số sử dụng đất, tầng cao |

## Ví dụ câu hỏi

- *"Tìm thửa đất tờ 7 thửa 171, Phường 1, TP. Tân An (Long An cũ)."*
- *"Thửa đất tại 11.30075, 106.10636 ở TP. Tây Ninh dùng vào mục đích gì?"*
- *"Ở Bến Lức có những thửa nào là tờ 7 thửa 11? Thửa nào là đất ở?"*

## Nguồn dữ liệu

Thửa đất từ cổng thông tin đất đai Long An (datdai.longan.gov.vn) và guland.vn. Mỗi thửa ghi rõ nguồn.

## Các xã, phường có dữ liệu

Xếp theo quận, huyện, thị xã, thành phố cũ. Mỗi xã, phường mới (từ 1/7/2025) kèm các phường, xã, thị trấn cũ đã nhập vào.

### Tây Ninh cũ

#### Huyện Bến Cầu

- **Xã Bến Cầu**: Tiên Thuận, An Thạnh, Lợi Thuận, Bến Cầu
- **Xã Long Chữ**: Long Chữ, Long Phước; Long Vĩnh (Huyện Châu Thành)
- **Xã Long Thuận**: Long Thuận, Long Khánh, Long Giang

#### Huyện Châu Thành

- **Xã Châu Thành**: Đồng Khởi, Châu Thành, Thái Bình, An Bình
- **Xã Hảo Đước**: Hảo Đước, An Cơ, Trí Bình
- **Xã Hòa Hội**: Biên Giới, Hòa Thạnh, Hòa Hội
- **Xã Ninh Điền**: Thành Long, Ninh Điền
- **Xã Phước Vinh**: Phước Vinh; Hòa Hiệp (Huyện Tân Biên)

#### Huyện Dương Minh Châu

- **Xã Cầu Khởi**: Cầu Khởi, Chà Là; Thạnh Đức (Huyện Gò Dầu)
- **Xã Dương Minh Châu**: Phan, Suối Đá, Dương Minh Châu
- **Xã Lộc Ninh**: Phước Minh, Lộc Ninh

#### Huyện Gò Dầu

- **Phường Gò Dầu**: Thanh Phước, Gò Dầu; Gia Bình (Thị xã Trảng Bàng)
- **Xã Phước Thạnh**: Hiệp Thạnh, Phước Thạnh, Phước Trạch
- **Xã Thạnh Đức**: Thạnh Đức, Cẩm Giang
- **Xã Truông Mít**: Bàu Đồn; Truông Mít (Huyện Dương Minh Châu)

#### Huyện Tân Biên

- **Xã Tân Biên**: Tân Biên, Thạnh Tây
- **Xã Thạnh Bình**: Thạnh Bình, Tân Phong; Thạnh Đông (Huyện Tân Châu)
- **Xã Trà Vong**: Mỏ Công, Trà Vong

#### Huyện Tân Châu

- **Xã Tân Châu**: Tân Châu, Thạnh Đông, Tân Phú
- **Xã Tân Đông**: Tân Đông, Tân Hà
- **Xã Tân Hòa**: Suối Ngô, Tân Hòa, Suối Dây
- **Xã Tân Hội**: Tân Hội, Tân Hiệp
- **Xã Tân Phú**: Tân Hưng, Tân Phú
- **Xã Tân Thành**: Suối Dây, Tân Thành

#### Thành phố Tây Ninh

- **Phường Bình Minh**: Ninh Sơn, Thạnh Tân, Tân Bình, Bình Minh
- **Phường Ninh Thạnh**: Ninh Thạnh; Bàu Năng, Chà Là (Huyện Dương Minh Châu)
- **Phường Tân Ninh**: Phường 1, Hiệp Ninh, Phường 4, Phường 3, Phường 2

#### Thị xã Hòa Thành

- **Phường Hòa Thành**: Long Thành Trung, Long Thành Nam _(phần lớn chưa có mục đích sử dụng đất)_
- **Phường Long Hoa**: Trường Đông, Trường Hòa, Trường Tây, Long Thành Bắc, Long Hoa _(phần lớn chưa có mục đích sử dụng đất)_
- **Phường Thanh Điền**: Hiệp Tân, Long Hoa; Thanh Điền (Huyện Châu Thành) _(phần lớn chưa có mục đích sử dụng đất)_

#### Thị xã Trảng Bàng

- **Phường An Tịnh**: Lộc Hưng, An Tịnh
- **Phường Gia Lộc**: Gia Lộc; Phước Đông (Huyện Gò Dầu)
- **Phường Trảng Bàng**: An Hòa, Trảng Bàng, Gia Lộc
- **Xã Hưng Thuận**: Hưng Thuận, Đôn Thuận
- **Xã Phước Chỉ**: Phước Chỉ, Phước Bình

### Long An cũ

#### Huyện Bến Lức

- **Xã Bến Lức**: Bến Lức, An Thạnh, Thanh Phú
- **Xã Bình Đức**: Nhựt Chánh, Bình Đức, Thạnh Đức
- **Xã Lương Hòa**: Tân Bửu, Lương Hòa
- **Xã Mỹ Yên**: Long Hiệp, Mỹ Yên, Phước Lợi
- **Xã Thạnh Lợi**: Thạnh Lợi, Thạnh Hòa, Lương Bình

#### Huyện Cần Đước

- **Xã Cần Đước**: Phước Tuy, Tân Chánh, Cần Đước, Tân Ân
- **Xã Long Cang**: Phước Vân, Long Định, Long Cang
- **Xã Long Hựu**: Long Hựu Đông, Long Hựu Tây
- **Xã Mỹ Lệ**: Tân Trạch, Mỹ Lệ, Long Sơn
- **Xã Rạch Kiến**: Long Trạch, Long Khê, Long Hòa
- **Xã Tân Lân**: Phước Đông, Tân Lân

#### Huyện Cần Giuộc

- **Xã Cần Giuộc**: Long Hậu, Phước Lại, Cần Giuộc
- **Xã Mỹ Lộc**: Mỹ Lộc, Phước Lâm, Thuận Thành, Cần Giuộc
- **Xã Phước Lý**: Phước Lý, Long Thượng, Phước Hậu
- **Xã Phước Vĩnh Tây**: Phước Vĩnh Tây, Long An, Long Phụng
- **Xã Tân Tập**: Tân Tập, Phước Vĩnh Đông, Đông Thạnh

#### Huyện Đức Hòa

- **Xã An Ninh**: An Ninh Tây, An Ninh Đông, Lộc Giang
- **Xã Đức Hòa**: Đức Hòa Hạ, Hựu Thạnh, Đức Hòa
- **Xã Đức Lập**: Đức Lập Hạ, Mỹ Hạnh Bắc, Đức Hòa Thượng
- **Xã Hậu Nghĩa**: Tân Mỹ, Đức Lập Thượng, Hậu Nghĩa
- **Xã Hiệp Hòa**: Tân Phú, Hiệp Hòa, Hiệp Hòa
- **Xã Hòa Khánh**: Hòa Khánh Đông, Hòa Khánh Tây, Hòa Khánh Nam
- **Xã Mỹ Hạnh**: Đức Hòa Thượng, Mỹ Hạnh Nam, Đức Hòa Đông

#### Huyện Đức Huệ

- **Xã Đông Thành**: Mỹ Thạnh Đông, Mỹ Thạnh Tây, Đông Thành, Mỹ Bình
- **Xã Đức Huệ**: Bình Hòa Bắc, Bình Hòa Nam, Bình Thành
- **Xã Mỹ Quý**: Mỹ Quý Tây, Mỹ Quý Đông, Mỹ Thạnh Bắc

#### Huyện Mộc Hóa

- **Xã Bình Hiệp**: Bình Hòa Tây; Bình Hiệp, Thạnh Trị, Bình Tân (Thị xã Kiến Tường)
- **Xã Bình Hòa**: Bình Thạnh, Bình Hòa Trung, Bình Hòa Đông
- **Xã Mộc Hóa**: Bình Phong Thạnh, Tân Lập, Tân Thành

#### Huyện Tân Hưng

- **Xã Hưng Điền**: Hưng Điền, Hưng Điền B, Hưng Hà
- **Xã Tân Hưng**: Vĩnh Thạnh, Vĩnh Lợi, Tân Hưng
- **Xã Vĩnh Châu**: Vĩnh Châu A, Vĩnh Bửu, Vĩnh Đại
- **Xã Vĩnh Thạnh**: Thạnh Hưng, Vĩnh Châu B, Hưng Thạnh

#### Huyện Tân Thạnh

- **Xã Hậu Thạnh**: Hậu Thạnh Tây, Hậu Thạnh Đông, Bắc Hòa
- **Xã Nhơn Hòa Lập**: Tân Lập, Nhơn Hòa Lập, Nhơn Hoà
- **Xã Nhơn Ninh**: Nhơn Ninh, Tân Thành, Tân Ninh
- **Xã Tân Thạnh**: Tân Hòa, Tân Thạnh, Kiến Bình, Tân Bình

#### Huyện Tân Trụ

- **Xã Nhựt Tảo**: Tân Bình, Quê Mỹ Thạnh, Lạc Tấn; Nhị Thành (Huyện Thủ Thừa)
- **Xã Tân Trụ**: Bình Trinh Đông, Bình Lãng, Bình Tịnh, Tân Trụ
- **Xã Vàm Cỏ**: Nhựt Ninh, Tân Phước Tây, Đức Tân

#### Huyện Thạnh Hóa

- **Xã Bình Thành**: Tân Hiệp, Thuận Bình; Bình Hòa Hưng (Huyện Đức Huệ)
- **Xã Tân Tây**: Thủy Đông, Tân Đông, Tân Tây
- **Xã Thạnh Hóa**: Thạnh An, Thủy Tây, Thạnh Hóa
- **Xã Thạnh Phước**: Thạnh Phước, Thuận Nghĩa Hòa, Thạnh Phú

#### Huyện Thủ Thừa

- **Xã Mỹ An**: Mỹ An, Mỹ Phú
- **Xã Mỹ Thạnh**: Mỹ Thạnh, Mỹ Lạc, Bình An, Tân Thành
- **Xã Tân Long**: Long Thuận, Long Thạnh, Tân Long
- **Xã Thủ Thừa**: Thủ Thừa, Nhị Thành, Bình Thạnh, Tân Thành

#### Huyện Vĩnh Hưng

- **Xã Khánh Hưng**: Hưng Điền A, Khánh Hưng, Thái Trị, Vĩnh Trị, Thái Bình Trung
- **Xã Tuyên Bình**: Thái Bình Trung, Tuyên Bình, Tuyên Bình Tây, Vĩnh Bình, Vĩnh Thuận
- **Xã Vĩnh Hưng**: Vĩnh Trị, Vĩnh Hưng, Vĩnh Thuận, Thái Bình Trung, Vĩnh Bình, Thái Trị

#### Thành phố Tân An

- **Phường Khánh Hậu**: Lợi Bình Nhơn, Tân Khánh, Khánh Hậu
- **Phường Long An**: Phường 6, Phường 4, Phường 5, Phường 3, Hướng Thọ Phú, Phường 1; Bình Thạnh (Huyện Thủ Thừa)
- **Phường Tân An**: Nhơn Thạnh Trung, Bình Tâm, Phường 7, An Vĩnh Ngãi

#### Thị xã Kiến Tường

- **Phường Kiến Tường**: Phường 1, Phường 2, Phường 3
- **Xã Tuyên Thạnh**: Tuyên Thạnh, Thạnh Hưng; Bắc Hòa (Huyện Tân Thạnh)

**Chưa có dữ liệu:** Xã An Lục Long, Xã Tầm Vu, Xã Tân Lập, Xã Thuận Mỹ, Xã Vĩnh Công.
