---
description: Die WM- \_ Abfrage "querynewpalette" informiert ein Fenster darüber, dass es im Begriff ist, den Tastaturfokus zu erhalten, sodass das Fenster seine logische Palette erkennen kann, wenn es den Fokus erhält.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: WM_QUERYNEWPALETTE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979353"
---
# <a name="wm_querynewpalette-message"></a><span data-ttu-id="038f1-103">WM \_ querynewpalette-Meldung</span><span class="sxs-lookup"><span data-stu-id="038f1-103">WM\_QUERYNEWPALETTE message</span></span>

<span data-ttu-id="038f1-104">Die **WM- \_ Abfrage "querynewpalette** " informiert ein Fenster darüber, dass es im Begriff ist, den Tastaturfokus zu erhalten, sodass das Fenster seine logische Palette erkennen kann, wenn es den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="038f1-104">The **WM\_QUERYNEWPALETTE** message informs a window that it is about to receive the keyboard focus, giving the window the opportunity to realize its logical palette when it receives the focus.</span></span>

<span data-ttu-id="038f1-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="038f1-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="038f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="038f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="038f1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="038f1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="038f1-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="038f1-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="038f1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="038f1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="038f1-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="038f1-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="038f1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="038f1-111">Return value</span></span>

<span data-ttu-id="038f1-112">Wenn das Fenster seine logische Palette erkennt, muss es **true** zurückgeben. Andernfalls muss Sie **false** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="038f1-112">If the window realizes its logical palette, it must return **TRUE**; otherwise, it must return **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="038f1-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="038f1-113">Requirements</span></span>



| <span data-ttu-id="038f1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="038f1-114">Requirement</span></span> | <span data-ttu-id="038f1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="038f1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="038f1-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="038f1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="038f1-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="038f1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="038f1-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="038f1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="038f1-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="038f1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="038f1-120">Header</span><span class="sxs-lookup"><span data-stu-id="038f1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="038f1-121"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="038f1-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="038f1-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="038f1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038f1-123">Übersicht über Farben</span><span class="sxs-lookup"><span data-stu-id="038f1-123">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="038f1-124">Farb Meldungen</span><span class="sxs-lookup"><span data-stu-id="038f1-124">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="038f1-125">**WM \_ palettechanged**</span><span class="sxs-lookup"><span data-stu-id="038f1-125">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="038f1-126">**WM- \_ paletteischanging**</span><span class="sxs-lookup"><span data-stu-id="038f1-126">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> </dl>

 

 
