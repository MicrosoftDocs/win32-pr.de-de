---
title: CD3DX12_PIPELINE_STATE_STREAM_DS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um einen Domänen-Shader als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist
ms.assetid: 42F8B7C1-B754-4B07-BF04-DBF450A942E6
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbae1d75894e1fb8ffaa5bf95a45cc1eb3b2d9f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371889"
---
# <a name="cd3dx12_pipeline_state_stream_ds-structure"></a><span data-ttu-id="326b3-104">CD3DX12 \_ Pipeline \_ State \_ Stream \_ DS-Struktur</span><span class="sxs-lookup"><span data-stu-id="326b3-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS structure</span></span>

<span data-ttu-id="326b3-105">Eine hilfsstruktur, die verwendet wird, um einen Domänen-Shader als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist</span><span class="sxs-lookup"><span data-stu-id="326b3-105">A helper structure used to describe a domain shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="326b3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="326b3-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DS {
                                   CD3DX12_PIPELINE_STATE_STREAM_DS;
                                   CD3DX12_PIPELINE_STATE_STREAM_DS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="326b3-107">Member</span><span class="sxs-lookup"><span data-stu-id="326b3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="326b3-108">**CD3DX12 \_ Pipeline \_ State- \_ Stream- \_ DS**</span><span class="sxs-lookup"><span data-stu-id="326b3-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>
</dt> <dd>

<span data-ttu-id="326b3-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Pipeline- \_ \_ Zustandsdaten \_ Stroms \_ DS.</span><span class="sxs-lookup"><span data-stu-id="326b3-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS.</span></span>

</dd> <dt>

<span data-ttu-id="326b3-110">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ DS (D3D12 \_ Shader \_ Bytecode Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="326b3-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="326b3-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ State- \_ Streams \_ , der mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ DS** initialisiert wurde, und aus untergeordneten Daten, die aus *i* kopiert wurden, einer [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="326b3-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="326b3-112">**Operator = (D3D12 \_ Shader \_ Bytecode Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="326b3-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="326b3-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="326b3-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="326b3-114">**Operator D3D12 \_ Shader \_ Bytecode () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="326b3-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="326b3-115">Implizite Konvertierung in eine [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="326b3-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="326b3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="326b3-116">Remarks</span></span>

<span data-ttu-id="326b3-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ DS ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="326b3-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DS>
    CD3DX12_PIPELINE_STATE_STREAM_DS;
          
```



## <a name="requirements"></a><span data-ttu-id="326b3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="326b3-118">Requirements</span></span>



| <span data-ttu-id="326b3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="326b3-119">Requirement</span></span> | <span data-ttu-id="326b3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="326b3-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="326b3-121">Header</span><span class="sxs-lookup"><span data-stu-id="326b3-121">Header</span></span><br/> | <dl> <span data-ttu-id="326b3-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="326b3-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="326b3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="326b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="326b3-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="326b3-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="326b3-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="326b3-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="326b3-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="326b3-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

