---
description: Berechnet die Tangenten Vektoren für die in der Textur Phase angegebenen Texturkoordinaten. Wird zur Unterstützung von Legacy Anwendungen bereitgestellt. Verwenden Sie D3DXComputeTangentFrameEx, um bessere Ergebnisse zu erzielen.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: D3DXComputeTangent-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366638"
---
# <a name="d3dxcomputetangent-function"></a><span data-ttu-id="ca225-105">D3DXComputeTangent-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca225-105">D3DXComputeTangent function</span></span>

<span data-ttu-id="ca225-106">Berechnet die Tangenten Vektoren für die in der Textur Phase angegebenen Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="ca225-106">Computes the tangent vectors for the texture coordinates given in the texture stage.</span></span> <span data-ttu-id="ca225-107">Wird zur Unterstützung von Legacy Anwendungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ca225-107">Provided to support legacy applications.</span></span> <span data-ttu-id="ca225-108">Verwenden Sie [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) , um bessere Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="ca225-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca225-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca225-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="ca225-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca225-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca225-111">*Mesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca225-111">*Mesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca225-112">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ca225-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="ca225-113">Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das Eingabe Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca225-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represent the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ca225-114">*Texstagumdex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca225-114">*TexStageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca225-115">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca225-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca225-116">Der Index, der die Textur Phase darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca225-116">Index that represents the texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ca225-117">*Tangentindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca225-117">*TangentIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca225-118">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca225-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca225-119">Index, der den Verwendungs Index für die Tangens Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ca225-119">Index that provides the usage index for the tangent data.</span></span> <span data-ttu-id="ca225-120">Die Vertex-Deklaration impliziert die Verwendung. Dieser Index ändert die Verwendung mit dem Verwendungs Index.</span><span class="sxs-lookup"><span data-stu-id="ca225-120">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="ca225-121">Weitere Informationen zu einer Scheitelpunkt Deklaration finden Sie unter [Vertex-Deklaration (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="ca225-121">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca225-122">*Binormindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca225-122">*BinormIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca225-123">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca225-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca225-124">Index, der den Verwendungs Index für die Binärdaten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ca225-124">Index that provides the usage index for the binormal data.</span></span> <span data-ttu-id="ca225-125">Die Vertex-Deklaration impliziert die Verwendung. Dieser Index ändert die Verwendung mit dem Verwendungs Index.</span><span class="sxs-lookup"><span data-stu-id="ca225-125">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="ca225-126">Weitere Informationen zu einer Scheitelpunkt Deklaration finden Sie unter [Vertex-Deklaration (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="ca225-126">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca225-127"> Umbruch \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca225-127">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca225-128">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca225-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca225-129">Legen Sie diesen Wert auf 0 (null) fest, um keine Umbrüchen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ca225-129">Set this value to 0 for no wrapping, or to 1 for wrapping in the U and V directions.</span></span>

</dd> <dt>

<span data-ttu-id="ca225-130">*padjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca225-130">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca225-131">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ca225-131">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ca225-132">Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das mit angrenzenden Gesichts Indizes aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca225-132">Pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="ca225-133">Die Anzahl der Bytes in diesem Array muss mindestens ((3 \* [**getnumgesichter**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)) betragen.</span><span class="sxs-lookup"><span data-stu-id="ca225-133">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca225-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca225-134">Return value</span></span>

<span data-ttu-id="ca225-135">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca225-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca225-136">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca225-136">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ca225-137">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="ca225-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca225-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca225-138">Remarks</span></span>

<span data-ttu-id="ca225-139">Wenn die Mesh-Vertex-Deklaration Tangens-oder Binormale-Felder angibt, aktualisiert **D3DXComputeTangent** alle vom Benutzer bereitgestellten Tangens-oder Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="ca225-139">If the mesh vertex declaration specifies tangent or binormal fields, **D3DXComputeTangent** will update any user-supplied tangent or binormal data.</span></span> <span data-ttu-id="ca225-140">Alternativ können Sie tangentindex auf [D3DX \_ default](other-d3dx-constants.md) festlegen, um die vom Benutzer bereitgestellten Tangens Daten nicht zu aktualisieren, oder binormindex auf D3DX default festlegen, \_ um die vom Benutzer bereitgestellten Binärdaten nicht zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ca225-140">Alternatively, set TangentIndex to [D3DX\_DEFAULT](other-d3dx-constants.md) to not update the user-supplied tangent data, or set BinormIndex to D3DX\_DEFAULT to not update the user-supplied binormal data.</span></span> <span data-ttu-id="ca225-141">Texstageindex kann nicht auf D3DX Default festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="ca225-141">TexStageIndex cannot be set to D3DX\_DEFAULT.</span></span>

<span data-ttu-id="ca225-142">**D3DXComputeTangent** hängt von der Mesh-Vertexdeklaration ab, die entweder das Binormal-Feld (binormindex), das Tangens Feld (tangentindex) oder beides enthält.</span><span class="sxs-lookup"><span data-stu-id="ca225-142">**D3DXComputeTangent** depends on the mesh vertex declaration containing either the binormal field (BinormIndex), the tangent field (TangentIndex), or both.</span></span> <span data-ttu-id="ca225-143">Wenn beide fehlen, schlägt diese Funktion fehl.</span><span class="sxs-lookup"><span data-stu-id="ca225-143">If both are missing, this function will fail.</span></span>

<span data-ttu-id="ca225-144">Diese Funktion ruft einfach [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) mit den folgenden Eingabe Parametern auf:</span><span class="sxs-lookup"><span data-stu-id="ca225-144">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="ca225-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca225-145">Requirements</span></span>



| <span data-ttu-id="ca225-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca225-146">Requirement</span></span> | <span data-ttu-id="ca225-147">Wert</span><span class="sxs-lookup"><span data-stu-id="ca225-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca225-148">Header</span><span class="sxs-lookup"><span data-stu-id="ca225-148">Header</span></span><br/>  | <dl> <span data-ttu-id="ca225-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca225-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ca225-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca225-150">Library</span></span><br/> | <dl> <span data-ttu-id="ca225-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca225-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ca225-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca225-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca225-153">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ca225-153">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
