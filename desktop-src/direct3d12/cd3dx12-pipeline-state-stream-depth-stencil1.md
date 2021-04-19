---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Beschreibung der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1-Struktur (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367348"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a><span data-ttu-id="3c9b9-105">CD3DX12 \_ Daten \_ Strom Tiefe des Pipeline Zustands \_ \_ \_ STENCIL1 Struktur</span><span class="sxs-lookup"><span data-stu-id="3c9b9-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 structure</span></span>

<span data-ttu-id="3c9b9-106">Eine hilfsstruktur, die verwendet wird, um eine Beschreibung der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3c9b9-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c9b9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c9b9-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a><span data-ttu-id="3c9b9-108">Member</span><span class="sxs-lookup"><span data-stu-id="3c9b9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3c9b9-109">**CD3DX12 \_ Daten \_ Strom Tiefe des Pipeline Zustands \_ \_ \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="3c9b9-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>
</dt> <dd>

<span data-ttu-id="3c9b9-110">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ Pipeline \_ State \_ Stream \_ Tiefe \_ STENCIL1.</span><span class="sxs-lookup"><span data-stu-id="3c9b9-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1.</span></span>

</dd> <dt>

<span data-ttu-id="3c9b9-111">**CD3DX12 \_ Daten \_ Strom Tiefe des Pipeline Zustands \_ \_ \_ STENCIL1 (CD3DX12- \_ tiefen \_ Schablone \_ DESC1 Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="3c9b9-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1(CD3DX12\_DEPTH\_STENCIL\_DESC1 const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="3c9b9-112">Erstellt eine neue Instanz einer CD3DX12 \_ Pipeline \_ State Stream \_ - \_ Tiefe \_ STENCIL1, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Tiefe \_ STENCIL1** und untergeordnete Daten, die aus *i* kopiert werden, einer [**CD3DX12- \_ tiefen \_ Schablone \_ DESC1**](cd3dx12-depth-stencil-desc1.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3c9b9-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3c9b9-113">**Operator = (CD3DX12- \_ tiefen \_ Schablone \_ DESC1 Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="3c9b9-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC1 const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="3c9b9-114">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="3c9b9-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="3c9b9-115">**Operator CD3DX12 \_ Tiefe \_ Schablone \_ DESC1 () konstant**</span><span class="sxs-lookup"><span data-stu-id="3c9b9-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC1() const**</span></span>
</dt> <dd>

<span data-ttu-id="3c9b9-116">Implizite Konvertierung in eine [**CD3DX12 \_ Tiefe \_ Schablone \_ DESC1**](cd3dx12-depth-stencil-desc1.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3c9b9-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c9b9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c9b9-117">Remarks</span></span>

<span data-ttu-id="3c9b9-118">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Tiefe \_ STENCIL1 ist eine typedef-Spezialisierung der Vorlage " [**CD3DX12 \_ Pipeline \_ State \_ Stream \_ SubObject**](cd3dx12-pipeline-state-stream-subobject.md) " und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3c9b9-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
```



## <a name="requirements"></a><span data-ttu-id="3c9b9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c9b9-119">Requirements</span></span>



| <span data-ttu-id="3c9b9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c9b9-120">Requirement</span></span> | <span data-ttu-id="3c9b9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3c9b9-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9b9-122">Header</span><span class="sxs-lookup"><span data-stu-id="3c9b9-122">Header</span></span><br/> | <dl> <span data-ttu-id="3c9b9-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c9b9-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c9b9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c9b9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c9b9-125">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="3c9b9-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3c9b9-126">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="3c9b9-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="3c9b9-127">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="3c9b9-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

