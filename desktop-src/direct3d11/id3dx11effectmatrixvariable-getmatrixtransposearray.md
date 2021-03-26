---
title: ID3DX11EffectMatrixVariable getmatrixtransposearray-Methode (D3dx11effect. h)
description: Austauschen und erhalten eines Arrays von Gleit Komma Matrizen.
ms.assetid: cfcdbda0-b321-4e94-8d09-bb9d7ddfb4a5
keywords:
- Getmatrixtransposearray-Methode Direct3D 11
- Getmatrixtransposearray-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11, getmatrixtransposearray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d0a43e69ccf88c15d8296c024535dec42b3f31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982263"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtransposearray-method"></a><span data-ttu-id="e8e44-106">ID3DX11EffectMatrixVariable:: getmatrixtransposearray-Methode</span><span class="sxs-lookup"><span data-stu-id="e8e44-106">ID3DX11EffectMatrixVariable::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="e8e44-107">Austauschen und erhalten eines Arrays von Gleit Komma Matrizen.</span><span class="sxs-lookup"><span data-stu-id="e8e44-107">Transpose and get an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e44-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8e44-108">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="e8e44-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8e44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e44-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="e8e44-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e44-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="e8e44-111">Type: **float\***</span></span>

<span data-ttu-id="e8e44-112">Ein Zeiger auf das erste Element eines Arrays von überstellten Matrizen.</span><span class="sxs-lookup"><span data-stu-id="e8e44-112">A pointer to the first element of an array of tranposed matrices.</span></span>

</dd> <dt>

<span data-ttu-id="e8e44-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="e8e44-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e44-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8e44-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8e44-115">Der Offset (in Anzahl von Matrizen) zwischen dem Anfang des Arrays und der ersten Matrix, die abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8e44-115">The offset (in number of matrices) between the start of the array and the first matrix to get.</span></span>

</dd> <dt>

<span data-ttu-id="e8e44-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="e8e44-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e44-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8e44-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8e44-118">Die Anzahl der zu Get-Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="e8e44-118">The number of matrices in the array to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8e44-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8e44-119">Return value</span></span>

<span data-ttu-id="e8e44-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8e44-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8e44-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="e8e44-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8e44-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8e44-122">Remarks</span></span>

<span data-ttu-id="e8e44-123">Beim Durchführen einer Matrix wird die Reihenfolge der Daten in der Reihenfolge der Zeilen Spalten in der Reihenfolge der Spalten Zeilen (oder umgekehrt) neu angeordnet.</span><span class="sxs-lookup"><span data-stu-id="e8e44-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="e8e44-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="e8e44-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e8e44-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e8e44-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e8e44-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e8e44-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8e44-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e8e44-127">Requirements</span></span>



| <span data-ttu-id="e8e44-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8e44-128">Requirement</span></span> | <span data-ttu-id="e8e44-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e8e44-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e44-130">Header</span><span class="sxs-lookup"><span data-stu-id="e8e44-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e8e44-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e44-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e8e44-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8e44-132">Library</span></span><br/> | <dl> <span data-ttu-id="e8e44-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="e8e44-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e44-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8e44-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e44-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="e8e44-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

