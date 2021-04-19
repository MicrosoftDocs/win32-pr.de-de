---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um das Format der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363960"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a><span data-ttu-id="11920-104">Struktur des CD3DX12-Daten \_ \_ Strom- \_ \_ tiefen \_ Schablonen \_ Formats</span><span class="sxs-lookup"><span data-stu-id="11920-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT structure</span></span>

<span data-ttu-id="11920-105">Eine hilfsstruktur, die verwendet wird, um das Format der tiefen Schablone als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="11920-105">A helper structure used to describe the depth stencil format as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="11920-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11920-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a><span data-ttu-id="11920-107">Member</span><span class="sxs-lookup"><span data-stu-id="11920-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="11920-108">**CD3DX12 \_ Daten \_ \_ Strom- \_ tiefen \_ Schablone- \_ Format des Pipeline Zustands**</span><span class="sxs-lookup"><span data-stu-id="11920-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="11920-109">Erstellt eine neue, nicht initialisierte Instanz des \_ tiefen Schablone-Formats eines CD3DX12 Pipeline \_ Zustandsdaten \_ Stroms \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="11920-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT.</span></span>

</dd> <dt>

<span data-ttu-id="11920-110">**CD3DX12-Daten \_ \_ Strom- \_ \_ tiefen Schablone- \_ \_ Format (DXGI-Format, Konstante \_ &i)**</span><span class="sxs-lookup"><span data-stu-id="11920-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT(DXGI\_FORMAT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="11920-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ \_ \_ \_ -tiefen Schablone \_ -Formats, das mit einem untergeordneten Typ des untergeordneten Typs **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ tiefen \_ Schablone \_ Format** und aus *i* kopierten untergeordneten Daten, einer [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="11920-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL\_FORMAT** and subobject data copied from *i*, a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="11920-112">**Operator = (DXGI- \_ Format Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="11920-112">**operator=(DXGI\_FORMAT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="11920-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="11920-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="11920-114">**Operator DXGI \_ Format () konstant**</span><span class="sxs-lookup"><span data-stu-id="11920-114">**operator DXGI\_FORMAT() const**</span></span>
</dt> <dd>

<span data-ttu-id="11920-115">Implizite Konvertierung in eine [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="11920-115">Implicit conversion to a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11920-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11920-116">Remarks</span></span>

<span data-ttu-id="11920-117">CD3DX12 \_ \_ \_ \_ \_ das tiefen Schablone \_ -Format des Pipeline Zustands Stroms ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="11920-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
```



## <a name="requirements"></a><span data-ttu-id="11920-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11920-118">Requirements</span></span>



| <span data-ttu-id="11920-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11920-119">Requirement</span></span> | <span data-ttu-id="11920-120">Wert</span><span class="sxs-lookup"><span data-stu-id="11920-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11920-121">Header</span><span class="sxs-lookup"><span data-stu-id="11920-121">Header</span></span><br/> | <dl> <span data-ttu-id="11920-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="11920-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11920-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11920-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11920-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="11920-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="11920-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="11920-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="11920-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="11920-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

