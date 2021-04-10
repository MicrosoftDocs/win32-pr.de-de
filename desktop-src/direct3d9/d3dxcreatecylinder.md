---
description: Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das einen Zylinder enthält.
ms.assetid: 54b8a59e-d13f-44cb-84c0-f63c7b1ffb1b
title: D3DXCreateCylinder-Funktion (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCylinder
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec97755d45b21a85e1a73bbcd2214ee4c1e2358f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762090"
---
# <a name="d3dxcreatecylinder-function"></a><span data-ttu-id="7ece3-103">D3DXCreateCylinder-Funktion</span><span class="sxs-lookup"><span data-stu-id="7ece3-103">D3DXCreateCylinder function</span></span>

<span data-ttu-id="7ece3-104">Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das einen Zylinder enthält.</span><span class="sxs-lookup"><span data-stu-id="7ece3-104">Uses a left-handed coordinate system to create a mesh containing a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ece3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ece3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCylinder(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius1,
  _In_  FLOAT             Radius2,
  _In_  FLOAT             Length,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="7ece3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ece3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ece3-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ece3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ece3-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7ece3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7ece3-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das dem erstellten Zylinder Netz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7ece3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created cylinder mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7ece3-110">*Radius1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ece3-110">*Radius1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ece3-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ece3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ece3-112">Radius am negativen Z-Ende.</span><span class="sxs-lookup"><span data-stu-id="7ece3-112">Radius at the negative Z end.</span></span> <span data-ttu-id="7ece3-113">Der Wert muss größer oder gleich 0,0 f sein.</span><span class="sxs-lookup"><span data-stu-id="7ece3-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="7ece3-114">*Radius2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ece3-114">*Radius2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ece3-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ece3-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ece3-116">Radius am positiven Z-Ende.</span><span class="sxs-lookup"><span data-stu-id="7ece3-116">Radius at the positive Z end.</span></span> <span data-ttu-id="7ece3-117">Der Wert muss größer oder gleich 0,0 f sein.</span><span class="sxs-lookup"><span data-stu-id="7ece3-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="7ece3-118">*Länge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ece3-118">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ece3-119">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ece3-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ece3-120">Länge des Zylinders entlang der z-Achse.</span><span class="sxs-lookup"><span data-stu-id="7ece3-120">Length of the cylinder along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="7ece3-121">*Slices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ece3-121">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ece3-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ece3-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ece3-123">Anzahl der Slices zur Hauptachse.</span><span class="sxs-lookup"><span data-stu-id="7ece3-123">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="7ece3-124">*Stapel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ece3-124">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ece3-125">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ece3-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ece3-126">Anzahl der Stapel entlang der Hauptachse.</span><span class="sxs-lookup"><span data-stu-id="7ece3-126">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="7ece3-127">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ece3-127">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ece3-128">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ece3-128">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="7ece3-129">Adresse eines Zeigers auf die Ausgabe Form, eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7ece3-129">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7ece3-130">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ece3-130">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ece3-131">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ece3-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7ece3-132">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7ece3-132">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="7ece3-133">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="7ece3-133">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="7ece3-134">**Null** kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7ece3-134">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ece3-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ece3-135">Return value</span></span>

<span data-ttu-id="7ece3-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ece3-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ece3-137">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7ece3-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7ece3-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="7ece3-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ece3-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ece3-139">Remarks</span></span>

<span data-ttu-id="7ece3-140">Der erstellte Zylinder wird am Ursprung zentriert, und seine Achse wird an der z-Achse ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="7ece3-140">The created cylinder is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="7ece3-141">Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="7ece3-141">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ece3-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ece3-142">Requirements</span></span>



| <span data-ttu-id="7ece3-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ece3-143">Requirement</span></span> | <span data-ttu-id="7ece3-144">Wert</span><span class="sxs-lookup"><span data-stu-id="7ece3-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ece3-145">Header</span><span class="sxs-lookup"><span data-stu-id="7ece3-145">Header</span></span><br/>  | <dl> <span data-ttu-id="7ece3-146"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ece3-146"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="7ece3-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7ece3-147">Library</span></span><br/> | <dl> <span data-ttu-id="7ece3-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ece3-148"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7ece3-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ece3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ece3-150">Formen Zeichnungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="7ece3-150">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
