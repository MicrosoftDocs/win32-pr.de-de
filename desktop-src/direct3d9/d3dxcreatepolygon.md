---
description: Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das ein n-seitiges Polygon enthält.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: D3DXCreatePolygon-Funktion (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a7e48f512d25ca53d1f3ff80889a013e2ecdcb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050858"
---
# <a name="d3dxcreatepolygon-function"></a><span data-ttu-id="3c278-103">D3DXCreatePolygon-Funktion</span><span class="sxs-lookup"><span data-stu-id="3c278-103">D3DXCreatePolygon function</span></span>

<span data-ttu-id="3c278-104">Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das ein n-seitiges Polygon enthält.</span><span class="sxs-lookup"><span data-stu-id="3c278-104">Uses a left-handed coordinate system to create a mesh containing an n-sided polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c278-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c278-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="3c278-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c278-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c278-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c278-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c278-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3c278-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3c278-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das dem erstellten Polygonnetz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3c278-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created polygon mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3c278-110">*Länge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c278-110">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c278-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c278-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c278-112">Länge jeder Seite.</span><span class="sxs-lookup"><span data-stu-id="3c278-112">Length of each side.</span></span>

</dd> <dt>

<span data-ttu-id="3c278-113">*Seiten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c278-113">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c278-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c278-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c278-115">Anzahl der Seiten für das Polygon.</span><span class="sxs-lookup"><span data-stu-id="3c278-115">Number of sides for the polygon.</span></span> <span data-ttu-id="3c278-116">Der Wert muss größer oder gleich 3 sein.</span><span class="sxs-lookup"><span data-stu-id="3c278-116">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="3c278-117">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c278-117">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c278-118">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c278-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="3c278-119">Adresse eines Zeigers auf die Ausgabe Form, eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3c278-119">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3c278-120">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c278-120">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c278-121">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c278-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3c278-122">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3c278-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="3c278-123">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="3c278-123">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="3c278-124">**Null** kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3c278-124">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c278-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c278-125">Return value</span></span>

<span data-ttu-id="3c278-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c278-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c278-127">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c278-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3c278-128">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="3c278-128">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c278-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c278-129">Remarks</span></span>

<span data-ttu-id="3c278-130">Das erstellte Polygon wird am Ursprung zentriert.</span><span class="sxs-lookup"><span data-stu-id="3c278-130">The created polygon is centered at the origin.</span></span>

<span data-ttu-id="3c278-131">Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="3c278-131">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c278-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c278-132">Requirements</span></span>



| <span data-ttu-id="3c278-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c278-133">Requirement</span></span> | <span data-ttu-id="3c278-134">Wert</span><span class="sxs-lookup"><span data-stu-id="3c278-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c278-135">Header</span><span class="sxs-lookup"><span data-stu-id="3c278-135">Header</span></span><br/>  | <dl> <span data-ttu-id="3c278-136"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c278-136"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="3c278-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c278-137">Library</span></span><br/> | <dl> <span data-ttu-id="3c278-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c278-138"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3c278-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c278-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c278-140">Formen Zeichnungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="3c278-140">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
