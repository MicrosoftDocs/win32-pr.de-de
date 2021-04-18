---
description: Zeichnet einen Zeilen Streifen im Bildschirmbereich mit einer angegebenen Eingabe Transformationsmatrix.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: ID3DXLine::D rawtransform-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354405"
---
# <a name="id3dxlinedrawtransform-method"></a><span data-ttu-id="4b092-103">ID3DXLine::D rawtransform-Methode</span><span class="sxs-lookup"><span data-stu-id="4b092-103">ID3DXLine::DrawTransform method</span></span>

<span data-ttu-id="4b092-104">Zeichnet einen Zeilen Streifen im Bildschirmbereich mit einer angegebenen Eingabe Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="4b092-104">Draws a line strip in screen space with a specified input transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b092-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b092-105">Syntax</span></span>


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="4b092-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b092-107">*pvertexlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b092-107">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b092-108">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b092-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4b092-109">Ein Array von Scheitel Punkten, die die Linie bilden.</span><span class="sxs-lookup"><span data-stu-id="4b092-109">Array of vertices that make up the line.</span></span> <span data-ttu-id="4b092-110">Siehe [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="4b092-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b092-111">*dwvertexlistcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b092-111">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b092-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b092-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b092-113">Anzahl der Scheitel Punkte in der Scheitelpunkt Liste.</span><span class="sxs-lookup"><span data-stu-id="4b092-113">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="4b092-114">*ptransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b092-114">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b092-115">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4b092-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4b092-116">Eine Formel für Skalierung, Drehung und Übersetzung (SRT) zum Transformieren der Punkte.</span><span class="sxs-lookup"><span data-stu-id="4b092-116">A scale, rotate, and translate (SRT) matrix for transforming the points.</span></span> <span data-ttu-id="4b092-117">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="4b092-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span> <span data-ttu-id="4b092-118">Wenn diese Matrix eine Projektions Matrix ist, werden alle gezeichneten Zeilen mit einem perspektivischen stippling-Muster gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4b092-118">If this matrix is a projection matrix, any stippled lines will be drawn with a perspective-correct stippling pattern.</span></span> <span data-ttu-id="4b092-119">Oder Sie können die Scheitel Punkte transformieren und [**ID3DXLine::D RAW**](id3dxline--draw.md) verwenden, um die Linie mit einem nicht Perspektiven-korrekten Stippel Muster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4b092-119">Or, you can transform the vertices and use [**ID3DXLine::Draw**](id3dxline--draw.md) to draw the line with a nonperspective-correct stipple pattern.</span></span>

</dd> <dt>

<span data-ttu-id="4b092-120">*Farbe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b092-120">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b092-121">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="4b092-121">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="4b092-122">Die Farbe der Linie.</span><span class="sxs-lookup"><span data-stu-id="4b092-122">Color of the line.</span></span> <span data-ttu-id="4b092-123">Siehe [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="4b092-123">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b092-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b092-124">Return value</span></span>

<span data-ttu-id="4b092-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b092-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b092-126">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4b092-126">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4b092-127">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="4b092-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b092-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b092-128">Requirements</span></span>



| <span data-ttu-id="4b092-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b092-129">Requirement</span></span> | <span data-ttu-id="4b092-130">Wert</span><span class="sxs-lookup"><span data-stu-id="4b092-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b092-131">Header</span><span class="sxs-lookup"><span data-stu-id="4b092-131">Header</span></span><br/>  | <dl> <span data-ttu-id="4b092-132"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b092-132"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="4b092-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b092-133">Library</span></span><br/> | <dl> <span data-ttu-id="4b092-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b092-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4b092-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b092-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b092-136">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="4b092-136">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
