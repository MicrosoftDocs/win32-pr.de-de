---
description: Erstellt ein ID3DXTextureGutterHelper-Objekt aus einem eingabemesh und Textur Daten.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: D3DXCreateTextureGutterHelper-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353729"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a><span data-ttu-id="40dfc-103">D3DXCreateTextureGutterHelper-Funktion</span><span class="sxs-lookup"><span data-stu-id="40dfc-103">D3DXCreateTextureGutterHelper function</span></span>

<span data-ttu-id="40dfc-104">Erstellt ein [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekt aus einem eingabemesh und Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="40dfc-104">Creates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object from an input mesh and texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="40dfc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40dfc-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="40dfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40dfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40dfc-107">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40dfc-107">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40dfc-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40dfc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40dfc-109">Breite der Textur in Pixel.</span><span class="sxs-lookup"><span data-stu-id="40dfc-109">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="40dfc-110">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40dfc-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40dfc-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40dfc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40dfc-112">Höhe der Textur in Pixel.</span><span class="sxs-lookup"><span data-stu-id="40dfc-112">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="40dfc-113">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40dfc-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40dfc-114">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="40dfc-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="40dfc-115">Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Eingabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="40dfc-115">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="40dfc-116">*Guttersize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40dfc-116">*GutterSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40dfc-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40dfc-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40dfc-118">Die Anzahl von texeln, nach denen die Textur über Stichprobe und der bundlockbereich erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40dfc-118">Number of texels by which to over-sample the texture and create the gutter region.</span></span> <span data-ttu-id="40dfc-119">Muss mindestens 1 sein.</span><span class="sxs-lookup"><span data-stu-id="40dfc-119">Must be at least 1.</span></span>

</dd> <dt>

<span data-ttu-id="40dfc-120">*ppbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40dfc-120">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40dfc-121">Typ: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span><span class="sxs-lookup"><span data-stu-id="40dfc-121">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span></span>

<span data-ttu-id="40dfc-122">Zeiger auf ein [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekt, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40dfc-122">Pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40dfc-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40dfc-123">Return value</span></span>

<span data-ttu-id="40dfc-124">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="40dfc-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="40dfc-125">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40dfc-125">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="40dfc-126">Wenn die Funktion fehlschlägt, kann der Rückgabewert eines der folgenden Werte sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="40dfc-126">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="40dfc-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40dfc-127">Remarks</span></span>

<span data-ttu-id="40dfc-128">Verwenden Sie [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) , um eine Szene in neue Koordinaten umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="40dfc-128">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to transform a scene to new coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="40dfc-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40dfc-129">Requirements</span></span>



| <span data-ttu-id="40dfc-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40dfc-130">Requirement</span></span> | <span data-ttu-id="40dfc-131">Wert</span><span class="sxs-lookup"><span data-stu-id="40dfc-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40dfc-132">Header</span><span class="sxs-lookup"><span data-stu-id="40dfc-132">Header</span></span><br/>  | <dl> <span data-ttu-id="40dfc-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="40dfc-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="40dfc-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40dfc-134">Library</span></span><br/> | <dl> <span data-ttu-id="40dfc-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40dfc-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="40dfc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40dfc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40dfc-137">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="40dfc-137">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
