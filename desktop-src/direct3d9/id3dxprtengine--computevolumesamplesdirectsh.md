---
description: Berechnet eine Projektion entfernter Beleuchtung in eine kugelförmige (SH) Basis Vektoren, die die Ereignis Strahlen an angegebenen Orten darstellen.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'ID3DXPRTEngine:: computevolumesamplesdirectsh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351984"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a><span data-ttu-id="75b92-103">ID3DXPRTEngine:: computevolumesamplesdirectsh-Methode</span><span class="sxs-lookup"><span data-stu-id="75b92-103">ID3DXPRTEngine::ComputeVolumeSamplesDirectSH method</span></span>

<span data-ttu-id="75b92-104">Berechnet eine Projektion entfernter Beleuchtung in eine kugelförmige (SH) Basis Vektoren, die die Ereignis Strahlen an angegebenen Orten darstellen.</span><span class="sxs-lookup"><span data-stu-id="75b92-104">Computes a projection of distant lighting into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75b92-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="75b92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75b92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b92-107">*OrderIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b92-107">*OrderIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b92-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75b92-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75b92-109">Die Reihenfolge der SH-Darstellung der entfernten Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="75b92-109">Order of the SH representation of distant lighting.</span></span> <span data-ttu-id="75b92-110">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="75b92-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="75b92-111">Der Bewertungs Grad ist OrderIn-1.</span><span class="sxs-lookup"><span data-stu-id="75b92-111">The degree of the evaluation is OrderIn - 1.</span></span>

</dd> <dt>

<span data-ttu-id="75b92-112">*Order out* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b92-112">*OrderOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b92-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75b92-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75b92-114">Die Reihenfolge der SH-Darstellung der lokalen Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="75b92-114">Order of the SH representation of local lighting.</span></span> <span data-ttu-id="75b92-115">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="75b92-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="75b92-116">Der Bewertungs Grad ist orderout-1.</span><span class="sxs-lookup"><span data-stu-id="75b92-116">The degree of the evaluation is OrderOut - 1.</span></span>

</dd> <dt>

<span data-ttu-id="75b92-117">*NumVolSamples.xml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b92-117">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b92-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75b92-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75b92-119">Anzahl der Beispiel Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="75b92-119">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="75b92-120">*psamplelocs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b92-120">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b92-121">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="75b92-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="75b92-122">Die Position für jede Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="75b92-122">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="75b92-123">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="75b92-123">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75b92-124">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="75b92-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="75b92-125">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das die entfernte Beleuchtung in SH-Basis Vektoren projiziert.</span><span class="sxs-lookup"><span data-stu-id="75b92-125">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the distant lighting into SH basis vectors.</span></span> <span data-ttu-id="75b92-126">Dieser Puffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="75b92-126">This buffer must have the proper number of color channels allocated for the simulation.</span></span> <span data-ttu-id="75b92-127">Diese Methode generiert \* Orser ² orderout "² Skars pro Kanal an jedem Beispiel Speicherort.</span><span class="sxs-lookup"><span data-stu-id="75b92-127">This method generates OrderIn² \* OrderOut"² scalars per channel at each sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b92-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75b92-128">Return value</span></span>

<span data-ttu-id="75b92-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75b92-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75b92-130">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75b92-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="75b92-131">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="75b92-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b92-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75b92-132">Remarks</span></span>

<span data-ttu-id="75b92-133">Mit dieser Methode wird berechnet, wie Light aus einer entfernten Quelle an jedem von psamplelocs angegebenen Raum erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="75b92-133">This method computes how light from a distant source arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="75b92-134">Die SH-Koeffizienten stellen die Zuordnung der Quell Strahlung an jedem psamplelocs-Punkt zur Übertragung von Ereignis Strahlen dar.</span><span class="sxs-lookup"><span data-stu-id="75b92-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

<span data-ttu-id="75b92-135">Um diese Methode erfolgreich zu verwenden, müssen Sie die Stichprobenentnahme für eine Kugel mit usesphere = **true** und usecosinus = **false** in [**ID3DXPRTEngine:: setsamplinginfo**](id3dxprtengine--setsamplinginfo.md); festlegen. Andernfalls gibt diese Methode einen Fehler mit D3DERR \_ invalidcallzurück.</span><span class="sxs-lookup"><span data-stu-id="75b92-135">To use this method successfully, you must set sampling over a sphere with UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); otherwise, this method will return an error with D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b92-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75b92-136">Requirements</span></span>



| <span data-ttu-id="75b92-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75b92-137">Requirement</span></span> | <span data-ttu-id="75b92-138">Wert</span><span class="sxs-lookup"><span data-stu-id="75b92-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75b92-139">Header</span><span class="sxs-lookup"><span data-stu-id="75b92-139">Header</span></span><br/>  | <dl> <span data-ttu-id="75b92-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b92-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="75b92-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75b92-141">Library</span></span><br/> | <dl> <span data-ttu-id="75b92-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75b92-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75b92-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75b92-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b92-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="75b92-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="75b92-145">**ID3DXPRTEngine:: computevolumesamples**</span><span class="sxs-lookup"><span data-stu-id="75b92-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span></span>](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
