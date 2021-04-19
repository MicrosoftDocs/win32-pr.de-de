---
description: Legt die Texturkoordinaten (u, v) der einzelnen textsets fest.
ms.assetid: b1f8f5d6-568f-4868-87c9-9d6b1034d898
title: 'ID3DXTextureGutterHelper:: settexelmap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee00394e81dadf147d54dffe0dc02199b2274e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357271"
---
# <a name="id3dxtexturegutterhelpersettexelmap-method"></a><span data-ttu-id="f21d8-103">ID3DXTextureGutterHelper:: settexelmap-Methode</span><span class="sxs-lookup"><span data-stu-id="f21d8-103">ID3DXTextureGutterHelper::SetTexelMap method</span></span>

<span data-ttu-id="f21d8-104">Legt die Texturkoordinaten (u, v) der einzelnen textsets fest.</span><span class="sxs-lookup"><span data-stu-id="f21d8-104">Sets the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f21d8-105">Syntax</span></span>


```C++
HRESULT SetTexelMap(
  [in] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="f21d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f21d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f21d8-107">*ptexeldata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f21d8-107">*pTexelData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21d8-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f21d8-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f21d8-109">Zeiger auf den Speicherort in Pixel-Texturkoordinaten (u, v), in dem sich die einzelnen textexorte befinden.</span><span class="sxs-lookup"><span data-stu-id="f21d8-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f21d8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f21d8-110">Return value</span></span>

<span data-ttu-id="f21d8-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f21d8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f21d8-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f21d8-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f21d8-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="f21d8-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="f21d8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f21d8-114">Requirements</span></span>



| <span data-ttu-id="f21d8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f21d8-115">Requirement</span></span> | <span data-ttu-id="f21d8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f21d8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f21d8-117">Header</span><span class="sxs-lookup"><span data-stu-id="f21d8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f21d8-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f21d8-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f21d8-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f21d8-119">Library</span></span><br/> | <dl> <span data-ttu-id="f21d8-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f21d8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f21d8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f21d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21d8-122">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="f21d8-122">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




