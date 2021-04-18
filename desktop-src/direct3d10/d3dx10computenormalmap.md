---
description: Konvertiert eine Höhen Zuordnung in eine normale Karte. Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: D3DX10ComputeNormalMap-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1d7318e6d00d921ba0d573eb6fb696eed6c6a58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365319"
---
# <a name="d3dx10computenormalmap-function"></a><span data-ttu-id="112a5-104">D3DX10ComputeNormalMap-Funktion</span><span class="sxs-lookup"><span data-stu-id="112a5-104">D3DX10ComputeNormalMap function</span></span>

<span data-ttu-id="112a5-105">Konvertiert eine Höhen Zuordnung in eine normale Karte.</span><span class="sxs-lookup"><span data-stu-id="112a5-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="112a5-106">Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="112a5-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="112a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="112a5-107">Syntax</span></span>


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="112a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="112a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="112a5-109">*psrctexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="112a5-109">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="112a5-110">Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="112a5-110">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="112a5-111">Ein Zeiger auf eine ID3D10Texture2D-Schnittstelle, die die Textur der Quell Höhe darstellt.</span><span class="sxs-lookup"><span data-stu-id="112a5-111">Pointer to an ID3D10Texture2D interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="112a5-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="112a5-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="112a5-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="112a5-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="112a5-114">Ein oder mehrere D3DX \_ normalmap-Flags, die die Generierung normaler Karten steuern.</span><span class="sxs-lookup"><span data-stu-id="112a5-114">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="112a5-115">*Channel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="112a5-115">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="112a5-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="112a5-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="112a5-117">Ein D3DX- \_ kanalflag, das die Quelle der Höheninformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="112a5-117">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="112a5-118">*Amplitude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="112a5-118">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="112a5-119">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="112a5-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="112a5-120">Konstanter Wert Multiplikator, der die Werte in der normalen Zuordnung vergrößert (oder verringert).</span><span class="sxs-lookup"><span data-stu-id="112a5-120">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="112a5-121">Höhere Werte machen in der Regel zu Leistungseinbußen, niedrigere Werte werden in der Regel weniger sichtbar.</span><span class="sxs-lookup"><span data-stu-id="112a5-121">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="112a5-122">*pdesttexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="112a5-122">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="112a5-123">Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="112a5-123">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="112a5-124">Zeiger auf eine ID3D10Texture2D-Schnittstelle, die die Ziel Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="112a5-124">Pointer to an ID3D10Texture2D interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="112a5-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="112a5-125">Return value</span></span>

<span data-ttu-id="112a5-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="112a5-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="112a5-127">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="112a5-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="112a5-128">Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="112a5-128">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="112a5-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="112a5-129">Remarks</span></span>

<span data-ttu-id="112a5-130">Diese Methode berechnet die normale, indem der zentrale Unterschied mit einer Kernel Größe von 3X3 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="112a5-130">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="112a5-131">RGB-Kanäle im Ziel enthalten unausgewogene (x, y, z) Komponenten der normalen.</span><span class="sxs-lookup"><span data-stu-id="112a5-131">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="112a5-132">Der zentrale Differenzierungs Nenner ist hart codiert in 2,0.</span><span class="sxs-lookup"><span data-stu-id="112a5-132">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="112a5-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="112a5-133">Requirements</span></span>



| <span data-ttu-id="112a5-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="112a5-134">Requirement</span></span> | <span data-ttu-id="112a5-135">Wert</span><span class="sxs-lookup"><span data-stu-id="112a5-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="112a5-136">Header</span><span class="sxs-lookup"><span data-stu-id="112a5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="112a5-137"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="112a5-137"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="112a5-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="112a5-138">Library</span></span><br/> | <dl> <span data-ttu-id="112a5-139"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="112a5-139"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="112a5-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="112a5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112a5-141">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="112a5-141">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
