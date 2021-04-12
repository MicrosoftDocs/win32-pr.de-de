---
description: Klont ein Skin Info-Objekt.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'ID3DXSkinInfo:: Clone-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edd9776b75d027a32b32b58c59fc82daaebfa3ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219483"
---
# <a name="id3dxskininfoclone-method"></a><span data-ttu-id="550e7-103">ID3DXSkinInfo:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="550e7-103">ID3DXSkinInfo::Clone method</span></span>

<span data-ttu-id="550e7-104">Klont ein Skin Info-Objekt.</span><span class="sxs-lookup"><span data-stu-id="550e7-104">Clones a skin info object.</span></span>

## <a name="syntax"></a><span data-ttu-id="550e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="550e7-105">Syntax</span></span>


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="550e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="550e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="550e7-107">*ppskininfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="550e7-107">*ppSkinInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="550e7-108">Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="550e7-108">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="550e7-109">Adresse eines Zeigers auf ein [**ID3DXSkinInfo**](id3dxskininfo.md) -Objekt, das das geklonte Objekt enthält, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="550e7-109">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) object, which will contain the cloned object if the method is successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="550e7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="550e7-110">Return value</span></span>

<span data-ttu-id="550e7-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="550e7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="550e7-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="550e7-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="550e7-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="550e7-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="550e7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="550e7-114">Requirements</span></span>



| <span data-ttu-id="550e7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="550e7-115">Requirement</span></span> | <span data-ttu-id="550e7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="550e7-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="550e7-117">Header</span><span class="sxs-lookup"><span data-stu-id="550e7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="550e7-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="550e7-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="550e7-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="550e7-119">Library</span></span><br/> | <dl> <span data-ttu-id="550e7-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="550e7-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="550e7-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="550e7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550e7-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="550e7-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 




