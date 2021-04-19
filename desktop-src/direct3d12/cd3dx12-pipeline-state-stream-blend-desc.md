---
title: CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Blend-Beschreibung als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361843"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a><span data-ttu-id="778d5-104">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend- \_ DESC-Struktur</span><span class="sxs-lookup"><span data-stu-id="778d5-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC structure</span></span>

<span data-ttu-id="778d5-105">Eine hilfsstruktur, die verwendet wird, um eine Blend-Beschreibung als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="778d5-105">A helper structure used to describe a blend description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="778d5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="778d5-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="778d5-107">Member</span><span class="sxs-lookup"><span data-stu-id="778d5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="778d5-108">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="778d5-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="778d5-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="778d5-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="778d5-110">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC (CD3DX12 \_ Blend \_ DESC Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="778d5-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC(CD3DX12\_BLEND\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="778d5-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Blend** -und unter Objekt-Daten, die aus *i* kopiert wurden, einer [**CD3DX12 \_ Blend \_ DESC**](cd3dx12-blend-desc.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="778d5-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_BLEND** and subobject data copied from *i*, a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="778d5-112">**Operator = (CD3DX12 \_ Blend \_& i)**</span><span class="sxs-lookup"><span data-stu-id="778d5-112">**operator=(CD3DX12\_BLEND\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="778d5-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="778d5-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="778d5-114">**Operator CD3DX12 \_ Blend-Operator \_ ()**</span><span class="sxs-lookup"><span data-stu-id="778d5-114">**operator CD3DX12\_BLEND\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="778d5-115">Implizite Konvertierung in eine [**CD3DX12 \_ Blend \_**](cd3dx12-blend-desc.md) -Debug-Struktur.</span><span class="sxs-lookup"><span data-stu-id="778d5-115">Implicit conversion to a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="778d5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="778d5-116">Remarks</span></span>

<span data-ttu-id="778d5-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Blend \_ DESC ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="778d5-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="778d5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="778d5-118">Requirements</span></span>



| <span data-ttu-id="778d5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="778d5-119">Requirement</span></span> | <span data-ttu-id="778d5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="778d5-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="778d5-121">Header</span><span class="sxs-lookup"><span data-stu-id="778d5-121">Header</span></span><br/> | <dl> <span data-ttu-id="778d5-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="778d5-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="778d5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="778d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="778d5-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="778d5-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="778d5-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="778d5-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="778d5-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="778d5-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

