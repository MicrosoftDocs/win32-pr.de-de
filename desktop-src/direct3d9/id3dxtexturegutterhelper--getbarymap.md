---
description: Ruft texzentrische texzentrische Koordinaten ab.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'ID3DXTextureGutterHelper:: getbarymap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355026"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a><span data-ttu-id="737aa-103">ID3DXTextureGutterHelper:: getbarymap-Methode</span><span class="sxs-lookup"><span data-stu-id="737aa-103">ID3DXTextureGutterHelper::GetBaryMap method</span></span>

<span data-ttu-id="737aa-104">Ruft texzentrische texzentrische Koordinaten ab.</span><span class="sxs-lookup"><span data-stu-id="737aa-104">Retrieves texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="737aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="737aa-105">Syntax</span></span>


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="737aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="737aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="737aa-107">*pbarydata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="737aa-107">*pBaryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="737aa-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="737aa-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="737aa-109">Ein Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die ersten beiden über die beiden texzentrischen Koordinaten jeder texenstruktur enthält.</span><span class="sxs-lookup"><span data-stu-id="737aa-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="737aa-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="737aa-110">Return value</span></span>

<span data-ttu-id="737aa-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="737aa-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="737aa-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="737aa-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="737aa-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="737aa-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="737aa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="737aa-114">Remarks</span></span>

<span data-ttu-id="737aa-115">Die dritte barzentrierte Koordinate wird durch Folgendes angegeben:</span><span class="sxs-lookup"><span data-stu-id="737aa-115">The third barycentric coordinate is given by:</span></span>


```
    1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="737aa-116">Barzentrierte Koordinaten werden immer in Bezug auf das von [**ID3DXTextureGutterHelper:: getfacemap**](id3dxtexturegutterhelper--getfacemap.md)zurückgegebene Dreieck angegeben.</span><span class="sxs-lookup"><span data-stu-id="737aa-116">Barycentric coordinates are always specified with respect to the triangle returned by [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span></span>

<span data-ttu-id="737aa-117">Die von dieser Methode zurückgegebenen von dieser Methode zurückgegebenen, von dieser Methode zurückgegebenen Koordinaten sind nur gültig für gültige Texels (nicht Class 0).</span><span class="sxs-lookup"><span data-stu-id="737aa-117">The barycentric coordinates returned by this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="737aa-118">[**ID3DXTextureGutterHelper:: getguttermap**](id3dxtexturegutterhelper--getguttermap.md) gibt Werte ungleich 0 (null) für gültige Texels zurück.</span><span class="sxs-lookup"><span data-stu-id="737aa-118">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid texels.</span></span>

<span data-ttu-id="737aa-119">[**Class 2 texeln**](id3dxtexturegutterhelper.md) werden dem nächstgelegenen Punkt auf dem Dreieck im textraum zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="737aa-119">[**Class 2 texels**](id3dxtexturegutterhelper.md) are mapped to the nearest point on the triangle in texel space.</span></span>

<span data-ttu-id="737aa-120">Die Anwendung muss pbarydata zuordnen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="737aa-120">The application must allocate and manage pBaryData.</span></span>

<span data-ttu-id="737aa-121">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="737aa-121">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="737aa-122">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="737aa-122">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="737aa-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="737aa-123">Requirements</span></span>



| <span data-ttu-id="737aa-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="737aa-124">Requirement</span></span> | <span data-ttu-id="737aa-125">Wert</span><span class="sxs-lookup"><span data-stu-id="737aa-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="737aa-126">Header</span><span class="sxs-lookup"><span data-stu-id="737aa-126">Header</span></span><br/>  | <dl> <span data-ttu-id="737aa-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="737aa-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="737aa-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="737aa-128">Library</span></span><br/> | <dl> <span data-ttu-id="737aa-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="737aa-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="737aa-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="737aa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737aa-131">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="737aa-131">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




