---
title: ID3DX11EffectMatrixVariable setMatrix-Methode (D3dx11effect. h)
description: Legen Sie eine Gleit Komma Matrix fest.
ms.assetid: 91c69bc0-c8c6-4232-8c70-801ac8ddbcda
keywords:
- SetMatrix-Methode Direct3D 11
- SetMatrix-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11, setMatrix-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af7b64e7391461efc47b6f65ca676b870174347
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982372"
---
# <a name="id3dx11effectmatrixvariablesetmatrix-method"></a><span data-ttu-id="412c9-106">ID3DX11EffectMatrixVariable:: setMatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="412c9-106">ID3DX11EffectMatrixVariable::SetMatrix method</span></span>

<span data-ttu-id="412c9-107">Legen Sie eine Gleit Komma Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="412c9-107">Set a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="412c9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="412c9-108">Syntax</span></span>


```C++
HRESULT SetMatrix(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="412c9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="412c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="412c9-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="412c9-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="412c9-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="412c9-111">Type: **float\***</span></span>

<span data-ttu-id="412c9-112">Ein Zeiger auf das erste Element in der Matrix.</span><span class="sxs-lookup"><span data-stu-id="412c9-112">A pointer to the first element in the matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="412c9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="412c9-113">Return value</span></span>

<span data-ttu-id="412c9-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="412c9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="412c9-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="412c9-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="412c9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="412c9-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="412c9-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="412c9-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="412c9-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="412c9-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="412c9-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="412c9-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="412c9-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="412c9-120">Requirements</span></span>



| <span data-ttu-id="412c9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="412c9-121">Requirement</span></span> | <span data-ttu-id="412c9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="412c9-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="412c9-123">Header</span><span class="sxs-lookup"><span data-stu-id="412c9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="412c9-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="412c9-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="412c9-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="412c9-125">Library</span></span><br/> | <dl> <span data-ttu-id="412c9-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="412c9-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="412c9-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="412c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="412c9-128">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="412c9-128">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





