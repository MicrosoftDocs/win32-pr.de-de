---
description: Mit dieser Methode kann der Benutzer die Mesh-Deklaration ändern, ohne das Datenlayout des Vertexpuffers zu ändern. Der-Rückruf ist nur gültig, wenn die alten und neuen Deklarations Formate die gleiche Scheitelpunkt Größe aufweisen.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'ID3DXBaseMesh:: updatesemantics-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050869"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a><span data-ttu-id="73fe0-104">ID3DXBaseMesh:: updatesemantics-Methode</span><span class="sxs-lookup"><span data-stu-id="73fe0-104">ID3DXBaseMesh::UpdateSemantics method</span></span>

<span data-ttu-id="73fe0-105">Mit dieser Methode kann der Benutzer die Mesh-Deklaration ändern, ohne das Datenlayout des Vertexpuffers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="73fe0-105">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="73fe0-106">Der-Rückruf ist nur gültig, wenn die alten und neuen Deklarations Formate die gleiche Scheitelpunkt Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="73fe0-106">The call is valid only if the old and new declaration formats have the same vertex size.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fe0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73fe0-107">Syntax</span></span>


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="73fe0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="73fe0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fe0-109">*Deklaration* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="73fe0-109">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73fe0-110">Typ: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="73fe0-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="73fe0-111">Ein Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das das Scheitelpunkt Format der mesvertices beschreibt.</span><span class="sxs-lookup"><span data-stu-id="73fe0-111">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="73fe0-112">Die Obergrenze dieses deklaratorarrays ist [**Max \_ \_ \_**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="73fe0-112">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73fe0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73fe0-113">Return value</span></span>

<span data-ttu-id="73fe0-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73fe0-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73fe0-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73fe0-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="73fe0-116">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="73fe0-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="73fe0-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73fe0-117">Remarks</span></span>

<span data-ttu-id="73fe0-118">[**ID3DXBaseMesh:: clonemesh**](id3dxbasemesh--clonemesh.md) dient zum erneuten Formatieren und Ändern des Vertex-Daten Layouts.</span><span class="sxs-lookup"><span data-stu-id="73fe0-118">[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="73fe0-119">Verwenden Sie es z. b. zum Hinzufügen von Platz für normale, Texturkoordinaten, Farben, Gewichtungen usw., die zuvor nicht vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="73fe0-119">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="73fe0-120">**ID3DXBaseMesh:: updatesemantics** ist eine Methode zum Aktualisieren der Scheitelpunkt Deklaration mit unterschiedlichen Semantik Informationen, ohne das Layout des Vertexpuffers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="73fe0-120">**ID3DXBaseMesh::UpdateSemantics** is a method for updating the vertex declaration with different semantic information, without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="73fe0-121">Verwenden Sie diese z. b., um eine 3D-Textur Koordinate als Binormal oder Tangens neu zu bezeichnen (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="73fe0-121">For example, use it to relabel a 3D texture coordinate as a binormal or tangent, or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="73fe0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73fe0-122">Requirements</span></span>



| <span data-ttu-id="73fe0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73fe0-123">Requirement</span></span> | <span data-ttu-id="73fe0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="73fe0-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73fe0-125">Header</span><span class="sxs-lookup"><span data-stu-id="73fe0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="73fe0-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="73fe0-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="73fe0-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73fe0-127">Library</span></span><br/> | <dl> <span data-ttu-id="73fe0-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73fe0-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73fe0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73fe0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fe0-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="73fe0-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="73fe0-131">**ID3DXBaseMesh:: clonemeshf VF**</span><span class="sxs-lookup"><span data-stu-id="73fe0-131">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="73fe0-132">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="73fe0-132">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
