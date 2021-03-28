---
title: ID3DX11EffectScalarVariable GetFloat-Methode (D3dx11effect. h)
description: Eine Gleit Komma Variable erhalten.
ms.assetid: 0416db40-5e70-44e4-905f-86f49a9b58b8
keywords:
- GetFloat-Methode Direct3D 11
- GetFloat-Methode Direct3D 11, ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11, GetFloat-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1d8f7ae63bc8312c2432e50f5b6dcfeccdf525
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355746"
---
# <a name="id3dx11effectscalarvariablegetfloat-method"></a><span data-ttu-id="d651a-106">ID3DX11EffectScalarVariable:: GetFloat-Methode</span><span class="sxs-lookup"><span data-stu-id="d651a-106">ID3DX11EffectScalarVariable::GetFloat method</span></span>

<span data-ttu-id="d651a-107">Eine Gleit Komma Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="d651a-107">Get a floating-point variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d651a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d651a-108">Syntax</span></span>


```C++
HRESULT GetFloat(
   float *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="d651a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d651a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d651a-110">*pValue*</span><span class="sxs-lookup"><span data-stu-id="d651a-110">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="d651a-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="d651a-111">Type: **float\***</span></span>

<span data-ttu-id="d651a-112">Ein Zeiger auf die Variable.</span><span class="sxs-lookup"><span data-stu-id="d651a-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d651a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d651a-113">Return value</span></span>

<span data-ttu-id="d651a-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d651a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d651a-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="d651a-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d651a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d651a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d651a-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="d651a-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d651a-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d651a-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d651a-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d651a-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d651a-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d651a-120">Requirements</span></span>



| <span data-ttu-id="d651a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d651a-121">Requirement</span></span> | <span data-ttu-id="d651a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d651a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d651a-123">Header</span><span class="sxs-lookup"><span data-stu-id="d651a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d651a-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d651a-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d651a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d651a-125">Library</span></span><br/> | <dl> <span data-ttu-id="d651a-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="d651a-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d651a-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d651a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d651a-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="d651a-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





