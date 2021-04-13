---
description: Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: 'ID3DXRenderToEnvMap:: OnLostDevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b644ab595fd8bc6ebdfa544cc004598f5570d262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354526"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a><span data-ttu-id="8cfae-104">ID3DXRenderToEnvMap:: OnLostDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="8cfae-104">ID3DXRenderToEnvMap::OnLostDevice method</span></span>

<span data-ttu-id="8cfae-105">Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8cfae-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="8cfae-106">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8cfae-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cfae-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cfae-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="8cfae-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cfae-108">Parameters</span></span>

<span data-ttu-id="8cfae-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8cfae-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8cfae-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cfae-110">Return value</span></span>

<span data-ttu-id="8cfae-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cfae-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cfae-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8cfae-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8cfae-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="8cfae-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cfae-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cfae-114">Remarks</span></span>

<span data-ttu-id="8cfae-115">Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9:: Reset**](/windows/desktop/api)aufruft.</span><span class="sxs-lookup"><span data-stu-id="8cfae-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="8cfae-116">Auch wenn das Gerät nicht verloren ging, ist **ID3DXRenderToEnvMap:: OnLostDevice** für das Freigeben von stateblocks und anderen Ressourcen zuständig, die vor dem Zurücksetzen des Geräts möglicherweise freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8cfae-116">Even if the device was not actually lost, **ID3DXRenderToEnvMap::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="8cfae-117">Folglich kann das Schriftart Objekt nicht erneut verwendet werden, bevor **IDirect3DDevice9:: Reset** und dann [**ID3DXRenderToEnvMap:: OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8cfae-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfae-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cfae-118">Requirements</span></span>



| <span data-ttu-id="8cfae-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cfae-119">Requirement</span></span> | <span data-ttu-id="8cfae-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8cfae-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfae-121">Header</span><span class="sxs-lookup"><span data-stu-id="8cfae-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8cfae-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cfae-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8cfae-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8cfae-123">Library</span></span><br/> | <dl> <span data-ttu-id="8cfae-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cfae-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8cfae-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cfae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cfae-126">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="8cfae-126">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




