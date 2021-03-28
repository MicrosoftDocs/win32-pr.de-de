---
title: ID3DX11EffectVariable asshaderresource-Methode (D3dx11effect. h)
description: Eine Shader-Resource-Variable erhalten.
ms.assetid: 02db94eb-980a-4677-af89-3006aef6faca
keywords:
- Asshaderresource-Methode Direct3D 11
- Asshaderresource-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, asshaderresource-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShaderResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3af6236d25e8a2c652f5a551bf7199f3a78d8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996314"
---
# <a name="id3dx11effectvariableasshaderresource-method"></a><span data-ttu-id="88fa6-106">ID3DX11EffectVariable:: asshaderresource-Methode</span><span class="sxs-lookup"><span data-stu-id="88fa6-106">ID3DX11EffectVariable::AsShaderResource method</span></span>

<span data-ttu-id="88fa6-107">Eine Shader-Resource-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="88fa6-107">Get a shader-resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="88fa6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="88fa6-108">Syntax</span></span>


```C++
ID3DX11EffectShaderResourceVariable* AsShaderResource();
```



## <a name="parameters"></a><span data-ttu-id="88fa6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="88fa6-109">Parameters</span></span>

<span data-ttu-id="88fa6-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="88fa6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88fa6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88fa6-111">Return value</span></span>

<span data-ttu-id="88fa6-112">Typ: **[ **ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="88fa6-112">Type: **[**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***</span></span>

<span data-ttu-id="88fa6-113">Ein Zeiger auf eine Shader-Resource-Variable.</span><span class="sxs-lookup"><span data-stu-id="88fa6-113">A pointer to a shader-resource variable.</span></span> <span data-ttu-id="88fa6-114">Siehe [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).</span><span class="sxs-lookup"><span data-stu-id="88fa6-114">See [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="88fa6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88fa6-115">Remarks</span></span>

<span data-ttu-id="88fa6-116">Asshaderresource gibt eine Version der Effekt Variablen zurück, die auf eine Shader-Resource-Variable spezialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="88fa6-116">AsShaderResource returns a version of the effect variable that has been specialized to a shader-resource variable.</span></span> <span data-ttu-id="88fa6-117">Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effekt Variable keine Shader-Ressourcen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="88fa6-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader-resource data.</span></span>

<span data-ttu-id="88fa6-118">Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem Sie [**IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="88fa6-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="88fa6-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="88fa6-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="88fa6-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="88fa6-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="88fa6-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="88fa6-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88fa6-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="88fa6-122">Requirements</span></span>



| <span data-ttu-id="88fa6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88fa6-123">Requirement</span></span> | <span data-ttu-id="88fa6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="88fa6-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88fa6-125">Header</span><span class="sxs-lookup"><span data-stu-id="88fa6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="88fa6-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="88fa6-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="88fa6-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88fa6-127">Library</span></span><br/> | <dl> <span data-ttu-id="88fa6-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="88fa6-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88fa6-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88fa6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88fa6-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="88fa6-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





