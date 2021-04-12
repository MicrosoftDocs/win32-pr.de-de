---
description: Legt texzentrische texse-Koordinaten fest.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'ID3DXTextureGutterHelper:: setbarymap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219658"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a><span data-ttu-id="f0212-103">ID3DXTextureGutterHelper:: setbarymap-Methode</span><span class="sxs-lookup"><span data-stu-id="f0212-103">ID3DXTextureGutterHelper::SetBaryMap method</span></span>

<span data-ttu-id="f0212-104">Legt texzentrische texse-Koordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="f0212-104">Sets texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0212-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0212-105">Syntax</span></span>


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="f0212-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0212-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0212-107">*pbarydata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0212-107">*pBaryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0212-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0212-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f0212-109">Ein Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die ersten beiden über die beiden texzentrischen Koordinaten jeder texenstruktur enthält.</span><span class="sxs-lookup"><span data-stu-id="f0212-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0212-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0212-110">Return value</span></span>

<span data-ttu-id="f0212-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0212-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0212-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f0212-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f0212-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="f0212-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="f0212-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0212-114">Remarks</span></span>

<span data-ttu-id="f0212-115">Die dritte barzentrierte Koordinate wird durch Folgendes angegeben:</span><span class="sxs-lookup"><span data-stu-id="f0212-115">The third barycentric coordinate is given by:</span></span>


```
1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="f0212-116">Die Eingabe von Text zentrierten Koordinaten für diese Methode ist nur gültig für gültige Texels (Non-Class 0).</span><span class="sxs-lookup"><span data-stu-id="f0212-116">The barycentric coordinates input to this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="f0212-117">[**ID3DXTextureGutterHelper:: getguttermap**](id3dxtexturegutterhelper--getguttermap.md) gibt Werte ungleich 0 (null) für gültige Texels zurück.</span><span class="sxs-lookup"><span data-stu-id="f0212-117">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

<span data-ttu-id="f0212-118">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="f0212-118">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="f0212-119">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="f0212-119">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0212-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0212-120">Requirements</span></span>



| <span data-ttu-id="f0212-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0212-121">Requirement</span></span> | <span data-ttu-id="f0212-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f0212-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0212-123">Header</span><span class="sxs-lookup"><span data-stu-id="f0212-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f0212-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0212-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f0212-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0212-125">Library</span></span><br/> | <dl> <span data-ttu-id="f0212-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0212-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0212-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0212-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0212-128">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="f0212-128">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




