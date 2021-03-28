---
title: ID3DX11EffectScalarVariable getfloatarray-Methode (D3dx11effect. h)
description: Ein Array von Gleit Komma Variablen erhalten.
ms.assetid: e5e0dbee-47f5-46ed-89a0-01782345498f
keywords:
- Getfloatarray-Methode Direct3D 11
- Getfloatarray-Methode Direct3D 11, ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable Interface Direct3D 11, getfloatarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloatArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc760b7b7b57172becee0b9df9765be4d097f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982517"
---
# <a name="id3dx11effectscalarvariablegetfloatarray-method"></a><span data-ttu-id="aa852-106">ID3DX11EffectScalarVariable:: getfloatarray-Methode</span><span class="sxs-lookup"><span data-stu-id="aa852-106">ID3DX11EffectScalarVariable::GetFloatArray method</span></span>

<span data-ttu-id="aa852-107">Ein Array von Gleit Komma Variablen erhalten.</span><span class="sxs-lookup"><span data-stu-id="aa852-107">Get an array of floating-point variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa852-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa852-108">Syntax</span></span>


```C++
HRESULT GetFloatArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="aa852-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa852-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa852-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="aa852-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="aa852-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="aa852-111">Type: **float\***</span></span>

<span data-ttu-id="aa852-112">Ein Zeiger auf den Anfang der festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="aa852-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="aa852-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="aa852-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="aa852-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aa852-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="aa852-115">Muss auf 0 (null) festgelegt werden. Dies ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="aa852-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="aa852-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="aa852-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="aa852-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aa852-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="aa852-118">Die Anzahl der festzulegenden Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="aa852-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa852-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa852-119">Return value</span></span>

<span data-ttu-id="aa852-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aa852-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aa852-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="aa852-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa852-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa852-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aa852-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="aa852-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="aa852-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aa852-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="aa852-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="aa852-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aa852-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aa852-126">Requirements</span></span>



| <span data-ttu-id="aa852-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa852-127">Requirement</span></span> | <span data-ttu-id="aa852-128">Wert</span><span class="sxs-lookup"><span data-stu-id="aa852-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa852-129">Header</span><span class="sxs-lookup"><span data-stu-id="aa852-129">Header</span></span><br/>  | <dl> <span data-ttu-id="aa852-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa852-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="aa852-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa852-131">Library</span></span><br/> | <dl> <span data-ttu-id="aa852-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="aa852-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa852-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aa852-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa852-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="aa852-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

