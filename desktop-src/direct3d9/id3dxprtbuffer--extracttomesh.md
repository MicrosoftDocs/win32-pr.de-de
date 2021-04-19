---
description: Extrahiert Koeffizienten-Daten aus einem Puffer mit einem einzelnen Kanal und fügt die Daten einem ID3DXMesh-Objekt hinzu.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'ID3DXPRTBuffer:: extracttomesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367501"
---
# <a name="id3dxprtbufferextracttomesh-method"></a><span data-ttu-id="dbc03-103">ID3DXPRTBuffer:: extracttomesh-Methode</span><span class="sxs-lookup"><span data-stu-id="dbc03-103">ID3DXPRTBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="dbc03-104">Extrahiert Koeffizienten-Daten aus einem Puffer mit einem einzelnen Kanal und fügt die Daten einem [**ID3DXMesh**](id3dxmesh.md) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="dbc03-104">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbc03-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="dbc03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbc03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc03-107">*Numkoefficients* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbc03-107">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc03-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbc03-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbc03-109">Anzahl der Koeffizienten, die aus dem Puffer extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dbc03-109">Number of coefficients to extract from the buffer.</span></span> <span data-ttu-id="dbc03-110">Bei Verwendung von "sphärischen harmonisch (SH) preberechneten Radiance Transfer (PRT)" sollte die Anzahl der Koeffizienten "Order ²" lauten.</span><span class="sxs-lookup"><span data-stu-id="dbc03-110">When using spherical harmonic (SH) precomputed radiance transfer (PRT), the number of coefficients should be Order ².</span></span> <span data-ttu-id="dbc03-111">Die Reihenfolge muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="dbc03-111">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="dbc03-112">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbc03-112">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc03-113">Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="dbc03-113">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="dbc03-114">Vertex-Verwendungs Beschreibungen des Netzes.</span><span class="sxs-lookup"><span data-stu-id="dbc03-114">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="dbc03-115">Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="dbc03-115">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbc03-116">" *Startwert* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="dbc03-116">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc03-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbc03-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbc03-118">Der Start Index für Koeffizienten, die im Mesh gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dbc03-118">Starting index for coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="dbc03-119">*pscene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbc03-119">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbc03-120">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="dbc03-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="dbc03-121">Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt, in dem Koeffizienten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dbc03-121">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc03-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbc03-122">Return value</span></span>

<span data-ttu-id="dbc03-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dbc03-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dbc03-124">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dbc03-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dbc03-125">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="dbc03-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc03-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbc03-126">Requirements</span></span>



| <span data-ttu-id="dbc03-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbc03-127">Requirement</span></span> | <span data-ttu-id="dbc03-128">Wert</span><span class="sxs-lookup"><span data-stu-id="dbc03-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc03-129">Header</span><span class="sxs-lookup"><span data-stu-id="dbc03-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dbc03-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc03-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dbc03-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dbc03-131">Library</span></span><br/> | <dl> <span data-ttu-id="dbc03-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbc03-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dbc03-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbc03-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc03-134">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="dbc03-134">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
