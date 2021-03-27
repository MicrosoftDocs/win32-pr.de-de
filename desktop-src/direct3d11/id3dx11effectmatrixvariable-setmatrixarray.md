---
title: ID3DX11EffectMatrixVariable setmatrixarray-Methode (D3dx11effect. h)
description: Legen Sie ein Array von Gleit Komma Matrizen fest.
ms.assetid: c90d621c-7500-49c3-ab40-2d0630fc4bec
keywords:
- Setmatrixarray-Methode Direct3D 11
- Setmatrixarray-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11, setmatrixarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffe0f6a81e0086a9afd6da9e464f09ae577dab2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982371"
---
# <a name="id3dx11effectmatrixvariablesetmatrixarray-method"></a><span data-ttu-id="35119-106">ID3DX11EffectMatrixVariable:: setmatrixarray-Methode</span><span class="sxs-lookup"><span data-stu-id="35119-106">ID3DX11EffectMatrixVariable::SetMatrixArray method</span></span>

<span data-ttu-id="35119-107">Legen Sie ein Array von Gleit Komma Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="35119-107">Set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="35119-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="35119-108">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="35119-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="35119-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35119-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="35119-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="35119-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="35119-111">Type: **float\***</span></span>

<span data-ttu-id="35119-112">Ein Zeiger auf die erste Matrix.</span><span class="sxs-lookup"><span data-stu-id="35119-112">A pointer to the first matrix.</span></span>

</dd> <dt>

<span data-ttu-id="35119-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="35119-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="35119-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35119-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="35119-115">Die Anzahl der Matrix Elemente, die vom Anfang des Arrays übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="35119-115">The number of matrix elements to skip from the start of the array.</span></span>

</dd> <dt>

<span data-ttu-id="35119-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="35119-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="35119-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="35119-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="35119-118">Die Anzahl der festzulegenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="35119-118">The number of elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35119-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35119-119">Return value</span></span>

<span data-ttu-id="35119-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35119-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35119-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="35119-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="35119-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35119-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="35119-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="35119-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="35119-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="35119-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="35119-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="35119-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="35119-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="35119-126">Requirements</span></span>



| <span data-ttu-id="35119-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35119-127">Requirement</span></span> | <span data-ttu-id="35119-128">Wert</span><span class="sxs-lookup"><span data-stu-id="35119-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35119-129">Header</span><span class="sxs-lookup"><span data-stu-id="35119-129">Header</span></span><br/>  | <dl> <span data-ttu-id="35119-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="35119-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="35119-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35119-131">Library</span></span><br/> | <dl> <span data-ttu-id="35119-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="35119-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35119-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="35119-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35119-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="35119-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

