---
title: WM_CAP_PAL_OPEN Meldung (VFW. h)
description: Die "WM \_ Cap \_ PAL Open" \_ -Nachricht lädt eine neue Palette aus einer Palettendatei und übergibt sie an einen Aufzeichnungs Treiber.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340973"
---
# <a name="wm_cap_pal_open-message"></a><span data-ttu-id="a5b4e-104">WM- \_ Cap- \_ \_ Öffnungs Nachricht öffnen</span><span class="sxs-lookup"><span data-stu-id="a5b4e-104">WM\_CAP\_PAL\_OPEN message</span></span>

<span data-ttu-id="a5b4e-105">Die " **WM \_ Cap \_ PAL \_ Open** "-Nachricht lädt eine neue Palette aus einer Palettendatei und übergibt sie an einen Aufzeichnungs Treiber.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-105">The **WM\_CAP\_PAL\_OPEN** message loads a new palette from a palette file and passes it to a capture driver.</span></span> <span data-ttu-id="a5b4e-106">Palettendateien verwenden normalerweise die Dateinamenerweiterung. Straf.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-106">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="a5b4e-107">Ein Aufzeichnungs Treiber verwendet eine Palette, wenn dies für das angegebene digitalisierte Bildformat erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-107">A capture driver uses a palette when required by the specified digitized image format.</span></span> <span data-ttu-id="a5b4e-108">Sie können diese Nachricht explizit oder mithilfe des [**cappaletteopen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-108">You can send this message explicitly or by using the [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) macro.</span></span>


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="a5b4e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5b4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5b4e-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="a5b4e-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="a5b4e-111">Zeiger auf eine mit NULL endenden Zeichenfolge, die den palettendateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-111">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5b4e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5b4e-112">Return Value</span></span>

<span data-ttu-id="a5b4e-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="a5b4e-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="a5b4e-114">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a5b4e-114">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b4e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5b4e-115">Requirements</span></span>



| <span data-ttu-id="a5b4e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5b4e-116">Requirement</span></span> | <span data-ttu-id="a5b4e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a5b4e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a5b4e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5b4e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b4e-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5b4e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a5b4e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5b4e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b4e-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5b4e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a5b4e-122">Header</span><span class="sxs-lookup"><span data-stu-id="a5b4e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5b4e-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5b4e-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b4e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5b4e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b4e-125">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="a5b4e-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="a5b4e-126">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="a5b4e-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





