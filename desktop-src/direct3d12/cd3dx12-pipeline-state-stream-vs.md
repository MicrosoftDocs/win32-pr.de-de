---
title: CD3DX12_PIPELINE_STATE_STREAM_VS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um einen Vertexshader als ein einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_VS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ea426c857893b98b25792ecc8e6c3d5803546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354989"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a><span data-ttu-id="c3e07-104">CD3DX12 \_ Pipeline \_ State- \_ Stream im Vergleich zu \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="c3e07-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_VS structure</span></span>

<span data-ttu-id="c3e07-105">Eine hilfsstruktur, die verwendet wird, um einen Vertexshader als ein einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c3e07-105">A helper structure used to describe a vertex shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3e07-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3e07-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_VS {
                                   CD3DX12_PIPELINE_STATE_STREAM_VS;
                                   CD3DX12_PIPELINE_STATE_STREAM_VS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_VS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="c3e07-107">Member</span><span class="sxs-lookup"><span data-stu-id="c3e07-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3e07-108">**CD3DX12 \_ Pipeline \_ State \_ Stream im \_ Vergleich zu**</span><span class="sxs-lookup"><span data-stu-id="c3e07-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>
</dt> <dd>

<span data-ttu-id="c3e07-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Pipeline State- \_ \_ Streams im \_ Vergleich zu</span><span class="sxs-lookup"><span data-stu-id="c3e07-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_VS.</span></span>

</dd> <dt>

<span data-ttu-id="c3e07-110">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ vs (D3D12 \_ Shader \_ Bytecode const &i)**</span><span class="sxs-lookup"><span data-stu-id="c3e07-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="c3e07-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline- \_ Zustands \_ \_ Datenstroms im Vergleich zu einer Initialisierung mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ vs** und unter Objekt-Daten, die aus *i* kopiert wurden, einer [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3e07-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_VS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_VS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c3e07-112">**Operator = (D3D12 \_ Shader \_ Bytecode Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="c3e07-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="c3e07-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="c3e07-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="c3e07-114">**Operator D3D12 \_ Shader \_ Bytecode () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="c3e07-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="c3e07-115">Implizite Konvertierung in eine [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c3e07-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3e07-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3e07-116">Remarks</span></span>

<span data-ttu-id="c3e07-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ vs ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="c3e07-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_VS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
```



## <a name="requirements"></a><span data-ttu-id="c3e07-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3e07-118">Requirements</span></span>



| <span data-ttu-id="c3e07-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3e07-119">Requirement</span></span> | <span data-ttu-id="c3e07-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c3e07-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e07-121">Header</span><span class="sxs-lookup"><span data-stu-id="c3e07-121">Header</span></span><br/> | <dl> <span data-ttu-id="c3e07-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3e07-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3e07-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3e07-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3e07-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="c3e07-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c3e07-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="c3e07-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="c3e07-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="c3e07-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

