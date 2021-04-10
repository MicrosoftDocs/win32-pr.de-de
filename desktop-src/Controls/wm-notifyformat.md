---
title: WM_NOTIFYFORMAT Meldung (Winuser. h)
description: Bestimmt, ob ein Fenster ANSI-oder Unicode-Strukturen in der WM- \_ Benachrichtigungs Meldung akzeptiert. WM \_ notifyformat-Meldungen werden von einem allgemeinen Steuerelement an das übergeordnete Fenster und vom übergeordneten Fenster an das allgemeine Steuerelement gesendet.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- Windows-Steuerelemente für WM_NOTIFYFORMAT Meldung
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956710"
---
# <a name="wm_notifyformat-message"></a><span data-ttu-id="9407b-105">WM \_ notifyformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="9407b-105">WM\_NOTIFYFORMAT message</span></span>

<span data-ttu-id="9407b-106">Bestimmt, ob ein Fenster ANSI-oder Unicode-Strukturen in der [**WM- \_**](wm-notify.md) Benachrichtigungs Meldung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9407b-106">Determines if a window accepts ANSI or Unicode structures in the [**WM\_NOTIFY**](wm-notify.md) notification message.</span></span> <span data-ttu-id="9407b-107">**WM \_ Notifyformat** -Meldungen werden von einem allgemeinen Steuerelement an das übergeordnete Fenster und vom übergeordneten Fenster an das allgemeine Steuerelement gesendet.</span><span class="sxs-lookup"><span data-stu-id="9407b-107">**WM\_NOTIFYFORMAT** messages are sent from a common control to its parent window and from the parent window to the common control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9407b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9407b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9407b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9407b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9407b-110">Ein Handle für das Fenster, das die **WM \_ notifyformat** -Meldung sendet.</span><span class="sxs-lookup"><span data-stu-id="9407b-110">A handle to the window that is sending the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="9407b-111">Wenn *LPARAM* eine NF- \_ Abfrage ist, ist dieser Parameter das Handle für ein Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9407b-111">If *lParam* is NF\_QUERY, this parameter is the handle to a control.</span></span> <span data-ttu-id="9407b-112">Wenn *LPARAM* eine "NF \_ Requery" ist, ist dieser Parameter das Handle für das übergeordnete Fenster eines Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="9407b-112">If *lParam* is NF\_REQUERY, this parameter is the handle to the parent window of a control.</span></span>

</dd> <dt>

<span data-ttu-id="9407b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9407b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9407b-114">Der-Befehls Wert, der die Art der " **WM \_ notifyformat** "-Meldung angibt.</span><span class="sxs-lookup"><span data-stu-id="9407b-114">The command value that specifies the nature of the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="9407b-115">Dies ist einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="9407b-115">This will be one of the following values:</span></span>



| <span data-ttu-id="9407b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9407b-116">Value</span></span>                                                                                                                                                | <span data-ttu-id="9407b-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9407b-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <span data-ttu-id="9407b-118"><dt>**NF- \_ Abfrage**</dt></span><span class="sxs-lookup"><span data-stu-id="9407b-118"><dt>**NF\_QUERY**</dt></span></span> </dl>       | <span data-ttu-id="9407b-119">Die Meldung ist eine Abfrage, mit der bestimmt wird, ob ANSI-oder Unicode-Strukturen in [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9407b-119">The message is a query to determine whether ANSI or Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="9407b-120">Dieser Befehl wird von einem-Steuerelement an das übergeordnete Fenster während der Erstellung eines-Steuer Elements und als Reaktion auf einen NF- \_ requenbefehl gesendet.</span><span class="sxs-lookup"><span data-stu-id="9407b-120">This command is sent from a control to its parent window during the creation of a control and in response to an NF\_REQUERY command.</span></span><br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <span data-ttu-id="9407b-121"><dt>**NF- \_ Requery**</dt></span><span class="sxs-lookup"><span data-stu-id="9407b-121"><dt>**NF\_REQUERY**</dt></span></span> </dl> | <span data-ttu-id="9407b-122">Die Meldung ist eine Anforderung für ein Steuerelement, ein NF- \_ Abfrageformular dieser Nachricht an das übergeordnete Fenster zu senden.</span><span class="sxs-lookup"><span data-stu-id="9407b-122">The message is a request for a control to send an NF\_QUERY form of this message to its parent window.</span></span> <span data-ttu-id="9407b-123">Dieser Befehl wird vom übergeordneten Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="9407b-123">This command is sent from the parent window.</span></span> <span data-ttu-id="9407b-124">Das übergeordnete Fenster fordert das Steuerelement auf, ihn über den in der [**WM- \_ Benachrichtigungs Meldung**](wm-notify.md) zu verwendenden Typ von Strukturen aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="9407b-124">The parent window is asking the control to requery it about the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="9407b-125">Wenn *LPARAM* eine "NF \_ Requery" ist, ist der Rückgabewert das Ergebnis des anfragevorgangs.</span><span class="sxs-lookup"><span data-stu-id="9407b-125">If *lParam* is NF\_REQUERY, the return value is the result of the requery operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9407b-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9407b-126">Return value</span></span>

<span data-ttu-id="9407b-127">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9407b-127">Returns one of the following values.</span></span>



