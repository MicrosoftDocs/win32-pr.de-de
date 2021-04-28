---
description: 'ID3DXRenderToEnvMap::OnLostDevice-Methode: Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.'
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: ID3DXRenderToEnvMap::OnLostDevice-Methode (D3dx9core.h)
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
ms.openlocfilehash: 88f27c259262eb7abb57246e547ad66866bb3dcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107198"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a><span data-ttu-id="02f95-104">ID3DXRenderToEnvMap::OnLostDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="02f95-104">ID3DXRenderToEnvMap::OnLostDevice method</span></span>

<span data-ttu-id="02f95-105">Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="02f95-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="02f95-106">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.</span><span class="sxs-lookup"><span data-stu-id="02f95-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f95-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="02f95-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="02f95-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02f95-108">Parameters</span></span>

<span data-ttu-id="02f95-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="02f95-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02f95-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02f95-110">Return value</span></span>

<span data-ttu-id="02f95-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02f95-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02f95-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="02f95-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="02f95-113">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="02f95-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f95-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02f95-114">Remarks</span></span>

<span data-ttu-id="02f95-115">Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9::Reset aufruft.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="02f95-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="02f95-116">Selbst wenn das Gerät nicht tatsächlich verloren gegangen ist, ist **ID3DXRenderToEnvMap::OnLostDevice** für die Freigabe von Zustandsblocks und anderen Ressourcen verantwortlich, die möglicherweise vor dem Zurücksetzen des Geräts freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="02f95-116">Even if the device was not actually lost, **ID3DXRenderToEnvMap::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="02f95-117">Daher kann das Schriftartobjekt vor dem Aufruf von **IDirect3DDevice9::Reset** und [**id3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)nicht erneut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02f95-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02f95-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02f95-118">Requirements</span></span>



| <span data-ttu-id="02f95-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02f95-119">Requirement</span></span> | <span data-ttu-id="02f95-120">Wert</span><span class="sxs-lookup"><span data-stu-id="02f95-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02f95-121">Header</span><span class="sxs-lookup"><span data-stu-id="02f95-121">Header</span></span><br/>  | <dl> <span data-ttu-id="02f95-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="02f95-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="02f95-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02f95-123">Library</span></span><br/> | <dl> <span data-ttu-id="02f95-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="02f95-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02f95-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="02f95-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f95-126">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="02f95-126">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




