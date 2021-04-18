---
title: WM_CAP_PAL_SAVE Meldung (VFW. h)
description: Die "WM \_ Cap \_ PAL Save"- \_ Nachricht speichert die aktuelle Palette in einer Palettendatei. Palettendateien verwenden normalerweise die Dateinamenerweiterung. Straf. Sie können diese Nachricht explizit oder mithilfe des-Makros cappalettesave senden.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- WM_CAP_PAL_SAVE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339988"
---
# <a name="wm_cap_pal_save-message"></a><span data-ttu-id="4cc07-106">WM- \_ Cap- \_ Nachricht zum \_ Speichern</span><span class="sxs-lookup"><span data-stu-id="4cc07-106">WM\_CAP\_PAL\_SAVE message</span></span>

<span data-ttu-id="4cc07-107">Die " **WM \_ Cap \_ PAL \_ Save** "-Nachricht speichert die aktuelle Palette in einer Palettendatei.</span><span class="sxs-lookup"><span data-stu-id="4cc07-107">The **WM\_CAP\_PAL\_SAVE** message saves the current palette to a palette file.</span></span> <span data-ttu-id="4cc07-108">Palettendateien verwenden normalerweise die Dateinamenerweiterung. Straf.</span><span class="sxs-lookup"><span data-stu-id="4cc07-108">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="4cc07-109">Sie können diese Nachricht explizit oder mithilfe des-Makros [**cappalettesave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) senden.</span><span class="sxs-lookup"><span data-stu-id="4cc07-109">You can send this message explicitly or by using the [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) macro.</span></span>


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="4cc07-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cc07-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cc07-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="4cc07-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="4cc07-112">Zeiger auf eine mit NULL endenden Zeichenfolge, die den palettendateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="4cc07-112">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cc07-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cc07-113">Return Value</span></span>

<span data-ttu-id="4cc07-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="4cc07-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="4cc07-115">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4cc07-115">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc07-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cc07-116">Requirements</span></span>



| <span data-ttu-id="4cc07-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cc07-117">Requirement</span></span> | <span data-ttu-id="4cc07-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4cc07-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4cc07-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cc07-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4cc07-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cc07-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4cc07-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cc07-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4cc07-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cc07-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4cc07-123">Header</span><span class="sxs-lookup"><span data-stu-id="4cc07-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cc07-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cc07-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc07-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cc07-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc07-126">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="4cc07-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4cc07-127">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="4cc07-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





