---
description: Die Meldung "WM \_ Display Change" wird an alle Fenster gesendet, wenn sich die Bildschirmauflösung geändert hat.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: WM_DISPLAYCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215642"
---
# <a name="wm_displaychange-message"></a><span data-ttu-id="38d05-103">WM \_ Display Change-Meldung</span><span class="sxs-lookup"><span data-stu-id="38d05-103">WM\_DISPLAYCHANGE message</span></span>

<span data-ttu-id="38d05-104">Die Meldung " **WM \_ Display Change** " wird an alle Fenster gesendet, wenn sich die Bildschirmauflösung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="38d05-104">The **WM\_DISPLAYCHANGE** message is sent to all windows when the display resolution has changed.</span></span>

<span data-ttu-id="38d05-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="38d05-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="38d05-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38d05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d05-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38d05-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38d05-108">Die neue Bildtiefe der Anzeige in Bits pro Pixel.</span><span class="sxs-lookup"><span data-stu-id="38d05-108">The new image depth of the display, in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="38d05-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38d05-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38d05-110">Das nieder wertige Wort gibt die horizontale Auflösung des Bildschirms an.</span><span class="sxs-lookup"><span data-stu-id="38d05-110">The low-order word specifies the horizontal resolution of the screen.</span></span>

<span data-ttu-id="38d05-111">Das höchst wertige Wort gibt die vertikale Auflösung des Bildschirms an.</span><span class="sxs-lookup"><span data-stu-id="38d05-111">The high-order word specifies the vertical resolution of the screen.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38d05-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38d05-112">Remarks</span></span>

<span data-ttu-id="38d05-113">Diese Meldung wird nur an Fenster der obersten Ebene gesendet.</span><span class="sxs-lookup"><span data-stu-id="38d05-113">This message is only sent to top-level windows.</span></span> <span data-ttu-id="38d05-114">Für alle anderen Fenster wird Sie gepostet.</span><span class="sxs-lookup"><span data-stu-id="38d05-114">For all other windows it is posted.</span></span>

## <a name="requirements"></a><span data-ttu-id="38d05-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="38d05-115">Requirements</span></span>



| <span data-ttu-id="38d05-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38d05-116">Requirement</span></span> | <span data-ttu-id="38d05-117">Wert</span><span class="sxs-lookup"><span data-stu-id="38d05-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38d05-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38d05-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38d05-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38d05-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38d05-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38d05-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38d05-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38d05-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38d05-122">Header</span><span class="sxs-lookup"><span data-stu-id="38d05-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="38d05-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="38d05-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d05-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="38d05-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d05-125">Übersicht über das Zeichnen und zeichnen</span><span class="sxs-lookup"><span data-stu-id="38d05-125">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="38d05-126">Zeichnen und Zeichnen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="38d05-126">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

<span data-ttu-id="38d05-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38d05-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="38d05-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38d05-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

 
