---
title: WM_UPDATEUISTATE Meldung (Winuser. h)
description: Eine Anwendung sendet die WM \_ -updateuistate-Meldung, um den Benutzeroberflächen Status für das angegebene Fenster und alle untergeordneten Fenster zu ändern.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106454"
---
# <a name="wm_updateuistate-message"></a><span data-ttu-id="8b17d-104">WM \_ updateuistate-Meldung</span><span class="sxs-lookup"><span data-stu-id="8b17d-104">WM\_UPDATEUISTATE message</span></span>

<span data-ttu-id="8b17d-105">Eine Anwendung sendet die **WM- \_ updateuistate** -Meldung, um den Benutzeroberflächen Status für das angegebene Fenster und alle untergeordneten Fenster zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8b17d-105">An application sends the **WM\_UPDATEUISTATE** message to change the UI state for the specified window and all its child windows.</span></span>


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a><span data-ttu-id="8b17d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b17d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b17d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b17d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b17d-108">Das nieder wertige Wort gibt die Aktion an, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b17d-108">The low-order word specifies the action to be performed.</span></span> <span data-ttu-id="8b17d-109">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="8b17d-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8b17d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8b17d-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="8b17d-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8b17d-111">Meaning</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="8b17d-112"><dt>**UIs \_ Löschen**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8b17d-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="8b17d-113">Das Benutzeroberflächen-Zustands Element, das durch das hochwertige Wort angegeben wird, sollte ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b17d-113">The UI state element specified by the high-order word should be hidden.</span></span><br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="8b17d-114"><dt>**UIs \_ Initialisieren**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8b17d-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="8b17d-115">Das Benutzeroberflächen-Zustands Element, das durch das hochwertige Wort angegeben wird, sollte basierend auf dem letzten Eingabe Ereignis geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8b17d-115">The UI state element specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="8b17d-116">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="8b17d-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="8b17d-117"><dt>**UIs \_**</dt> <dt>1</dt> festlegen</span><span class="sxs-lookup"><span data-stu-id="8b17d-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="8b17d-118">Das Benutzeroberflächen-Zustands Element, das durch das hochwertige Wort angegeben wird, sollte sichtbar sein.</span><span class="sxs-lookup"><span data-stu-id="8b17d-118">The UI state element specified by the high-order word should be visible.</span></span><br/>                                                                  |



 

<span data-ttu-id="8b17d-119">Das hochwertige Wort gibt an, welche Benutzeroberflächen-Zustands Elemente betroffen sind, oder die Art des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="8b17d-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="8b17d-120">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8b17d-120">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8b17d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8b17d-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="8b17d-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8b17d-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="8b17d-123"><dt>**Uisf \_ Aktiv**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="8b17d-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="8b17d-124">Ein Steuerelement sollte in dem Format gezeichnet werden, das für aktive Steuerelemente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b17d-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="8b17d-125"><dt>**Uisf \_ Hideaccel**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="8b17d-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="8b17d-126">Tastaturbeschleuniger.</span><span class="sxs-lookup"><span data-stu-id="8b17d-126">Keyboard accelerators.</span></span><br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="8b17d-127"><dt>**Uisf \_ Hidefocus**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="8b17d-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="8b17d-128">Fokus Indikatoren.</span><span class="sxs-lookup"><span data-stu-id="8b17d-128">Focus indicators.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="8b17d-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b17d-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b17d-130">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b17d-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b17d-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b17d-131">Remarks</span></span>

<span data-ttu-id="8b17d-132">Diese Meldung sollte von einem Fenster gesendet werden, um den Benutzeroberflächen Status aller untergeordneten Fenster zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8b17d-132">A window should send this message to change the UI state of all its child windows.</span></span> <span data-ttu-id="8b17d-133">Im Gegensatz zur " [**WM \_ changeuistate**](wm-changeuistate.md) "-Meldung, bei der es sich um eine Benachrichtigung handelt, wird der Benutzeroberflächen Zustand geändert, wenn [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die " **WM \_ updateuistate** "-Meldung verarbeitet und die Änderungen an alle untergeordneten Fenster weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="8b17d-133">In contrast to the [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message, which is a notification, when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processes the **WM\_UPDATEUISTATE** message it changes the UI state and propagates the changes to all child windows.</span></span>

<span data-ttu-id="8b17d-134">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion aktualisiert den UI-Status gemäß dem *wParam* -Wert.</span><span class="sxs-lookup"><span data-stu-id="8b17d-134">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function updates the UI state according to the *wParam* value.</span></span> <span data-ttu-id="8b17d-135">Wenn der Zustand der Benutzeroberfläche geändert wird, sendet die Funktion die Nachricht an alle unmittelbaren untergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="8b17d-135">If the UI state is modified, the function sends the message to all the immediate child windows.</span></span> <span data-ttu-id="8b17d-136">**Defwindowproc** sendet diese Nachricht auch dann, wenn Sie eine [**WM \_ changeuistate**](wm-changeuistate.md) -Meldung empfängt, in der das System darüber benachrichtigt wird, dass ein untergeordnetes Fenster den Benutzeroberflächen Zustand ändern soll.</span><span class="sxs-lookup"><span data-stu-id="8b17d-136">**DefWindowProc** also sends this message when it receives a [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message notifying the system that a child window intends to modify the UI state.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b17d-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b17d-137">Requirements</span></span>



| <span data-ttu-id="8b17d-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b17d-138">Requirement</span></span> | <span data-ttu-id="8b17d-139">Wert</span><span class="sxs-lookup"><span data-stu-id="8b17d-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b17d-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b17d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8b17d-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b17d-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8b17d-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b17d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8b17d-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b17d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b17d-144">Header</span><span class="sxs-lookup"><span data-stu-id="8b17d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b17d-145"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8b17d-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b17d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b17d-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b17d-147">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8b17d-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8b17d-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="8b17d-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="8b17d-149">**WM \_ changeuistate**</span><span class="sxs-lookup"><span data-stu-id="8b17d-149">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="8b17d-150">**WM \_ queryuistate**</span><span class="sxs-lookup"><span data-stu-id="8b17d-150">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="8b17d-151">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8b17d-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8b17d-152">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="8b17d-152">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

