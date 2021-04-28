---
description: 'D3DX10CreateMesh-Funktion: Erstellt ein Gittermodellobjekt mithilfe eines Deklarators.'
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: D3DX10CreateMesh-Funktion (D3DX10Mesh.h)
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
ms.openlocfilehash: cc744536336a4a102bafeaeae3ba87bbad58eb97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113358"
---
# <a name="d3dx10createmesh-function"></a><span data-ttu-id="beda8-103">D3DX10CreateMesh-Funktion</span><span class="sxs-lookup"><span data-stu-id="beda8-103">D3DX10CreateMesh function</span></span>

<span data-ttu-id="beda8-104">Erstellt ein Gittermodellobjekt mithilfe eines Deklarators.</span><span class="sxs-lookup"><span data-stu-id="beda8-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="beda8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="beda8-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="beda8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="beda8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beda8-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="beda8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beda8-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="beda8-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="beda8-109">Zeiger auf eine [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), das Geräteobjekt, das dem Netz zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="beda8-109">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="beda8-110">*pDeclaration* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="beda8-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beda8-111">Typ: **const [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="beda8-111">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="beda8-112">Array von [**D3D10 \_ INPUT ELEMENT \_ \_ DESC-Elementen,**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) das das Scheitelpunktformat für das zurückgegebene Netz beschreibt.</span><span class="sxs-lookup"><span data-stu-id="beda8-112">Array of [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="beda8-113">Dieser Parameter muss direkt einem flexiblen Scheitelpunktformat (FVF) zuordnen.</span><span class="sxs-lookup"><span data-stu-id="beda8-113">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="beda8-114">*DeclCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="beda8-114">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beda8-115">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="beda8-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="beda8-116">Die Anzahl der Elemente in pDeclaration.</span><span class="sxs-lookup"><span data-stu-id="beda8-116">The number of elements in pDeclaration.</span></span>

</dd> <dt>

<span data-ttu-id="beda8-117">*pPositionSemantic* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="beda8-117">*pPositionSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beda8-118">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="beda8-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="beda8-119">Semantik, die identifiziert, welcher Teil der Scheitelpunktdeklaration Positionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="beda8-119">Semantic that identifies which part of the vertex declaration contains position information.</span></span>

</dd> <dt>

<span data-ttu-id="beda8-120">*VertexCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="beda8-120">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beda8-121">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="beda8-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="beda8-122">Anzahl der Scheitelzeichen für das Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="beda8-122">Number of vertices for the mesh.</span></span> <span data-ttu-id="beda8-123">Dieser Parameter muss größer als 0 sein.</span><span class="sxs-lookup"><span data-stu-id="beda8-123">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="beda8-124">*FaceCount* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="beda8-124">*FaceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beda8-125">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="beda8-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="beda8-126">Anzahl der Gesichter für das Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="beda8-126">Number of faces for the mesh.</span></span> <span data-ttu-id="beda8-127">Der gültige Bereich für diese Zahl ist größer als 0 und einer kleiner als der maximale DWORD-Wert (in der Regel 65534), da der letzte Index reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="beda8-127">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="beda8-128">*Optionen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="beda8-128">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beda8-129">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="beda8-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="beda8-130">Kombination aus einem oder mehreren Flags aus dem [**D3DX10 \_ MESH,**](d3dx10-mesh.md)die Optionen für das Gitternetz angeben.</span><span class="sxs-lookup"><span data-stu-id="beda8-130">Combination of one or more flags from the [**D3DX10\_MESH**](d3dx10-mesh.md), specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="beda8-131">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="beda8-131">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beda8-132">Typ: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="beda8-132">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="beda8-133">Adresse eines Zeigers auf eine [**ID3DX10Mesh-Schnittstelle,**](id3dx10mesh.md)die das erstellte Gittermodellobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="beda8-133">Address of a pointer to an [**ID3DX10Mesh Interface**](id3dx10mesh.md), representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beda8-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="beda8-134">Return value</span></span>

<span data-ttu-id="beda8-135">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="beda8-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="beda8-136">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="beda8-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="beda8-137">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="beda8-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="beda8-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="beda8-138">Requirements</span></span>



| <span data-ttu-id="beda8-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="beda8-139">Requirement</span></span> | <span data-ttu-id="beda8-140">Wert</span><span class="sxs-lookup"><span data-stu-id="beda8-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beda8-141">Header</span><span class="sxs-lookup"><span data-stu-id="beda8-141">Header</span></span><br/>  | <dl> <span data-ttu-id="beda8-142"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="beda8-142"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="beda8-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="beda8-143">Library</span></span><br/> | <dl> <span data-ttu-id="beda8-144"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="beda8-144"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="beda8-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="beda8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beda8-146">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="beda8-146">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="beda8-147">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="beda8-147">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
