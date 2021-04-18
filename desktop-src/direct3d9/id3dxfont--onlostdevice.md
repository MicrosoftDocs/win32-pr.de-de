---
description: Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: 'ID3DXFont:: OnLostDevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae2dc711ffe57a2605a0cc43c7ba673d444105f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354383"
---
# <a name="id3dxfontonlostdevice-method"></a><span data-ttu-id="c4a72-104">ID3DXFont:: OnLostDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="c4a72-104">ID3DXFont::OnLostDevice method</span></span>

<span data-ttu-id="c4a72-105">Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c4a72-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="c4a72-106">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c4a72-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a72-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4a72-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="c4a72-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4a72-108">Parameters</span></span>

<span data-ttu-id="c4a72-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c4a72-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4a72-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4a72-110">Return value</span></span>

<span data-ttu-id="c4a72-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4a72-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4a72-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4a72-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c4a72-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="c4a72-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4a72-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4a72-114">Remarks</span></span>

<span data-ttu-id="c4a72-115">Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer die [**zurück**](/windows/desktop/api)Setzung aufruft.</span><span class="sxs-lookup"><span data-stu-id="c4a72-115">This method should be called whenever the device is lost or before the user calls [**Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="c4a72-116">Auch wenn das Gerät nicht verloren gegangen ist, ist **OnLostDevice** für das Freigeben von stateblocks und anderen Ressourcen zuständig, die vor dem Zurücksetzen des Geräts möglicherweise freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c4a72-116">Even if the device was not actually lost, **OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="c4a72-117">Folglich kann das Schriftart Objekt nicht erneut verwendet werden, bevor **Reset** und dann [**OnResetDevice**](id3dxfont--onresetdevice.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c4a72-117">As a result, the font object cannot be used again before calling **Reset** and then [**OnResetDevice**](id3dxfont--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a72-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4a72-118">Requirements</span></span>



| <span data-ttu-id="c4a72-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4a72-119">Requirement</span></span> | <span data-ttu-id="c4a72-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c4a72-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a72-121">Header</span><span class="sxs-lookup"><span data-stu-id="c4a72-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c4a72-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4a72-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c4a72-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4a72-123">Library</span></span><br/> | <dl> <span data-ttu-id="c4a72-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4a72-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4a72-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4a72-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a72-126">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="c4a72-126">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




