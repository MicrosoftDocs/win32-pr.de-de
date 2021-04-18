---
description: Eine Anwendung sendet die WM- \_ mdisetmenu-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das gesamte Menü eines MDI-Rahmen Fensters zu ersetzen, um das Fenstermenü des Rahmen Fensters oder beides zu ersetzen.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: WM_MDISETMENU Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368756"
---
# <a name="wm_mdisetmenu-message"></a><span data-ttu-id="95378-103">WM- \_ mdisetmenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="95378-103">WM\_MDISETMENU message</span></span>

<span data-ttu-id="95378-104">Eine Anwendung sendet die **WM- \_ mdisetmenu** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das gesamte Menü eines MDI-Rahmen Fensters zu ersetzen, um das Fenstermenü des Rahmen Fensters oder beides zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="95378-104">An application sends the **WM\_MDISETMENU** message to a multiple-document interface (MDI) client window to replace the entire menu of an MDI frame window, to replace the window menu of the frame window, or both.</span></span>


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a><span data-ttu-id="95378-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="95378-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95378-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95378-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95378-107">Ein Handle für das neue Rahmen Fenstermenü.</span><span class="sxs-lookup"><span data-stu-id="95378-107">A handle to the new frame window menu.</span></span> <span data-ttu-id="95378-108">Wenn dieser Parameter **null** ist, wird das Menü Rahmen Fenster nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="95378-108">If this parameter is **NULL**, the frame window menu is not changed.</span></span>

</dd> <dt>

<span data-ttu-id="95378-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95378-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95378-110">Ein Handle für das neue Fenstermenü.</span><span class="sxs-lookup"><span data-stu-id="95378-110">A handle to the new window menu.</span></span> <span data-ttu-id="95378-111">Wenn dieser Parameter **null** ist, wird das Menü Fenster nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="95378-111">If this parameter is **NULL**, the window menu is not changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95378-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95378-112">Return value</span></span>

<span data-ttu-id="95378-113">Typ: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="95378-113">Type: **HMENU**</span></span>

<span data-ttu-id="95378-114">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert das Handle für das alte Rahmen Fenstermenü.</span><span class="sxs-lookup"><span data-stu-id="95378-114">If the message succeeds, the return value is the handle to the old frame window menu.</span></span>

<span data-ttu-id="95378-115">Wenn die Meldung fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="95378-115">If the message fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="95378-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95378-116">Remarks</span></span>

<span data-ttu-id="95378-117">Nach dem Senden dieser Nachricht muss eine Anwendung die [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) -Funktion zum Aktualisieren der Menüleiste aufruft.</span><span class="sxs-lookup"><span data-stu-id="95378-117">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

<span data-ttu-id="95378-118">Wenn diese Meldung das Fenstermenü ersetzt, werden die Menü Elemente des untergeordneten MDI-Fensters aus dem vorherigen Fenstermenü entfernt und dem Menü neues Fenster hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="95378-118">If this message replaces the window menu, the MDI child window menu items are removed from the previous window menu and added to the new window menu.</span></span>

<span data-ttu-id="95378-119">Wenn ein untergeordnetes MDI-Fenster maximiert ist und diese Meldung das MDI-Frame Fenster-Menü ersetzt, werden das Fenstermenü Symbol und das Wiederherstellungs Symbol aus dem vorherigen Menü Fenster des Frames entfernt und dem Menü neues Rahmen Fenster hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="95378-119">If an MDI child window is maximized and this message replaces the MDI frame window menu, the window menu icon and restore icon are removed from the previous frame window menu and added to the new frame window menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="95378-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95378-120">Requirements</span></span>



| <span data-ttu-id="95378-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95378-121">Requirement</span></span> | <span data-ttu-id="95378-122">Wert</span><span class="sxs-lookup"><span data-stu-id="95378-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95378-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95378-123">Minimum supported client</span></span><br/> | <span data-ttu-id="95378-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95378-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="95378-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95378-125">Minimum supported server</span></span><br/> | <span data-ttu-id="95378-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95378-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95378-127">Header</span><span class="sxs-lookup"><span data-stu-id="95378-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="95378-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="95378-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95378-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95378-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="95378-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="95378-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="95378-131">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="95378-131">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="95378-132">**WM- \_ mumgeleitet-freshmenu**</span><span class="sxs-lookup"><span data-stu-id="95378-132">**WM\_MDIREFRESHMENU**</span></span>](wm-mdirefreshmenu.md)
</dt> <dt>

<span data-ttu-id="95378-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="95378-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="95378-134">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="95378-134">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
