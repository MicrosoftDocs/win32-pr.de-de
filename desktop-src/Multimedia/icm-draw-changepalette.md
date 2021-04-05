---
title: ICM_DRAW_CHANGEPALETTE Meldung (VFW. h)
description: Die ICM \_ Draw \_ changepalette-Meldung benachrichtigt einen renderingtreiber, dass sich die Film Palette ändert. Sie können diese Nachricht explizit oder mithilfe des icdrawchangepalette-Makros senden.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- ICM_DRAW_CHANGEPALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858986"
---
# <a name="icm_draw_changepalette-message"></a><span data-ttu-id="a756b-105">ICM- \_ Meldung zum Zeichnen der \_ changepalette</span><span class="sxs-lookup"><span data-stu-id="a756b-105">ICM\_DRAW\_CHANGEPALETTE message</span></span>

<span data-ttu-id="a756b-106">Die **ICM \_ Draw \_ changepalette** -Meldung benachrichtigt einen renderingtreiber, dass sich die Film Palette ändert.</span><span class="sxs-lookup"><span data-stu-id="a756b-106">The **ICM\_DRAW\_CHANGEPALETTE** message notifies a rendering driver that the movie palette is changing.</span></span> <span data-ttu-id="a756b-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawchangepalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="a756b-107">You can send this message explicitly or by using the [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) macro.</span></span>


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="a756b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a756b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a756b-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="a756b-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="a756b-110">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das neue Format und die optionale Farbtabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="a756b-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the new format and optional color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a756b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a756b-111">Return Value</span></span>

<span data-ttu-id="a756b-112">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="a756b-112">Returns ICERR\_OK if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a756b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a756b-113">Remarks</span></span>

<span data-ttu-id="a756b-114">Diese Meldung sollte von installierbaren renderhandlern unterstützt werden, die Disb mit einer internen Struktur zeichnen, die eine Palette enthält.</span><span class="sxs-lookup"><span data-stu-id="a756b-114">This message should be supported by installable rendering handlers that draw DIBs with an internal structure that includes a palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="a756b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a756b-115">Requirements</span></span>



| <span data-ttu-id="a756b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a756b-116">Requirement</span></span> | <span data-ttu-id="a756b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a756b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a756b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a756b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a756b-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a756b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a756b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a756b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a756b-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a756b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a756b-122">Header</span><span class="sxs-lookup"><span data-stu-id="a756b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a756b-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a756b-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a756b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a756b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a756b-125">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="a756b-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a756b-126">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="a756b-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

