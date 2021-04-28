---
description: 'ID3DXFont::OnLostDevice-Methode: Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.'
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: ID3DXFont::OnLostDevice-Methode (D3dx9core.h)
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
ms.openlocfilehash: 9c484d7867745805e29bda88e2f8d49ca8bc21be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090368"
---
# <a name="id3dxfontonlostdevice-method"></a><span data-ttu-id="56207-104">ID3DXFont::OnLostDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="56207-104">ID3DXFont::OnLostDevice method</span></span>

<span data-ttu-id="56207-105">Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="56207-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="56207-106">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.</span><span class="sxs-lookup"><span data-stu-id="56207-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="56207-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56207-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="56207-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56207-108">Parameters</span></span>

<span data-ttu-id="56207-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="56207-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56207-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56207-110">Return value</span></span>

<span data-ttu-id="56207-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56207-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56207-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="56207-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="56207-113">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="56207-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="56207-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56207-114">Remarks</span></span>

<span data-ttu-id="56207-115">Diese Methode sollte immer aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer Reset [**aufruft.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="56207-115">This method should be called whenever the device is lost or before the user calls [**Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="56207-116">Auch wenn das Gerät nicht tatsächlich verloren gegangen ist, ist **OnLostDevice** für die Freigabe von Zustandsblocks und anderen Ressourcen verantwortlich, die möglicherweise freigegeben werden müssen, bevor das Gerät zurück gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="56207-116">Even if the device was not actually lost, **OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="56207-117">Daher kann das Schriftartobjekt vor dem Aufruf von **Reset** und [**onResetDevice nicht erneut verwendet werden.**](id3dxfont--onresetdevice.md)</span><span class="sxs-lookup"><span data-stu-id="56207-117">As a result, the font object cannot be used again before calling **Reset** and then [**OnResetDevice**](id3dxfont--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56207-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56207-118">Requirements</span></span>



| <span data-ttu-id="56207-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56207-119">Requirement</span></span> | <span data-ttu-id="56207-120">Wert</span><span class="sxs-lookup"><span data-stu-id="56207-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56207-121">Header</span><span class="sxs-lookup"><span data-stu-id="56207-121">Header</span></span><br/>  | <dl> <span data-ttu-id="56207-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="56207-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="56207-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56207-123">Library</span></span><br/> | <dl> <span data-ttu-id="56207-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="56207-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56207-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="56207-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56207-126">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="56207-126">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




