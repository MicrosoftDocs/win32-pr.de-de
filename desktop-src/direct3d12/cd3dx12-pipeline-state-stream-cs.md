---
title: CD3DX12_PIPELINE_STATE_STREAM_CS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die zum Beschreiben eines Compute-Shaders als einzelnes Objekt verwendet wird, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: B76B0CB4-FC76-4C5B-84FC-DCFF907BE2F8
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_CS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5796e0f96ad4e2a87d2a45519321c363078a34b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373489"
---
# <a name="cd3dx12_pipeline_state_stream_cs-structure"></a><span data-ttu-id="d5ec0-104">CD3DX12 \_ Pipeline \_ State \_ Stream \_ CS-Struktur</span><span class="sxs-lookup"><span data-stu-id="d5ec0-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_CS structure</span></span>

<span data-ttu-id="d5ec0-105">Eine hilfsstruktur, die zum Beschreiben eines Compute-Shaders als einzelnes Objekt verwendet wird, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="d5ec0-105">A helper structure used to describe a compute shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ec0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5ec0-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CS {
                                   CD3DX12_PIPELINE_STATE_STREAM_CS;
                                   CD3DX12_PIPELINE_STATE_STREAM_CS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="d5ec0-107">Member</span><span class="sxs-lookup"><span data-stu-id="d5ec0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d5ec0-108">**CD3DX12- \_ Pipeline- \_ Stream- \_ \_ Datenstrom**</span><span class="sxs-lookup"><span data-stu-id="d5ec0-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>
</dt> <dd>

<span data-ttu-id="d5ec0-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Pipeline- \_ State-Stream- \_ \_ cs.</span><span class="sxs-lookup"><span data-stu-id="d5ec0-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CS.</span></span>

</dd> <dt>

<span data-ttu-id="d5ec0-110">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ cs (D3D12 \_ Shader \_ Bytecode Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="d5ec0-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="d5ec0-111">Erstellt eine neue Instanz eines CD3DX12 \_ -Pipeline \_ -State- \_ Stream \_ -cs, initialisiert mit einem untergeordneten Typ von **D3D12 Pipeline State-untergeordneten \_ \_ Typ- \_ \_ \_ CS** und unter aus *i* kopierten Daten, einer [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d5ec0-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_CS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d5ec0-112">**Operator = (D3D12 \_ Shader \_ Bytecode Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="d5ec0-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="d5ec0-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="d5ec0-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="d5ec0-114">**Operator D3D12 \_ Shader \_ Bytecode () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="d5ec0-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="d5ec0-115">Implizite Konvertierung in eine [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d5ec0-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5ec0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5ec0-116">Remarks</span></span>

<span data-ttu-id="d5ec0-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ CS ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="d5ec0-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_CS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CS>
    CD3DX12_PIPELINE_STATE_STREAM_CS;
          
```



## <a name="requirements"></a><span data-ttu-id="d5ec0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5ec0-118">Requirements</span></span>



| <span data-ttu-id="d5ec0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5ec0-119">Requirement</span></span> | <span data-ttu-id="d5ec0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d5ec0-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ec0-121">Header</span><span class="sxs-lookup"><span data-stu-id="d5ec0-121">Header</span></span><br/> | <dl> <span data-ttu-id="d5ec0-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ec0-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5ec0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5ec0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ec0-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="d5ec0-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d5ec0-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="d5ec0-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="d5ec0-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="d5ec0-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

