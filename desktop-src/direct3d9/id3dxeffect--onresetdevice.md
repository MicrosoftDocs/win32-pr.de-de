---
description: Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: 'ID3DXEffect:: OnResetDevice-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: d419ad456fcefbf0d6e4a201d4949556d6694e46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355793"
---
# <a name="id3dxeffectonresetdevice-method"></a><span data-ttu-id="f36cc-103">ID3DXEffect:: OnResetDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="f36cc-103">ID3DXEffect::OnResetDevice method</span></span>

<span data-ttu-id="f36cc-104">Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f36cc-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f36cc-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="f36cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f36cc-106">Parameters</span></span>

<span data-ttu-id="f36cc-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f36cc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f36cc-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f36cc-108">Return value</span></span>

<span data-ttu-id="f36cc-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f36cc-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f36cc-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f36cc-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f36cc-111">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="f36cc-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f36cc-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f36cc-112">Remarks</span></span>

<span data-ttu-id="f36cc-113">**ID3DXEffect:: OnResetDevice** sollte jedes Mal aufgerufen werden, wenn das Gerät zurückgesetzt wird (mit [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), bevor andere Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f36cc-113">**ID3DXEffect::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="f36cc-114">Dies ist ein guter Ort zum erneuten Abrufen von Video-Memory-Ressourcen und zum Erfassen von Zustands Blöcken.</span><span class="sxs-lookup"><span data-stu-id="f36cc-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="f36cc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f36cc-115">Requirements</span></span>



| <span data-ttu-id="f36cc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f36cc-116">Requirement</span></span> | <span data-ttu-id="f36cc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f36cc-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f36cc-118">Header</span><span class="sxs-lookup"><span data-stu-id="f36cc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f36cc-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f36cc-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f36cc-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f36cc-120">Library</span></span><br/> | <dl> <span data-ttu-id="f36cc-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f36cc-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f36cc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f36cc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36cc-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="f36cc-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
