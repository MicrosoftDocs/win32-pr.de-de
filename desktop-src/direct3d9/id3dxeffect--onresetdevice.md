---
description: 'ID3DXEffect::OnResetDevice-Methode: Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.'
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: ID3DXEffect::OnResetDevice-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a10d9d0a9092bf7a0fdd345cde8220675503acd0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114928"
---
# <a name="id3dxeffectonresetdevice-method"></a><span data-ttu-id="0bc6d-103">ID3DXEffect::OnResetDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="0bc6d-103">ID3DXEffect::OnResetDevice method</span></span>

<span data-ttu-id="0bc6d-104">Verwenden Sie diese Methode, um Ressourcen erneut zu beziehen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0bc6d-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bc6d-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="0bc6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bc6d-106">Parameters</span></span>

<span data-ttu-id="0bc6d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0bc6d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bc6d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bc6d-108">Return value</span></span>

<span data-ttu-id="0bc6d-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bc6d-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bc6d-110">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0bc6d-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0bc6d-111">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="0bc6d-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc6d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bc6d-112">Remarks</span></span>

<span data-ttu-id="0bc6d-113">**ID3DXEffect::OnResetDevice** sollte jedes Mal aufgerufen werden, wenn das Gerät zurückgesetzt wird (mit [**IDirect3DDevice9::Reset),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)bevor andere Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0bc6d-113">**ID3DXEffect::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="0bc6d-114">Dies ist ein guter Ort zum erneuten Abrufen von Videospeicherressourcen und Erfassen von Zustandsblöcken.</span><span class="sxs-lookup"><span data-stu-id="0bc6d-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bc6d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bc6d-115">Requirements</span></span>



| <span data-ttu-id="0bc6d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bc6d-116">Requirement</span></span> | <span data-ttu-id="0bc6d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0bc6d-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc6d-118">Header</span><span class="sxs-lookup"><span data-stu-id="0bc6d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0bc6d-119"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc6d-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0bc6d-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0bc6d-120">Library</span></span><br/> | <dl> <span data-ttu-id="0bc6d-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bc6d-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0bc6d-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0bc6d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc6d-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="0bc6d-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
