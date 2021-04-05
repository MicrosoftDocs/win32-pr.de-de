---
description: Wird an ein Fenster gesendet, in dem der Benutzer die Größe ändert. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Größe und Position des Zieh Rechtecks überwachen und ggf. die Größe oder Position ändern.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: WM_SIZING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756631"
---
# <a name="wm_sizing-message"></a><span data-ttu-id="7caca-104">Meldung zur WM- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="7caca-104">WM\_SIZING message</span></span>

<span data-ttu-id="7caca-105">Wird an ein Fenster gesendet, in dem der Benutzer die Größe ändert.</span><span class="sxs-lookup"><span data-stu-id="7caca-105">Sent to a window that the user is resizing.</span></span> <span data-ttu-id="7caca-106">Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Größe und Position des Zieh Rechtecks überwachen und ggf. die Größe oder Position ändern.</span><span class="sxs-lookup"><span data-stu-id="7caca-106">By processing this message, an application can monitor the size and position of the drag rectangle and, if needed, change its size or position.</span></span>

<span data-ttu-id="7caca-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7caca-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a><span data-ttu-id="7caca-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7caca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7caca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7caca-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7caca-110">Der Rand des Fensters mit der Größenanpassung.</span><span class="sxs-lookup"><span data-stu-id="7caca-110">The edge of the window that is being sized.</span></span> <span data-ttu-id="7caca-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="7caca-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7caca-112">Wert</span><span class="sxs-lookup"><span data-stu-id="7caca-112">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="7caca-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7caca-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <span data-ttu-id="7caca-114"><dt>**Wmsz \_ Unten**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-114"><dt>**WMSZ\_BOTTOM**</dt> <dt>6</dt></span></span> </dl>                | <span data-ttu-id="7caca-115">Unterer Rand</span><span class="sxs-lookup"><span data-stu-id="7caca-115">Bottom edge</span></span><br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <span data-ttu-id="7caca-116"><dt>**Wmsz \_ BottomLeft**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-116"><dt>**WMSZ\_BOTTOMLEFT**</dt> <dt>7</dt></span></span> </dl>    | <span data-ttu-id="7caca-117">Unten links</span><span class="sxs-lookup"><span data-stu-id="7caca-117">Bottom-left corner</span></span><br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <span data-ttu-id="7caca-118"><dt>**Wmsz \_ BottomRight**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-118"><dt>**WMSZ\_BOTTOMRIGHT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="7caca-119">Unten rechts</span><span class="sxs-lookup"><span data-stu-id="7caca-119">Bottom-right corner</span></span><br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <span data-ttu-id="7caca-120"><dt>**Wmsz \_ Links**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-120"><dt>**WMSZ\_LEFT**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="7caca-121">Linker Rand</span><span class="sxs-lookup"><span data-stu-id="7caca-121">Left edge</span></span><br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <span data-ttu-id="7caca-122"><dt>**Wmsz \_ Rechts**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-122"><dt>**WMSZ\_RIGHT**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="7caca-123">Rechter Rand</span><span class="sxs-lookup"><span data-stu-id="7caca-123">Right edge</span></span><br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <span data-ttu-id="7caca-124"><dt>**Wmsz \_ Top**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-124"><dt>**WMSZ\_TOP**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="7caca-125">Oberer Rand</span><span class="sxs-lookup"><span data-stu-id="7caca-125">Top edge</span></span><br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <span data-ttu-id="7caca-126"><dt>**Wmsz \_ TopLeft**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-126"><dt>**WMSZ\_TOPLEFT**</dt> <dt>4</dt></span></span> </dl>             | <span data-ttu-id="7caca-127">Linke obere Ecke</span><span class="sxs-lookup"><span data-stu-id="7caca-127">Top-left corner</span></span><br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <span data-ttu-id="7caca-128"><dt>**Wmsz \_ TopRight**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-128"><dt>**WMSZ\_TOPRIGHT**</dt> <dt>5</dt></span></span> </dl>          | <span data-ttu-id="7caca-129">Obere rechte Ecke</span><span class="sxs-lookup"><span data-stu-id="7caca-129">Top-right corner</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="7caca-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7caca-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7caca-131">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur mit den Bildschirm Koordinaten des Zieh Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="7caca-131">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the screen coordinates of the drag rectangle.</span></span> <span data-ttu-id="7caca-132">Um die Größe oder Position des Zieh Rechtecks zu ändern, muss eine Anwendung die Elemente dieser Struktur ändern.</span><span class="sxs-lookup"><span data-stu-id="7caca-132">To change the size or position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7caca-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7caca-133">Return value</span></span>

<span data-ttu-id="7caca-134">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7caca-134">Type: **LRESULT**</span></span>

<span data-ttu-id="7caca-135">Eine Anwendung sollte **true** zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7caca-135">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7caca-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7caca-136">Requirements</span></span>



| <span data-ttu-id="7caca-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7caca-137">Requirement</span></span> | <span data-ttu-id="7caca-138">Wert</span><span class="sxs-lookup"><span data-stu-id="7caca-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7caca-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7caca-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7caca-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7caca-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7caca-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7caca-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7caca-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7caca-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7caca-143">Header</span><span class="sxs-lookup"><span data-stu-id="7caca-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7caca-144"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7caca-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7caca-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="7caca-146">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7caca-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7caca-147">**WM- \_ Bewegung**</span><span class="sxs-lookup"><span data-stu-id="7caca-147">**WM\_MOVING**</span></span>](wm-moving.md)
</dt> <dt>

[<span data-ttu-id="7caca-148">**WM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="7caca-148">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

<span data-ttu-id="7caca-149">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7caca-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7caca-150">Windows</span><span class="sxs-lookup"><span data-stu-id="7caca-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="7caca-151">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="7caca-151">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="7caca-152">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7caca-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
