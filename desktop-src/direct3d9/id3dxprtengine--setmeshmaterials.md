---
description: Legt gittermaterial Eigenschaften in der 3D-Szene fest. Verwenden Sie diese Methode, um Parameter für die unter Surface-Verteilung anzugeben.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'ID3DXPRTEngine:: stmeschmaterials-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355686"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a><span data-ttu-id="d6c7e-104">ID3DXPRTEngine:: stmeschmaterials-Methode</span><span class="sxs-lookup"><span data-stu-id="d6c7e-104">ID3DXPRTEngine::SetMeshMaterials method</span></span>

<span data-ttu-id="d6c7e-105">Legt gittermaterial Eigenschaften in der 3D-Szene fest.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-105">Sets mesh material properties in the 3D scene.</span></span> <span data-ttu-id="d6c7e-106">Verwenden Sie diese Methode, um Parameter für die unter Surface-Verteilung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-106">Use this method to specify subsurface scattering parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c7e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6c7e-107">Syntax</span></span>


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a><span data-ttu-id="d6c7e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6c7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c7e-109">*ppmaterials* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6c7e-109">*ppMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c7e-110">Typ: **Konstanten [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="d6c7e-110">Type: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md)\*\***</span></span>

<span data-ttu-id="d6c7e-111">Adresse eines Zeigers auf gewünschte gittermaterial Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-111">Address of a pointer to desired mesh material properties.</span></span> <span data-ttu-id="d6c7e-112">Siehe [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="d6c7e-112">See [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6c7e-113">*Nummeshes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6c7e-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c7e-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6c7e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6c7e-115">Der Index des Netzes, in dem Materialeigenschaften festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-115">Index of the mesh on which to set material properties.</span></span>

</dd> <dt>

<span data-ttu-id="d6c7e-116">*Numchannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6c7e-116">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c7e-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6c7e-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6c7e-118">Anzahl von Farbkanälen, die im Mesh festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-118">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="d6c7e-119">Legen Sie auf 1 fest, um graue Materialien (R = G = B) oder 3 anzugeben, um Farb Blutungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-119">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span> <span data-ttu-id="d6c7e-120">Wenn Sie diesen Parameter ändern möchten, legen Sie zuerst "Albedo" mit einer anderen Methode fest, wie z. [**b. ID3DXPRTEngine:: setpertexelalbedo**](id3dxprtengine--setpertexelalbedo.md) oder [**ID3DXPRTEngine:: setpervertexalbedo**](id3dxprtengine--setpervertexalbedo.md).</span><span class="sxs-lookup"><span data-stu-id="d6c7e-120">If you intend to change this parameter, first set the albedo using another method such as [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) or [**ID3DXPRTEngine::SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6c7e-121">*babtalbedo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6c7e-121">*bSetAlbedo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c7e-122">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6c7e-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6c7e-123">Wenn **true**, wird die Albedo-Option des Netzes auf ppmaterials festgelegt, wobei alle vorhandenen texelwerte und Vertex-Albedo-Werte überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-123">If **TRUE**, sets the albedo of the mesh to ppMaterials, overwriting all existing texel and vertex albedo values.</span></span> <span data-ttu-id="d6c7e-124">Wenn **false**, werden alle vorhandenen texkingwerte und Vertex Albedo-Werte beibehalten, die von anderen Methoden festgelegt werden. Numchannels muss mit dem Parameter numchannels identisch sein, der zum Erstellen des Puffers in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) oder [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-124">If **FALSE**, preserves all existing texel and vertex albedo values set by other methods; NumChannels must match the NumChannels parameter used to create the buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6c7e-125">*flengthscale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6c7e-125">*fLengthScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c7e-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6c7e-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6c7e-127">Skalierung der 3D-Szene in Relation zu einem 1-mm-Cube.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-127">Scale of the 3D scene relative to a 1-mm cube.</span></span> <span data-ttu-id="d6c7e-128">Wird für die Berechnung von subsurface-Strukturen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-128">Used for subsurface scattering computations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c7e-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6c7e-129">Return value</span></span>

<span data-ttu-id="d6c7e-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6c7e-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6c7e-131">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-131">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d6c7e-132">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c7e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6c7e-133">Requirements</span></span>



| <span data-ttu-id="d6c7e-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6c7e-134">Requirement</span></span> | <span data-ttu-id="d6c7e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d6c7e-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c7e-136">Header</span><span class="sxs-lookup"><span data-stu-id="d6c7e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d6c7e-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c7e-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d6c7e-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d6c7e-138">Library</span></span><br/> | <dl> <span data-ttu-id="d6c7e-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6c7e-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6c7e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6c7e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c7e-141">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="d6c7e-141">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
