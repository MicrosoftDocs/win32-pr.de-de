---
description: Unterteilt Gesichter in einem Mesh und ermöglicht eine konservative Adaptive Stichprobenentnahme, bei der keine Features im Mesh entfernt werden.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'ID3DXPRTEngine:: RobustMeshRefine-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365337"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a><span data-ttu-id="6a9ac-103">ID3DXPRTEngine:: RobustMeshRefine-Methode</span><span class="sxs-lookup"><span data-stu-id="6a9ac-103">ID3DXPRTEngine::RobustMeshRefine method</span></span>

<span data-ttu-id="6a9ac-104">Unterteilt Gesichter in einem Mesh und ermöglicht eine konservative Adaptive Stichprobenentnahme, bei der keine Features im Mesh entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6a9ac-104">Subdivides faces on a mesh, allowing for conservative adaptive sampling that will not eliminate features on the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a9ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a9ac-105">Syntax</span></span>


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a><span data-ttu-id="6a9ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a9ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a9ac-107">*Minedgelength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a9ac-107">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9ac-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a9ac-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a9ac-109">Minimale Vorderseiten Länge, die bei der adaptiven Stichproben Erstellung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="6a9ac-109">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="6a9ac-110">Wenn 0 (null), wird ein angemessener Standardwert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6a9ac-110">If zero, a reasonable default value will be substituted.</span></span>

</dd> <dt>

<span data-ttu-id="6a9ac-111">*Maxsubdiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a9ac-111">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9ac-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a9ac-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a9ac-113">Maximale Ebene der Unterteilung einer Fläche, die bei der adaptiven Stichprobenentnahme verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6a9ac-113">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="6a9ac-114">Wenn der Wert 0 (null) ist, wird der Standardwert 5 ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6a9ac-114">If zero, a default value of 5 will be substituted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a9ac-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a9ac-115">Return value</span></span>

<span data-ttu-id="6a9ac-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a9ac-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a9ac-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a9ac-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6a9ac-118">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="6a9ac-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a9ac-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a9ac-119">Requirements</span></span>



| <span data-ttu-id="6a9ac-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a9ac-120">Requirement</span></span> | <span data-ttu-id="6a9ac-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6a9ac-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9ac-122">Header</span><span class="sxs-lookup"><span data-stu-id="6a9ac-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6a9ac-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a9ac-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6a9ac-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6a9ac-124">Library</span></span><br/> | <dl> <span data-ttu-id="6a9ac-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a9ac-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a9ac-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a9ac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a9ac-127">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="6a9ac-127">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="6a9ac-128">**ID3DXPRTEngine:: computebounceadaptive**</span><span class="sxs-lookup"><span data-stu-id="6a9ac-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span></span>](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[<span data-ttu-id="6a9ac-129">**ID3DXPRTEngine:: computedirectlightingshadaptive**</span><span class="sxs-lookup"><span data-stu-id="6a9ac-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span></span>](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
