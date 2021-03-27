---
title: ID3DX11EffectInterfaceVariable getclassinstance-Methode (D3dx11effect. h)
description: Eine Klasseninstanz erhalten.
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- Getclassinstance-Methode Direct3D 11
- Getclassinstance-Methode Direct3D 11, ID3DX11EffectInterfaceVariable-Schnittstelle
- ID3DX11EffectInterfaceVariable-Schnittstelle Direct3D 11, getclassinstance-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f729da6ee84d76dd37a40a7946438e367c1a4cbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961667"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a><span data-ttu-id="f45e1-106">ID3DX11EffectInterfaceVariable:: getclassinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="f45e1-106">ID3DX11EffectInterfaceVariable::GetClassInstance method</span></span>

<span data-ttu-id="f45e1-107">Eine Klasseninstanz erhalten.</span><span class="sxs-lookup"><span data-stu-id="f45e1-107">Get a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="f45e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f45e1-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="f45e1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f45e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f45e1-110">*ppeer-ectclassinstance*</span><span class="sxs-lookup"><span data-stu-id="f45e1-110">*ppEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f45e1-111">Typ: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f45e1-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span></span>

<span data-ttu-id="f45e1-112">Zeiger auf einen [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) -Zeiger, der auf die-Klasseninstanz festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f45e1-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) pointer that will be set to the class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f45e1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f45e1-113">Return value</span></span>

<span data-ttu-id="f45e1-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f45e1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f45e1-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="f45e1-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f45e1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f45e1-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f45e1-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="f45e1-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f45e1-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f45e1-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f45e1-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f45e1-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f45e1-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f45e1-120">Requirements</span></span>



| <span data-ttu-id="f45e1-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f45e1-121">Requirement</span></span> | <span data-ttu-id="f45e1-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f45e1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f45e1-123">Header</span><span class="sxs-lookup"><span data-stu-id="f45e1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f45e1-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f45e1-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f45e1-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f45e1-125">Library</span></span><br/> | <dl> <span data-ttu-id="f45e1-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="f45e1-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f45e1-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f45e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f45e1-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="f45e1-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