| <span data-ttu-id="9407b-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9407b-128">Return code</span></span>                                                                                 | <span data-ttu-id="9407b-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9407b-129">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9407b-130"><dt>**NFR- \_ ANSI**</dt></span><span class="sxs-lookup"><span data-stu-id="9407b-130"><dt>**NFR\_ANSI**</dt></span></span> </dl>    | <span data-ttu-id="9407b-131">ANSI-Strukturen sollten in [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen verwendet werden, die vom Steuerelement gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9407b-131">ANSI structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span><br/>     |
| <dl> <span data-ttu-id="9407b-132"><dt>**NFR- \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="9407b-132"><dt>**NFR\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="9407b-133">Unicode-Strukturen sollten in vom Steuerelement gesendeten [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9407b-133">Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span> <br/> |
| <dl> <span data-ttu-id="9407b-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="9407b-134"><dt>**0**</dt></span></span> </dl>            | <span data-ttu-id="9407b-135">Ein Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9407b-135">An error occurred.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="9407b-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9407b-136">Remarks</span></span>

<span data-ttu-id="9407b-137">Wenn ein gemeinsames Steuerelement erstellt wird, sendet das Steuerelement eine **WM \_ notifyformat** -Meldung an das übergeordnete Fenster, um den Typ der Strukturen zu ermitteln, die in [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9407b-137">When a common control is created, the control sends a **WM\_NOTIFYFORMAT** message to its parent window to determine the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="9407b-138">Wenn das übergeordnete Fenster diese Nachricht nicht verarbeitet, antwortet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion entsprechend dem Typ des übergeordneten Fensters.</span><span class="sxs-lookup"><span data-stu-id="9407b-138">If the parent window does not handle this message, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function responds according to the type of the parent window.</span></span> <span data-ttu-id="9407b-139">Das heißt, wenn das übergeordnete Fenster ein Unicode-Fenster ist, gibt **defwindowproc** NFR \_ Unicode zurück, und wenn das übergeordnete Fenster ein ANSI-Fenster ist, gibt **defwindowproc** NFR \_ ANSI zurück.</span><span class="sxs-lookup"><span data-stu-id="9407b-139">That is, if the parent window is a Unicode window, **DefWindowProc** returns NFR\_UNICODE, and if the parent window is an ANSI window, **DefWindowProc** returns NFR\_ANSI.</span></span> <span data-ttu-id="9407b-140">Wenn das übergeordnete Fenster ein Dialogfeld ist und diese Meldung nicht verarbeitet, antwortet die [**defdlgproc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) -Funktion entsprechend dem Typ des Dialog Felds (Unicode oder ANSI).</span><span class="sxs-lookup"><span data-stu-id="9407b-140">If the parent window is a dialog box and does not handle this message, the [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) function similarly responds according to the type of the dialog box (Unicode or ANSI).</span></span>

<span data-ttu-id="9407b-141">Ein übergeordnetes Fenster kann den Typ der Strukturen ändern, die von einem allgemeinen Steuerelement in [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen verwendet werden, indem *LPARAM* auf \_ die NF-Anforderung festgelegt und eine **WM \_ notifyformat** -Nachricht an das Steuerelement gesendet</span><span class="sxs-lookup"><span data-stu-id="9407b-141">A parent window can change the type of structures a common control uses in [**WM\_NOTIFY**](wm-notify.md) messages by setting *lParam* to NF\_REQUERY and sending a **WM\_NOTIFYFORMAT** message to the control.</span></span> <span data-ttu-id="9407b-142">Dies bewirkt, dass das Steuerelement ein NF- \_ Abfrageformular der **WM \_ notifyformat** -Nachricht an das übergeordnete Fenster sendet.</span><span class="sxs-lookup"><span data-stu-id="9407b-142">This causes the control to send an NF\_QUERY form of the **WM\_NOTIFYFORMAT** message to the parent window.</span></span>

<span data-ttu-id="9407b-143">Alle allgemeinen Steuerelemente senden **WM \_ notifyformat** -Meldungen.</span><span class="sxs-lookup"><span data-stu-id="9407b-143">All common controls will send **WM\_NOTIFYFORMAT** messages.</span></span> <span data-ttu-id="9407b-144">Bei den standardmäßigen Windows-Steuerelementen (Bearbeitungs Steuerelemente, Kombinations Felder, Listenfelder, Schaltflächen, Bild Lauf leisten und statische Steuerelemente) ist dies jedoch nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="9407b-144">However, the standard Windows controls (edit controls, combo boxes, list boxes, buttons, scroll bars, and static controls) do not.</span></span>

## <a name="requirements"></a><span data-ttu-id="9407b-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9407b-145">Requirements</span></span>



| <span data-ttu-id="9407b-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9407b-146">Requirement</span></span> | <span data-ttu-id="9407b-147">Wert</span><span class="sxs-lookup"><span data-stu-id="9407b-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9407b-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9407b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9407b-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9407b-149">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9407b-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9407b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9407b-151">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9407b-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9407b-152">Header</span><span class="sxs-lookup"><span data-stu-id="9407b-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="9407b-153"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="9407b-153"><dt>Winuser.h</dt></span></span> </dl> |



 

