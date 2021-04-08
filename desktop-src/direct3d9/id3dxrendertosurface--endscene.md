---
description: Beendet eine Szene.
ms.assetid: f721593e-6cba-4569-8276-6a4ffc0fc37a
title: 'ID3DXRenderToSurface:: EndScene-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.EndScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5aa0c1fbccb756ac612b813ad151813a782b122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761994"
---
# <a name="id3dxrendertosurfaceendscene-method"></a><span data-ttu-id="f2232-103">ID3DXRenderToSurface:: EndScene-Methode</span><span class="sxs-lookup"><span data-stu-id="f2232-103">ID3DXRenderToSurface::EndScene method</span></span>

<span data-ttu-id="f2232-104">Beendet eine Szene.</span><span class="sxs-lookup"><span data-stu-id="f2232-104">Ends a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2232-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2232-105">Syntax</span></span>


```C++
HRESULT EndScene(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="f2232-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2232-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2232-107">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2232-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2232-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2232-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2232-109">Filteroptionen, aufgelistet in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f2232-109">Filter options, enumerated in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2232-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2232-110">Return value</span></span>

<span data-ttu-id="f2232-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2232-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2232-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f2232-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2232-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="f2232-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2232-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2232-114">Requirements</span></span>



| <span data-ttu-id="f2232-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2232-115">Requirement</span></span> | <span data-ttu-id="f2232-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f2232-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2232-117">Header</span><span class="sxs-lookup"><span data-stu-id="f2232-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f2232-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2232-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f2232-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2232-119">Library</span></span><br/> | <dl> <span data-ttu-id="f2232-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2232-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2232-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2232-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2232-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="f2232-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="f2232-123">**ID3DXRenderToSurface:: BeginScene**</span><span class="sxs-lookup"><span data-stu-id="f2232-123">**ID3DXRenderToSurface::BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)
</dt> </dl>

 

 
