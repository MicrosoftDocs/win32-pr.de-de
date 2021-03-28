---
title: ID3DX11EffectGroup getdesc-Methode (D3dx11effect. h)
description: Ruft eine Gruppenbeschreibung ab.
ms.assetid: 04bb707a-be21-43d1-8d9d-5a84d29fda74
keywords:
- Getdesc-Methode Direct3D 11
- Getdesc-Methode Direct3D 11, ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup-Schnittstelle Direct3D 11, getdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c32d44e215a6c89a7d71e899d9839509cbe39417
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961690"
---
# <a name="id3dx11effectgroupgetdesc-method"></a><span data-ttu-id="06eb4-106">ID3DX11EffectGroup:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="06eb4-106">ID3DX11EffectGroup::GetDesc method</span></span>

<span data-ttu-id="06eb4-107">Ruft eine Gruppenbeschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="06eb4-107">Gets a group description.</span></span>

## <a name="syntax"></a><span data-ttu-id="06eb4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06eb4-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_GROUP_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="06eb4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="06eb4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06eb4-110">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="06eb4-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="06eb4-111">Typ: **[ **Bibliothek d3dx11 \_ Group \_ DESC**](d3dx11-group-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="06eb4-111">Type: **[**D3DX11\_GROUP\_DESC**](d3dx11-group-desc.md)\***</span></span>

<span data-ttu-id="06eb4-112">Ein Zeiger auf eine [**Bibliothek d3dx11 \_ Group \_**](d3dx11-group-desc.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="06eb4-112">A pointer to a [**D3DX11\_GROUP\_DESC**](d3dx11-group-desc.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06eb4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06eb4-113">Return value</span></span>

<span data-ttu-id="06eb4-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06eb4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06eb4-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="06eb4-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="06eb4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06eb4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="06eb4-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="06eb4-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="06eb4-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="06eb4-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="06eb4-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="06eb4-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="06eb4-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="06eb4-120">Requirements</span></span>



| <span data-ttu-id="06eb4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06eb4-121">Requirement</span></span> | <span data-ttu-id="06eb4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="06eb4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06eb4-123">Header</span><span class="sxs-lookup"><span data-stu-id="06eb4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="06eb4-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="06eb4-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="06eb4-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06eb4-125">Library</span></span><br/> | <dl> <span data-ttu-id="06eb4-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="06eb4-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06eb4-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="06eb4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06eb4-128">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="06eb4-128">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

 





