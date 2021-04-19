---
description: Wird an das Fenster mit dem Fokus gesendet, wenn der Benutzer eine neue Eingabe Sprache auswählt, entweder mit dem Hotkey (angegeben in der System Steuerungsanwendung der Tastatur) oder über den Indikator auf der Taskleiste des Systems.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: WM_INPUTLANGCHANGEREQUEST Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348619"
---
# <a name="wm_inputlangchangerequest-message"></a><span data-ttu-id="1b8c7-103">WM- \_ inputlangchangerequest-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1b8c7-103">WM\_INPUTLANGCHANGEREQUEST message</span></span>

<span data-ttu-id="1b8c7-104">Wird an das Fenster mit dem Fokus gesendet, wenn der Benutzer eine neue Eingabe Sprache auswählt, entweder mit dem Hotkey (angegeben in der System Steuerungsanwendung der Tastatur) oder über den Indikator auf der Taskleiste des Systems.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-104">Posted to the window with the focus when the user chooses a new input language, either with the hotkey (specified in the Keyboard control panel application) or from the indicator on the system taskbar.</span></span> <span data-ttu-id="1b8c7-105">Eine Anwendung kann die Änderung akzeptieren, indem Sie die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt oder die Änderung ablehnt (und Sie nicht findet), indem Sie sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-105">An application can accept the change by passing the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function or reject the change (and prevent it from taking place) by returning immediately.</span></span>

<span data-ttu-id="1b8c7-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a><span data-ttu-id="1b8c7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b8c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b8c7-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b8c7-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b8c7-109">Das neue Eingabe Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-109">The new input locale.</span></span> <span data-ttu-id="1b8c7-110">Dieser Parameter kann eine Kombination der folgenden Flags sein.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-110">This parameter can be a combination of the following flags.</span></span>



| <span data-ttu-id="1b8c7-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1b8c7-111">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="1b8c7-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1b8c7-112">Meaning</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <span data-ttu-id="1b8c7-113"><dt>**Inputlangchange \_ Rückwärts**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="1b8c7-113"><dt>**INPUTLANGCHANGE\_BACKWARD**</dt> <dt>0x0004</dt></span></span> </dl>       | <span data-ttu-id="1b8c7-114">Eine "Hot Key" wurde verwendet, um das vorherige Eingabe Gebiets Schema in der installierten Liste der Eingabe Gebiets Schemata auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-114">A hot key was used to choose the previous input locale in the installed list of input locales.</span></span> <span data-ttu-id="1b8c7-115">Dieses Flag kann nicht mit dem inputlangchange- \_ Forward-Flag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-115">This flag cannot be used with the INPUTLANGCHANGE\_FORWARD flag.</span></span><br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <span data-ttu-id="1b8c7-116"><dt>**Inputlangchange \_ Weiterleiten**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="1b8c7-116"><dt>**INPUTLANGCHANGE\_FORWARD**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="1b8c7-117">Eine "Hot Key" wurde verwendet, um das nächste Eingabe Gebiets Schema in der installierten Liste der Eingabe Gebiets Schemata auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-117">A hot key was used to choose the next input locale in the installed list of input locales.</span></span> <span data-ttu-id="1b8c7-118">Dieses Flag kann nicht mit dem inputlangchange-abwärts Flag verwendet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="1b8c7-118">This flag cannot be used with the INPUTLANGCHANGE\_BACKWARD flag.</span></span><br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <span data-ttu-id="1b8c7-119"><dt>**Inputlangchange \_ Syscharset**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="1b8c7-119"><dt>**INPUTLANGCHANGE\_SYSCHARSET**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="1b8c7-120">Das Tastaturlayout des neuen Eingabe Gebiets Schemas kann mit dem System Zeichensatz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-120">The new input locale's keyboard layout can be used with the system character set.</span></span><br/>                                                                               |



 

</dd> <dt>

<span data-ttu-id="1b8c7-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b8c7-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b8c7-122">Der Eingabe Gebiets Schema Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-122">The input locale identifier.</span></span> <span data-ttu-id="1b8c7-123">Weitere Informationen finden Sie unter [Sprachen, Gebiets Schemas und Tastatur Layouts](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="1b8c7-123">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b8c7-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b8c7-124">Return value</span></span>

<span data-ttu-id="1b8c7-125">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-125">Type: **LRESULT**</span></span>

<span data-ttu-id="1b8c7-126">Diese Nachricht wird gesendet, nicht an die Anwendung gesendet, sodass der Rückgabewert ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-126">This message is posted, not sent, to the application, so the return value is ignored.</span></span> <span data-ttu-id="1b8c7-127">Um die Änderung zu übernehmen, sollte die Anwendung die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-127">To accept the change, the application should pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="1b8c7-128">Um die Änderung abzulehnen, sollte die Anwendung 0 (null) zurückgeben, ohne **defwindowproc** aufrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-128">To reject the change, the application should return zero without calling **DefWindowProc**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b8c7-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b8c7-129">Remarks</span></span>

<span data-ttu-id="1b8c7-130">Wenn die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die " **WM \_ inputlangchangerequest** "-Nachricht empfängt, aktiviert Sie das neue Eingabe Gebiets Schema und benachrichtigt die Anwendung über die Änderung, indem die " [**WM \_ inputlangchange**](wm-inputlangchange.md) "-Meldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-130">When the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function receives the **WM\_INPUTLANGCHANGEREQUEST** message, it activates the new input locale and notifies the application of the change by sending the [**WM\_INPUTLANGCHANGE**](wm-inputlangchange.md) message.</span></span>

<span data-ttu-id="1b8c7-131">Der Sprachindikator ist nur auf der Taskleiste vorhanden, wenn Sie mehr als ein Tastaturlayout installiert haben und Sie den Indikator mithilfe der System Steuerungsanwendung der Tastatur aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="1b8c7-131">The language indicator is present on the taskbar only if you have installed more than one keyboard layout and if you have enabled the indicator using the Keyboard control panel application.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8c7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b8c7-132">Requirements</span></span>



| <span data-ttu-id="1b8c7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b8c7-133">Requirement</span></span> | <span data-ttu-id="1b8c7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="1b8c7-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8c7-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b8c7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8c7-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b8c7-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1b8c7-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b8c7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8c7-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b8c7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b8c7-139">Header</span><span class="sxs-lookup"><span data-stu-id="1b8c7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b8c7-140"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1b8c7-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b8c7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b8c7-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b8c7-142">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1b8c7-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1b8c7-144">**WM \_ inputlangchange**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-144">**WM\_INPUTLANGCHANGE**</span></span>](wm-inputlangchange.md)
</dt> <dt>

<span data-ttu-id="1b8c7-145">**Licher**</span><span class="sxs-lookup"><span data-stu-id="1b8c7-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1b8c7-146">Windows</span><span class="sxs-lookup"><span data-stu-id="1b8c7-146">Windows</span></span>](windows.md)
</dt> </dl>

 

 
