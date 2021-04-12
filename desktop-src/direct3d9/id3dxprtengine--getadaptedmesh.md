---
description: Gibt ein Mesh mit Änderungen zurück, die sich aus der Adaptive räumlichen Stichprobe ergeben Das zurückgegebene Mesh enthält nur Positionen, normale und Texturkoordinaten (sofern definiert).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'ID3DXPRTEngine:: getadaptedmesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d012344a5dfbc1bc17780cb4ab9a53820fe34f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355696"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a><span data-ttu-id="16515-104">ID3DXPRTEngine:: getadaptedmesh-Methode</span><span class="sxs-lookup"><span data-stu-id="16515-104">ID3DXPRTEngine::GetAdaptedMesh method</span></span>

<span data-ttu-id="16515-105">Gibt ein Mesh mit Änderungen zurück, die sich aus der Adaptive räumlichen Stichprobe ergeben</span><span class="sxs-lookup"><span data-stu-id="16515-105">Returns a mesh with modifications resulting from adaptive spatial sampling.</span></span> <span data-ttu-id="16515-106">Das zurückgegebene Mesh enthält nur Positionen, normale und Texturkoordinaten (sofern definiert).</span><span class="sxs-lookup"><span data-stu-id="16515-106">The returned mesh contains only positions, normals, and texture coordinates (if defined).</span></span>

## <a name="syntax"></a><span data-ttu-id="16515-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="16515-107">Syntax</span></span>


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="16515-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="16515-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16515-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16515-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16515-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="16515-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="16515-111">Zeiger auf ein [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Gerät, das zum Erstellen des Ausgabe Netzes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16515-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="16515-112">*pfakeremap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="16515-112">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16515-113">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="16515-113">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="16515-114">Zeiger auf das ursprüngliche Gitter Gesicht, das geteilt wurde, um die aktuelle Seite zu generieren.</span><span class="sxs-lookup"><span data-stu-id="16515-114">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> <dt>

<span data-ttu-id="16515-115">*pvertremap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="16515-115">*pVertRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16515-116">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="16515-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="16515-117">Ein Zeiger auf ein Ziel Array, das die drei ursprünglichen Gitter Scheitel Punkte enthält, die die übergeordneten Elemente des aktuellen Scheitel Punkts sind.</span><span class="sxs-lookup"><span data-stu-id="16515-117">Pointer to a destination array containing the three original mesh vertices that are the parents of the current vertex.</span></span>

</dd> <dt>

<span data-ttu-id="16515-118">*pfvertgewichtungen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="16515-118">*pfVertWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16515-119">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="16515-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="16515-120">Ein Zeiger auf ein Ziel Array, das die Mischungs Faktoren für die pvertremap-Vertices enthält.</span><span class="sxs-lookup"><span data-stu-id="16515-120">Pointer to a destination array containing blending factors for the pVertRemap vertices.</span></span>

</dd> <dt>

<span data-ttu-id="16515-121">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="16515-121">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16515-122">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="16515-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="16515-123">Zeiger auf das Ausgabe [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt.</span><span class="sxs-lookup"><span data-stu-id="16515-123">Pointer to the output [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16515-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16515-124">Return value</span></span>

<span data-ttu-id="16515-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16515-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16515-126">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="16515-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="16515-127">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="16515-127">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="16515-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16515-128">Remarks</span></span>

<span data-ttu-id="16515-129">pvertremap und pfvertgewichtungen können verwendet werden, um einen beliebigen pro-Vertex-Wert über das Mesh zu interpolieren.</span><span class="sxs-lookup"><span data-stu-id="16515-129">pVertRemap and pfVertWeights can be used to interpolate any per-vertex value over the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="16515-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16515-130">Requirements</span></span>



| <span data-ttu-id="16515-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16515-131">Requirement</span></span> | <span data-ttu-id="16515-132">Wert</span><span class="sxs-lookup"><span data-stu-id="16515-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16515-133">Header</span><span class="sxs-lookup"><span data-stu-id="16515-133">Header</span></span><br/>  | <dl> <span data-ttu-id="16515-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="16515-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="16515-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="16515-135">Library</span></span><br/> | <dl> <span data-ttu-id="16515-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16515-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16515-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16515-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16515-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="16515-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
