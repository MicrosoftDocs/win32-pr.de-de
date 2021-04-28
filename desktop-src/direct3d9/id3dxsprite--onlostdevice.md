---
description: 'ID3DXSprite::OnLostDevice-Methode: Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.'
ms.assetid: 60028f18-21fe-428b-9bee-d5359671da81
title: ID3DXSprite::OnLostDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5515945ec8575937a90eb719eca4efd681be5d0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117778"
---
# <a name="id3dxspriteonlostdevice-method"></a><span data-ttu-id="acf51-104">ID3DXSprite::OnLostDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="acf51-104">ID3DXSprite::OnLostDevice method</span></span>

<span data-ttu-id="acf51-105">Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="acf51-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="acf51-106">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.</span><span class="sxs-lookup"><span data-stu-id="acf51-106">This method should be called whenever a device is lost or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf51-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="acf51-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="acf51-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="acf51-108">Parameters</span></span>

<span data-ttu-id="acf51-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="acf51-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="acf51-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="acf51-110">Return value</span></span>

<span data-ttu-id="acf51-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="acf51-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="acf51-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="acf51-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="acf51-113">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="acf51-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="acf51-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acf51-114">Remarks</span></span>

<span data-ttu-id="acf51-115">Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9::Reset aufruft.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="acf51-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="acf51-116">Selbst wenn das Gerät nicht tatsächlich verloren gegangen ist, ist **ID3DXSprite::OnLostDevice** für die Freigabe von Zustandsblocks und anderen Ressourcen verantwortlich, die möglicherweise freigegeben werden müssen, bevor das Gerät zurück gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="acf51-116">Even if the device was not actually lost, **ID3DXSprite::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="acf51-117">Daher kann das Schriftartobjekt nicht erneut verwendet werden, bevor **IDirect3DDevice9::Reset** und dann [**ID3DXSprite::OnResetDevice aufruft.**](id3dxsprite--onresetdevice.md)</span><span class="sxs-lookup"><span data-stu-id="acf51-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXSprite::OnResetDevice**](id3dxsprite--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="acf51-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acf51-118">Requirements</span></span>



| <span data-ttu-id="acf51-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acf51-119">Requirement</span></span> | <span data-ttu-id="acf51-120">Wert</span><span class="sxs-lookup"><span data-stu-id="acf51-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="acf51-121">Header</span><span class="sxs-lookup"><span data-stu-id="acf51-121">Header</span></span><br/>  | <dl> <span data-ttu-id="acf51-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="acf51-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="acf51-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="acf51-123">Library</span></span><br/> | <dl> <span data-ttu-id="acf51-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="acf51-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="acf51-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="acf51-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf51-126">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="acf51-126">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




