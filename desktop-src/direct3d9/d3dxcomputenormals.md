---
description: Berechnet Einheiten normale für jeden Scheitelpunkt in einem Mesh. Wird zur Unterstützung von Legacy Anwendungen bereitgestellt. Verwenden Sie D3DXComputeTangentFrameEx, um bessere Ergebnisse zu erzielen.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: D3DXComputeNormals-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961654"
---
# <a name="d3dxcomputenormals-function"></a><span data-ttu-id="ab3a3-105">D3DXComputeNormals-Funktion</span><span class="sxs-lookup"><span data-stu-id="ab3a3-105">D3DXComputeNormals function</span></span>

<span data-ttu-id="ab3a3-106">Berechnet Einheiten normale für jeden Scheitelpunkt in einem Mesh.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-106">Computes unit normals for each vertex in a mesh.</span></span> <span data-ttu-id="ab3a3-107">Wird zur Unterstützung von Legacy Anwendungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-107">Provided to support legacy applications.</span></span> <span data-ttu-id="ab3a3-108">Verwenden Sie [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) , um bessere Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab3a3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab3a3-109">Syntax</span></span>


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="ab3a3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab3a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab3a3-111">*pmesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ab3a3-111">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab3a3-112">Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ab3a3-112">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="ab3a3-113">Zeiger auf eine [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle, die das normalisierte Mesh-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-113">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the normalized mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="ab3a3-114">*padjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab3a3-114">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab3a3-115">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ab3a3-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ab3a3-116">Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im erstellten progressiven Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the created progressive mesh.</span></span> <span data-ttu-id="ab3a3-117">Dieser Parameter ist optional und sollte auf **null** festgelegt werden, wenn er nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-117">This parameter is optional and should be set to **NULL** if it is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab3a3-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab3a3-118">Return value</span></span>

<span data-ttu-id="ab3a3-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab3a3-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab3a3-120">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-120">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ab3a3-121">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab3a3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab3a3-122">Remarks</span></span>

<span data-ttu-id="ab3a3-123">Für das eingabemesh muss das Flag [D3DFVF \_ Normal](d3dfvf.md) in seinem flexiblen Scheitelpunkt Format (FVF) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-123">The input mesh must have the [D3DFVF\_NORMAL](d3dfvf.md) flag specified in its flexible vertex format (FVF).</span></span>

<span data-ttu-id="ab3a3-124">Ein normaler Wert für einen Scheitelpunkt wird generiert, indem die normale aller Gesichter, die den Scheitelpunkt teilen, überdurchschnittlich werden.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-124">A normal for a vertex is generated by averaging the normals of all faces that share that vertex.</span></span>

<span data-ttu-id="ab3a3-125">Wenn eine Angabe bereitgestellt wird, werden replizierte Scheitel Punkte ignoriert und "gegläoniert".</span><span class="sxs-lookup"><span data-stu-id="ab3a3-125">If adjacency is provided, replicated vertices are ignored and "smoothed" over.</span></span> <span data-ttu-id="ab3a3-126">Wenn keine Angabe bereitgestellt wird, weisen replizierte Scheitel Punkte, die von nur den Gesichtern abgeleitet werden, die explizit auf Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="ab3a3-126">If adjacency is not provided, replicated vertices will have normals averaged in from only the faces explicitly referencing them.</span></span>

<span data-ttu-id="ab3a3-127">Diese Funktion ruft einfach [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) mit den folgenden Eingabe Parametern auf:</span><span class="sxs-lookup"><span data-stu-id="ab3a3-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="ab3a3-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab3a3-128">Requirements</span></span>



| <span data-ttu-id="ab3a3-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab3a3-129">Requirement</span></span> | <span data-ttu-id="ab3a3-130">Wert</span><span class="sxs-lookup"><span data-stu-id="ab3a3-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab3a3-131">Header</span><span class="sxs-lookup"><span data-stu-id="ab3a3-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ab3a3-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab3a3-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ab3a3-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab3a3-133">Library</span></span><br/> | <dl> <span data-ttu-id="ab3a3-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab3a3-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab3a3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab3a3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab3a3-136">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ab3a3-136">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
