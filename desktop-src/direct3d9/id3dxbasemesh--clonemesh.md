---
description: Klont ein Mesh mit einem Deklarator.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: 'ID3DXBaseMesh:: clonemesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 421b72a080564886a10c187594223fb58a0b69fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355004"
---
# <a name="id3dxbasemeshclonemesh-method"></a><span data-ttu-id="5eb85-103">ID3DXBaseMesh:: clonemesh-Methode</span><span class="sxs-lookup"><span data-stu-id="5eb85-103">ID3DXBaseMesh::CloneMesh method</span></span>

<span data-ttu-id="5eb85-104">Klont ein Mesh mit einem Deklarator.</span><span class="sxs-lookup"><span data-stu-id="5eb85-104">Clones a mesh using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb85-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5eb85-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="5eb85-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5eb85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb85-107">*Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5eb85-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb85-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5eb85-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5eb85-109">Eine Kombination aus einem oder mehreren [**D3DXMESH**](./d3dxmesh.md) -Flags, die Erstellungs Optionen für das Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="5eb85-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5eb85-110">*pdeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5eb85-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb85-111">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="5eb85-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="5eb85-112">Ein Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, die das Scheitelpunkt Format für die Scheitel Punkte im Ausgabe Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="5eb85-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, which specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5eb85-113">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5eb85-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb85-114">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5eb85-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5eb85-115">Ein Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das dem Mesh zugeordnete Geräte Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5eb85-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5eb85-116">*ppclonemesh* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5eb85-116">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb85-117">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="5eb85-117">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="5eb85-118">Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das geklonte Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="5eb85-118">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eb85-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5eb85-119">Return value</span></span>

<span data-ttu-id="5eb85-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5eb85-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5eb85-121">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5eb85-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5eb85-122">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="5eb85-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eb85-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5eb85-123">Remarks</span></span>

<span data-ttu-id="5eb85-124">**ID3DXBaseMesh:: clonemesh** dient zum erneuten Formatieren und Ändern des Vertex-Daten Layouts.</span><span class="sxs-lookup"><span data-stu-id="5eb85-124">**ID3DXBaseMesh::CloneMesh** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="5eb85-125">Dies erfolgt durch Erstellen eines neuen Mesh-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5eb85-125">This is done by creating a new mesh object.</span></span> <span data-ttu-id="5eb85-126">Verwenden Sie diese z. b. zum Hinzufügen von Platz für normale, Texturkoordinaten, Farben, Gewichtungen usw., die zuvor nicht vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="5eb85-126">For example, use it to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="5eb85-127">[**ID3DXBaseMesh:: updatesemantics**](id3dxbasemesh--updatesemantics.md) aktualisiert die Vertex-Deklaration mit anderen Semantik Informationen, ohne das Layout des Vertexpuffers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5eb85-127">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="5eb85-128">Mit dieser Methode wird der Inhalt des Vertex-Puffers nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="5eb85-128">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="5eb85-129">Verwenden Sie diese z. b., um eine 3D-Textur Koordinate als Binormal oder Tangens neu zu bezeichnen, oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="5eb85-129">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eb85-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5eb85-130">Requirements</span></span>



| <span data-ttu-id="5eb85-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5eb85-131">Requirement</span></span> | <span data-ttu-id="5eb85-132">Wert</span><span class="sxs-lookup"><span data-stu-id="5eb85-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb85-133">Header</span><span class="sxs-lookup"><span data-stu-id="5eb85-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5eb85-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb85-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5eb85-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5eb85-135">Library</span></span><br/> | <dl> <span data-ttu-id="5eb85-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5eb85-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5eb85-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eb85-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb85-138">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="5eb85-138">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="5eb85-139">**ID3DXBaseMesh:: clonemeshf VF**</span><span class="sxs-lookup"><span data-stu-id="5eb85-139">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="5eb85-140">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="5eb85-140">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
