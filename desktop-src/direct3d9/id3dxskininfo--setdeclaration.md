---
description: Legt die Scheitelpunkt Deklaration fest.
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: 'ID3DXSkinInfo:: setdeclaration-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 821801647ca1aee3deabe69d911bd1cab5f7eb4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354047"
---
# <a name="id3dxskininfosetdeclaration-method"></a><span data-ttu-id="5f791-103">ID3DXSkinInfo:: setdeclaration-Methode</span><span class="sxs-lookup"><span data-stu-id="5f791-103">ID3DXSkinInfo::SetDeclaration method</span></span>

<span data-ttu-id="5f791-104">Legt die Scheitelpunkt Deklaration fest.</span><span class="sxs-lookup"><span data-stu-id="5f791-104">Sets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f791-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f791-105">Syntax</span></span>


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="5f791-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f791-107">*pdeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f791-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f791-108">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f791-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="5f791-109">Zeiger auf ein Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen.</span><span class="sxs-lookup"><span data-stu-id="5f791-109">Pointer to an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f791-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f791-110">Return value</span></span>

<span data-ttu-id="5f791-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5f791-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5f791-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5f791-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5f791-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="5f791-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f791-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f791-114">Requirements</span></span>



| <span data-ttu-id="5f791-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f791-115">Requirement</span></span> | <span data-ttu-id="5f791-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5f791-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f791-117">Header</span><span class="sxs-lookup"><span data-stu-id="5f791-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5f791-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f791-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5f791-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f791-119">Library</span></span><br/> | <dl> <span data-ttu-id="5f791-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f791-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f791-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f791-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f791-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="5f791-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="5f791-123">**ID3DXSkinInfo:: getDeclaration**</span><span class="sxs-lookup"><span data-stu-id="5f791-123">**ID3DXSkinInfo::GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




