---
description: Ruft die Daten in einem Index Puffer ab.
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: 'ID3DXBaseMesh:: getindexbuffer-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 5b7cf57cd8f31e54cf48ae7f0cab69a40783debe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355157"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="fa7a9-103">ID3DXBaseMesh:: getindexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="fa7a9-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="fa7a9-104">Ruft die Daten in einem Index Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="fa7a9-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa7a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa7a9-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="fa7a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa7a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa7a9-107">*ppib* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fa7a9-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fa7a9-108">Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="fa7a9-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="fa7a9-109">Adresse eines Zeigers auf eine [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) -Schnittstelle, die das dem Mesh zugeordnete Index Puffer Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fa7a9-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa7a9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa7a9-110">Return value</span></span>

<span data-ttu-id="fa7a9-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa7a9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa7a9-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fa7a9-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fa7a9-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="fa7a9-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa7a9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa7a9-114">Requirements</span></span>



| <span data-ttu-id="fa7a9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa7a9-115">Requirement</span></span> | <span data-ttu-id="fa7a9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fa7a9-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7a9-117">Header</span><span class="sxs-lookup"><span data-stu-id="fa7a9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fa7a9-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa7a9-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fa7a9-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa7a9-119">Library</span></span><br/> | <dl> <span data-ttu-id="fa7a9-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa7a9-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa7a9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa7a9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa7a9-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="fa7a9-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
