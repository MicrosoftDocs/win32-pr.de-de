---
title: CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um die primitive Topologie als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353343"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a><span data-ttu-id="f1b08-104">CD3DX12 \_ - \_ \_ Struktur der \_ primitiven \_ Topologie des Pipeline Zustands Stroms</span><span class="sxs-lookup"><span data-stu-id="f1b08-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY structure</span></span>

<span data-ttu-id="f1b08-105">Eine hilfsstruktur, die verwendet wird, um die primitive Topologie als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f1b08-105">A helper structure used to describe the primitive topology as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b08-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1b08-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a><span data-ttu-id="f1b08-107">Member</span><span class="sxs-lookup"><span data-stu-id="f1b08-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1b08-108">**CD3DX12 \_ \_ \_ \_ primitive Topologie des Pipeline Zustands Stroms \_**</span><span class="sxs-lookup"><span data-stu-id="f1b08-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>
</dt> <dd>

<span data-ttu-id="f1b08-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ Pipeline \_ State \_ Stream \_ primitive \_ Topologie.</span><span class="sxs-lookup"><span data-stu-id="f1b08-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY.</span></span>

</dd> <dt>

<span data-ttu-id="f1b08-110">**CD3DX12 \_ \_ \_ primitive Topologie des Pipeline Zustands Stroms \_ \_ (D3D12 \_ primitiver \_ \_ Topologietyp Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="f1b08-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="f1b08-111">Erstellt eine neue Instanz einer primitiven CD3DX12 \_ Pipeline \_ State \_ Stream \_ \_ -Topologie, die mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ primitive \_ Topologie** und aus *i* kopierten untergeordneten Daten in einer primitiven [**\_ \_ topologietypstruktur \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f1b08-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_PRIMITIVE\_TOPOLOGY** and subobject data copied from *i*, a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f1b08-112">**Operator = (D3D12 \_ primitiver \_ \_ Topologietyp Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="f1b08-112">**operator=(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="f1b08-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="f1b08-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="f1b08-114">**Operator D3D12 \_ primitiver \_ \_ Topologietyp () konstant**</span><span class="sxs-lookup"><span data-stu-id="f1b08-114">**operator D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE() const**</span></span>
</dt> <dd>

<span data-ttu-id="f1b08-115">Implizite Konvertierung in eine [**D3D12 \_ primitive \_ \_ Topologietyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f1b08-115">Implicit conversion to a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1b08-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1b08-116">Remarks</span></span>

<span data-ttu-id="f1b08-117">CD3DX12 \_ \_ \_ \_ \_ die primitive Topologie des Pipeline Zustands Stroms ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f1b08-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a><span data-ttu-id="f1b08-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1b08-118">Requirements</span></span>



| <span data-ttu-id="f1b08-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1b08-119">Requirement</span></span> | <span data-ttu-id="f1b08-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f1b08-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b08-121">Header</span><span class="sxs-lookup"><span data-stu-id="f1b08-121">Header</span></span><br/> | <dl> <span data-ttu-id="f1b08-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1b08-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b08-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1b08-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b08-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="f1b08-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f1b08-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="f1b08-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="f1b08-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="f1b08-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

