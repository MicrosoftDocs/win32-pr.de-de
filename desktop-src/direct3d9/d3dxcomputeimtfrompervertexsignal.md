---
description: Berechnen Sie die pro-Dreieck-IMT aus aus den einzelnen Scheitel Punkten. Diese Funktion ermöglicht es Ihnen, das IMT basierend auf einem beliebigen Wert in einem Mesh (Farbe, normal usw.) zu berechnen.
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: D3DXComputeIMTFromPerVertexSignal-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363981"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a><span data-ttu-id="6b322-104">D3DXComputeIMTFromPerVertexSignal-Funktion</span><span class="sxs-lookup"><span data-stu-id="6b322-104">D3DXComputeIMTFromPerVertexSignal function</span></span>

<span data-ttu-id="6b322-105">Berechnen Sie die pro-Dreieck-IMT aus aus den einzelnen Scheitel Punkten.</span><span class="sxs-lookup"><span data-stu-id="6b322-105">Calculate per-triangle IMT's from from per-vertex data.</span></span> <span data-ttu-id="6b322-106">Diese Funktion ermöglicht es Ihnen, das IMT basierend auf einem beliebigen Wert in einem Mesh (Farbe, normal usw.) zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="6b322-106">This function allows you to calculate the IMT based off of any value in a mesh (color, normal, etc).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b322-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b322-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="6b322-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b322-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b322-109">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b322-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b322-110">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="6b322-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="6b322-111">Ein Zeiger auf ein Eingabe Gitter (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des IMTS enthält.</span><span class="sxs-lookup"><span data-stu-id="6b322-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="6b322-112">*pfvertexsignal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b322-112">*pfVertexSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b322-113">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b322-113">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6b322-114">Ein Zeiger auf ein Array von pro-Vertex-Daten, aus denen IMT berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="6b322-114">A pointer to an array of per-vertex data from which IMT will be computed.</span></span> <span data-ttu-id="6b322-115">Die Array Größe ist "usignalstride \* v", wobei "v" die Anzahl der Scheitel Punkte im Mesh ist.</span><span class="sxs-lookup"><span data-stu-id="6b322-115">The array size is uSignalStride \* v, where v is the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6b322-116">*usignaldimension* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b322-116">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b322-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b322-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b322-118">Die Anzahl von Gleit Komma Zahlen pro Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="6b322-118">The number of floats per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="6b322-119">*usignalstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b322-119">*uSignalStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b322-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b322-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b322-121">Die Anzahl der Bytes pro Scheitelpunkt im Array.</span><span class="sxs-lookup"><span data-stu-id="6b322-121">The number of bytes per vertex in the array.</span></span> <span data-ttu-id="6b322-122">Dabei muss es sich um ein Vielfaches von sizeof (float) handeln.</span><span class="sxs-lookup"><span data-stu-id="6b322-122">This must be a multiple of sizeof(float)</span></span>

</dd> <dt>

<span data-ttu-id="6b322-123">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b322-123">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b322-124">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b322-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b322-125">Textur Umbruch Optionen.</span><span class="sxs-lookup"><span data-stu-id="6b322-125">Texture wrap options.</span></span> <span data-ttu-id="6b322-126">Dies ist eine Kombination aus einem oder mehreren [**D3DXIMT-Flags**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6b322-126">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b322-127">*pstatus Callback*</span><span class="sxs-lookup"><span data-stu-id="6b322-127">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="6b322-128">Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="6b322-128">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="6b322-129">Ein Zeiger auf eine Rückruffunktion zum Überwachen des Fortschritts der IMT-Berechnung.</span><span class="sxs-lookup"><span data-stu-id="6b322-129">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="6b322-130">*pusercontext*</span><span class="sxs-lookup"><span data-stu-id="6b322-130">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="6b322-131">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b322-131">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b322-132">Ein Zeiger auf eine benutzerdefinierte Variable, die an die Status Rückruffunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="6b322-132">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="6b322-133">Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6b322-133">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="6b322-134">*ppimtdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b322-134">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b322-135">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b322-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6b322-136">Ein Zeiger auf den Puffer (siehe [**ID3DXBuffer**](id3dxbuffer.md)), der das zurückgegebene IMT-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="6b322-136">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="6b322-137">Dieses Array kann als Eingabe für die D3DX [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md) bereitgestellt werden, um die Zuordnung des Textur Raums in der Textur Parametrisierung zu priorisieren.</span><span class="sxs-lookup"><span data-stu-id="6b322-137">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b322-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b322-138">Return value</span></span>

<span data-ttu-id="6b322-139">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b322-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b322-140">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="6b322-140">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b322-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b322-141">Requirements</span></span>



| <span data-ttu-id="6b322-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b322-142">Requirement</span></span> | <span data-ttu-id="6b322-143">Wert</span><span class="sxs-lookup"><span data-stu-id="6b322-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b322-144">Header</span><span class="sxs-lookup"><span data-stu-id="6b322-144">Header</span></span><br/>  | <dl> <span data-ttu-id="6b322-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b322-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6b322-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b322-146">Library</span></span><br/> | <dl> <span data-ttu-id="6b322-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b322-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b322-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b322-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b322-149">Uvatlas-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6b322-149">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="6b322-150">Verwenden von uvatlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6b322-150">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
