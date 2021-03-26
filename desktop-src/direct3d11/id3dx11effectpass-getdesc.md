---
title: ID3DX11EffectPass getdesc-Methode (D3dx11effect. h)
description: Eine Pass Beschreibung erhalten.
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- Getdesc-Methode Direct3D 11
- Getdesc-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, getdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a85a8c08faa100ecb3987a1a1421613d9c448b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355246"
---
# <a name="id3dx11effectpassgetdesc-method"></a><span data-ttu-id="b31a2-106">ID3DX11EffectPass:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="b31a2-106">ID3DX11EffectPass::GetDesc method</span></span>

<span data-ttu-id="b31a2-107">Eine Pass Beschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="b31a2-107">Get a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b31a2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b31a2-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="b31a2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b31a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b31a2-110">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="b31a2-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="b31a2-111">Typ: **[ **Bibliothek d3dx11 \_ Pass \_ DESC**](d3dx11-pass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="b31a2-111">Type: **[**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)\***</span></span>

<span data-ttu-id="b31a2-112">Ein Zeiger auf eine Pass Beschreibung (siehe [**Bibliothek d3dx11 \_ Pass \_**](d3dx11-pass-desc.md)Debug).</span><span class="sxs-lookup"><span data-stu-id="b31a2-112">A pointer to a pass description (see [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b31a2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b31a2-113">Return value</span></span>

<span data-ttu-id="b31a2-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b31a2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b31a2-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="b31a2-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b31a2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b31a2-116">Remarks</span></span>

<span data-ttu-id="b31a2-117">Ein Durchlauf ist ein Codeblock, der renderzustand und Shader festlegt (der wiederum Konstante Puffer, Samplern und Texturen festlegt).</span><span class="sxs-lookup"><span data-stu-id="b31a2-117">A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures).</span></span> <span data-ttu-id="b31a2-118">Ein Effekt Verfahren enthält einen oder mehrere Durchgänge.</span><span class="sxs-lookup"><span data-stu-id="b31a2-118">An effect technique contains one or more passes.</span></span>

> [!Note]  
> <span data-ttu-id="b31a2-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="b31a2-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b31a2-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b31a2-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b31a2-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b31a2-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b31a2-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b31a2-122">Requirements</span></span>



| <span data-ttu-id="b31a2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b31a2-123">Requirement</span></span> | <span data-ttu-id="b31a2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b31a2-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b31a2-125">Header</span><span class="sxs-lookup"><span data-stu-id="b31a2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b31a2-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b31a2-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b31a2-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b31a2-127">Library</span></span><br/> | <dl> <span data-ttu-id="b31a2-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="b31a2-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b31a2-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b31a2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b31a2-130">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="b31a2-130">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





