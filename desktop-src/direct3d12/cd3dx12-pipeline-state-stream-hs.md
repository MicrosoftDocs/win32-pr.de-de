---
title: CD3DX12_PIPELINE_STATE_STREAM_HS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um einen Hull-Shader als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.
ms.assetid: 4958161D-3E79-4227-ADD7-7F53E34B2175
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_HS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_HS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba94fa272a670a83547775a582c8be967eeb907e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361842"
---
# <a name="cd3dx12_pipeline_state_stream_hs-structure"></a><span data-ttu-id="299ac-104">CD3DX12 \_ Pipeline \_ State \_ Stream- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="299ac-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_HS structure</span></span>

<span data-ttu-id="299ac-105">Eine hilfsstruktur, die verwendet wird, um einen Hull-Shader als einzelnes Objekt zu beschreiben, das für eine streambeschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="299ac-105">A helper structure used to describe a hull shader as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="299ac-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="299ac-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_HS {
                                   CD3DX12_PIPELINE_STATE_STREAM_HS;
                                   CD3DX12_PIPELINE_STATE_STREAM_HS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_HS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a><span data-ttu-id="299ac-107">Member</span><span class="sxs-lookup"><span data-stu-id="299ac-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="299ac-108">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ HS**</span><span class="sxs-lookup"><span data-stu-id="299ac-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_HS**</span></span>
</dt> <dd>

<span data-ttu-id="299ac-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Pipeline- \_ \_ Zustandsdaten \_ Stroms \_ HS.</span><span class="sxs-lookup"><span data-stu-id="299ac-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_HS.</span></span>

</dd> <dt>

<span data-ttu-id="299ac-110">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ HS (D3D12 \_ Shader \_ Bytecode Konstanten &i)**</span><span class="sxs-lookup"><span data-stu-id="299ac-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_HS(D3D12\_SHADER\_BYTECODE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="299ac-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline- \_ Zustands \_ \_ Datenstroms HS, initialisiert mit einem untergeordneten Typ von **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ HS** und aus *i* kopierter, einer [**D3D12 \_ Shader \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="299ac-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_HS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_HS** and subobject data copied from *i*, a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="299ac-112">**Operator = (D3D12 \_ Shader \_ Bytecode Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="299ac-112">**operator=(D3D12\_SHADER\_BYTECODE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="299ac-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="299ac-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="299ac-114">**Operator D3D12 \_ Shader \_ Bytecode () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="299ac-114">**operator D3D12\_SHADER\_BYTECODE() const**</span></span>
</dt> <dd>

<span data-ttu-id="299ac-115">Implizite Konvertierung in eine [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="299ac-115">Implicit conversion to a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="299ac-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="299ac-116">Remarks</span></span>

<span data-ttu-id="299ac-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ HS ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="299ac-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_HS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_HS>
    CD3DX12_PIPELINE_STATE_STREAM_HS;
          
```



## <a name="requirements"></a><span data-ttu-id="299ac-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="299ac-118">Requirements</span></span>



| <span data-ttu-id="299ac-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="299ac-119">Requirement</span></span> | <span data-ttu-id="299ac-120">Wert</span><span class="sxs-lookup"><span data-stu-id="299ac-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="299ac-121">Header</span><span class="sxs-lookup"><span data-stu-id="299ac-121">Header</span></span><br/> | <dl> <span data-ttu-id="299ac-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="299ac-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="299ac-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="299ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299ac-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="299ac-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="299ac-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="299ac-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="299ac-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="299ac-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

