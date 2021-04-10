---
description: Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.
ms.assetid: a5c82a58-10f9-44bd-a42f-555867b2c857
title: 'ID3DXLine:: OnLostDevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40b42f5a4d027d00b458b572a28ea0c6987cf971
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961740"
---
# <a name="id3dxlineonlostdevice-method"></a><span data-ttu-id="ca115-104">ID3DXLine:: OnLostDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="ca115-104">ID3DXLine::OnLostDevice method</span></span>

<span data-ttu-id="ca115-105">Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ca115-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="ca115-106">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="ca115-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca115-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca115-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="ca115-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca115-108">Parameters</span></span>

<span data-ttu-id="ca115-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ca115-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca115-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca115-110">Return value</span></span>

<span data-ttu-id="ca115-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca115-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca115-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca115-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ca115-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="ca115-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca115-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca115-114">Remarks</span></span>

<span data-ttu-id="ca115-115">Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9:: Reset**](/windows/desktop/api)aufruft.</span><span class="sxs-lookup"><span data-stu-id="ca115-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="ca115-116">Auch wenn das Gerät nicht verloren ging, ist **ID3DXLine:: OnLostDevice** für das Freigeben von stateblocks und anderen Ressourcen zuständig, die vor dem Zurücksetzen des Geräts möglicherweise freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ca115-116">Even if the device was not actually lost, **ID3DXLine::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="ca115-117">Folglich kann das Schriftart Objekt nicht erneut verwendet werden, bevor **IDirect3DDevice9:: Reset** und dann [**ID3DXLine:: OnResetDevice**](id3dxline--onresetdevice.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ca115-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXLine::OnResetDevice**](id3dxline--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca115-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca115-118">Requirements</span></span>



| <span data-ttu-id="ca115-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca115-119">Requirement</span></span> | <span data-ttu-id="ca115-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ca115-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca115-121">Header</span><span class="sxs-lookup"><span data-stu-id="ca115-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ca115-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca115-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ca115-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca115-123">Library</span></span><br/> | <dl> <span data-ttu-id="ca115-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca115-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ca115-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca115-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca115-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="ca115-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 




