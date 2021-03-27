---
description: Die WM \_ paletteischanging-Nachricht informiert Anwendungen darüber, dass eine Anwendung ihre logische Palette erkennen wird.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: WM_PALETTEISCHANGING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757878"
---
# <a name="wm_paletteischanging-message"></a><span data-ttu-id="390b0-103">WM \_ paletteischanging-Meldung</span><span class="sxs-lookup"><span data-stu-id="390b0-103">WM\_PALETTEISCHANGING message</span></span>

<span data-ttu-id="390b0-104">Die **WM \_ paletteischanging** -Nachricht informiert Anwendungen darüber, dass eine Anwendung ihre logische Palette erkennen wird.</span><span class="sxs-lookup"><span data-stu-id="390b0-104">The **WM\_PALETTEISCHANGING** message informs applications that an application is going to realize its logical palette.</span></span>

<span data-ttu-id="390b0-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="390b0-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="390b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="390b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="390b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="390b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="390b0-108">Ein Handle für das Fenster, in dem die logische Palette erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="390b0-108">A handle to the window that is going to realize its logical palette.</span></span>

</dd> <dt>

<span data-ttu-id="390b0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="390b0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="390b0-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="390b0-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="390b0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="390b0-111">Return value</span></span>

<span data-ttu-id="390b0-112">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="390b0-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="390b0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="390b0-113">Remarks</span></span>

<span data-ttu-id="390b0-114">Die Anwendung, die die Palette ändert, wartet nicht auf die Bestätigung dieser Nachricht, bevor die Palette geändert und die [**WM \_ palettechanged**](wm-palettechanged.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="390b0-114">The application changing its palette does not wait for acknowledgment of this message before changing the palette and sending the [**WM\_PALETTECHANGED**](wm-palettechanged.md) message.</span></span> <span data-ttu-id="390b0-115">Folglich wird die Palette möglicherweise bereits geändert, wenn eine Anwendung diese Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="390b0-115">As a result, the palette may already be changed by the time an application receives this message.</span></span>

<span data-ttu-id="390b0-116">Wenn die Anwendung diese Nachricht ignoriert oder nicht verarbeitet, und eine zweite Anwendung ihre Palette erkennt, während die erste Palette-Indizes verwendet, besteht die Möglichkeit, dass der Benutzer bei nachfolgenden Zeichnungs Vorgängen unerwartete Farben erkennt.</span><span class="sxs-lookup"><span data-stu-id="390b0-116">If the application either ignores or fails to process this message and a second application realizes its palette while the first is using palette indexes, there is a strong possibility that the user will see unexpected colors during subsequent drawing operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="390b0-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="390b0-117">Requirements</span></span>



| <span data-ttu-id="390b0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="390b0-118">Requirement</span></span> | <span data-ttu-id="390b0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="390b0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="390b0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="390b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="390b0-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="390b0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="390b0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="390b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="390b0-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="390b0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="390b0-124">Header</span><span class="sxs-lookup"><span data-stu-id="390b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="390b0-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="390b0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="390b0-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="390b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390b0-127">Übersicht über Farben</span><span class="sxs-lookup"><span data-stu-id="390b0-127">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="390b0-128">Farb Meldungen</span><span class="sxs-lookup"><span data-stu-id="390b0-128">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="390b0-129">**WM \_ palettechanged**</span><span class="sxs-lookup"><span data-stu-id="390b0-129">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="390b0-130">**WM \_ querynewpalette**</span><span class="sxs-lookup"><span data-stu-id="390b0-130">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
