---
title: ID3DX11EffectMatrixVariable getMatrix-Methode (D3dx11effect. h)
description: Eine Matrix erhalten.
ms.assetid: 1d0b20f2-6e43-414d-a161-65ce13bef1e0
keywords:
- GetMatrix-Methode Direct3D 11
- GetMatrix-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11, getMatrix-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14c2f196c4072d7f81a75045fe4703bf51ea338
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050887"
---
# <a name="id3dx11effectmatrixvariablegetmatrix-method"></a><span data-ttu-id="e22ca-106">ID3DX11EffectMatrixVariable:: getMatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="e22ca-106">ID3DX11EffectMatrixVariable::GetMatrix method</span></span>

<span data-ttu-id="e22ca-107">Eine Matrix erhalten.</span><span class="sxs-lookup"><span data-stu-id="e22ca-107">Get a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e22ca-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e22ca-108">Syntax</span></span>


```C++
HRESULT GetMatrix(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="e22ca-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e22ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e22ca-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="e22ca-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="e22ca-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="e22ca-111">Type: **float\***</span></span>

<span data-ttu-id="e22ca-112">Ein Zeiger auf das erste Element in einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="e22ca-112">A pointer to the first element in a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e22ca-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e22ca-113">Return value</span></span>

<span data-ttu-id="e22ca-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e22ca-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e22ca-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="e22ca-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e22ca-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e22ca-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e22ca-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="e22ca-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e22ca-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e22ca-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e22ca-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e22ca-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e22ca-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e22ca-120">Requirements</span></span>



| <span data-ttu-id="e22ca-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e22ca-121">Requirement</span></span> | <span data-ttu-id="e22ca-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e22ca-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e22ca-123">Header</span><span class="sxs-lookup"><span data-stu-id="e22ca-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e22ca-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e22ca-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e22ca-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e22ca-125">Library</span></span><br/> | <dl> <span data-ttu-id="e22ca-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="e22ca-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e22ca-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e22ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e22ca-128">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="e22ca-128">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





