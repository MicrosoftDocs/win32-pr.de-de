---
description: Berechnet pro Dreieck von einem benutzerdefinierten, von der Anwendung angegebenen Signal, das sich über der Oberfläche des Netzes (in der Regel mit einer höheren Frequenz als Scheitelpunkt Daten) unterscheidet. Das Signal wird über eine vom Benutzer angegebene Rückruffunktion ausgewertet.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: D3DXComputeIMTFromSignal-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363155"
---
# <a name="d3dxcomputeimtfromsignal-function"></a><span data-ttu-id="73c58-104">D3DXComputeIMTFromSignal-Funktion</span><span class="sxs-lookup"><span data-stu-id="73c58-104">D3DXComputeIMTFromSignal function</span></span>

<span data-ttu-id="73c58-105">Berechnet pro Dreieck von einem benutzerdefinierten, von der Anwendung angegebenen Signal, das sich über der Oberfläche des Netzes (in der Regel mit einer höheren Frequenz als Scheitelpunkt Daten) unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="73c58-105">Calculates per-triangle IMT's from a custom application-specified signal that varies over the surface of the mesh (generally at a higher frequency than vertex data).</span></span> <span data-ttu-id="73c58-106">Das Signal wird über eine vom Benutzer angegebene Rückruffunktion ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="73c58-106">The signal is evaluated via a user-specified callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c58-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73c58-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="73c58-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73c58-109">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73c58-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c58-110">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="73c58-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="73c58-111">Ein Zeiger auf ein Eingabe Gitter (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des IMTS enthält.</span><span class="sxs-lookup"><span data-stu-id="73c58-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="73c58-112">*dwtextureindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73c58-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c58-113">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c58-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73c58-114">NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="73c58-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="73c58-115">*usignaldimension* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73c58-115">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c58-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c58-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73c58-117">Die Anzahl der Komponenten in jedem Datenpunkt im Signal.</span><span class="sxs-lookup"><span data-stu-id="73c58-117">The number of components in each data point in the signal.</span></span>

</dd> <dt>

<span data-ttu-id="73c58-118">*fmaxuvdistance* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73c58-118">*fMaxUVDistance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c58-119">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c58-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73c58-120">Der maximale Abstand zwischen Scheitel Punkten; der Algorithmus setzt die Unterteilung fort, bis der Abstand zwischen allen Scheitel Punkten kleiner oder gleich fmaxuvdistance ist.</span><span class="sxs-lookup"><span data-stu-id="73c58-120">The maximum distance between vertices; the algorithm continues subdividing until the distance between all vertices is less than or equal to fMaxUVDistance.</span></span>

</dd> <dt>

<span data-ttu-id="73c58-121">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73c58-121">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c58-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c58-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73c58-123">Textur Umbruch Optionen.</span><span class="sxs-lookup"><span data-stu-id="73c58-123">Texture wrap options.</span></span> <span data-ttu-id="73c58-124">Dies ist eine Kombination aus einem oder mehreren [**D3DXIMT-Flags**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="73c58-124">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c58-125">*psignalcallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73c58-125">*pSignalCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c58-126">Typ: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span><span class="sxs-lookup"><span data-stu-id="73c58-126">Type: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span></span>

<span data-ttu-id="73c58-127">Ein Zeiger auf eine vom Benutzer bereitgestellte evaluatorfunktion, die verwendet wird, um den Signalwert bei beliebigen U-, V-Koordinaten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="73c58-127">A pointer to a user-provided evaluator function, which will be used to compute the signal value at arbitrary U,V coordinates.</span></span> <span data-ttu-id="73c58-128">Die-Funktion folgt dem Prototyp von [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span><span class="sxs-lookup"><span data-stu-id="73c58-128">The function follows the prototype of [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c58-129">*puserdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73c58-129">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c58-130">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="73c58-130">Type: **VOID\***</span></span>

<span data-ttu-id="73c58-131">Ein Zeiger auf einen benutzerdefinierten Wert, der an die Signal Rückruffunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="73c58-131">A pointer to a user-defined value which is passed to the signal callback function.</span></span> <span data-ttu-id="73c58-132">Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="73c58-132">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="73c58-133">*pstatus Callback*</span><span class="sxs-lookup"><span data-stu-id="73c58-133">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="73c58-134">Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="73c58-134">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="73c58-135">Ein Zeiger auf eine Rückruffunktion zum Überwachen des Fortschritts der IMT-Berechnung.</span><span class="sxs-lookup"><span data-stu-id="73c58-135">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="73c58-136">*pusercontext*</span><span class="sxs-lookup"><span data-stu-id="73c58-136">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="73c58-137">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c58-137">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73c58-138">Ein Zeiger auf eine benutzerdefinierte Variable, die an die Status Rückruffunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="73c58-138">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="73c58-139">Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="73c58-139">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="73c58-140">*ppimtdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73c58-140">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73c58-141">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="73c58-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="73c58-142">Ein Zeiger auf den Puffer (siehe [**ID3DXBuffer**](id3dxbuffer.md)), der das zurückgegebene IMT-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="73c58-142">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="73c58-143">Dieses Array kann als Eingabe für die D3DX [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md) bereitgestellt werden, um die Zuordnung des Textur Raums in der Textur Parametrisierung zu priorisieren.</span><span class="sxs-lookup"><span data-stu-id="73c58-143">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73c58-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73c58-144">Return value</span></span>

<span data-ttu-id="73c58-145">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73c58-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73c58-146">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="73c58-146">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="73c58-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73c58-147">Remarks</span></span>

<span data-ttu-id="73c58-148">Diese Funktion erfordert, dass das eingabemesh eine Signal-zu-Mesh-Textur Zuordnung (d.h. Texturkoordinaten) enthält.</span><span class="sxs-lookup"><span data-stu-id="73c58-148">This function requires that the input mesh contain a signal-to-mesh texture mapping (ie. texture coordinates).</span></span> <span data-ttu-id="73c58-149">Dadurch kann der Benutzer ein Signal willkürlich über der Oberfläche des Netzes definieren.</span><span class="sxs-lookup"><span data-stu-id="73c58-149">It allows the user to define a signal arbitrarily over the surface of the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="73c58-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73c58-150">Requirements</span></span>



| <span data-ttu-id="73c58-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73c58-151">Requirement</span></span> | <span data-ttu-id="73c58-152">Wert</span><span class="sxs-lookup"><span data-stu-id="73c58-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73c58-153">Header</span><span class="sxs-lookup"><span data-stu-id="73c58-153">Header</span></span><br/>  | <dl> <span data-ttu-id="73c58-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c58-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="73c58-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73c58-155">Library</span></span><br/> | <dl> <span data-ttu-id="73c58-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73c58-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73c58-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73c58-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c58-158">Uvatlas-Funktionen</span><span class="sxs-lookup"><span data-stu-id="73c58-158">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="73c58-159">Verwenden von uvatlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="73c58-159">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
