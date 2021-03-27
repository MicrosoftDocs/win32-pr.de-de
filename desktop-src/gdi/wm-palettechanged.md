---
description: Die "WM \_ palettechanged"-Meldung wird an alle Fenster der obersten Ebene und überlappende Fenster gesendet, nachdem das Fenster mit dem Tastaturfokus seine logische Palette erreicht hat und dadurch die Systempalette geändert wurde.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: WM_PALETTECHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755824"
---
# <a name="wm_palettechanged-message"></a><span data-ttu-id="05905-103">WM \_ palettechanged-Meldung</span><span class="sxs-lookup"><span data-stu-id="05905-103">WM\_PALETTECHANGED message</span></span>

<span data-ttu-id="05905-104">Die " **WM \_ palettechanged** "-Meldung wird an alle Fenster der obersten Ebene und überlappende Fenster gesendet, nachdem das Fenster mit dem Tastaturfokus seine logische Palette erreicht hat und dadurch die Systempalette geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="05905-104">The **WM\_PALETTECHANGED** message is sent to all top-level and overlapped windows after the window with the keyboard focus has realized its logical palette, thereby changing the system palette.</span></span> <span data-ttu-id="05905-105">Diese Meldung ermöglicht ein Fenster, das eine Farbpalette verwendet, aber nicht den Tastaturfokus hat, um seine logische Palette zu erkennen und den Client Bereich zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="05905-105">This message enables a window that uses a color palette but does not have the keyboard focus to realize its logical palette and update its client area.</span></span>

<span data-ttu-id="05905-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="05905-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="05905-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="05905-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05905-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05905-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05905-109">Ein Handle für das Fenster, das bewirkt hat, dass die Systempalette geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="05905-109">A handle to the window that caused the system palette to change.</span></span>

</dd> <dt>

<span data-ttu-id="05905-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05905-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05905-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="05905-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05905-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05905-112">Remarks</span></span>

<span data-ttu-id="05905-113">Diese Nachricht muss an alle Fenster der obersten Ebene und überlappende Fenster gesendet werden, einschließlich derjenigen, die die Systempalette geändert hat.</span><span class="sxs-lookup"><span data-stu-id="05905-113">This message must be sent to all top-level and overlapped windows, including the one that changed the system palette.</span></span> <span data-ttu-id="05905-114">Wenn ein untergeordnetes Fenster eine Farbpalette verwendet, muss diese Meldung ebenfalls an Sie weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="05905-114">If any child windows use a color palette, this message must be passed on to them as well.</span></span>

<span data-ttu-id="05905-115">Um das Erstellen einer Endlosschleife zu vermeiden, darf ein Fenster, das diese Nachricht empfängt, seine Palette nicht erkennen, es sei denn, es wird festgelegt, dass *wParam* kein eigenes Fenster Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="05905-115">To avoid creating an infinite loop, a window that receives this message must not realize its palette, unless it determines that *wParam* does not contain its own window handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="05905-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="05905-116">Requirements</span></span>



| <span data-ttu-id="05905-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05905-117">Requirement</span></span> | <span data-ttu-id="05905-118">Wert</span><span class="sxs-lookup"><span data-stu-id="05905-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05905-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05905-119">Minimum supported client</span></span><br/> | <span data-ttu-id="05905-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05905-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="05905-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05905-121">Minimum supported server</span></span><br/> | <span data-ttu-id="05905-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05905-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05905-123">Header</span><span class="sxs-lookup"><span data-stu-id="05905-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="05905-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="05905-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05905-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="05905-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05905-126">Übersicht über Farben</span><span class="sxs-lookup"><span data-stu-id="05905-126">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="05905-127">Farb Meldungen</span><span class="sxs-lookup"><span data-stu-id="05905-127">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="05905-128">**WM- \_ paletteischanging**</span><span class="sxs-lookup"><span data-stu-id="05905-128">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> <dt>

[<span data-ttu-id="05905-129">**WM \_ querynewpalette**</span><span class="sxs-lookup"><span data-stu-id="05905-129">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
