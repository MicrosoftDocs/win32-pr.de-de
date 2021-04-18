---
description: Bereitet ein Gerät für Zeichnungs Zeilen vor.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'ID3DXLine:: Begin-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365340"
---
# <a name="id3dxlinebegin-method"></a><span data-ttu-id="22cdd-103">ID3DXLine:: Begin-Methode</span><span class="sxs-lookup"><span data-stu-id="22cdd-103">ID3DXLine::Begin method</span></span>

<span data-ttu-id="22cdd-104">Bereitet ein Gerät für Zeichnungs Zeilen vor.</span><span class="sxs-lookup"><span data-stu-id="22cdd-104">Prepares a device for drawing lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="22cdd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22cdd-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="22cdd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22cdd-106">Parameters</span></span>

<span data-ttu-id="22cdd-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="22cdd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22cdd-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22cdd-108">Return value</span></span>

<span data-ttu-id="22cdd-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22cdd-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22cdd-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22cdd-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="22cdd-111">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="22cdd-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="22cdd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22cdd-112">Remarks</span></span>

<span data-ttu-id="22cdd-113">Das Aufrufen von **ID3DXLine:: begin** ist optional.</span><span class="sxs-lookup"><span data-stu-id="22cdd-113">Calling **ID3DXLine::Begin** is optional.</span></span> <span data-ttu-id="22cdd-114">Wenn Sie außerhalb einer ID3DXLine:: begin/ID3DXLine:: End-Sequenz aufgerufen wird, werden die Draw-Funktionen intern ID3DXLine:: BEGIN und ID3DXLine:: End aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22cdd-114">If called outside of a ID3DXLine::Begin/ID3DXLine::End sequence, the draw functions will internally call ID3DXLine::Begin and ID3DXLine::End.</span></span> <span data-ttu-id="22cdd-115">Um zusätzlichen Aufwand zu vermeiden, sollte diese Methode verwendet werden, wenn mehr als eine Draw-Funktion nacheinander aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="22cdd-115">To avoid extra overhead, this method should be used if more than one draw function will be called successively.</span></span>

<span data-ttu-id="22cdd-116">Diese Methode muss innerhalb einer [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) -und [**IDirect3DDevice9:: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) -Sequenz aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="22cdd-116">This method must be called from inside an [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) and [**IDirect3DDevice9::EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) sequence.</span></span>

<span data-ttu-id="22cdd-117">ID3DXLine:: begin kann nicht als Ersatz für [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) oder [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22cdd-117">ID3DXLine::Begin cannot be used as a substitute for either [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22cdd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22cdd-118">Requirements</span></span>



| <span data-ttu-id="22cdd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22cdd-119">Requirement</span></span> | <span data-ttu-id="22cdd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="22cdd-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22cdd-121">Header</span><span class="sxs-lookup"><span data-stu-id="22cdd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="22cdd-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="22cdd-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="22cdd-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22cdd-123">Library</span></span><br/> | <dl> <span data-ttu-id="22cdd-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22cdd-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22cdd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22cdd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22cdd-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="22cdd-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
