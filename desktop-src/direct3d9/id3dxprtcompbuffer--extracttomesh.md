---
description: Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer und fügt die Daten einem ID3DXMesh-Objekt hinzu.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'ID3DXPRTCompBuffer:: extracttomesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370409"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a><span data-ttu-id="aefc1-103">ID3DXPRTCompBuffer:: extracttomesh-Methode</span><span class="sxs-lookup"><span data-stu-id="aefc1-103">ID3DXPRTCompBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="aefc1-104">Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Datenpuffer und fügt die Daten einem [**ID3DXMesh**](id3dxmesh.md) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="aefc1-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aefc1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aefc1-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="aefc1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aefc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aefc1-107">*Numpca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aefc1-107">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aefc1-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aefc1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aefc1-109">Anzahl der PCA-Koeffizienten, die aus dem Puffer extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aefc1-109">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="aefc1-110">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aefc1-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aefc1-111">Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="aefc1-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="aefc1-112">Vertex-Verwendungs Beschreibungen des Netzes.</span><span class="sxs-lookup"><span data-stu-id="aefc1-112">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="aefc1-113">Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="aefc1-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="aefc1-114">" *Startwert* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="aefc1-114">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aefc1-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aefc1-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aefc1-116">Der Start Index für die PCA-Koeffizienten, die im Mesh gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aefc1-116">Starting index for PCA coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="aefc1-117">*pscene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aefc1-117">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aefc1-118">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="aefc1-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="aefc1-119">Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt, in dem die PCA-Koeffizienten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="aefc1-119">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aefc1-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aefc1-120">Return value</span></span>

<span data-ttu-id="aefc1-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aefc1-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aefc1-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aefc1-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="aefc1-123">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="aefc1-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="aefc1-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aefc1-124">Requirements</span></span>



| <span data-ttu-id="aefc1-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aefc1-125">Requirement</span></span> | <span data-ttu-id="aefc1-126">Wert</span><span class="sxs-lookup"><span data-stu-id="aefc1-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aefc1-127">Header</span><span class="sxs-lookup"><span data-stu-id="aefc1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="aefc1-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="aefc1-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="aefc1-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aefc1-129">Library</span></span><br/> | <dl> <span data-ttu-id="aefc1-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aefc1-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aefc1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aefc1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aefc1-132">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="aefc1-132">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
