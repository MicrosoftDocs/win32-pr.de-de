---
title: CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um die Stamm Signatur als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363183"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a><span data-ttu-id="f8390-104">CD3DX12 \_ Pipeline \_ State-Datenstrom Stamm \_ \_ \_ Signatur Struktur</span><span class="sxs-lookup"><span data-stu-id="f8390-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE structure</span></span>

<span data-ttu-id="f8390-105">Eine hilfsstruktur, die verwendet wird, um die Stamm Signatur als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f8390-105">A helper structure used to describe the root signature as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8390-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8390-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a><span data-ttu-id="f8390-107">Member</span><span class="sxs-lookup"><span data-stu-id="f8390-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8390-108">**CD3DX12 \_ Pipeline-Statusdaten Strom-Stamm \_ \_ \_ \_ Signatur**</span><span class="sxs-lookup"><span data-stu-id="f8390-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="f8390-109">Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 Pipeline- \_ Zustandsdaten Strom-Stamm \_ \_ \_ \_ Signatur.</span><span class="sxs-lookup"><span data-stu-id="f8390-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE.</span></span>

</dd> <dt>

<span data-ttu-id="f8390-110">**CD3DX12 \_ Pipeline-Statusdaten Strom-Stamm \_ \_ \_ \_ Signatur (ID3D12RootSignature-Konstante \* &i)**</span><span class="sxs-lookup"><span data-stu-id="f8390-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE(ID3D12RootSignature\* const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="f8390-111">Erstellt eine neue Instanz einer CD3DX12 \_ Pipeline- \_ Zustands \_ Datenstrom-Stamm \_ \_ Signatur, initialisiert mit einem untergeordneten Typ der Stamm Signatur des untergeordneten **D3D12 \_ Pipeline \_ State \_ \_ \_ \_** - *untergeordneten* Typs und aus einer [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) -Struktur kopierten untergeordneten Daten.</span><span class="sxs-lookup"><span data-stu-id="f8390-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_ROOT\_SIGNATURE** and subobject data copied from *i*, a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f8390-112">**Operator = (ID3D12RootSignature \* Konstanten& i)**</span><span class="sxs-lookup"><span data-stu-id="f8390-112">**operator=(ID3D12RootSignature\* const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="f8390-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="f8390-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="f8390-114">**Operator ID3D12RootSignature \* () konstant**</span><span class="sxs-lookup"><span data-stu-id="f8390-114">**operator ID3D12RootSignature\*() const**</span></span>
</dt> <dd>

<span data-ttu-id="f8390-115">Implizite Konvertierung in einen [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) -Struktur Zeiger.</span><span class="sxs-lookup"><span data-stu-id="f8390-115">Implicit conversion to a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8390-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8390-116">Remarks</span></span>

<span data-ttu-id="f8390-117">\_Die CD3DX12 \_ -Stamm \_ Signatur des Pipeline Zustands Stroms \_ \_ ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f8390-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
```



## <a name="requirements"></a><span data-ttu-id="f8390-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8390-118">Requirements</span></span>



| <span data-ttu-id="f8390-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8390-119">Requirement</span></span> | <span data-ttu-id="f8390-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f8390-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f8390-121">Header</span><span class="sxs-lookup"><span data-stu-id="f8390-121">Header</span></span><br/> | <dl> <span data-ttu-id="f8390-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8390-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8390-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8390-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8390-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="f8390-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f8390-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="f8390-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="f8390-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="f8390-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

