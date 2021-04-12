---
description: Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das eine Kugel enthält.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: D3DXCreateSphere-Funktion (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56ac6b8e8cc2195e2176e505cf430ea33b6b6ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219524"
---
# <a name="d3dxcreatesphere-function"></a><span data-ttu-id="77df9-103">D3DXCreateSphere-Funktion</span><span class="sxs-lookup"><span data-stu-id="77df9-103">D3DXCreateSphere function</span></span>

<span data-ttu-id="77df9-104">Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das eine Kugel enthält.</span><span class="sxs-lookup"><span data-stu-id="77df9-104">Uses a left-handed coordinate system to create a mesh containing a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="77df9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="77df9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="77df9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77df9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77df9-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77df9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77df9-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="77df9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="77df9-109">Ein Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das dem erstellten Kugel Netz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="77df9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created sphere mesh.</span></span>

</dd> <dt>

<span data-ttu-id="77df9-110">*RADIUS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77df9-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77df9-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77df9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77df9-112">Der Radius der Kugel.</span><span class="sxs-lookup"><span data-stu-id="77df9-112">Radius of the sphere.</span></span> <span data-ttu-id="77df9-113">Dieser Wert muss größer oder gleich 0,0 f sein.</span><span class="sxs-lookup"><span data-stu-id="77df9-113">This value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="77df9-114">*Slices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77df9-114">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77df9-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77df9-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77df9-116">Anzahl der Slices zur Hauptachse.</span><span class="sxs-lookup"><span data-stu-id="77df9-116">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="77df9-117">*Stapel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77df9-117">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77df9-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77df9-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77df9-119">Anzahl der Stapel entlang der Hauptachse.</span><span class="sxs-lookup"><span data-stu-id="77df9-119">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="77df9-120">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="77df9-120">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77df9-121">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="77df9-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="77df9-122">Adresse eines Zeigers auf die Ausgabe Form, eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="77df9-122">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="77df9-123">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="77df9-123">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77df9-124">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="77df9-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="77df9-125">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="77df9-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="77df9-126">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="77df9-126">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="77df9-127">**Null** kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="77df9-127">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77df9-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77df9-128">Return value</span></span>

<span data-ttu-id="77df9-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77df9-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77df9-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77df9-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="77df9-131">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="77df9-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="77df9-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77df9-132">Remarks</span></span>

<span data-ttu-id="77df9-133">Die erstellte Kugel wird am Ursprung zentriert, und die zugehörige Achse wird an der z-Achse ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="77df9-133">The created sphere is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="77df9-134">Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="77df9-134">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="77df9-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77df9-135">Requirements</span></span>



| <span data-ttu-id="77df9-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77df9-136">Requirement</span></span> | <span data-ttu-id="77df9-137">Wert</span><span class="sxs-lookup"><span data-stu-id="77df9-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77df9-138">Header</span><span class="sxs-lookup"><span data-stu-id="77df9-138">Header</span></span><br/>  | <dl> <span data-ttu-id="77df9-139"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="77df9-139"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="77df9-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="77df9-140">Library</span></span><br/> | <dl> <span data-ttu-id="77df9-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77df9-141"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="77df9-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77df9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77df9-143">Formen Zeichnungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="77df9-143">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
