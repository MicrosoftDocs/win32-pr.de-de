---
description: 'ID3DXBaseMesh::GetVertexBuffer-Methode: Ruft den Scheitelpunktpuffer ab, der dem Gitternetz zugeordnet ist.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: ID3DXBaseMesh::GetVertexBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9533188e3e2effe1759b58f70c9f033cc491844c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115368"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a><span data-ttu-id="81147-103">ID3DXBaseMesh::GetVertexBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="81147-103">ID3DXBaseMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="81147-104">Ruft den Scheitelpunktpuffer ab, der dem Gitternetz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="81147-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="81147-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81147-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="81147-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81147-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81147-107">*ppVB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="81147-107">*ppVB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="81147-108">Typ: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="81147-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="81147-109">Adresse eines Zeigers auf eine [**IDirect3DVertexBuffer9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) die das dem Gittermodell zugeordnete Scheitelpunktpufferobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="81147-109">Address of a pointer to an [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface, representing the vertex buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81147-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81147-110">Return value</span></span>

<span data-ttu-id="81147-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81147-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81147-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81147-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="81147-113">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="81147-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="81147-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81147-114">Requirements</span></span>



| <span data-ttu-id="81147-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81147-115">Requirement</span></span> | <span data-ttu-id="81147-116">Wert</span><span class="sxs-lookup"><span data-stu-id="81147-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81147-117">Header</span><span class="sxs-lookup"><span data-stu-id="81147-117">Header</span></span><br/>  | <dl> <span data-ttu-id="81147-118"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="81147-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="81147-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81147-119">Library</span></span><br/> | <dl> <span data-ttu-id="81147-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="81147-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="81147-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="81147-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81147-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="81147-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
