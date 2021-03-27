---
title: ID3DX11EffectMatrixVariable getmatrixarray-Methode (D3dx11effect. h)
description: Ein Array von Matrizen erhalten.
ms.assetid: a7598687-a11c-41ad-9fb6-2c16d12f5edc
keywords:
- Getmatrixarray-Methode Direct3D 11
- Getmatrixarray-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11, getmatrixarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a339bf6918868473966b6d79bcbe6b6aa3eaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961666"
---
# <a name="id3dx11effectmatrixvariablegetmatrixarray-method"></a><span data-ttu-id="592a5-106">ID3DX11EffectMatrixVariable:: getmatrixarray-Methode</span><span class="sxs-lookup"><span data-stu-id="592a5-106">ID3DX11EffectMatrixVariable::GetMatrixArray method</span></span>

<span data-ttu-id="592a5-107">Ein Array von Matrizen erhalten.</span><span class="sxs-lookup"><span data-stu-id="592a5-107">Get an array of matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="592a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="592a5-108">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="592a5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="592a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="592a5-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="592a5-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="592a5-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="592a5-111">Type: **float\***</span></span>

<span data-ttu-id="592a5-112">Ein Zeiger auf das erste Element der ersten Matrix in einem Array von Matrizen.</span><span class="sxs-lookup"><span data-stu-id="592a5-112">A pointer to the first element of the first matrix in an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="592a5-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="592a5-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="592a5-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="592a5-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="592a5-115">Der Offset (in Anzahl von Matrizen) zwischen dem Anfang des Arrays und der ersten zurückgegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="592a5-115">The offset (in number of matrices) between the start of the array and the first matrix returned.</span></span>

</dd> <dt>

<span data-ttu-id="592a5-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="592a5-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="592a5-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="592a5-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="592a5-118">Die Anzahl von Matrizen im zurückgegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="592a5-118">The number of matrices in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="592a5-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="592a5-119">Return value</span></span>

<span data-ttu-id="592a5-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="592a5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="592a5-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="592a5-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="592a5-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="592a5-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="592a5-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="592a5-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="592a5-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="592a5-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="592a5-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="592a5-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="592a5-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="592a5-126">Requirements</span></span>



| <span data-ttu-id="592a5-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="592a5-127">Requirement</span></span> | <span data-ttu-id="592a5-128">Wert</span><span class="sxs-lookup"><span data-stu-id="592a5-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="592a5-129">Header</span><span class="sxs-lookup"><span data-stu-id="592a5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="592a5-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="592a5-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="592a5-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="592a5-131">Library</span></span><br/> | <dl> <span data-ttu-id="592a5-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="592a5-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="592a5-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="592a5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592a5-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="592a5-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

