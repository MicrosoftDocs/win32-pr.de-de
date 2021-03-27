---
title: ID3DX11EffectVariable asinterface-Methode (D3dx11effect. h)
description: Eine Schnittstellen Variable erhalten.
ms.assetid: 5b1e5d05-ab36-42c2-9990-154baff5e9a4
keywords:
- Asinterface-Methode Direct3D 11
- Asinterface-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, asinterface-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsInterface
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0134aceea3202e0965bf05b709d29279be2fc29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761937"
---
# <a name="id3dx11effectvariableasinterface-method"></a><span data-ttu-id="96a3a-106">ID3DX11EffectVariable:: asinterface-Methode</span><span class="sxs-lookup"><span data-stu-id="96a3a-106">ID3DX11EffectVariable::AsInterface method</span></span>

<span data-ttu-id="96a3a-107">Eine Schnittstellen Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="96a3a-107">Get an interface variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a3a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="96a3a-108">Syntax</span></span>


```C++
ID3DX11EffectInterfaceVariable* AsInterface();
```



## <a name="parameters"></a><span data-ttu-id="96a3a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="96a3a-109">Parameters</span></span>

<span data-ttu-id="96a3a-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="96a3a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96a3a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96a3a-111">Return value</span></span>

<span data-ttu-id="96a3a-112">Typ: **[ **ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="96a3a-112">Type: **[**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***</span></span>

<span data-ttu-id="96a3a-113">Ein Zeiger auf eine Schnittstellen Variable.</span><span class="sxs-lookup"><span data-stu-id="96a3a-113">A pointer to an interface variable.</span></span> <span data-ttu-id="96a3a-114">Siehe [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md).</span><span class="sxs-lookup"><span data-stu-id="96a3a-114">See [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="96a3a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96a3a-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="96a3a-116">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="96a3a-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="96a3a-117">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="96a3a-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="96a3a-118">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="96a3a-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96a3a-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="96a3a-119">Requirements</span></span>



| <span data-ttu-id="96a3a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96a3a-120">Requirement</span></span> | <span data-ttu-id="96a3a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="96a3a-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a3a-122">Header</span><span class="sxs-lookup"><span data-stu-id="96a3a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="96a3a-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="96a3a-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="96a3a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96a3a-124">Library</span></span><br/> | <dl> <span data-ttu-id="96a3a-125"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="96a3a-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96a3a-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="96a3a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a3a-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="96a3a-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





