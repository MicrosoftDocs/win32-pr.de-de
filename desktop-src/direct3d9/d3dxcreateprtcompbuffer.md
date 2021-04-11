---
description: Erstellt einen komprimierten PRT-Puffer (preberechneten Radiance Transfer) aus einem unkomprimierten ID3DXPRTBuffer-Objekt. Diese Funktion sollte mit pro-Vertex-oder volumepuffer verwendet werden.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: D3DXCreatePRTCompBuffer-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354917"
---
# <a name="d3dxcreateprtcompbuffer-function"></a><span data-ttu-id="4a3a4-104">D3DXCreatePRTCompBuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a3a4-104">D3DXCreatePRTCompBuffer function</span></span>

<span data-ttu-id="4a3a4-105">Erstellt einen komprimierten PRT-Puffer (preberechneten Radiance Transfer) aus einem unkomprimierten [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-105">Creates a compressed precomputed radiance transfer (PRT) buffer from an uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="4a3a4-106">Diese Funktion sollte mit pro-Vertex-oder volumepuffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-106">This function should be used with per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a3a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a3a4-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="4a3a4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a3a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a3a4-109">*Qualität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a3a4-109">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a3a4-110">Typ: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span><span class="sxs-lookup"><span data-stu-id="4a3a4-110">Type: **[**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span></span>

<span data-ttu-id="4a3a4-111">Qualität der kugelförmigen Komprimierung (SH).</span><span class="sxs-lookup"><span data-stu-id="4a3a4-111">Quality of spherical harmonic (SH) compression.</span></span> <span data-ttu-id="4a3a4-112">Siehe [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span><span class="sxs-lookup"><span data-stu-id="4a3a4-112">See [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a3a4-113">*Numclusters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a3a4-113">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a3a4-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a3a4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a3a4-115">Anzahl der für die Komprimierung zu verwendenden Cluster.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-115">Number of clusters to use for compression.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a4-116">*Numpca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a3a4-116">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a3a4-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a3a4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a3a4-118">Anzahl der PCA-Basis-Vektoren (Principal Component Analysis), die in jedem Cluster verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-118">Number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a4-119">*Platine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a3a4-119">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a3a4-120">Typ: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="4a3a4-120">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="4a3a4-121">Optionaler Zeiger auf die [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) -Rückruffunktion, die verwendet wird, um den Prozentsatz der abgeschlossenen PRT-Komprimierungs Berechnungen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-121">Optional pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that is used to compute the percentage of PRT compression computations completed.</span></span> <span data-ttu-id="4a3a4-122">Die Rückruffunktion muss implementiert werden, damit S OK zurückgegeben wird \_ , um die Komprimierungs Routine weiterhin ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-122">The callback function must be implemented to return S\_OK to keep running the compression routine.</span></span> <span data-ttu-id="4a3a4-123">Bei jedem anderen Wert wird die Komprimierung angehalten.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-123">Any other value will halt compression.</span></span> <span data-ttu-id="4a3a4-124">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a4-125">*lpusercontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a3a4-125">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a3a4-126">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a3a4-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a3a4-127">Optionaler Zeiger auf einen benutzerdefinierten Wert, der an die [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) -Rückruffunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-127">Optional pointer to a user-defined value passed to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function.</span></span> <span data-ttu-id="4a3a4-128">Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-128">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span> <span data-ttu-id="4a3a4-129">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-129">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a4-130">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a3a4-130">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a3a4-131">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="4a3a4-131">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="4a3a4-132">Adresse eines Zeigers auf das nicht komprimierte [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-132">Address of a pointer to the uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a4-133">*ppbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4a3a4-133">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a3a4-134">Typ: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a3a4-134">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="4a3a4-135">Adresse eines Zeigers auf das Output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-135">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a3a4-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a3a4-136">Return value</span></span>

<span data-ttu-id="4a3a4-137">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4a3a4-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4a3a4-138">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4a3a4-139">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="4a3a4-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a3a4-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a3a4-140">Requirements</span></span>



| <span data-ttu-id="4a3a4-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a3a4-141">Requirement</span></span> | <span data-ttu-id="4a3a4-142">Wert</span><span class="sxs-lookup"><span data-stu-id="4a3a4-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a3a4-143">Header</span><span class="sxs-lookup"><span data-stu-id="4a3a4-143">Header</span></span><br/>  | <dl> <span data-ttu-id="4a3a4-144"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a3a4-144"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4a3a4-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a3a4-145">Library</span></span><br/> | <dl> <span data-ttu-id="4a3a4-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a3a4-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a3a4-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a3a4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a3a4-148">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4a3a4-148">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="4a3a4-149">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="4a3a4-149">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="4a3a4-150">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="4a3a4-150">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
