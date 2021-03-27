---
title: ID3DX11EffectMatrixVariable setmatrixtransposearray-Methode (D3dx11effect. h)
description: Ein Array von Gleit Komma Matrizen wird aus-und festgelegt.
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- Setmatrixtransposearray-Methode Direct3D 11
- Setmatrixtransposearray-Methode Direct3D 11, ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11, setmatrixtransposearray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961714"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a><span data-ttu-id="6f204-106">ID3DX11EffectMatrixVariable:: setmatrixtransposearray-Methode</span><span class="sxs-lookup"><span data-stu-id="6f204-106">ID3DX11EffectMatrixVariable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="6f204-107">Ein Array von Gleit Komma Matrizen wird aus-und festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6f204-107">Transpose and set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f204-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f204-108">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="6f204-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f204-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f204-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="6f204-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="6f204-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="6f204-111">Type: **float\***</span></span>

<span data-ttu-id="6f204-112">Ein Zeiger auf ein Array von Matrizen.</span><span class="sxs-lookup"><span data-stu-id="6f204-112">A pointer to an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="6f204-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="6f204-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="6f204-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6f204-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6f204-115">Der Offset (in Anzahl von Matrizen) zwischen dem Anfang des Arrays und der ersten festzulegenden Matrix.</span><span class="sxs-lookup"><span data-stu-id="6f204-115">The offset (in number of matrices) between the start of the array and the first matrix to set.</span></span>

</dd> <dt>

<span data-ttu-id="6f204-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="6f204-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="6f204-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6f204-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6f204-118">Die Anzahl der Matrizen im Array, die festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f204-118">The number of matrices in the array to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f204-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f204-119">Return value</span></span>

<span data-ttu-id="6f204-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f204-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f204-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="6f204-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f204-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f204-122">Remarks</span></span>

<span data-ttu-id="6f204-123">Beim Durchführen einer Matrix wird die Reihenfolge der Daten in der Reihenfolge der Zeilen Spalten in der Reihenfolge der Spalten Zeilen (oder umgekehrt) neu angeordnet.</span><span class="sxs-lookup"><span data-stu-id="6f204-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="6f204-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="6f204-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6f204-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6f204-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6f204-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6f204-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f204-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6f204-127">Requirements</span></span>



| <span data-ttu-id="6f204-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f204-128">Requirement</span></span> | <span data-ttu-id="6f204-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6f204-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f204-130">Header</span><span class="sxs-lookup"><span data-stu-id="6f204-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6f204-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f204-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6f204-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f204-132">Library</span></span><br/> | <dl> <span data-ttu-id="6f204-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="6f204-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f204-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6f204-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f204-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="6f204-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

