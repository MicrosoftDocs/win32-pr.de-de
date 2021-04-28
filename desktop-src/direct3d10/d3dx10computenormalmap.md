---
description: 'D3DX10ComputeNormalMap-Funktion: Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jeder Normalen werden den (r,g,b) Kanälen der Ausgabetextur zugeordnet.'
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: D3DX10ComputeNormalMap-Funktion (D3DX10Tex.h)
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
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105318"
---
# <a name="d3dx10computenormalmap-function"></a><span data-ttu-id="b959f-104">D3DX10ComputeNormalMap-Funktion</span><span class="sxs-lookup"><span data-stu-id="b959f-104">D3DX10ComputeNormalMap function</span></span>

<span data-ttu-id="b959f-105">Konvertiert eine Höhenkarte in eine normale Karte.</span><span class="sxs-lookup"><span data-stu-id="b959f-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="b959f-106">Die (x,y,z)-Komponenten jeder Normalen werden den (r,g,b) Kanälen der Ausgabetextur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b959f-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b959f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b959f-107">Syntax</span></span>


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="b959f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b959f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b959f-109">*pSrcTexture* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b959f-109">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b959f-110">Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="b959f-110">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="b959f-111">Zeiger auf eine ID3D10Texture2D-Schnittstelle, die die Quelltextur der Höhenzuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b959f-111">Pointer to an ID3D10Texture2D interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="b959f-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b959f-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b959f-113">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b959f-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b959f-114">Mindestens ein D3DX \_ NORMALMAP-Flag, das die Generierung normaler Zuordnungen steuert.</span><span class="sxs-lookup"><span data-stu-id="b959f-114">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="b959f-115">*Kanal* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b959f-115">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b959f-116">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b959f-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b959f-117">Ein \_ D3DX-KANALflag, das die Quelle der Höheninformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="b959f-117">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="b959f-118">*Amplitude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b959f-118">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b959f-119">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b959f-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b959f-120">Konstanter Wertmultiplikator, der die Werte in der normalen Zuordnung erhöht (oder verringert).</span><span class="sxs-lookup"><span data-stu-id="b959f-120">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="b959f-121">Höhere Werte machen Bumps in der Regel sichtbarer, niedrigere Werte machen Bumps in der Regel weniger sichtbar.</span><span class="sxs-lookup"><span data-stu-id="b959f-121">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="b959f-122">*pDestTexture* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b959f-122">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b959f-123">Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="b959f-123">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="b959f-124">Zeiger auf eine ID3D10Texture2D-Schnittstelle, die die Zieltextur darstellt.</span><span class="sxs-lookup"><span data-stu-id="b959f-124">Pointer to an ID3D10Texture2D interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b959f-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b959f-125">Return value</span></span>

<span data-ttu-id="b959f-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b959f-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b959f-127">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b959f-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b959f-128">Wenn die Funktion fehlschlägt, kann der Rückgabewert folgender Wert sein: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b959f-128">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b959f-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b959f-129">Remarks</span></span>

<span data-ttu-id="b959f-130">Diese Methode berechnet den Normalwert, indem der zentrale Unterschied mit einer Kernelgröße von 3 x 3 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b959f-130">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="b959f-131">RGB-Kanäle im Ziel enthalten verzerrte (x,y,z)-Komponenten des Normals.</span><span class="sxs-lookup"><span data-stu-id="b959f-131">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="b959f-132">Der zentrale Unterscheidende Nenner ist auf 2,0 hartcodiert.</span><span class="sxs-lookup"><span data-stu-id="b959f-132">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="b959f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b959f-133">Requirements</span></span>



| <span data-ttu-id="b959f-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b959f-134">Requirement</span></span> | <span data-ttu-id="b959f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b959f-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b959f-136">Header</span><span class="sxs-lookup"><span data-stu-id="b959f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b959f-137"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="b959f-137"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b959f-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b959f-138">Library</span></span><br/> | <dl> <span data-ttu-id="b959f-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b959f-139"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b959f-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b959f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b959f-141">Texturfunktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="b959f-141">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
