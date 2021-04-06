---
title: WM_CHANGEUISTATE Meldung (Winuser. h)
description: Eine Anwendung sendet die WM \_ changeuistate-Nachricht, um anzugeben, dass der Benutzeroberflächen Zustand geändert werden soll.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743584"
---
# <a name="wm_changeuistate-message"></a><span data-ttu-id="b6e07-104">WM \_ changeuistate-Meldung</span><span class="sxs-lookup"><span data-stu-id="b6e07-104">WM\_CHANGEUISTATE message</span></span>

<span data-ttu-id="b6e07-105">Eine Anwendung sendet die **WM \_ changeuistate** -Nachricht, um anzugeben, dass der Benutzeroberflächen Zustand geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6e07-105">An application sends the **WM\_CHANGEUISTATE** message to indicate that the UI state should be changed.</span></span>


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a><span data-ttu-id="b6e07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6e07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6e07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e07-108">Das nieder wertige Wort gibt die Aktion an, die durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6e07-108">The low-order word specifies the action to be taken.</span></span> <span data-ttu-id="b6e07-109">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b6e07-109">This member can be one of the following values.</span></span>



| <span data-ttu-id="b6e07-110">Wert</span><span class="sxs-lookup"><span data-stu-id="b6e07-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="b6e07-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6e07-111">Meaning</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="b6e07-112"><dt>**UIs \_ Löschen**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b6e07-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="b6e07-113">Die vom höherwertigen Wort angegebenen benutzeroberflächenstatusflags sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b6e07-113">The UI state flags specified by the high-order word should be cleared.</span></span><br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="b6e07-114"><dt>**UIs \_ Initialisieren**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b6e07-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="b6e07-115">Die vom höherwertigen Wort angegebenen benutzeroberflächenstatusflags sollten basierend auf dem letzten Eingabe Ereignis geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b6e07-115">The UI state flags specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="b6e07-116">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="b6e07-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="b6e07-117"><dt>**UIs \_**</dt> <dt>1</dt> festlegen</span><span class="sxs-lookup"><span data-stu-id="b6e07-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="b6e07-118">Die vom höherwertigen Wort angegebenen benutzeroberflächenstatusflags müssen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b6e07-118">The UI state flags specified by the high-order word should be set.</span></span><br/>                                                                      |



 

<span data-ttu-id="b6e07-119">Das hochwertige Wort gibt an, welche Benutzeroberflächen-Zustands Elemente betroffen sind, oder die Art des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="b6e07-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="b6e07-120">Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b6e07-120">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="b6e07-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b6e07-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="b6e07-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6e07-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="b6e07-123"><dt>**Uisf \_ Aktiv**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="b6e07-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="b6e07-124">Ein Steuerelement sollte in dem Format gezeichnet werden, das für aktive Steuerelemente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6e07-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="b6e07-125"><dt>**Uisf \_ Hideaccel**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="b6e07-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="b6e07-126">Tastaturbeschleuniger werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="b6e07-126">Keyboard accelerators are hidden.</span></span><br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="b6e07-127"><dt>**Uisf \_ Hidefocus**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="b6e07-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="b6e07-128">Fokus Indikatoren werden ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="b6e07-128">Focus indicators are hidden.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="b6e07-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6e07-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6e07-130">Dieser Parameter wird nicht verwendet und muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="b6e07-130">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6e07-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6e07-131">Remarks</span></span>

<span data-ttu-id="b6e07-132">Diese Nachricht sollte von einem Fenster an sich selbst oder über das übergeordnete Fenster gesendet werden, wenn die Benutzeroberflächen-Zustands Elemente aller Fenster in derselben Hierarchie geändert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b6e07-132">A window should send this message to itself or its parent when it must change the UI state elements of all windows in the same hierarchy.</span></span> <span data-ttu-id="b6e07-133">Die Fenster Prozedur muss die Verarbeitung dieser Nachricht durch [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) zulassen, damit die gesamte Fenster Struktur einen konsistenten Benutzeroberflächen Zustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="b6e07-133">The window procedure must let [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) process this message so that the entire window tree has a consistent UI state.</span></span> <span data-ttu-id="b6e07-134">Wenn das Fenster der obersten Ebene die **WM \_ changeuistate** -Nachricht empfängt, sendet es eine [**WM- \_ updateuistate**](wm-updateuistate.md) -Nachricht mit denselben Parametern an alle untergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="b6e07-134">When the top-level window receives the **WM\_CHANGEUISTATE** message, it sends a [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with the same parameters to all child windows.</span></span> <span data-ttu-id="b6e07-135">Wenn das System die **WM- \_ updateuistate** -Nachricht verarbeitet, wird die Änderung im Zustand der Benutzeroberfläche vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="b6e07-135">When the system processes the **WM\_UPDATEUISTATE** message, it makes the change in the UI state.</span></span>

<span data-ttu-id="b6e07-136">Wenn das nieder wertige Wort von *wParam* "UIs \_ Initialize" lautet, sendet das System die [**WM- \_ updateuistate**](wm-updateuistate.md) -Nachricht mit einem UI-Status, der auf dem letzten Eingabe Ereignis basiert.</span><span class="sxs-lookup"><span data-stu-id="b6e07-136">If the low-order word of *wParam* is UIS\_INITIALIZE, the system will send the [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with a UI state based on the last input event.</span></span> <span data-ttu-id="b6e07-137">Wenn z. b. die letzte Eingabe von der Maus stammt, werden die Tastatur-Cues vom System ausgeblendet. Und wenn die letzte Eingabe von der Tastatur stammt, zeigt das System die Tastatur Hinweise an. Wenn der Status, der sich aus der Verarbeitung von **WM \_ changeuistate** ergibt, mit dem alten Zustand identisch ist, wird diese Meldung von [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="b6e07-137">For example, if the last input came from the mouse, the system will hide the keyboard cues. And, if the last input came from the keyboard, the system will show the keyboard cues. If the state that results from processing **WM\_CHANGEUISTATE** is the same as the old state, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not send this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e07-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6e07-138">Requirements</span></span>



| <span data-ttu-id="b6e07-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6e07-139">Requirement</span></span> | <span data-ttu-id="b6e07-140">Wert</span><span class="sxs-lookup"><span data-stu-id="b6e07-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e07-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6e07-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e07-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6e07-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b6e07-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6e07-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e07-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6e07-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6e07-145">Header</span><span class="sxs-lookup"><span data-stu-id="b6e07-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6e07-146"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b6e07-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6e07-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6e07-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6e07-148">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b6e07-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="b6e07-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6e07-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b6e07-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6e07-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b6e07-151">**WM \_ queryuistate**</span><span class="sxs-lookup"><span data-stu-id="b6e07-151">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="b6e07-152">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b6e07-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b6e07-153">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="b6e07-153">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

