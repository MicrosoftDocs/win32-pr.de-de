---
description: Zeichnet einen Zeilen Streifen im Bildschirmbereich. Die Eingabe erfolgt in Form eines Arrays, das Punkte (of D3DXVECTOR2) im Zeilen Streifen definiert.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: ID3DXLine::D RAW-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364004"
---
# <a name="id3dxlinedraw-method"></a><span data-ttu-id="3492a-104">ID3DXLine::D RAW-Methode</span><span class="sxs-lookup"><span data-stu-id="3492a-104">ID3DXLine::Draw method</span></span>

<span data-ttu-id="3492a-105">Zeichnet einen Zeilen Streifen im Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="3492a-105">Draws a line strip in screen space.</span></span> <span data-ttu-id="3492a-106">Die Eingabe erfolgt in Form eines Arrays, das Punkte (of [**D3DXVECTOR2**](d3dxvector2.md)) im Zeilen Streifen definiert.</span><span class="sxs-lookup"><span data-stu-id="3492a-106">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="3492a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3492a-107">Syntax</span></span>


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="3492a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3492a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3492a-109">*pvertexlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3492a-109">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3492a-110">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3492a-110">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3492a-111">Ein Array von Scheitel Punkten, die die Linie bilden.</span><span class="sxs-lookup"><span data-stu-id="3492a-111">Array of vertices that make up the line.</span></span> <span data-ttu-id="3492a-112">Siehe [**D3DXVECTOR2**](d3dxvector2.md).</span><span class="sxs-lookup"><span data-stu-id="3492a-112">See [**D3DXVECTOR2**](d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="3492a-113">*dwvertexlistcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3492a-113">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3492a-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3492a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3492a-115">Anzahl der Scheitel Punkte in der Scheitelpunkt Liste.</span><span class="sxs-lookup"><span data-stu-id="3492a-115">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="3492a-116">*Farbe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3492a-116">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3492a-117">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="3492a-117">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="3492a-118">Die Farbe der Linie.</span><span class="sxs-lookup"><span data-stu-id="3492a-118">Color of the line.</span></span> <span data-ttu-id="3492a-119">Siehe [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="3492a-119">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3492a-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3492a-120">Return value</span></span>

<span data-ttu-id="3492a-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3492a-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3492a-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3492a-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3492a-123">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="3492a-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="3492a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3492a-124">Requirements</span></span>



| <span data-ttu-id="3492a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3492a-125">Requirement</span></span> | <span data-ttu-id="3492a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3492a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3492a-127">Header</span><span class="sxs-lookup"><span data-stu-id="3492a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3492a-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3492a-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3492a-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3492a-129">Library</span></span><br/> | <dl> <span data-ttu-id="3492a-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3492a-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3492a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3492a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3492a-132">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="3492a-132">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
