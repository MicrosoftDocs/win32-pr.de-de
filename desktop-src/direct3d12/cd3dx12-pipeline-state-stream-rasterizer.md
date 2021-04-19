---
title: CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Beschreibung des Rasterizers als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373486"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a><span data-ttu-id="540a0-104">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer Structure</span><span class="sxs-lookup"><span data-stu-id="540a0-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER structure</span></span>

<span data-ttu-id="540a0-105">Eine hilfsstruktur, die verwendet wird, um eine Beschreibung des Rasterizers als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="540a0-105">A helper structure used to describe a rasterizer description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="540a0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="540a0-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="540a0-107">Member</span><span class="sxs-lookup"><span data-stu-id="540a0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="540a0-108">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer**</span><span class="sxs-lookup"><span data-stu-id="540a0-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>
</dt> <dd>

<span data-ttu-id="540a0-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Pipeline \_ State Stream- \_ \_ Rasterizers.</span><span class="sxs-lookup"><span data-stu-id="540a0-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER.</span></span>

</dd> <dt>

<span data-ttu-id="540a0-110">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer (CD3DX12 \_ Rasterizer \_ DESC Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="540a0-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER(CD3DX12\_RASTERIZER\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="540a0-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ -Rasterizers, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Rasterizer** und unter Objekt Data kopiert aus *i*, einer [**CD3DX12 \_ Rasterizer \_ DESC**](cd3dx12-rasterizer-desc.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="540a0-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RASTERIZER** and subobject data copied from *i*, a [**CD3DX12\_RASTERIZER\_DESC**](cd3dx12-rasterizer-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="540a0-112">**Operator = (CD3DX12 \_ Rasterizer \_ resc Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="540a0-112">**operator=(CD3DX12\_RASTERIZER\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="540a0-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="540a0-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="540a0-114">**Operator CD3DX12 \_ Rasterizer \_ Entsc () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="540a0-114">**operator CD3DX12\_RASTERIZER\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="540a0-115">Implizite Konvertierung in eine [**CD3DX12 \_ Rasterizer \_**](cd3dx12-rasterizer-desc.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="540a0-115">Implicit conversion to a [**CD3DX12\_RASTERIZER\_DESC**](cd3dx12-rasterizer-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="540a0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="540a0-116">Remarks</span></span>

<span data-ttu-id="540a0-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Rasterizer ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="540a0-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
```



## <a name="requirements"></a><span data-ttu-id="540a0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="540a0-118">Requirements</span></span>



| <span data-ttu-id="540a0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="540a0-119">Requirement</span></span> | <span data-ttu-id="540a0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="540a0-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="540a0-121">Header</span><span class="sxs-lookup"><span data-stu-id="540a0-121">Header</span></span><br/> | <dl> <span data-ttu-id="540a0-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="540a0-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="540a0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="540a0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="540a0-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="540a0-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="540a0-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="540a0-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="540a0-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="540a0-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

