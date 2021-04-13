---
description: Ruft die Texturkoordinaten (u, v) der einzelnen texaus.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'ID3DXTextureGutterHelper:: gettexelmap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354997"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a><span data-ttu-id="f8c2a-103">ID3DXTextureGutterHelper:: gettexelmap-Methode</span><span class="sxs-lookup"><span data-stu-id="f8c2a-103">ID3DXTextureGutterHelper::GetTexelMap method</span></span>

<span data-ttu-id="f8c2a-104">Ruft die Texturkoordinaten (u, v) der einzelnen texaus.</span><span class="sxs-lookup"><span data-stu-id="f8c2a-104">Retrieves the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c2a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8c2a-105">Syntax</span></span>


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="f8c2a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8c2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c2a-107">*ptexeldata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f8c2a-107">*pTexelData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c2a-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8c2a-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f8c2a-109">Zeiger auf den Speicherort in Pixel-Texturkoordinaten (u, v), in dem sich die einzelnen textexorte befinden.</span><span class="sxs-lookup"><span data-stu-id="f8c2a-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c2a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8c2a-110">Return value</span></span>

<span data-ttu-id="f8c2a-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8c2a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8c2a-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8c2a-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f8c2a-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="f8c2a-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c2a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8c2a-114">Remarks</span></span>

<span data-ttu-id="f8c2a-115">Bei den [**texeln der Klasse 2 und 4**](id3dxtexturegutterhelper.md)entsprechen die zurückgegebenen Texturkoordinaten (u, v) dem nächstgelegenen Punkt am nächstgelegenen Dreieck.</span><span class="sxs-lookup"><span data-stu-id="f8c2a-115">For [**class 2 and 4 texels**](id3dxtexturegutterhelper.md), the returned (u, v) texture coordinates correspond to the closest point on the closest triangle.</span></span>

<span data-ttu-id="f8c2a-116">Die Anwendung muss ptexeldata zuordnen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="f8c2a-116">The application must allocate and manage pTexelData.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c2a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8c2a-117">Requirements</span></span>



| <span data-ttu-id="f8c2a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8c2a-118">Requirement</span></span> | <span data-ttu-id="f8c2a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f8c2a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c2a-120">Header</span><span class="sxs-lookup"><span data-stu-id="f8c2a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f8c2a-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8c2a-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f8c2a-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8c2a-122">Library</span></span><br/> | <dl> <span data-ttu-id="f8c2a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8c2a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8c2a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8c2a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c2a-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="f8c2a-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




