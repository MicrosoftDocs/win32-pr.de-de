---
title: CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um ein Eingabe Layout als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366622"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a><span data-ttu-id="a004e-104">CD3DX12 \_ Pipeline \_ State \_ Stream- \_ Eingabe \_ Layout-Struktur</span><span class="sxs-lookup"><span data-stu-id="a004e-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT structure</span></span>

<span data-ttu-id="a004e-105">Eine hilfsstruktur, die verwendet wird, um ein Eingabe Layout als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="a004e-105">A helper structure used to describe an input layout as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a004e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a004e-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="a004e-107">Member</span><span class="sxs-lookup"><span data-stu-id="a004e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a004e-108">**CD3DX12 \_ - \_ \_ \_ Eingabe \_ Layout des Pipeline Zustandsdaten Stroms**</span><span class="sxs-lookup"><span data-stu-id="a004e-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>
</dt> <dd>

<span data-ttu-id="a004e-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Pipeline- \_ Zustandsdaten Strom- \_ \_ Eingabe \_ Layouts.</span><span class="sxs-lookup"><span data-stu-id="a004e-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT.</span></span>

</dd> <dt>

<span data-ttu-id="a004e-110">**CD3DX12 \_ - \_ Eingabe Layout für Pipeline Zustandsdaten \_ Strom \_ \_ (D3D12 \_ input \_ Layout \_ DESC Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="a004e-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT(D3D12\_INPUT\_LAYOUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="a004e-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline- \_ Zustands \_ Datenstrom- \_ Eingabe \_ Layouts, initialisiert mit einem untergeordneten Typ **des \_ \_ \_ \_ \_ Eingabe \_ Layouts von D3D12-Pipeline** Zuständen und untergeordneten Objekten, die aus *i* kopiert wurden, einer [**D3D12- \_ Eingabe Layout- \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a004e-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_INPUT\_LAYOUT** and subobject data copied from *i*, a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a004e-112">**Operator = (D3D12 \_ input \_ Layout \_ resc Konstante& i)**</span><span class="sxs-lookup"><span data-stu-id="a004e-112">**operator=(D3D12\_INPUT\_LAYOUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="a004e-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="a004e-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="a004e-114">**Operator D3D12 \_ Eingabe \_ Layout \_ () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="a004e-114">**operator D3D12\_INPUT\_LAYOUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="a004e-115">Implizite Konvertierung in eine [**D3D12 \_ - \_ Eingabe \_ Layout**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a004e-115">Implicit conversion to a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a004e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a004e-116">Remarks</span></span>

<span data-ttu-id="a004e-117">CD3DX12 \_ \_ \_ \_ -Eingabe Layout des Pipeline Zustandsdaten Stroms \_ ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="a004e-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
```



## <a name="requirements"></a><span data-ttu-id="a004e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a004e-118">Requirements</span></span>



| <span data-ttu-id="a004e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a004e-119">Requirement</span></span> | <span data-ttu-id="a004e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a004e-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a004e-121">Header</span><span class="sxs-lookup"><span data-stu-id="a004e-121">Header</span></span><br/> | <dl> <span data-ttu-id="a004e-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a004e-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a004e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a004e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a004e-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="a004e-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a004e-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="a004e-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="a004e-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="a004e-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

