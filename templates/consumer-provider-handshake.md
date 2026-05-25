# Consumer–Provider Handshake

## Thông tin chung

- Lab: FIT4110 Lab 03
- Ngày: 25/05/2026
- Provider team: A6
- Consumer team: A7
- Provider service: Core Business
- Consumer service: Notification

## Contract

- Contract file: contracts/A6_core.openapi.yaml
- Mock base URL: http://localhost:4011
- Auth method: Bearer Token
- Endpoint được test: GET /alerts/{alertId}

## Smoke test

### Request

```http
GET /alerts/0196fb3d-4ad7-7d1e-9f49-5d5148d2babc
Authorization: Bearer {{authToken}}
```

### Expected response

```json
{
  "id": "0196fb3d-4ad7-7d1e-9f49-5d5148d2babc",
  "alertType": "UNAUTHORIZED_ACCESS",
  "severity": "HIGH",
  "message": "Phát hiện truy cập trái phép tại cổng chính"
}
```

## Kết quả

- [x] Consumer gọi mock thành công.
- [x] Consumer parse được field cần dùng.
- [x] Consumer hiểu lỗi 4xx/5xx provider trả về.
- [x] Có Newman report hoặc screenshot.

## Ghi chú thay đổi hợp đồng

| Nội dung | Trước | Sau | Người đồng ý |
|---|---|---|---|
| N/A | | | |

## Xác nhận

- Provider representative: A6 lead
- Consumer representative: A7 lead
