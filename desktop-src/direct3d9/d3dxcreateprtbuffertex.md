---
description: Erstellt einen PRT-Puffer (preberechneten Radiance Transfer), der von einem Simulator komprimiert oder ausgefüllt werden kann. Diese Funktion sollte zum Erstellen von pro Pixel Puffer verwendet werden.
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: D3DXCreatePRTBufferTex-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3e88073f85d281e164c002ba5180493f6217e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365314"
---
# <a name="d3dxcreateprtbuffertex-function"></a><span data-ttu-id="6b052-104">D3DXCreatePRTBufferTex-Funktion</span><span class="sxs-lookup"><span data-stu-id="6b052-104">D3DXCreatePRTBufferTex function</span></span>

<span data-ttu-id="6b052-105">Erstellt einen PRT-Puffer (preberechneten Radiance Transfer), der von einem Simulator komprimiert oder ausgefüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b052-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="6b052-106">Diese Funktion sollte zum Erstellen von pro Pixel Puffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b052-106">This function should be used to create per-pixel buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b052-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b052-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="6b052-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b052-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b052-109">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b052-109">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b052-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b052-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b052-111">Breite der Textur in Pixel.</span><span class="sxs-lookup"><span data-stu-id="6b052-111">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6b052-112">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b052-112">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b052-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b052-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b052-114">Höhe der Textur in Pixel.</span><span class="sxs-lookup"><span data-stu-id="6b052-114">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6b052-115">*Numkoeffs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b052-115">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b052-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b052-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b052-117">Anzahl der Koeffizienten pro Stichproben Speicherort.</span><span class="sxs-lookup"><span data-stu-id="6b052-117">Number of coefficients per sample location.</span></span> <span data-ttu-id="6b052-118">Bei Verwendung von "sphärischen harmonisch (SH) PRT" sollte die Anzahl der Koeffizienten "Order ²" lauten, wobei "Order" die Reihenfolge der SH-Auswertung ist.</span><span class="sxs-lookup"><span data-stu-id="6b052-118">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="6b052-119">Die Reihenfolge muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="6b052-119">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="6b052-120">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="6b052-120">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="6b052-121">*Numchannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b052-121">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b052-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b052-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b052-123">Anzahl von Farbkanälen, die im Mesh festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b052-123">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="6b052-124">Legen Sie auf 1 fest, um graue Materialien (R = G = B) oder 3 anzugeben, um Farb Blutungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6b052-124">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="6b052-125">*ppbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6b052-125">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b052-126">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b052-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="6b052-127">Adresse eines Zeigers auf das erstellte [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b052-127">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b052-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b052-128">Return value</span></span>

<span data-ttu-id="6b052-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b052-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b052-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6b052-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6b052-131">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="6b052-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b052-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b052-132">Remarks</span></span>

<span data-ttu-id="6b052-133">Beim Erstellen des Puffers werden alle Werte mit 0 (null) initialisiert.</span><span class="sxs-lookup"><span data-stu-id="6b052-133">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b052-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b052-134">Requirements</span></span>



| <span data-ttu-id="6b052-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b052-135">Requirement</span></span> | <span data-ttu-id="6b052-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6b052-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b052-137">Header</span><span class="sxs-lookup"><span data-stu-id="6b052-137">Header</span></span><br/>  | <dl> <span data-ttu-id="6b052-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b052-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6b052-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b052-139">Library</span></span><br/> | <dl> <span data-ttu-id="6b052-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b052-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b052-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b052-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b052-142">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="6b052-142">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="6b052-143">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="6b052-143">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
