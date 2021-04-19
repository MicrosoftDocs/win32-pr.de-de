---
title: CD3DX12_RT_FORMAT_ARRAY-Struktur (D3dx12. h)
description: Eine hilfsstruktur, mit der die einfache Initialisierung einer \_ Array Struktur im D3D12 RT-Format aktiviert werden kann \_ \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- CD3DX12_RT_FORMAT_ARRAY Struktur
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360238"
---
# <a name="cd3dx12_rt_format_array-structure"></a><span data-ttu-id="b5ddc-104">CD3DX12 \_ RT- \_ Format \_ Array Struktur</span><span class="sxs-lookup"><span data-stu-id="b5ddc-104">CD3DX12\_RT\_FORMAT\_ARRAY structure</span></span>

<span data-ttu-id="b5ddc-105">Eine hilfsstruktur, mit der die einfache Initialisierung einer Array Struktur im [**D3D12 \_ RT- \_ \_ Format**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-105">A helper structure to enable easy initialization of a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ddc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5ddc-106">Syntax</span></span>


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a><span data-ttu-id="b5ddc-107">Member</span><span class="sxs-lookup"><span data-stu-id="b5ddc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5ddc-108">**CD3DX12 \_ RT- \_ Format \_ Array ()**</span><span class="sxs-lookup"><span data-stu-id="b5ddc-108">**CD3DX12\_RT\_FORMAT\_ARRAY()**</span></span>
</dt> <dd>

<span data-ttu-id="b5ddc-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 RT- \_ \_ Format \_ Arrays.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-109">Creates a new, uninitialized, instance of a CD3DX12\_RT\_FORMAT\_ARRAY.</span></span>

</dd> <dt>

<span data-ttu-id="b5ddc-110">**explizites CD3DX12 \_ RT- \_ Format \_ Array (konstant D3D12 \_ RT- \_ Format \_ Array& o)**</span><span class="sxs-lookup"><span data-stu-id="b5ddc-110">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const D3D12\_RT\_FORMAT\_ARRAY& o)**</span></span>
</dt> <dd>

<span data-ttu-id="b5ddc-111">Erstellt eine neue Instanz eines CD3DX12 \_ RT- \_ Format \_ Arrays, das mit Werten initialisiert wird, die aus einer Array Struktur des [**D3D12 RT- \_ \_ Formats \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-111">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with values copied from a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5ddc-112">**explizites CD3DX12 \_ RT- \_ Format \_ Array (Konstante DXGI- \_ Format \* pformats, uint-numformats)**</span><span class="sxs-lookup"><span data-stu-id="b5ddc-112">**explicit CD3DX12\_RT\_FORMAT\_ARRAY(const DXGI\_FORMAT\* pFormats, UINT NumFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="b5ddc-113">Erstellt eine neue Instanz eines CD3DX12 \_ RT- \_ Format \_ Arrays, das mit den in der Parameterliste übergebenen Werten initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-113">Creates a new instance of a CD3DX12\_RT\_FORMAT\_ARRAY, initialized with the values passed in the parameter list.</span></span> <span data-ttu-id="b5ddc-114">Der Inhalt des Arrays, das durch den *pformats* -Parameter angegeben wird, wird in das Member-Array **rtformats** kopiert.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-114">Contents of the array specified by the *pFormats* parameter are copied into the member array **RTFormats**.</span></span> <span data-ttu-id="b5ddc-115">Das von *pformats* angegebene Array hat die gleiche Größe wie **rtformats**.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-115">The array specified by *pFormats* is assumed to have the same size as **RTFormats**.</span></span>

</dd> <dt>

<span data-ttu-id="b5ddc-116">**Operator Konstanten D3D12 \_ RT- \_ Format \_ Array& () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="b5ddc-116">**operator const D3D12\_RT\_FORMAT\_ARRAY&() const**</span></span>
</dt> <dd>

<span data-ttu-id="b5ddc-117">Implizite Konvertierung in eine [**Array Struktur im D3D12 \_ RT- \_ Format \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .</span><span class="sxs-lookup"><span data-stu-id="b5ddc-117">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span> <span data-ttu-id="b5ddc-118">Da das D3D12 \_ RT- \_ Format \_ Array der zugrunde liegende Typ von CD3DX12- \_ tiefen \_ Schablone DESC1 ist \_ , wird das-Objekt einfach als Array Verweis des Konstanten D3D12 \_ RT- \_ Formats \_ an sich selbst zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-118">Because D3D12\_RT\_FORMAT\_ARRAY is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_RT\_FORMAT\_ARRAY reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5ddc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5ddc-119">Requirements</span></span>



| <span data-ttu-id="b5ddc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5ddc-120">Requirement</span></span> | <span data-ttu-id="b5ddc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b5ddc-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ddc-122">Header</span><span class="sxs-lookup"><span data-stu-id="b5ddc-122">Header</span></span><br/> | <dl> <span data-ttu-id="b5ddc-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ddc-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ddc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5ddc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ddc-125">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="b5ddc-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b5ddc-126">**D3D12 \_ RT- \_ Format \_ Array**</span><span class="sxs-lookup"><span data-stu-id="b5ddc-126">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





