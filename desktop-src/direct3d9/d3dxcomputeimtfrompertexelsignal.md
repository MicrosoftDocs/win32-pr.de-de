---
description: Berechnen von pro-Dreieck-Daten aus pro-Texttypen. Diese Funktion ähnelt D3DXComputeIMTFromTexture, aber Sie verwendet ein Float-Array, um die Daten zu übergeben, und Sie kann höhere Dimensions Werte berechnen als 4.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: D3DXComputeIMTFromPerTexelSignal-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353734"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a><span data-ttu-id="4992e-104">D3DXComputeIMTFromPerTexelSignal-Funktion</span><span class="sxs-lookup"><span data-stu-id="4992e-104">D3DXComputeIMTFromPerTexelSignal function</span></span>

<span data-ttu-id="4992e-105">Berechnen von pro-Dreieck-Daten aus pro-Texttypen.</span><span class="sxs-lookup"><span data-stu-id="4992e-105">Calculate per-triangle IMT's from per-texel data.</span></span> <span data-ttu-id="4992e-106">Diese Funktion ähnelt [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), aber Sie verwendet ein Float-Array, um die Daten zu übergeben, und Sie kann höhere Dimensions Werte berechnen als 4.</span><span class="sxs-lookup"><span data-stu-id="4992e-106">This function is similar to [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), but it uses a float array to pass in the data, and it can calculate higher dimensional values than 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="4992e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4992e-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="4992e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4992e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4992e-109">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4992e-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4992e-110">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="4992e-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="4992e-111">Ein Zeiger auf ein Eingabe Gitter (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des IMTS enthält.</span><span class="sxs-lookup"><span data-stu-id="4992e-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="4992e-112">*dwtextureindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4992e-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4992e-113">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4992e-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4992e-114">NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4992e-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="4992e-115">*pftexelsignal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4992e-115">*pfTexelSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4992e-116">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4992e-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4992e-117">Ein Zeiger auf ein Array von Eingabe texeln, von dem IMT berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4992e-117">A pointer to an array of input texels from which IMT will be computed.</span></span> <span data-ttu-id="4992e-118">Die Array Größe ist \* uheight uheight \* ucomponents.</span><span class="sxs-lookup"><span data-stu-id="4992e-118">The array size is uWidth\*uHeight\*uComponents.</span></span>

</dd> <dt>

<span data-ttu-id="4992e-119">*uwidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4992e-119">*uWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4992e-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4992e-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4992e-121">Textur Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4992e-121">Texture width in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4992e-122">*uheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4992e-122">*uHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4992e-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4992e-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4992e-124">Textur Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4992e-124">Texture height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4992e-125">*usignaldimension* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4992e-125">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4992e-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4992e-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4992e-127">Die Anzahl von Gleit Komma Zahlen pro Komponente in jedem Element des Signal Arrays.</span><span class="sxs-lookup"><span data-stu-id="4992e-127">The number of floats per-component in each element of the signal array.</span></span>

</dd> <dt>

<span data-ttu-id="4992e-128">*ucomponents* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4992e-128">*uComponents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4992e-129">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4992e-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4992e-130">Die Anzahl der Komponenten in jeder tex.</span><span class="sxs-lookup"><span data-stu-id="4992e-130">The number of components in each texel.</span></span>

</dd> <dt>

<span data-ttu-id="4992e-131">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4992e-131">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4992e-132">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4992e-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4992e-133">Textur Umbruch Optionen.</span><span class="sxs-lookup"><span data-stu-id="4992e-133">Texture wrap options.</span></span> <span data-ttu-id="4992e-134">Dies ist eine Kombination aus einem oder mehreren [**D3DXIMT-Flags**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4992e-134">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="4992e-135">*pstatus Callback*</span><span class="sxs-lookup"><span data-stu-id="4992e-135">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="4992e-136">Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="4992e-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="4992e-137">Ein Zeiger auf eine Rückruffunktion zum Überwachen des Fortschritts der IMT-Berechnung.</span><span class="sxs-lookup"><span data-stu-id="4992e-137">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="4992e-138">*pusercontext*</span><span class="sxs-lookup"><span data-stu-id="4992e-138">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="4992e-139">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4992e-139">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4992e-140">Ein Zeiger auf eine benutzerdefinierte Variable, die an die Status Rückruffunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4992e-140">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="4992e-141">Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4992e-141">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="4992e-142">*ppimtdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4992e-142">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4992e-143">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4992e-143">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4992e-144">Ein Zeiger auf den Puffer (siehe [**ID3DXBuffer**](id3dxbuffer.md)), der das zurückgegebene IMT-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="4992e-144">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="4992e-145">Dieses Array kann als Eingabe für die D3DX [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md) bereitgestellt werden, um die Zuordnung des Textur Raums in der Textur Parametrisierung zu priorisieren.</span><span class="sxs-lookup"><span data-stu-id="4992e-145">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4992e-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4992e-146">Return value</span></span>

<span data-ttu-id="4992e-147">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4992e-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4992e-148">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="4992e-148">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4992e-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4992e-149">Requirements</span></span>



| <span data-ttu-id="4992e-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4992e-150">Requirement</span></span> | <span data-ttu-id="4992e-151">Wert</span><span class="sxs-lookup"><span data-stu-id="4992e-151">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4992e-152">Header</span><span class="sxs-lookup"><span data-stu-id="4992e-152">Header</span></span><br/>  | <dl> <span data-ttu-id="4992e-153"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4992e-153"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4992e-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4992e-154">Library</span></span><br/> | <dl> <span data-ttu-id="4992e-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4992e-155"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4992e-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4992e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4992e-157">Uvatlas-Funktionen</span><span class="sxs-lookup"><span data-stu-id="4992e-157">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="4992e-158">Verwenden von uvatlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4992e-158">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
