---
title: ID3DX11EffectDepthStencilViewVariable getdepthstencil-Methode (D3dx11effect. h)
description: Holen Sie sich eine tiefen Schablone-Ansichts Ressource.
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- Getdepthstencil-Methode Direct3D 11
- Getdepthstencil-Methode Direct3D 11, ID3DX11EffectDepthStencilViewVariable-Schnittstelle
- ID3DX11EffectDepthStencilViewVariable-Schnittstelle Direct3D 11, getdepthstencil-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49206f051922982ac77265e68fa3d7b7397d1348
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982449"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a><span data-ttu-id="cfb2b-106">ID3DX11EffectDepthStencilViewVariable:: getdepthstencil-Methode</span><span class="sxs-lookup"><span data-stu-id="cfb2b-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencil method</span></span>

<span data-ttu-id="cfb2b-107">Holen Sie sich eine tiefen Schablone-Ansichts Ressource.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-107">Get a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb2b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfb2b-108">Syntax</span></span>


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="cfb2b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfb2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb2b-110">*ppresource*</span><span class="sxs-lookup"><span data-stu-id="cfb2b-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb2b-111">Typ: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="cfb2b-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="cfb2b-112">Die Adresse eines Zeigers auf eine tiefen Schablone-Ansichts Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-112">The address of a pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="cfb2b-113">Siehe [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="cfb2b-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb2b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfb2b-114">Return value</span></span>

<span data-ttu-id="cfb2b-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cfb2b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cfb2b-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb2b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfb2b-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cfb2b-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cfb2b-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cfb2b-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cfb2b-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfb2b-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cfb2b-121">Requirements</span></span>



| <span data-ttu-id="cfb2b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfb2b-122">Requirement</span></span> | <span data-ttu-id="cfb2b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb2b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb2b-124">Header</span><span class="sxs-lookup"><span data-stu-id="cfb2b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cfb2b-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb2b-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cfb2b-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cfb2b-126">Library</span></span><br/> | <dl> <span data-ttu-id="cfb2b-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="cfb2b-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfb2b-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cfb2b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb2b-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="cfb2b-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





