---
title: ID3DX11EffectScalarVariable SetBool-Methode (D3dx11effect. h)
description: Legen Sie eine boolesche Variable fest.
ms.assetid: b5385ed3-6e65-4d65-bb8e-835967e6f610
keywords:
- SetBool-Methode Direct3D 11
- SetBool-Methode Direct3D 11, ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11, SetBool-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1d3670b3a41f47bf1b5ec7ac3d2fb93441e72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982413"
---
# <a name="id3dx11effectscalarvariablesetbool-method"></a><span data-ttu-id="ad27e-106">ID3DX11EffectScalarVariable:: SetBool-Methode</span><span class="sxs-lookup"><span data-stu-id="ad27e-106">ID3DX11EffectScalarVariable::SetBool method</span></span>

<span data-ttu-id="ad27e-107">Legen Sie eine boolesche Variable fest.</span><span class="sxs-lookup"><span data-stu-id="ad27e-107">Set a boolean variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad27e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad27e-108">Syntax</span></span>


```C++
HRESULT SetBool(
   BOOL Value
);
```



## <a name="parameters"></a><span data-ttu-id="ad27e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad27e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad27e-110">*Wert*</span><span class="sxs-lookup"><span data-stu-id="ad27e-110">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="ad27e-111">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ad27e-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ad27e-112">Ein Zeiger auf die Variable.</span><span class="sxs-lookup"><span data-stu-id="ad27e-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad27e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad27e-113">Return value</span></span>

<span data-ttu-id="ad27e-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad27e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad27e-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="ad27e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad27e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad27e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ad27e-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="ad27e-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ad27e-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad27e-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ad27e-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ad27e-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad27e-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ad27e-120">Requirements</span></span>



| <span data-ttu-id="ad27e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad27e-121">Requirement</span></span> | <span data-ttu-id="ad27e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ad27e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad27e-123">Header</span><span class="sxs-lookup"><span data-stu-id="ad27e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ad27e-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad27e-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ad27e-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ad27e-125">Library</span></span><br/> | <dl> <span data-ttu-id="ad27e-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="ad27e-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad27e-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad27e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad27e-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="ad27e-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

