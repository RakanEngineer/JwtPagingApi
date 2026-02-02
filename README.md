# JwtPagingApi - ASP.NET Core Web API
✅ JWT Authentication
✅ Pagination
✅ Filtering
✅ Sorting
✅ JsonPatch (Partial Update)
✅ DTO + Clean Structure

packages:
- dotnet add package Microsoft.AspNetCore.Authentication.JwtBearer
- dotnet add package Microsoft.AspNetCore.JsonPatch
- dotnet add package Microsoft.AspNetCore.Mvc.NewtonsoftJson

Postman

Post:
api/auth/login

Response:
{
  "token": "eyJhbGciOiJIUzI1NiIs..."
}
---
GET
Authorization: Bearer YOUR_TOKEN
api/products?page=1&pageSize=2

---
Filtering
api/products?category=Phones
-------

Sorting
api/products?sort=price
Descending
api/products?sort=-price
---
🔹 JsonPatch Update
PATCH
api/products/1
Body
[
  { "op": "replace", "path": "/price", "value": 999 }
]

