---
description: Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.
ms.assetid: 74f8616e-c3ed-4231-b701-009213ea48c0
title: 'ID3DXSprite:: OnResetDevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f09e08a32aca8df0577a5fb73ef09ec69742556b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363985"
---
# <a name="id3dxspriteonresetdevice-method"></a><span data-ttu-id="7a092-103">ID3DXSprite:: OnResetDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="7a092-103">ID3DXSprite::OnResetDevice method</span></span>

<span data-ttu-id="7a092-104">Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7a092-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a092-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a092-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="7a092-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a092-106">Parameters</span></span>

<span data-ttu-id="7a092-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7a092-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a092-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a092-108">Return value</span></span>

<span data-ttu-id="7a092-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7a092-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7a092-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7a092-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7a092-111">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="7a092-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a092-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a092-112">Remarks</span></span>

<span data-ttu-id="7a092-113">**ID3DXSprite:: OnResetDevice** sollte jedes Mal aufgerufen werden, wenn das Gerät zurückgesetzt wird (mit [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), bevor andere Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7a092-113">**ID3DXSprite::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="7a092-114">Dies ist ein guter Ort zum erneuten Abrufen von Video-Memory-Ressourcen und zum Erfassen von Zustands Blöcken.</span><span class="sxs-lookup"><span data-stu-id="7a092-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a092-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a092-115">Requirements</span></span>



| <span data-ttu-id="7a092-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a092-116">Requirement</span></span> | <span data-ttu-id="7a092-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7a092-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a092-118">Header</span><span class="sxs-lookup"><span data-stu-id="7a092-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7a092-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a092-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7a092-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7a092-120">Library</span></span><br/> | <dl> <span data-ttu-id="7a092-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a092-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7a092-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a092-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a092-123">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="7a092-123">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 
