---
title: ID3DX11EffectVariable asconstantbuffer-Methode (D3dx11effect. h)
description: Einen konstanten Puffer erhalten. | ID3DX11EffectVariable asconstantbuffer-Methode (D3dx11effect. h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Asconstantbuffer-Methode Direct3D 11
- Asconstantbuffer-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, asconstantbuffer-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4caca60216df0c04a773da22150dbc6f7be717
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995919"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a><span data-ttu-id="cf609-107">ID3DX11EffectVariable:: asconstantbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="cf609-107">ID3DX11EffectVariable::AsConstantBuffer method</span></span>

<span data-ttu-id="cf609-108">Einen konstanten Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf609-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf609-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf609-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="cf609-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf609-110">Parameters</span></span>

<span data-ttu-id="cf609-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cf609-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf609-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf609-112">Return value</span></span>

<span data-ttu-id="cf609-113">Typ: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf609-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="cf609-114">Ein Zeiger auf einen konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="cf609-114">A pointer to a constant buffer.</span></span> <span data-ttu-id="cf609-115">Siehe [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="cf609-115">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf609-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf609-116">Remarks</span></span>

<span data-ttu-id="cf609-117">Asconstantbuffer gibt eine Version der Effekt Variablen zurück, die auf einen konstanten Puffer spezialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cf609-117">AsConstantBuffer returns a version of the effect variable that has been specialized to a constant buffer.</span></span> <span data-ttu-id="cf609-118">Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effekt Variable keine Konstanten Puffer Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="cf609-118">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain constant buffer data.</span></span>

<span data-ttu-id="cf609-119">Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem Sie [**IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cf609-119">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="cf609-120">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="cf609-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cf609-121">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf609-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cf609-122">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cf609-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf609-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cf609-123">Requirements</span></span>



| <span data-ttu-id="cf609-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf609-124">Requirement</span></span> | <span data-ttu-id="cf609-125">Wert</span><span class="sxs-lookup"><span data-stu-id="cf609-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf609-126">Header</span><span class="sxs-lookup"><span data-stu-id="cf609-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cf609-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf609-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cf609-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf609-128">Library</span></span><br/> | <dl> <span data-ttu-id="cf609-129"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="cf609-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf609-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cf609-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf609-131">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="cf609-131">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





