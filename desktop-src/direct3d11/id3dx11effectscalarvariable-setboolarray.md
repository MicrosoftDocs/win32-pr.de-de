---
title: ID3DX11EffectScalarVariable setboolarray-Methode (D3dx11effect. h)
description: Legen Sie ein Array von booleschen Variablen fest.
ms.assetid: 861634a2-547d-497b-b575-bbe6151ade25
keywords:
- Setboolarray-Methode Direct3D 11
- Setboolarray-Methode Direct3D 11, ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11, setboolarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBoolArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e982e2475fe20a2aa12bef9c52095eed228bf44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354277"
---
# <a name="id3dx11effectscalarvariablesetboolarray-method"></a><span data-ttu-id="30e8d-106">ID3DX11EffectScalarVariable:: setboolarray-Methode</span><span class="sxs-lookup"><span data-stu-id="30e8d-106">ID3DX11EffectScalarVariable::SetBoolArray method</span></span>

<span data-ttu-id="30e8d-107">Legen Sie ein Array von booleschen Variablen fest.</span><span class="sxs-lookup"><span data-stu-id="30e8d-107">Set an array of boolean variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="30e8d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30e8d-108">Syntax</span></span>


```C++
HRESULT SetBoolArray(
   BOOL *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="30e8d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30e8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e8d-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="30e8d-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="30e8d-111">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="30e8d-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="30e8d-112">Ein Zeiger auf den Anfang der festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="30e8d-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="30e8d-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="30e8d-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="30e8d-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30e8d-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="30e8d-115">Muss auf 0 (null) festgelegt werden. Dies ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="30e8d-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="30e8d-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="30e8d-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="30e8d-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30e8d-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="30e8d-118">Die Anzahl der festzulegenden Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="30e8d-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e8d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30e8d-119">Return value</span></span>

<span data-ttu-id="30e8d-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30e8d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30e8d-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="30e8d-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30e8d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30e8d-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30e8d-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="30e8d-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="30e8d-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="30e8d-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="30e8d-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="30e8d-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30e8d-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="30e8d-126">Requirements</span></span>



| <span data-ttu-id="30e8d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30e8d-127">Requirement</span></span> | <span data-ttu-id="30e8d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="30e8d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30e8d-129">Header</span><span class="sxs-lookup"><span data-stu-id="30e8d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="30e8d-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="30e8d-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="30e8d-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30e8d-131">Library</span></span><br/> | <dl> <span data-ttu-id="30e8d-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="30e8d-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30e8d-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="30e8d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e8d-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="30e8d-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

