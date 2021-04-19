---
description: Skaliert alle einem angegebenen submesh zugeordneten Beispiele. Die-Methode ist nützlich für das Berechnen der unter Surface-Struktur.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'ID3DXPRTEngine:: scalemeschchunk-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367480"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a><span data-ttu-id="53b92-104">ID3DXPRTEngine:: scalemeschchunk-Methode</span><span class="sxs-lookup"><span data-stu-id="53b92-104">ID3DXPRTEngine::ScaleMeshChunk method</span></span>

<span data-ttu-id="53b92-105">Skaliert alle einem angegebenen submesh zugeordneten Beispiele.</span><span class="sxs-lookup"><span data-stu-id="53b92-105">Scales all the samples associated with a given submesh.</span></span> <span data-ttu-id="53b92-106">Die-Methode ist nützlich für das Berechnen der unter Surface-Struktur.</span><span class="sxs-lookup"><span data-stu-id="53b92-106">The method is useful for computing subsurface scattering.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b92-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53b92-107">Syntax</span></span>


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="53b92-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53b92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53b92-109">*Umschlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53b92-109">*uMeshChunk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b92-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53b92-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53b92-111">Speicherort im Mesh, an dem mit dem Skalieren von Beispielen begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="53b92-111">Location in the mesh at which to start scaling samples.</span></span>

</dd> <dt>

<span data-ttu-id="53b92-112">*f-Skala* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53b92-112">*fScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b92-113">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53b92-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53b92-114">Der Wert, um den die einzelnen Vektor im submesh multipliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="53b92-114">Value by which to multiply each vector in the submesh.</span></span>

</dd> <dt>

<span data-ttu-id="53b92-115">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53b92-115">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53b92-116">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="53b92-116">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="53b92-117">Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, um die im submesh übernommenen Beispiele zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="53b92-117">Pointer to a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object to receive rescaled samples in the submesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53b92-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53b92-118">Return value</span></span>

<span data-ttu-id="53b92-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53b92-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53b92-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="53b92-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="53b92-121">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="53b92-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="53b92-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53b92-122">Requirements</span></span>



| <span data-ttu-id="53b92-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53b92-123">Requirement</span></span> | <span data-ttu-id="53b92-124">Wert</span><span class="sxs-lookup"><span data-stu-id="53b92-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53b92-125">Header</span><span class="sxs-lookup"><span data-stu-id="53b92-125">Header</span></span><br/>  | <dl> <span data-ttu-id="53b92-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="53b92-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="53b92-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53b92-127">Library</span></span><br/> | <dl> <span data-ttu-id="53b92-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53b92-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53b92-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53b92-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b92-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="53b92-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
