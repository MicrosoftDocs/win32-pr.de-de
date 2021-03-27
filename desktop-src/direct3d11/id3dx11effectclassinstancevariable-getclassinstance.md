---
title: ID3DX11EffectClassInstanceVariable getclassinstance-Methode (D3dx11effect. h)
description: Ruft eine-Klasseninstanz ab.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Getclassinstance-Methode Direct3D 11
- Getclassinstance-Methode Direct3D 11, ID3DX11EffectClassInstanceVariable-Schnittstelle
- ID3DX11EffectClassInstanceVariable-Schnittstelle Direct3D 11, getclassinstance-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dae96d42a0088adc683ca93d7e3215c12912a87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356037"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a><span data-ttu-id="507a1-106">ID3DX11EffectClassInstanceVariable:: getclassinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="507a1-106">ID3DX11EffectClassInstanceVariable::GetClassInstance method</span></span>

<span data-ttu-id="507a1-107">Ruft eine-Klasseninstanz ab.</span><span class="sxs-lookup"><span data-stu-id="507a1-107">Gets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="507a1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="507a1-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="507a1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="507a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="507a1-110">*ppclassinstance*</span><span class="sxs-lookup"><span data-stu-id="507a1-110">*ppClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="507a1-111">Typ: **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span><span class="sxs-lookup"><span data-stu-id="507a1-111">Type: **[**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span></span>

<span data-ttu-id="507a1-112">Zeiger auf einen [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) -Zeiger, der auf eine Klasseninstanz festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="507a1-112">Pointer to an [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointer that will be set to class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="507a1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="507a1-113">Return value</span></span>

<span data-ttu-id="507a1-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="507a1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="507a1-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="507a1-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="507a1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="507a1-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="507a1-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="507a1-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="507a1-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="507a1-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="507a1-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="507a1-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="507a1-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="507a1-120">Requirements</span></span>



| <span data-ttu-id="507a1-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="507a1-121">Requirement</span></span> | <span data-ttu-id="507a1-122">Wert</span><span class="sxs-lookup"><span data-stu-id="507a1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="507a1-123">Header</span><span class="sxs-lookup"><span data-stu-id="507a1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="507a1-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="507a1-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="507a1-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="507a1-125">Library</span></span><br/> | <dl> <span data-ttu-id="507a1-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="507a1-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="507a1-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="507a1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="507a1-128">ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="507a1-128">ID3DX11EffectClassInstanceVariable</span></span>](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





