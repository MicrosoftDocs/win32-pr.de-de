---
title: ID3DX11EffectStringVariable getStringArray-Methode (D3dx11effect. h)
description: Ein Array von Zeichen folgen erhalten.
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- GetStringArray-Methode Direct3D 11
- GetStringArray-Methode Direct3D 11, ID3DX11EffectStringVariable-Schnittstelle
- ID3DX11EffectStringVariable-Schnittstelle Direct3D 11, getStringArray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2050ebd7c9ae3735385a379e6ef7bdff0e1cfd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982138"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a><span data-ttu-id="5dfc7-106">ID3DX11EffectStringVariable:: getStringArray-Methode</span><span class="sxs-lookup"><span data-stu-id="5dfc7-106">ID3DX11EffectStringVariable::GetStringArray method</span></span>

<span data-ttu-id="5dfc7-107">Ein Array von Zeichen folgen erhalten.</span><span class="sxs-lookup"><span data-stu-id="5dfc7-107">Get an array of strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dfc7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dfc7-108">Syntax</span></span>


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a><span data-ttu-id="5dfc7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dfc7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dfc7-110">*ppstrings*</span><span class="sxs-lookup"><span data-stu-id="5dfc7-110">*ppStrings*</span></span> 
</dt> <dd>

<span data-ttu-id="5dfc7-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="5dfc7-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5dfc7-112">Ein Zeiger auf die erste Zeichenfolge im Array.</span><span class="sxs-lookup"><span data-stu-id="5dfc7-112">A pointer to the first string in the array.</span></span>

</dd> <dt>

<span data-ttu-id="5dfc7-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="5dfc7-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="5dfc7-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5dfc7-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5dfc7-115">Der Offset (in Anzahl von Zeichen folgen) zwischen dem Anfang des Arrays und der ersten zu ersetzenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5dfc7-115">The offset (in number of strings) between the start of the array and the first string to get.</span></span>

</dd> <dt>

<span data-ttu-id="5dfc7-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="5dfc7-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="5dfc7-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5dfc7-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5dfc7-118">Die Anzahl der Zeichen folgen im zurückgegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="5dfc7-118">The number of strings in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dfc7-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5dfc7-119">Return value</span></span>

<span data-ttu-id="5dfc7-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5dfc7-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5dfc7-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="5dfc7-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5dfc7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5dfc7-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5dfc7-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="5dfc7-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5dfc7-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5dfc7-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5dfc7-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5dfc7-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5dfc7-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5dfc7-126">Requirements</span></span>



| <span data-ttu-id="5dfc7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5dfc7-127">Requirement</span></span> | <span data-ttu-id="5dfc7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5dfc7-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dfc7-129">Header</span><span class="sxs-lookup"><span data-stu-id="5dfc7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5dfc7-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dfc7-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5dfc7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5dfc7-131">Library</span></span><br/> | <dl> <span data-ttu-id="5dfc7-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="5dfc7-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dfc7-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5dfc7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dfc7-134">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="5dfc7-134">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

