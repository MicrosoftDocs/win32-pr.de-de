---
title: ID3DX11Effect getdesc-Methode (D3dx11effect. h)
description: Sie erhalten eine Beschreibung des Effekts.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Getdesc-Methode Direct3D 11
- Getdesc-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, getdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996123"
---
# <a name="id3dx11effectgetdesc-method"></a><span data-ttu-id="4ae03-106">ID3DX11Effect:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="4ae03-106">ID3DX11Effect::GetDesc method</span></span>

<span data-ttu-id="4ae03-107">Sie erhalten eine Beschreibung des Effekts.</span><span class="sxs-lookup"><span data-stu-id="4ae03-107">Get an effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae03-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ae03-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="4ae03-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ae03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ae03-110">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="4ae03-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="4ae03-111">Type: **[ **Bibliothek d3dx11 \_ Effect \_ DESC**](d3dx11-effect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ae03-111">Type: **[**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)\***</span></span>

<span data-ttu-id="4ae03-112">Ein Zeiger auf eine Effekt Beschreibung (siehe [**Bibliothek d3dx11 \_ Effect \_ ensc**](d3dx11-effect-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="4ae03-112">A pointer to an effect description (see [**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ae03-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ae03-113">Return value</span></span>

<span data-ttu-id="4ae03-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ae03-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ae03-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="4ae03-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ae03-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ae03-116">Remarks</span></span>

<span data-ttu-id="4ae03-117">Eine Effekt Beschreibung enthält grundlegende Informationen zu einem Effekt, wie z. b. die darin enthaltenen Techniken und die erforderlichen Konstanten Puffer Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4ae03-117">An effect description contains basic information about an effect such as the techniques it contains and the constant buffer resources it requires.</span></span>

> [!Note]  
> <span data-ttu-id="4ae03-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="4ae03-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4ae03-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ae03-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4ae03-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4ae03-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ae03-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4ae03-121">Requirements</span></span>



| <span data-ttu-id="4ae03-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ae03-122">Requirement</span></span> | <span data-ttu-id="4ae03-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4ae03-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae03-124">Header</span><span class="sxs-lookup"><span data-stu-id="4ae03-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4ae03-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae03-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4ae03-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4ae03-126">Library</span></span><br/> | <dl> <span data-ttu-id="4ae03-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="4ae03-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ae03-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4ae03-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae03-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="4ae03-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





