---
description: Stellen Sie alle Renderziele wieder her, und erstellen Sie, falls erforderlich, alle gerenderten Gesichter in der Umgebungs Zuordnungs Oberfläche.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'ID3DXRenderToEnvMap:: End-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354566"
---
# <a name="id3dxrendertoenvmapend-method"></a><span data-ttu-id="e0ec5-103">ID3DXRenderToEnvMap:: End-Methode</span><span class="sxs-lookup"><span data-stu-id="e0ec5-103">ID3DXRenderToEnvMap::End method</span></span>

<span data-ttu-id="e0ec5-104">Stellen Sie alle Renderziele wieder her, und erstellen Sie, falls erforderlich, alle gerenderten Gesichter in der Umgebungs Zuordnungs Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="e0ec5-104">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ec5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0ec5-105">Syntax</span></span>


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="e0ec5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0ec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0ec5-107">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0ec5-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0ec5-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0ec5-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0ec5-109">Eine gültige Kombination aus einem oder mehreren [D3DX- \_ Filterflags](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="e0ec5-109">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0ec5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0ec5-110">Return value</span></span>

<span data-ttu-id="e0ec5-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0ec5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0ec5-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0ec5-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e0ec5-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="e0ec5-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ec5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0ec5-114">Requirements</span></span>



| <span data-ttu-id="e0ec5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0ec5-115">Requirement</span></span> | <span data-ttu-id="e0ec5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e0ec5-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ec5-117">Header</span><span class="sxs-lookup"><span data-stu-id="e0ec5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e0ec5-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0ec5-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e0ec5-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0ec5-119">Library</span></span><br/> | <dl> <span data-ttu-id="e0ec5-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0ec5-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0ec5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0ec5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0ec5-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="e0ec5-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="e0ec5-123">**ID3DXRenderToEnvMap:: Face**</span><span class="sxs-lookup"><span data-stu-id="e0ec5-123">**ID3DXRenderToEnvMap::Face**</span></span>](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
