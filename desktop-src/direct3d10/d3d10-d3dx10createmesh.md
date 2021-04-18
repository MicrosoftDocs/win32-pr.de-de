---
description: Erstellt ein Mesh-Objekt mit einem Deklarator.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: D3DX10CreateMesh-Funktion (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354399"
---
# <a name="d3dx10createmesh-function"></a><span data-ttu-id="d0f59-103">D3DX10CreateMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="d0f59-103">D3DX10CreateMesh function</span></span>

<span data-ttu-id="d0f59-104">Erstellt ein Mesh-Objekt mit einem Deklarator.</span><span class="sxs-lookup"><span data-stu-id="d0f59-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f59-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0f59-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="d0f59-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0f59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f59-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f59-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f59-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="d0f59-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="d0f59-109">Zeiger auf eine [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), das Geräte Objekt, das dem Mesh zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0f59-109">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d0f59-110">*pdeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f59-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f59-111">Type: **Konstanten [**d3d10 \_ input- \_ Element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d0f59-111">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="d0f59-112">Array von [**d3d10 \_ input \_ Element \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) -Elementen, das das Vertex-Format für das zurückgegebene Mesh beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d0f59-112">Array of [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="d0f59-113">Dieser Parameter muss einem flexiblen Scheitelpunkt Format (FVF) direkt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d0f59-113">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="d0f59-114">*Declcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f59-114">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f59-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0f59-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0f59-116">Die Anzahl der Elemente in der pdeclaration.</span><span class="sxs-lookup"><span data-stu-id="d0f59-116">The number of elements in pDeclaration.</span></span>

</dd> <dt>

<span data-ttu-id="d0f59-117">*ppositionsemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f59-117">*pPositionSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f59-118">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0f59-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0f59-119">Semantik, die den Teil der Vertexdeklaration identifiziert, der Positionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="d0f59-119">Semantic that identifies which part of the vertex declaration contains position information.</span></span>

</dd> <dt>

<span data-ttu-id="d0f59-120">*VertexCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f59-120">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f59-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0f59-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0f59-122">Anzahl der Scheitel Punkte für das Mesh.</span><span class="sxs-lookup"><span data-stu-id="d0f59-122">Number of vertices for the mesh.</span></span> <span data-ttu-id="d0f59-123">Dieser Parameter muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="d0f59-123">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="d0f59-124">*FaceCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f59-124">*FaceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f59-125">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0f59-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0f59-126">Anzahl der Flächen für das Mesh.</span><span class="sxs-lookup"><span data-stu-id="d0f59-126">Number of faces for the mesh.</span></span> <span data-ttu-id="d0f59-127">Der gültige Bereich für diese Zahl ist größer als 0 und ein kleiner als der maximale DWORD-Wert (in der Regel 65534), da der letzte Index reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="d0f59-127">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d0f59-128">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0f59-128">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f59-129">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0f59-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0f59-130">Eine Kombination aus einem oder mehreren Flags aus dem [**d3dx10 \_ Mesh**](d3dx10-mesh.md), das Optionen für das Mesh angibt.</span><span class="sxs-lookup"><span data-stu-id="d0f59-130">Combination of one or more flags from the [**D3DX10\_MESH**](d3dx10-mesh.md), specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d0f59-131">*ppmesh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d0f59-131">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f59-132">Typ: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d0f59-132">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="d0f59-133">Adresse eines Zeigers auf eine [**ID3DX10Mesh-Schnittstelle**](id3dx10mesh.md), die das erstellte Mesh-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d0f59-133">Address of a pointer to an [**ID3DX10Mesh Interface**](id3dx10mesh.md), representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f59-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0f59-134">Return value</span></span>

<span data-ttu-id="d0f59-135">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0f59-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0f59-136">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d0f59-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d0f59-137">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="d0f59-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f59-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0f59-138">Requirements</span></span>



| <span data-ttu-id="d0f59-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0f59-139">Requirement</span></span> | <span data-ttu-id="d0f59-140">Wert</span><span class="sxs-lookup"><span data-stu-id="d0f59-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f59-141">Header</span><span class="sxs-lookup"><span data-stu-id="d0f59-141">Header</span></span><br/>  | <dl> <span data-ttu-id="d0f59-142"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0f59-142"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d0f59-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d0f59-143">Library</span></span><br/> | <dl> <span data-ttu-id="d0f59-144"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0f59-144"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0f59-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0f59-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f59-146">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d0f59-146">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d0f59-147">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d0f59-147">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
