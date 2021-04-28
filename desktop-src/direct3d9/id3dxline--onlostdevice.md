---
description: 'ID3DXLine::OnLostDevice-Methode: Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.'
ms.assetid: a5c82a58-10f9-44bd-a42f-555867b2c857
title: ID3DXLine::OnLostDevice-Methode (D3dx9core.h)
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
ms.openlocfilehash: 9f3845e40e4ece115704c38904a61dbca3c24443
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093678"
---
# <a name="id3dxlineonlostdevice-method"></a><span data-ttu-id="b3c6c-104">ID3DXLine::OnLostDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="b3c6c-104">ID3DXLine::OnLostDevice method</span></span>

<span data-ttu-id="b3c6c-105">Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="b3c6c-106">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c6c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3c6c-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="b3c6c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3c6c-108">Parameters</span></span>

<span data-ttu-id="b3c6c-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3c6c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3c6c-110">Return value</span></span>

<span data-ttu-id="b3c6c-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3c6c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3c6c-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b3c6c-113">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c6c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3c6c-114">Remarks</span></span>

<span data-ttu-id="b3c6c-115">Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9::Reset aufruft.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="b3c6c-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="b3c6c-116">Selbst wenn das Gerät nicht verloren gegangen ist, ist **ID3DXLine::OnLostDevice** für die Freigabe von Zustandsblocks und anderen Ressourcen verantwortlich, die möglicherweise freigegeben werden müssen, bevor das Gerät zurücksetzungen.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-116">Even if the device was not actually lost, **ID3DXLine::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="b3c6c-117">Daher kann das Schriftartobjekt vor dem Aufruf von **IDirect3DDevice9::Reset** und [**id3DXLine::OnResetDevice**](id3dxline--onresetdevice.md)nicht erneut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3c6c-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXLine::OnResetDevice**](id3dxline--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c6c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3c6c-118">Requirements</span></span>



| <span data-ttu-id="b3c6c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3c6c-119">Requirement</span></span> | <span data-ttu-id="b3c6c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b3c6c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c6c-121">Header</span><span class="sxs-lookup"><span data-stu-id="b3c6c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b3c6c-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c6c-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b3c6c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3c6c-123">Library</span></span><br/> | <dl> <span data-ttu-id="b3c6c-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3c6c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3c6c-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3c6c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c6c-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="b3c6c-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 




