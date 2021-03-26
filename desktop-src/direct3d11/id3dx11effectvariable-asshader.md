---
title: ID3DX11EffectVariable asshader-Methode (D3dx11effect. h)
description: Eine shadervariable erhalten.
ms.assetid: 660ba087-5320-44f7-946f-e500101fc6bb
keywords:
- Asshader-Methode Direct3D 11
- Asshader-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable Interface Direct3D 11, asshader-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c8d9f1a487e4003bd032180d1f815e4a48fe0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996075"
---
# <a name="id3dx11effectvariableasshader-method"></a><span data-ttu-id="95d85-106">ID3DX11EffectVariable:: asshader-Methode</span><span class="sxs-lookup"><span data-stu-id="95d85-106">ID3DX11EffectVariable::AsShader method</span></span>

<span data-ttu-id="95d85-107">Eine shadervariable erhalten.</span><span class="sxs-lookup"><span data-stu-id="95d85-107">Get a shader variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d85-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="95d85-108">Syntax</span></span>


```C++
ID3DX11EffectShaderVariable* AsShader();
```



## <a name="parameters"></a><span data-ttu-id="95d85-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="95d85-109">Parameters</span></span>

<span data-ttu-id="95d85-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="95d85-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95d85-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95d85-111">Return value</span></span>

<span data-ttu-id="95d85-112">Typ: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="95d85-112">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

<span data-ttu-id="95d85-113">Ein Zeiger auf eine shadervariable.</span><span class="sxs-lookup"><span data-stu-id="95d85-113">A pointer to a shader variable.</span></span> <span data-ttu-id="95d85-114">Siehe [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md).</span><span class="sxs-lookup"><span data-stu-id="95d85-114">See [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95d85-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95d85-115">Remarks</span></span>

<span data-ttu-id="95d85-116">Asshader gibt eine Version der Effekt Variablen zurück, die auf eine Shader-Variable spezialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="95d85-116">AsShader returns a version of the effect variable that has been specialized to a shader variable.</span></span> <span data-ttu-id="95d85-117">Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effekt Variable keine shaderdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="95d85-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader data.</span></span>

<span data-ttu-id="95d85-118">Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem Sie [**IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="95d85-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="95d85-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="95d85-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="95d85-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="95d85-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="95d85-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="95d85-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95d85-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="95d85-122">Requirements</span></span>



| <span data-ttu-id="95d85-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95d85-123">Requirement</span></span> | <span data-ttu-id="95d85-124">Wert</span><span class="sxs-lookup"><span data-stu-id="95d85-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d85-125">Header</span><span class="sxs-lookup"><span data-stu-id="95d85-125">Header</span></span><br/>  | <dl> <span data-ttu-id="95d85-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d85-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="95d85-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95d85-127">Library</span></span><br/> | <dl> <span data-ttu-id="95d85-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="95d85-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d85-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="95d85-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d85-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="95d85-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





