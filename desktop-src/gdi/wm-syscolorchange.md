---
description: Die WM- \_ syscolorchange-Meldung wird an alle Fenster der obersten Ebene gesendet, wenn eine Änderung an einer System Farbeinstellung vorgenommen wird.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: WM_SYSCOLORCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980792"
---
# <a name="wm_syscolorchange-message"></a><span data-ttu-id="f7e38-103">WM- \_ syscolorchange-Meldung</span><span class="sxs-lookup"><span data-stu-id="f7e38-103">WM\_SYSCOLORCHANGE message</span></span>

<span data-ttu-id="f7e38-104">Die **WM- \_ syscolorchange** -Meldung wird an alle Fenster der obersten Ebene gesendet, wenn eine Änderung an einer System Farbeinstellung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="f7e38-104">The **WM\_SYSCOLORCHANGE** message is sent to all top-level windows when a change is made to a system color setting.</span></span>

<span data-ttu-id="f7e38-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f7e38-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="f7e38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7e38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7e38-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7e38-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7e38-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7e38-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f7e38-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7e38-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7e38-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7e38-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7e38-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7e38-111">Remarks</span></span>

<span data-ttu-id="f7e38-112">Das System sendet eine [**WM \_**](wm-paint.md) -Zeichnungs Meldung an jedes Fenster, das von einer System Farbänderung betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="f7e38-112">The system sends a [**WM\_PAINT**](wm-paint.md) message to any window that is affected by a system color change.</span></span>

<span data-ttu-id="f7e38-113">Anwendungen mit Pinseln, die die vorhandenen Systemfarben verwenden, sollten diese Pinsel löschen und mithilfe der neuen Systemfarben neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7e38-113">Applications that have brushes using the existing system colors should delete those brushes and re-create them using the new system colors.</span></span>

<span data-ttu-id="f7e38-114">Fenster der obersten Ebene, die allgemeine Steuerelemente verwenden, müssen die **WM- \_ syscolorchange** -Meldung an die Steuerelemente weiterleiten. andernfalls werden die Steuerelemente nicht über die Farbänderung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="f7e38-114">Top level windows that use common controls must forward the **WM\_SYSCOLORCHANGE** message to the controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="f7e38-115">Dadurch wird sichergestellt, dass die von den allgemeinen Steuerelementen verwendeten Farben mit den Farben übereinstimmen, die von anderen Benutzeroberflächen Objekten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7e38-115">This ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="f7e38-116">Beispielsweise verwendet ein ToolBar-Steuerelement die Farbe "3D-Objekte", um seine Schaltflächen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="f7e38-116">For example, a toolbar control uses the "3D Objects" color to draw its buttons.</span></span> <span data-ttu-id="f7e38-117">Wenn der Benutzer die 3D-Objekt Farbe ändert, aber die **WM- \_ syscolorchange** -Meldung nicht an die Symbolleiste weitergeleitet wird, bleiben die Schaltflächen der Symbolleiste in der ursprünglichen Farbe, während sich die Farbe anderer Schaltflächen im System ändert.</span><span class="sxs-lookup"><span data-stu-id="f7e38-117">If the user changes the 3D Objects color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color while the color of other buttons in the system changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e38-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f7e38-118">Requirements</span></span>



| <span data-ttu-id="f7e38-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7e38-119">Requirement</span></span> | <span data-ttu-id="f7e38-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f7e38-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e38-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7e38-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e38-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7e38-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f7e38-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7e38-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e38-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7e38-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f7e38-125">Header</span><span class="sxs-lookup"><span data-stu-id="f7e38-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7e38-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f7e38-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7e38-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f7e38-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e38-128">Übersicht über Farben</span><span class="sxs-lookup"><span data-stu-id="f7e38-128">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="f7e38-129">Farb Meldungen</span><span class="sxs-lookup"><span data-stu-id="f7e38-129">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="f7e38-130">**WM- \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="f7e38-130">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
