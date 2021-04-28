---
description: 'ID3DXBaseMesh::GetIndexBuffer-Methode: Ruft die Daten in einem Indexpuffer ab.'
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: ID3DXBaseMesh::GetIndexBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40e57193a2bf9a47ed0c57e6d13644441fbc42ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115428"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="b2d6b-103">ID3DXBaseMesh::GetIndexBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="b2d6b-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="b2d6b-104">Ruft die Daten in einem Indexpuffer ab.</span><span class="sxs-lookup"><span data-stu-id="b2d6b-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2d6b-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="b2d6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d6b-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b2d6b-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d6b-108">Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="b2d6b-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="b2d6b-109">Adresse eines Zeigers auf eine [**IDirect3DIndexBuffer9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) die das Indexpufferobjekt darstellt, das dem Gittermodell zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b2d6b-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d6b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2d6b-110">Return value</span></span>

<span data-ttu-id="b2d6b-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2d6b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2d6b-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b2d6b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2d6b-113">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="b2d6b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2d6b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2d6b-114">Requirements</span></span>



| <span data-ttu-id="b2d6b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2d6b-115">Requirement</span></span> | <span data-ttu-id="b2d6b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b2d6b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d6b-117">Header</span><span class="sxs-lookup"><span data-stu-id="b2d6b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b2d6b-118"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="b2d6b-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b2d6b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2d6b-119">Library</span></span><br/> | <dl> <span data-ttu-id="b2d6b-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2d6b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2d6b-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b2d6b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d6b-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="b2d6b-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
