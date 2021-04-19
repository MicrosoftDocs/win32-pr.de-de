---
description: Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das ein Achsen Bündiges Feld enthält.
ms.assetid: 396ef0f7-65d5-46f9-9b97-e6471f2fb5fe
title: D3DXCreateBox-Funktion (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 187c389dd2d90b4457237540026a63edc4ab4f4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361191"
---
# <a name="d3dxcreatebox-function"></a><span data-ttu-id="d2154-103">D3DXCreateBox-Funktion</span><span class="sxs-lookup"><span data-stu-id="d2154-103">D3DXCreateBox function</span></span>

<span data-ttu-id="d2154-104">Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das ein Achsen Bündiges Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="d2154-104">Uses a left-handed coordinate system to create a mesh containing an axis-aligned box.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2154-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2154-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBox(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Width,
  _In_  FLOAT             Height,
  _In_  FLOAT             Depth,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="d2154-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2154-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2154-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2154-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2154-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d2154-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d2154-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das dem erstellten Box-Mesh zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d2154-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d2154-110">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2154-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2154-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2154-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2154-112">Breite des Felds entlang der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="d2154-112">Width of the box, along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="d2154-113">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2154-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2154-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2154-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2154-115">Die Höhe des Felds entlang der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="d2154-115">Height of the box, along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="d2154-116">*Tiefe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2154-116">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2154-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2154-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2154-118">Die Tiefe des Felds entlang der z-Achse.</span><span class="sxs-lookup"><span data-stu-id="d2154-118">Depth of the box, along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="d2154-119">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d2154-119">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2154-120">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2154-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d2154-121">Adresse eines Zeigers auf die Ausgabe Form, eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d2154-121">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d2154-122">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d2154-122">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2154-123">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2154-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d2154-124">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d2154-124">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="d2154-125">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="d2154-125">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="d2154-126">**Null** kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d2154-126">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2154-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2154-127">Return value</span></span>

<span data-ttu-id="d2154-128">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2154-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2154-129">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2154-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d2154-130">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="d2154-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2154-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2154-131">Remarks</span></span>

<span data-ttu-id="d2154-132">Das erstellte Feld wird am Ursprung zentriert.</span><span class="sxs-lookup"><span data-stu-id="d2154-132">The created box is centered at the origin.</span></span>

<span data-ttu-id="d2154-133">Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="d2154-133">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2154-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2154-134">Requirements</span></span>



| <span data-ttu-id="d2154-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2154-135">Requirement</span></span> | <span data-ttu-id="d2154-136">Wert</span><span class="sxs-lookup"><span data-stu-id="d2154-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2154-137">Header</span><span class="sxs-lookup"><span data-stu-id="d2154-137">Header</span></span><br/>  | <dl> <span data-ttu-id="d2154-138"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2154-138"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="d2154-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d2154-139">Library</span></span><br/> | <dl> <span data-ttu-id="d2154-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2154-140"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d2154-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2154-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2154-142">Formen Zeichnungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="d2154-142">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
