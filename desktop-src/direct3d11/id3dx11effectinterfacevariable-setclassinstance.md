---
title: ID3DX11EffectInterfaceVariable setclassinstance-Methode (D3dx11effect. h)
description: Legt eine Klasseninstanz fest.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Setclassinstance-Methode Direct3D 11
- Setclassinstance-Methode Direct3D 11, ID3DX11EffectInterfaceVariable-Schnittstelle
- ID3DX11EffectInterfaceVariable-Schnittstelle Direct3D 11, setclassinstance-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982275"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a><span data-ttu-id="8ba14-106">ID3DX11EffectInterfaceVariable:: setclassinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="8ba14-106">ID3DX11EffectInterfaceVariable::SetClassInstance method</span></span>

<span data-ttu-id="8ba14-107">Legt eine Klasseninstanz fest.</span><span class="sxs-lookup"><span data-stu-id="8ba14-107">Sets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba14-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ba14-108">Syntax</span></span>


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="8ba14-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ba14-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba14-110">*"Peer-ectclassinstance"*</span><span class="sxs-lookup"><span data-stu-id="8ba14-110">*pEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8ba14-111">Typ: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ba14-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="8ba14-112">Zeiger auf eine [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8ba14-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba14-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ba14-113">Return value</span></span>

<span data-ttu-id="8ba14-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ba14-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ba14-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="8ba14-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba14-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ba14-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ba14-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="8ba14-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8ba14-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8ba14-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8ba14-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8ba14-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ba14-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8ba14-120">Requirements</span></span>



| <span data-ttu-id="8ba14-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ba14-121">Requirement</span></span> | <span data-ttu-id="8ba14-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8ba14-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba14-123">Header</span><span class="sxs-lookup"><span data-stu-id="8ba14-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8ba14-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ba14-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8ba14-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ba14-125">Library</span></span><br/> | <dl> <span data-ttu-id="8ba14-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="8ba14-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ba14-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8ba14-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba14-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="8ba14-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





