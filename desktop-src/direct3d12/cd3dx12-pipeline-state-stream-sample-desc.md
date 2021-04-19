---
title: CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um eine Beispiel Beschreibung als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351988"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a><span data-ttu-id="f34dd-104">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample ( \_ DESC-Struktur)</span><span class="sxs-lookup"><span data-stu-id="f34dd-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC structure</span></span>

<span data-ttu-id="f34dd-105">Eine hilfsstruktur, die verwendet wird, um eine Beispiel Beschreibung als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f34dd-105">A helper structure used to describe a sample description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f34dd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f34dd-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="f34dd-107">Member</span><span class="sxs-lookup"><span data-stu-id="f34dd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f34dd-108">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="f34dd-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="f34dd-109">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="f34dd-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="f34dd-110">**CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC (DXGI \_ Sample \_ DESC resc &i)**</span><span class="sxs-lookup"><span data-stu-id="f34dd-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC(DXGI\_SAMPLE\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="f34dd-111">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC, initialisiert with a unter Objekt Type of **D3D12 \_ Pipeline \_ State \_ unter Objekt \_ Type \_ Sample \_ DESC** and unter Objekt Data kopiert from *i*, a [**DXGI \_ Sample \_ DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) Structure.</span><span class="sxs-lookup"><span data-stu-id="f34dd-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_DESC** and subobject data copied from *i*, a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f34dd-112">**Operator = (DXGI \_ Sample \_& i)**</span><span class="sxs-lookup"><span data-stu-id="f34dd-112">**operator=(DXGI\_SAMPLE\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="f34dd-113">Kopier Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="f34dd-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="f34dd-114">**Operator DXGI \_ Sample Debug \_ () Konstanten**</span><span class="sxs-lookup"><span data-stu-id="f34dd-114">**operator DXGI\_SAMPLE\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="f34dd-115">Implizite Konvertierung in eine [**DXGI \_ - \_ Beispiel**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f34dd-115">Implicit conversion to a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f34dd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f34dd-116">Remarks</span></span>

<span data-ttu-id="f34dd-117">CD3DX12 \_ Pipeline \_ State \_ Stream \_ Sample \_ DESC ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f34dd-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="f34dd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f34dd-118">Requirements</span></span>



| <span data-ttu-id="f34dd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f34dd-119">Requirement</span></span> | <span data-ttu-id="f34dd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f34dd-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f34dd-121">Header</span><span class="sxs-lookup"><span data-stu-id="f34dd-121">Header</span></span><br/> | <dl> <span data-ttu-id="f34dd-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f34dd-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f34dd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f34dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f34dd-124">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="f34dd-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f34dd-125">**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="f34dd-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="f34dd-126">**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="f34dd-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

