---
title: ID3DX11EffectMatrixVariable setmatrixtransform-Methode (D3dx11effect. h)
description: Sie sollten eine Gleit Komma Matrix austauschen und festlegen.
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- Setmatrixtransform-Methode Direct3D 11
- Setmatrixtransform-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11, setmatrixtransform-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daf77b6e2e9578dcbc6c9cfe80f57b149097c32
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982258"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a><span data-ttu-id="b50a0-106">ID3DX11EffectMatrixVariable:: setmatrixtransform-Methode</span><span class="sxs-lookup"><span data-stu-id="b50a0-106">ID3DX11EffectMatrixVariable::SetMatrixTranspose method</span></span>

<span data-ttu-id="b50a0-107">Sie sollten eine Gleit Komma Matrix austauschen und festlegen.</span><span class="sxs-lookup"><span data-stu-id="b50a0-107">Transpose and set a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b50a0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b50a0-108">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="b50a0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b50a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b50a0-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="b50a0-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="b50a0-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="b50a0-111">Type: **float\***</span></span>

<span data-ttu-id="b50a0-112">Ein Zeiger auf das erste Element einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="b50a0-112">A pointer to the first element of a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b50a0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b50a0-113">Return value</span></span>

<span data-ttu-id="b50a0-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b50a0-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b50a0-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="b50a0-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b50a0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b50a0-116">Remarks</span></span>

<span data-ttu-id="b50a0-117">Beim Durchführen einer Matrix wird die Reihenfolge der Daten in der Reihenfolge der Zeilen Spalten in der Reihenfolge der Spalten Zeilen (oder umgekehrt) neu angeordnet.</span><span class="sxs-lookup"><span data-stu-id="b50a0-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="b50a0-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="b50a0-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b50a0-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b50a0-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b50a0-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b50a0-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b50a0-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b50a0-121">Requirements</span></span>



| <span data-ttu-id="b50a0-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b50a0-122">Requirement</span></span> | <span data-ttu-id="b50a0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b50a0-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b50a0-124">Header</span><span class="sxs-lookup"><span data-stu-id="b50a0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b50a0-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b50a0-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b50a0-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b50a0-126">Library</span></span><br/> | <dl> <span data-ttu-id="b50a0-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="b50a0-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b50a0-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b50a0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b50a0-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="b50a0-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





