---
description: Initiieren Sie die Zeichnung der einzelnen Gesichter einer Umgebungs Zuordnung.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'ID3DXRenderToEnvMap:: Face-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762345"
---
# <a name="id3dxrendertoenvmapface-method"></a><span data-ttu-id="83e8e-103">ID3DXRenderToEnvMap:: Face-Methode</span><span class="sxs-lookup"><span data-stu-id="83e8e-103">ID3DXRenderToEnvMap::Face method</span></span>

<span data-ttu-id="83e8e-104">Initiieren Sie die Zeichnung der einzelnen Gesichter einer Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="83e8e-104">Initiate the drawing of each face of an environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e8e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83e8e-105">Syntax</span></span>


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="83e8e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83e8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83e8e-107">*Gesicht* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83e8e-107">*Face* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e8e-108">Typ: **[ **D3DCUBEMAP \_ Gesichter**](./d3dcubemap-faces.md)**</span><span class="sxs-lookup"><span data-stu-id="83e8e-108">Type: **[**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md)**</span></span>

<span data-ttu-id="83e8e-109">Das erste Gesicht der Umgebungs Cube-Karte.</span><span class="sxs-lookup"><span data-stu-id="83e8e-109">The first face of the environmental cube map.</span></span> <span data-ttu-id="83e8e-110">Siehe [**D3DCUBEMAP \_ Gesichter**](./d3dcubemap-faces.md).</span><span class="sxs-lookup"><span data-stu-id="83e8e-110">See [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e8e-111">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83e8e-111">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e8e-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83e8e-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83e8e-113">Eine gültige Kombination aus einem oder mehreren [D3DX- \_ Filterflags](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="83e8e-113">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83e8e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83e8e-114">Return value</span></span>

<span data-ttu-id="83e8e-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83e8e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83e8e-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83e8e-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83e8e-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="83e8e-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="83e8e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83e8e-118">Remarks</span></span>

<span data-ttu-id="83e8e-119">Diese Methode muss für jeden Typ von Umgebungs Zuordnung einmal aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="83e8e-119">This method must be called once for each type of environment map.</span></span> <span data-ttu-id="83e8e-120">Die einzige Ausnahme ist eine kubische Umgebungs Zuordnung, die erfordert, dass diese Methode sechs Mal aufgerufen wird, einmal für jedes Gesicht in D3DCUBEMAP \_ Gesichter.</span><span class="sxs-lookup"><span data-stu-id="83e8e-120">The only exception is a cubic environment map which requires this method to be called six times, once for each face in D3DCUBEMAP\_FACES.</span></span> <span data-ttu-id="83e8e-121">Weitere Informationen finden Sie unter [Umgebungs Zuordnung (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="83e8e-121">For more information, see [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83e8e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83e8e-122">Requirements</span></span>



| <span data-ttu-id="83e8e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83e8e-123">Requirement</span></span> | <span data-ttu-id="83e8e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="83e8e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83e8e-125">Header</span><span class="sxs-lookup"><span data-stu-id="83e8e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="83e8e-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="83e8e-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="83e8e-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="83e8e-127">Library</span></span><br/> | <dl> <span data-ttu-id="83e8e-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83e8e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83e8e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83e8e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e8e-130">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="83e8e-130">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
