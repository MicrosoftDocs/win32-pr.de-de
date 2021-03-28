---
title: ID3DX11EffectTechnique getdesc-Methode (D3dx11effect. h)
description: Hier finden Sie eine Technik Beschreibung.
ms.assetid: ed82d873-0540-4aa8-ac0f-198852b886ad
keywords:
- Getdesc-Methode Direct3D 11
- Getdesc-Methode Direct3D 11, ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11, getdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b847bd8381ec7d190931c04e5940f713676ff0b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995841"
---
# <a name="id3dx11effecttechniquegetdesc-method"></a><span data-ttu-id="3e509-106">ID3DX11EffectTechnique:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="3e509-106">ID3DX11EffectTechnique::GetDesc method</span></span>

<span data-ttu-id="3e509-107">Hier finden Sie eine Technik Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="3e509-107">Get a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e509-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e509-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_TECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="3e509-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e509-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e509-110">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="3e509-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="3e509-111">Type: **[ **Bibliothek d3dx11 \_ Technique ( \_ DESC** )](d3dx11-technique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e509-111">Type: **[**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)\***</span></span>

<span data-ttu-id="3e509-112">Ein Zeiger auf eine Technik Beschreibung (siehe [**Bibliothek d3dx11 \_ Technique \_**](d3dx11-technique-desc.md)Debug).</span><span class="sxs-lookup"><span data-stu-id="3e509-112">A pointer to a technique description (see [**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e509-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e509-113">Return value</span></span>

<span data-ttu-id="3e509-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e509-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e509-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="3e509-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e509-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e509-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3e509-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="3e509-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3e509-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e509-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3e509-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3e509-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e509-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3e509-120">Requirements</span></span>



| <span data-ttu-id="3e509-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e509-121">Requirement</span></span> | <span data-ttu-id="3e509-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3e509-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e509-123">Header</span><span class="sxs-lookup"><span data-stu-id="3e509-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3e509-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e509-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3e509-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e509-125">Library</span></span><br/> | <dl> <span data-ttu-id="3e509-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="3e509-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e509-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3e509-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e509-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="3e509-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 





