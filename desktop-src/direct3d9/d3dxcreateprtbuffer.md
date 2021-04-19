---
description: Erstellt einen PRT-Puffer (preberechneten Radiance Transfer), der von einem Simulator komprimiert oder ausgefüllt werden kann. Diese Funktion sollte verwendet werden, um Puffer-oder volumepuffer zu erstellen.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: D3DXCreatePRTBuffer-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350689"
---
# <a name="d3dxcreateprtbuffer-function"></a><span data-ttu-id="1b0e9-104">D3DXCreatePRTBuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b0e9-104">D3DXCreatePRTBuffer function</span></span>

<span data-ttu-id="1b0e9-105">Erstellt einen PRT-Puffer (preberechneten Radiance Transfer), der von einem Simulator komprimiert oder ausgefüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="1b0e9-106">Diese Funktion sollte verwendet werden, um Puffer-oder volumepuffer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-106">This function should be used to create per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b0e9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b0e9-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="1b0e9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b0e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b0e9-109">*NumSamples* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b0e9-109">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b0e9-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b0e9-111">Anzahl der abtasteten Scheitel Punkte (oder Texels).</span><span class="sxs-lookup"><span data-stu-id="1b0e9-111">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="1b0e9-112">*Numkoeffs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b0e9-112">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b0e9-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b0e9-114">Anzahl der Koeffizienten pro Stichproben Speicherort.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-114">Number of coefficients per sample location.</span></span> <span data-ttu-id="1b0e9-115">Bei Verwendung von "sphärischen harmonisch (SH) PRT" sollte die Anzahl der Koeffizienten "Order ²" lauten, wobei "Order" die Reihenfolge der SH-Auswertung ist.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-115">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="1b0e9-116">Die Reihenfolge muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-116">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1b0e9-117">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1b0e9-118">*Numchannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b0e9-118">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b0e9-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b0e9-120">Anzahl von Farbkanälen, die im Mesh festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-120">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="1b0e9-121">Legen Sie auf 1 fest, um graue Materialien (R = G = B) oder 3 anzugeben, um Farb Blutungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-121">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="1b0e9-122">*ppbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1b0e9-122">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b0e9-123">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b0e9-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="1b0e9-124">Adresse eines Zeigers auf das erstellte [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-124">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b0e9-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b0e9-125">Return value</span></span>

<span data-ttu-id="1b0e9-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1b0e9-127">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-127">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1b0e9-128">Wenn die Funktion fehlschlägt, kann der Rückgabewert eines der folgenden Werte sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-128">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b0e9-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b0e9-129">Remarks</span></span>

<span data-ttu-id="1b0e9-130">Beim Erstellen des Puffers werden alle Werte mit 0 (null) initialisiert.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-130">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b0e9-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b0e9-131">Requirements</span></span>



| <span data-ttu-id="1b0e9-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b0e9-132">Requirement</span></span> | <span data-ttu-id="1b0e9-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1b0e9-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b0e9-134">Header</span><span class="sxs-lookup"><span data-stu-id="1b0e9-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1b0e9-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b0e9-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1b0e9-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b0e9-136">Library</span></span><br/> | <dl> <span data-ttu-id="1b0e9-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b0e9-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1b0e9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b0e9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b0e9-139">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1b0e9-139">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="1b0e9-140">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-140">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
