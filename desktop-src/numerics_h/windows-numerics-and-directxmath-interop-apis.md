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
# <a name="windows-numerics-and-directxmath-interop-apis"></a><span data-ttu-id="cc1c7-104">Windows-Numerics und directxmath-Interop-APIs</span><span class="sxs-lookup"><span data-stu-id="cc1c7-104">Windows numerics and DirectXMath interop APIs</span></span>

<span data-ttu-id="cc1c7-105">Diese Funktionen konvertieren [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) -Typen in und aus den directxmath-SIMD-Typen [xmvector](../dxmath/xmvector-data-type.md) und [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="cc1c7-105">These functions convert [**Windows.Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) types to and from the DirectXMath SIMD types [XMVECTOR](../dxmath/xmvector-data-type.md) and [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span>

## <a name="functions"></a><span data-ttu-id="cc1c7-106">Functions</span><span class="sxs-lookup"><span data-stu-id="cc1c7-106">Functions</span></span>

| <span data-ttu-id="cc1c7-107">Name</span><span class="sxs-lookup"><span data-stu-id="cc1c7-107">Name</span></span> | <span data-ttu-id="cc1c7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc1c7-108">Description</span></span> |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | <span data-ttu-id="cc1c7-109">Lädt ein float2-Objekt in einen directxmath- [xmvector](../dxmath/xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cc1c7-109">Loads a float2 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | <span data-ttu-id="cc1c7-110">Lädt ein float3-Objekt in einen directxmath- [xmvector](../dxmath/xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cc1c7-110">Loads a float3 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | <span data-ttu-id="cc1c7-111">Lädt ein float4-Objekt in einen directxmath- [xmvector](../dxmath/xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="cc1c7-111">Loads a float4 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | <span data-ttu-id="cc1c7-112">Lädt ein float3x2-Objekt in eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="cc1c7-112">Loads a float3x2 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | <span data-ttu-id="cc1c7-113">Lädt ein float4x4-Objekt in eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="cc1c7-113">Loads a float4x4 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | <span data-ttu-id="cc1c7-114">Lädt eine Ebene in eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="cc1c7-114">Loads a plane into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | <span data-ttu-id="cc1c7-115">Lädt eine Quaternion in eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="cc1c7-115">Loads a quaternion into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="cc1c7-116">Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einem float2-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc1c7-116">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float2.</span></span> |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="cc1c7-117">Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einem float3-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc1c7-117">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float3.</span></span> |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="cc1c7-118">Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einem float4-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc1c7-118">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float4.</span></span> |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="cc1c7-119">Speichert eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) in einem float3x2-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc1c7-119">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float3x2.</span></span> |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="cc1c7-120">Speichert eine directxmath- [xmmatrix](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) in einem float4x4-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc1c7-120">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float4x4.</span></span> |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="cc1c7-121">Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einer Ebene.</span><span class="sxs-lookup"><span data-stu-id="cc1c7-121">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a plane.</span></span> |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="cc1c7-122">Speichert einen directxmath- [xmvector](../dxmath/xmvector-data-type.md) in einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="cc1c7-122">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="cc1c7-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc1c7-123">Requirements</span></span>

| <span data-ttu-id="cc1c7-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc1c7-124">Requirement</span></span> | <span data-ttu-id="cc1c7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="cc1c7-125">Value</span></span> |
|-|-|
| <span data-ttu-id="cc1c7-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc1c7-126">Namespace</span></span> | <span data-ttu-id="cc1c7-127">DirectX</span><span class="sxs-lookup"><span data-stu-id="cc1c7-127">DirectX</span></span> |
| <span data-ttu-id="cc1c7-128">Header</span><span class="sxs-lookup"><span data-stu-id="cc1c7-128">Header</span></span> | <dl> <span data-ttu-id="cc1c7-129"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc1c7-129"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="cc1c7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc1c7-130">See also</span></span>

[<span data-ttu-id="cc1c7-131">windowsnumerics. h-APIs</span><span class="sxs-lookup"><span data-stu-id="cc1c7-131">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
