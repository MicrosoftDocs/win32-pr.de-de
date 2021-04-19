---
title: CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um den Wert des Index Puffer Streifens als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357222"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a><span data-ttu-id="f2581-104">CD3DX12 \_ Pipeline \_ State Stream-Datenstrom-Wert der IB-Bereichs \_ \_ \_ \_ Kürzung \_</span><span class="sxs-lookup"><span data-stu-id="f2581-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE structure</span></span>

<span data-ttu-id="f2581-105">Eine hilfsstruktur, die verwendet wird, um den Wert des Index Puffer Streifens als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f2581-105">A helper structure used to describe the index buffer strip cut value as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2581-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2581-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a><span data-ttu-id="f2581-107">Member</span><span class="sxs-lookup"><span data-stu-id="f2581-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2581-108">**CD3DX12- \_ Pipeline- \_ \_ \_ \_ \_ Ausschneide \_ Wert des Pipeline Zustandsdaten Stroms**</span><span class="sxs-lookup"><span data-stu-id="f2581-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>
</dt> <dd>

<span data-ttu-id="f2581-109">Erstellt eine neue, nicht initialisierte Instanz eines Datenstrom-Enumerationswerts für den CD3DX12 \_ Pipeline- \_ Statusdaten \_ Strom \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f2581-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="f2581-110">**CD3DX12-Daten \_ Strom des Pipeline- \_ \_ \_ \_ \_ \_ statusausschnitts (D3D12- \_ Index- \_ Puffer Strip- \_ \_ Ausschneide \_ Wert Konstanten Konstante &i)**</span><span class="sxs-lookup"><span data-stu-id="f2581-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="f2581-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline- \_ statusausschneide Werts (Pipeline State) \_ \_ \_ \_ \_ , initialisiert mit einem untergeordneten Typ des **D3D12 \_ Pipeline \_ State \_ unter Objekt- \_ \_ \_ \_ \_ Werts** und aus den aus *i* kopierten Daten, einer [**D3D12 \_ Index \_ Puffer \_ Strip \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) -Struktur</span><span class="sxs-lookup"><span data-stu-id="f2581-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_IB\_STRIP\_CUT\_VALUE** and subobject data copied from *i*, a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f2581-112">**Operator = (D3D12 \_ Index- \_ Puffer \_ Strip- \_ Ausschneide \_ Wert konstant& i)**</span><span class="sxs-lookup"><span data-stu-id="f2581-112">**operator=(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="f2581-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="f2581-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="f2581-114">**Operator D3D12 der \_ Index \_ Puffer Strip- \_ \_ Ausschneide \_ Wert () konstant.**</span><span class="sxs-lookup"><span data-stu-id="f2581-114">**operator D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE() const**</span></span>
</dt> <dd>

<span data-ttu-id="f2581-115">Implizite Konvertierung in eine [**D3D12 \_ Index- \_ Puffer \_ Strip- \_ Ausschneide \_ Wert**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f2581-115">Implicit conversion to a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2581-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2581-116">Remarks</span></span>

<span data-ttu-id="f2581-117">\_Der CD3DX12 \_ - \_ Pipeline \_ -Status-Stream \_ \_ \_ -Wert des Pipeline-Ausschnitts ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f2581-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
```



## <a name="requirements"></a><span data-ttu-id="f2581-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2581-118">Requirements</span></span>



| <span data-ttu-id="f2581-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2581-119">Requirement</span></span> | <span data-ttu-id="f2581-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f2581-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f2581-121">Header</span><span class="sxs-lookup"><span data-stu-id="f2581-121">Header</span></span><br/> | <dl> <span data-ttu-id="f2581-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2581-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2581-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2581-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2581-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="f2581-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f2581-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="f2581-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="f2581-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="f2581-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

