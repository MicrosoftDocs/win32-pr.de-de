---
description: Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das eine "Teapot" enthält.
ms.assetid: c002d6d4-1829-4293-9a86-d8560d6ec0e9
title: D3DXCreateTeapot-Funktion (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTeapot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 13f5ed44bdc31958729209f01183eba409298fcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219523"
---
# <a name="d3dxcreateteapot-function"></a><span data-ttu-id="a0a6d-103">D3DXCreateTeapot-Funktion</span><span class="sxs-lookup"><span data-stu-id="a0a6d-103">D3DXCreateTeapot function</span></span>

<span data-ttu-id="a0a6d-104">Verwendet ein Links händiges Koordinatensystem zum Erstellen eines Netzes, das eine "Teapot" enthält.</span><span class="sxs-lookup"><span data-stu-id="a0a6d-104">Uses a left-handed coordinate system to create a mesh containing a teapot.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0a6d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTeapot(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="a0a6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0a6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0a6d-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0a6d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a6d-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a0a6d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a0a6d-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das dem erstellten Teekanne-Mesh zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a0a6d-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created teapot mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a0a6d-110">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a0a6d-110">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a6d-111">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0a6d-111">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a0a6d-112">Adresse eines Zeigers auf die Ausgabe Form, eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a0a6d-112">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a0a6d-113">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a0a6d-113">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a6d-114">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0a6d-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a0a6d-115">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a0a6d-115">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="a0a6d-116">Wenn die-Methode zurückgibt, wird dieser Parameter mit einem Array von drei DWORDs pro Gesicht gefüllt, die die drei Nachbarn für jedes Gesicht im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="a0a6d-116">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="a0a6d-117">**Null** kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0a6d-117">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0a6d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0a6d-118">Return value</span></span>

<span data-ttu-id="a0a6d-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0a6d-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0a6d-120">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0a6d-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a0a6d-121">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="a0a6d-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a6d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0a6d-122">Remarks</span></span>

<span data-ttu-id="a0a6d-123">Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="a0a6d-123">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a6d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0a6d-124">Requirements</span></span>



| <span data-ttu-id="a0a6d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0a6d-125">Requirement</span></span> | <span data-ttu-id="a0a6d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a0a6d-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a6d-127">Header</span><span class="sxs-lookup"><span data-stu-id="a0a6d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a0a6d-128"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0a6d-128"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="a0a6d-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0a6d-129">Library</span></span><br/> | <dl> <span data-ttu-id="a0a6d-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0a6d-130"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a0a6d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0a6d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a6d-132">Formen Zeichnungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="a0a6d-132">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
