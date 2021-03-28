---
title: ID3DX11EffectVariable asclassinstance-Methode (D3dx11effect. h)
description: Eine Klasseninstanz-Variable erhalten.
ms.assetid: c1d4adb5-7cd2-4ba2-9a91-3d03f9596a10
keywords:
- Asclassinstance-Methode Direct3D 11
- Asclassinstance-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, asclassinstance-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17dc9124f4b9a24ead503694c10a4a2d2205ed3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995806"
---
# <a name="id3dx11effectvariableasclassinstance-method"></a><span data-ttu-id="d9dde-106">ID3DX11EffectVariable:: asclassinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="d9dde-106">ID3DX11EffectVariable::AsClassInstance method</span></span>

<span data-ttu-id="d9dde-107">Eine Klasseninstanz-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9dde-107">Get a class-instance variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9dde-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9dde-108">Syntax</span></span>


```C++
ID3DX11EffectClassInstanceVariable* AsClassInstance();
```



## <a name="parameters"></a><span data-ttu-id="d9dde-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9dde-109">Parameters</span></span>

<span data-ttu-id="d9dde-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d9dde-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9dde-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9dde-111">Return value</span></span>

<span data-ttu-id="d9dde-112">Typ: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9dde-112">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="d9dde-113">Ein Zeiger auf eine Klasseninstanzvariable.</span><span class="sxs-lookup"><span data-stu-id="d9dde-113">A pointer to class-instance variable.</span></span> <span data-ttu-id="d9dde-114">Siehe [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md).</span><span class="sxs-lookup"><span data-stu-id="d9dde-114">See [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9dde-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9dde-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d9dde-116">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="d9dde-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d9dde-117">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d9dde-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d9dde-118">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d9dde-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d9dde-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d9dde-119">Requirements</span></span>



| <span data-ttu-id="d9dde-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9dde-120">Requirement</span></span> | <span data-ttu-id="d9dde-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d9dde-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9dde-122">Header</span><span class="sxs-lookup"><span data-stu-id="d9dde-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d9dde-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9dde-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d9dde-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9dde-124">Library</span></span><br/> | <dl> <span data-ttu-id="d9dde-125"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="d9dde-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9dde-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d9dde-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9dde-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="d9dde-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





