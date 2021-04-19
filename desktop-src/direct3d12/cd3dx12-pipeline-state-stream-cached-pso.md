---
title: CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um ein zwischengespeichertes PSO als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355786"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a><span data-ttu-id="bbb9c-104">CD3DX12 \_ - \_ \_ \_ PSO-Struktur zwischengespeicherten Pipeline Zustandsdaten Strom \_</span><span class="sxs-lookup"><span data-stu-id="bbb9c-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO structure</span></span>

<span data-ttu-id="bbb9c-105">Eine hilfsstruktur, die verwendet wird, um ein zwischengespeichertes PSO als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bbb9c-105">A helper structure used to describe a cached PSO as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb9c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbb9c-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a><span data-ttu-id="bbb9c-107">Member</span><span class="sxs-lookup"><span data-stu-id="bbb9c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bbb9c-108">**CD3DX12 \_ - \_ \_ \_ PSO zwischen gespeicherter Pipeline Zustandsdaten Strom \_**</span><span class="sxs-lookup"><span data-stu-id="bbb9c-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>
</dt> <dd>

<span data-ttu-id="bbb9c-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Pipeline-Statusdaten Stroms, der \_ \_ \_ \_ zwischengespeichert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="bbb9c-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO.</span></span>

</dd> <dt>

<span data-ttu-id="bbb9c-110">**CD3DX12- \_ Pipeline- \_ \_ \_ \_ StatusStream zwischengespeichert PSO (D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Status konstant &i)**</span><span class="sxs-lookup"><span data-stu-id="bbb9c-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO(D3D12\_CACHED\_PIPELINE\_STATE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="bbb9c-111">Erstellt eine neue Instanz eines CD3DX12 \_ -Pipeline- \_ Statusdaten \_ Stroms \_ zwischengespeicherten \_ PSO, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Cache \_ PSO** und unter unter Objekt-Daten, die aus *i* kopiert wurden, einer [**D3D12 \_ zwischengespeicherten \_ Pipeline \_ Zustands**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) Struktur.</span><span class="sxs-lookup"><span data-stu-id="bbb9c-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_CACHED\_PSO** and subobject data copied from *i*, a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bbb9c-112">**Operator = (D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Status konstant& i)**</span><span class="sxs-lookup"><span data-stu-id="bbb9c-112">**operator=(D3D12\_CACHED\_PIPELINE\_STATE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="bbb9c-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="bbb9c-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="bbb9c-114">**Operator D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Zustand () konstant**</span><span class="sxs-lookup"><span data-stu-id="bbb9c-114">**operator D3D12\_CACHED\_PIPELINE\_STATE() const**</span></span>
</dt> <dd>

<span data-ttu-id="bbb9c-115">Implizite Konvertierung in eine [**\_ zwischengespeicherte D3D12- \_ Pipeline \_ Zustands**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) Struktur.</span><span class="sxs-lookup"><span data-stu-id="bbb9c-115">Implicit conversion to a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbb9c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbb9c-116">Remarks</span></span>

<span data-ttu-id="bbb9c-117">CD3DX12 \_ \_ -Pipeline \_ -StatusStream \_ , der zwischengespeichert \_ ist, ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="bbb9c-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
```



## <a name="requirements"></a><span data-ttu-id="bbb9c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbb9c-118">Requirements</span></span>



| <span data-ttu-id="bbb9c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbb9c-119">Requirement</span></span> | <span data-ttu-id="bbb9c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bbb9c-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb9c-121">Header</span><span class="sxs-lookup"><span data-stu-id="bbb9c-121">Header</span></span><br/> | <dl> <span data-ttu-id="bbb9c-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbb9c-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbb9c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbb9c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbb9c-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="bbb9c-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="bbb9c-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="bbb9c-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="bbb9c-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="bbb9c-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

