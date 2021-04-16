---
description: 'Ruft ID3DXSprite:: Flush auf und stellt den Gerätezustand vor dem Aufrufen von ID3DXSprite:: begin wieder her.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'ID3DXSprite:: End-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394185"
---
# <a name="id3dxspriteend-method"></a><span data-ttu-id="3a821-103">ID3DXSprite:: End-Methode</span><span class="sxs-lookup"><span data-stu-id="3a821-103">ID3DXSprite::End method</span></span>

<span data-ttu-id="3a821-104">Ruft [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) auf und stellt den Gerätezustand vor dem Aufrufen von [**ID3DXSprite:: begin**](id3dxsprite--begin.md) wieder her.</span><span class="sxs-lookup"><span data-stu-id="3a821-104">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a821-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a821-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="3a821-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a821-106">Parameters</span></span>

<span data-ttu-id="3a821-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3a821-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a821-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a821-108">Return value</span></span>

<span data-ttu-id="3a821-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a821-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a821-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a821-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3a821-111">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="3a821-111">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="3a821-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a821-112">Remarks</span></span>

<span data-ttu-id="3a821-113">**ID3DXSprite:: End** kann nicht als Ersatz für [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) oder [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a821-113">**ID3DXSprite::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a821-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a821-114">Requirements</span></span>



| <span data-ttu-id="3a821-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a821-115">Requirement</span></span> | <span data-ttu-id="3a821-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3a821-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a821-117">Header</span><span class="sxs-lookup"><span data-stu-id="3a821-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3a821-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a821-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3a821-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a821-119">Library</span></span><br/> | <dl> <span data-ttu-id="3a821-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a821-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3a821-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a821-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a821-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="3a821-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="3a821-123">**ID3DXSprite:: begin**</span><span class="sxs-lookup"><span data-stu-id="3a821-123">**ID3DXSprite::Begin**</span></span>](id3dxsprite--begin.md)
</dt> </dl>

 

 




