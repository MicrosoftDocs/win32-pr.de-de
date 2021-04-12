---
description: Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das einen "Tor" enthält.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: D3DXCreateTorus-Funktion (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219520"
---
# <a name="d3dxcreatetorus-function"></a><span data-ttu-id="a0331-103">D3DXCreateTorus-Funktion</span><span class="sxs-lookup"><span data-stu-id="a0331-103">D3DXCreateTorus function</span></span>

<span data-ttu-id="a0331-104">Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das einen "Tor" enthält.</span><span class="sxs-lookup"><span data-stu-id="a0331-104">Uses a left-handed coordinate system to create a mesh containing a torus.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0331-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0331-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="a0331-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0331-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0331-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0331-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0331-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a0331-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a0331-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das dem erstellten Tor-Mesh zugeordnete Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0331-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created torus mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a0331-110">*Innerradius* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0331-110">*InnerRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0331-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0331-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0331-112">Innerer Radius des "Tor".</span><span class="sxs-lookup"><span data-stu-id="a0331-112">Inner-radius of the torus.</span></span> <span data-ttu-id="a0331-113">Der Wert muss größer oder gleich 0,0 f sein.</span><span class="sxs-lookup"><span data-stu-id="a0331-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="a0331-114">*Outerradius* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0331-114">*OuterRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0331-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0331-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0331-116">Äußerer Radius des "Tor".</span><span class="sxs-lookup"><span data-stu-id="a0331-116">Outer-radius of the torus.</span></span> <span data-ttu-id="a0331-117">Der Wert muss größer oder gleich 0,0 f sein.</span><span class="sxs-lookup"><span data-stu-id="a0331-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="a0331-118">*Seiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0331-118">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0331-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0331-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0331-120">Anzahl der Seiten in einem Querschnitt.</span><span class="sxs-lookup"><span data-stu-id="a0331-120">Number of sides in a cross-section.</span></span> <span data-ttu-id="a0331-121">Der Wert muss größer oder gleich 3 sein.</span><span class="sxs-lookup"><span data-stu-id="a0331-121">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="a0331-122">*Ringe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0331-122">*Rings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0331-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0331-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0331-124">Anzahl von Ringen, die den Tor bilden.</span><span class="sxs-lookup"><span data-stu-id="a0331-124">Number of rings making up the torus.</span></span> <span data-ttu-id="a0331-125">Der Wert muss größer oder gleich 3 sein.</span><span class="sxs-lookup"><span data-stu-id="a0331-125">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="a0331-126">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a0331-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0331-127">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0331-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a0331-128">Adresse eines Zeigers auf die Ausgabe Form, eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a0331-128">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a0331-129">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a0331-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0331-130">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0331-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a0331-131">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a0331-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="a0331-132">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="a0331-132">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="a0331-133">**Null** kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0331-133">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0331-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0331-134">Return value</span></span>

<span data-ttu-id="a0331-135">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0331-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0331-136">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0331-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a0331-137">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="a0331-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0331-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0331-138">Remarks</span></span>

<span data-ttu-id="a0331-139">Der erstellte ' Tor ' wird am Ursprung zentriert, und seine Achse ist an der z-Achse ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="a0331-139">The created torus is centered at the origin, and its axis is aligned with the z-axis.</span></span> <span data-ttu-id="a0331-140">Der innere Radius des "Tor" ist der Radius des Kreuz Abschnitts (der kleinere Radius), und der äußere Radius des "Tor" ist der Radius der zentralen Lücke.</span><span class="sxs-lookup"><span data-stu-id="a0331-140">The inner radius of the torus is the radius of the cross-section (the minor radius), and the outer radius of the torus is the radius of the central hole.</span></span>

<span data-ttu-id="a0331-141">Diese Funktion gibt ein Mesh zurück, das später zum Zeichnen oder manipulieren durch die Anwendung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0331-141">This function returns a mesh that can be used later for drawing or manipulation by the application.</span></span>

<span data-ttu-id="a0331-142">Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="a0331-142">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0331-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0331-143">Requirements</span></span>



| <span data-ttu-id="a0331-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0331-144">Requirement</span></span> | <span data-ttu-id="a0331-145">Wert</span><span class="sxs-lookup"><span data-stu-id="a0331-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0331-146">Header</span><span class="sxs-lookup"><span data-stu-id="a0331-146">Header</span></span><br/>  | <dl> <span data-ttu-id="a0331-147"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0331-147"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="a0331-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0331-148">Library</span></span><br/> | <dl> <span data-ttu-id="a0331-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0331-149"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a0331-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0331-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0331-151">Formen Zeichnungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="a0331-151">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
