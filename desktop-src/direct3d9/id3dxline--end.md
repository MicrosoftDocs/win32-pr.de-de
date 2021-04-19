---
description: 'Stellt den Zustand des Geräts in dem Zustand wieder her, in dem es sich beim Aufrufen von ID3DXLine:: begin befand'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'ID3DXLine:: End-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370467"
---
# <a name="id3dxlineend-method"></a><span data-ttu-id="ebf95-103">ID3DXLine:: End-Methode</span><span class="sxs-lookup"><span data-stu-id="ebf95-103">ID3DXLine::End method</span></span>

<span data-ttu-id="ebf95-104">Stellt den Zustand des Geräts in dem Zustand wieder her, in dem es sich beim Aufrufen von [**ID3DXLine:: begin**](id3dxline--begin.md) befand</span><span class="sxs-lookup"><span data-stu-id="ebf95-104">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf95-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebf95-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="ebf95-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebf95-106">Parameters</span></span>

<span data-ttu-id="ebf95-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ebf95-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebf95-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebf95-108">Return value</span></span>

<span data-ttu-id="ebf95-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ebf95-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ebf95-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ebf95-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ebf95-111">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="ebf95-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf95-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebf95-112">Remarks</span></span>

<span data-ttu-id="ebf95-113">**ID3DXLine:: End** kann nicht als Ersatz für [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) oder [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebf95-113">**ID3DXLine::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf95-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebf95-114">Requirements</span></span>



| <span data-ttu-id="ebf95-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebf95-115">Requirement</span></span> | <span data-ttu-id="ebf95-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ebf95-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf95-117">Header</span><span class="sxs-lookup"><span data-stu-id="ebf95-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ebf95-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebf95-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ebf95-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ebf95-119">Library</span></span><br/> | <dl> <span data-ttu-id="ebf95-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebf95-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ebf95-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebf95-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf95-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="ebf95-122">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="ebf95-123">**ID3DXLine:: begin**</span><span class="sxs-lookup"><span data-stu-id="ebf95-123">**ID3DXLine::Begin**</span></span>](id3dxline--begin.md)
</dt> </dl>

 

 




