---
title: ID3DX11EffectMatrixVariable getmatrixtransform-Methode (D3dx11effect. h)
description: Eine Gleit Komma Matrix austauschen und erhalten.
ms.assetid: a261128c-d1f9-4864-b562-5fe9a69c9969
keywords:
- Getmatrixtransform-Methode Direct3D 11
- Getmatrixtransform-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11, getmatrixtransform-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa5c8eb8e424041a05461636d1eaf7b65c7cd4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050886"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtranspose-method"></a><span data-ttu-id="67fdf-106">ID3DX11EffectMatrixVariable:: getmatrixtransform-Methode</span><span class="sxs-lookup"><span data-stu-id="67fdf-106">ID3DX11EffectMatrixVariable::GetMatrixTranspose method</span></span>

<span data-ttu-id="67fdf-107">Eine Gleit Komma Matrix austauschen und erhalten.</span><span class="sxs-lookup"><span data-stu-id="67fdf-107">Transpose and get a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="67fdf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="67fdf-108">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="67fdf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="67fdf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67fdf-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="67fdf-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="67fdf-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="67fdf-111">Type: **float\***</span></span>

<span data-ttu-id="67fdf-112">Ein Zeiger auf das erste Element einer übersetzten Matrix.</span><span class="sxs-lookup"><span data-stu-id="67fdf-112">A pointer to the first element of a transposed matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67fdf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67fdf-113">Return value</span></span>

<span data-ttu-id="67fdf-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67fdf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67fdf-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="67fdf-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="67fdf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67fdf-116">Remarks</span></span>

<span data-ttu-id="67fdf-117">Beim Durchführen einer Matrix wird die Reihenfolge der Daten in der Reihenfolge der Zeilen Spalten in der Reihenfolge der Spalten Zeilen (oder umgekehrt) neu angeordnet.</span><span class="sxs-lookup"><span data-stu-id="67fdf-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="67fdf-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="67fdf-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="67fdf-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67fdf-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="67fdf-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="67fdf-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67fdf-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="67fdf-121">Requirements</span></span>



| <span data-ttu-id="67fdf-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67fdf-122">Requirement</span></span> | <span data-ttu-id="67fdf-123">Wert</span><span class="sxs-lookup"><span data-stu-id="67fdf-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67fdf-124">Header</span><span class="sxs-lookup"><span data-stu-id="67fdf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="67fdf-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="67fdf-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="67fdf-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67fdf-126">Library</span></span><br/> | <dl> <span data-ttu-id="67fdf-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="67fdf-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67fdf-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="67fdf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67fdf-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="67fdf-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





