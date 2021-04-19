---
title: CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um die Datenstrom-Ausgabe Beschreibung als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367347"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a><span data-ttu-id="3b9b9-104">CD3DX12 \_ Pipeline Status-Stream- \_ \_ \_ \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="3b9b9-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT structure</span></span>

<span data-ttu-id="3b9b9-105">Eine hilfsstruktur, die verwendet wird, um die Datenstrom-Ausgabe Beschreibung als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist</span><span class="sxs-lookup"><span data-stu-id="3b9b9-105">A helper structure used to describe the stream output description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9b9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b9b9-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="3b9b9-107">Member</span><span class="sxs-lookup"><span data-stu-id="3b9b9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b9b9-108">**Stream-Ausgabe des CD3DX12- \_ Pipeline \_ Zustandsdaten \_ \_ Stroms \_**</span><span class="sxs-lookup"><span data-stu-id="3b9b9-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="3b9b9-109">Erstellt eine neue, nicht initialisierte Instanz der Stream-Ausgabe eines CD3DX12 \_ Pipeline-Statusdaten \_ \_ Stroms \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3b9b9-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT.</span></span>

</dd> <dt>

<span data-ttu-id="3b9b9-110">**CD3DX12 Pipeline-Stream-Stream- \_ Ausgabe des Pipeline \_ Status \_ \_ \_ (D3D12 \_ Stream- \_ Ausgabe \_ DESC Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="3b9b9-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT(D3D12\_STREAM\_OUTPUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="3b9b9-111">Erstellt eine neue Instanz der Stream- \_ Ausgabe eines CD3DX12 Pipeline \_ \_ -Statusdaten Stroms \_ \_ , initialisiert mit einem untergeordneten Typ von D3D12-Pipeline-statusausgabetyp- **\_ \_ \_ \_ \_ \_ Streamausgabe** und untergeordneten Daten, die aus *i* kopiert werden, einer D3D12- [**Stream- \_ \_ Ausgabe \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3b9b9-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_STREAM\_OUTPUT** and subobject data copied from *i*, a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3b9b9-112">**Operator = (D3D12 \_ Stream \_ Output \_ DESC& i)**</span><span class="sxs-lookup"><span data-stu-id="3b9b9-112">**operator=(D3D12\_STREAM\_OUTPUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="3b9b9-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="3b9b9-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="3b9b9-114">**Operator D3D12 \_ Stream \_ Output \_ DESC () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="3b9b9-114">**operator D3D12\_STREAM\_OUTPUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="3b9b9-115">Implizite Konvertierung in eine [**\_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) -Struktur der D3D12 Stream-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3b9b9-115">Implicit conversion to a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b9b9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b9b9-116">Remarks</span></span>

<span data-ttu-id="3b9b9-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Stream \_ Output ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3b9b9-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
```



## <a name="requirements"></a><span data-ttu-id="3b9b9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b9b9-118">Requirements</span></span>



| <span data-ttu-id="3b9b9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b9b9-119">Requirement</span></span> | <span data-ttu-id="3b9b9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3b9b9-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9b9-121">Header</span><span class="sxs-lookup"><span data-stu-id="3b9b9-121">Header</span></span><br/> | <dl> <span data-ttu-id="3b9b9-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b9b9-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9b9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b9b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9b9-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="3b9b9-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3b9b9-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="3b9b9-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="3b9b9-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="3b9b9-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

