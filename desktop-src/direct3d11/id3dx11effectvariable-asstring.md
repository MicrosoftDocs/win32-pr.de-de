---
title: ID3DX11EffectVariable AsString-Methode (D3dx11effect. h)
description: Eine Zeichen folgen Variable erhalten.
ms.assetid: 60f8a730-bf95-4577-9259-7348d479ac3d
keywords:
- AsString-Methode Direct3D 11
- AsString-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, AsString-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73092dcd27b5651ad6205fa05bcbb13cc1f86116
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356146"
---
# <a name="id3dx11effectvariableasstring-method"></a><span data-ttu-id="1be62-106">ID3DX11EffectVariable:: AsString-Methode</span><span class="sxs-lookup"><span data-stu-id="1be62-106">ID3DX11EffectVariable::AsString method</span></span>

<span data-ttu-id="1be62-107">Eine Zeichen folgen Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="1be62-107">Get a string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="1be62-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1be62-108">Syntax</span></span>


```C++
ID3DX11EffectStringVariable* AsString();
```



## <a name="parameters"></a><span data-ttu-id="1be62-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1be62-109">Parameters</span></span>

<span data-ttu-id="1be62-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1be62-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1be62-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1be62-111">Return value</span></span>

<span data-ttu-id="1be62-112">Typ: **[ **ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="1be62-112">Type: **[**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***</span></span>

<span data-ttu-id="1be62-113">Ein Zeiger auf eine Zeichen folgen Variable.</span><span class="sxs-lookup"><span data-stu-id="1be62-113">A pointer to a string variable.</span></span> <span data-ttu-id="1be62-114">Siehe [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).</span><span class="sxs-lookup"><span data-stu-id="1be62-114">See [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1be62-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1be62-115">Remarks</span></span>

<span data-ttu-id="1be62-116">AsString gibt eine Version der Effekt Variablen zurück, die auf eine Zeichen folgen Variable spezialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1be62-116">AsString returns a version of the effect variable that has been specialized to a string variable.</span></span> <span data-ttu-id="1be62-117">Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effekt Variable keine Zeichen folgen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="1be62-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain string data.</span></span>

<span data-ttu-id="1be62-118">Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem Sie [**IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1be62-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="1be62-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="1be62-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1be62-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1be62-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1be62-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1be62-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1be62-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1be62-122">Requirements</span></span>



| <span data-ttu-id="1be62-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1be62-123">Requirement</span></span> | <span data-ttu-id="1be62-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1be62-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be62-125">Header</span><span class="sxs-lookup"><span data-stu-id="1be62-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1be62-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1be62-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1be62-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1be62-127">Library</span></span><br/> | <dl> <span data-ttu-id="1be62-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="1be62-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1be62-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1be62-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be62-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="1be62-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





