---
title: Windows-Numerics und directxmath-Interop-APIs (windowsnumerics. h)
description: Diese Funktionen konvertieren Windows. Foundation. Numerics-Typen in und aus den directxmath-SIMD-Typen xmvector und xmmatrix.
ms.assetid: 05851054-196E-4955-B9C5-85C2E33EF488
keywords:
- Windows-Numerics und directxmath-Interop-APIs
topic_type:
- apiref
api_name:
- WWindows numerics and DirectXMath interop APIs
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e39057c92eeed87c3f429acb56f0afa2468ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358764"
---
# <a name="windows-numerics-and-directxmath-interop-apis"></a>Windows-Numerics und directxmath-Interop-APIs

Diese Funktionen konvertieren [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) -Typen in und aus den directxmath-SIMD-Typen [xmvector](../dxmath/xmvector-data-type.md) und [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).

## <a name="functions"></a>Functions

| Name | BESCHREIBUNG |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | Lädt ein float2-Objekt in einen directxmath- [xmvector](../dxmath/xmvector-data-type.md). |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | Lädt ein float3-Objekt in einen directxmath- [xmvector](../dxmath/xmvector-data-type.md). |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | Lädt ein float4-Objekt in einen directxmath- [xmvector](../dxmath/xmvector-data-type.md). |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | Lädt ein float3x2-Objekt in eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | Lädt ein float4x4-Objekt in eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | Lädt eine Ebene in eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | Lädt eine Quaternion in eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einem float2-Objekt. |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einem float3-Objekt. |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einem float4-Objekt. |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | Speichert eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) in einem float3x2-Objekt. |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | Speichert eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) in einem float4x4-Objekt. |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einer Ebene. |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einer Quaternion. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Namespace | DirectX |
| Header | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[windowsnumerics. h-APIs](windowsnumerics-h-apis-portal.md)
