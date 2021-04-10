---
description: Eine Anwendung sendet die WM- \_ mditile-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle untergeordneten MDI-Fenster in einem Kachel Format anzuordnen.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: WM_MDITILE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214544"
---
# <a name="wm_mditile-message"></a><span data-ttu-id="c6c34-103">WM- \_ mditile-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c6c34-103">WM\_MDITILE message</span></span>

<span data-ttu-id="c6c34-104">Eine Anwendung sendet die **WM- \_ mditile** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle untergeordneten MDI-Fenster in einem Kachel Format anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c6c34-104">An application sends the **WM\_MDITILE** message to a multiple-document interface (MDI) client window to arrange all of its MDI child windows in a tile format.</span></span>


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a><span data-ttu-id="c6c34-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6c34-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c34-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6c34-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c34-107">Die gezitzungsoption.</span><span class="sxs-lookup"><span data-stu-id="c6c34-107">The tiling option.</span></span> <span data-ttu-id="c6c34-108">Dieser Parameter kann einen der folgenden Werte aufweisen, optional kombiniert mit **mditile \_ skipdeaktiviert** , um zu verhindern, dass deaktivierte untergeordnete MDI-Fenster nebeneinander gekachelt werden.</span><span class="sxs-lookup"><span data-stu-id="c6c34-108">This parameter can be one of the following values, optionally combined with **MDITILE\_SKIPDISABLED** to prevent disabled MDI child windows from being tiled.</span></span>



| <span data-ttu-id="c6c34-109">Wert</span><span class="sxs-lookup"><span data-stu-id="c6c34-109">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="c6c34-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c6c34-110">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <span data-ttu-id="c6c34-111"><dt>**Mditile \_ HORIZONTAL**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c6c34-111"><dt>**MDITILE\_HORIZONTAL**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="c6c34-112">Kacheln Fenster horizontal.</span><span class="sxs-lookup"><span data-stu-id="c6c34-112">Tiles windows horizontally.</span></span><br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <span data-ttu-id="c6c34-113"><dt>**Mditile \_ Vertikal**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="c6c34-113"><dt>**MDITILE\_VERTICAL**</dt> <dt>0x0000</dt></span></span> </dl>       | <span data-ttu-id="c6c34-114">Kacheln Fenster vertikal.</span><span class="sxs-lookup"><span data-stu-id="c6c34-114">Tiles windows vertically.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c6c34-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6c34-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c34-116">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6c34-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c34-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6c34-117">Return value</span></span>

<span data-ttu-id="c6c34-118">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="c6c34-118">Type: **BOOL**</span></span>

<span data-ttu-id="c6c34-119">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="c6c34-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="c6c34-120">Wenn die Meldung fehlschlägt, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="c6c34-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c34-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6c34-121">Requirements</span></span>



| <span data-ttu-id="c6c34-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6c34-122">Requirement</span></span> | <span data-ttu-id="c6c34-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c6c34-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c34-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6c34-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c34-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6c34-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c6c34-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6c34-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c34-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6c34-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6c34-128">Header</span><span class="sxs-lookup"><span data-stu-id="c6c34-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c34-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c34-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c34-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6c34-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6c34-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c6c34-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c6c34-132">**WM- \_ mdicascade**</span><span class="sxs-lookup"><span data-stu-id="c6c34-132">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="c6c34-133">**WM- \_ mdiiconarrange**</span><span class="sxs-lookup"><span data-stu-id="c6c34-133">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

<span data-ttu-id="c6c34-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c6c34-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c6c34-135">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c6c34-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




