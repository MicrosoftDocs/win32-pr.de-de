---
title: PSM_SETWIZBUTTONS Meldung (prsht. h)
description: Aktiviert oder deaktiviert die Schaltflächen "zurück", "weiter" und "Fertigstellen" in einem Assistenten. Sie können die Nachricht auch mit dem propsheet- \_ Makro für das ""-/twizbuttons-Makro veröffentlichen.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- Windows-Steuerelemente für PSM_SETWIZBUTTONS Meldung
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104193"
---
# <a name="psm_setwizbuttons-message"></a><span data-ttu-id="29615-105">PSM-Meldung "Setup \_ Buttons"</span><span class="sxs-lookup"><span data-stu-id="29615-105">PSM\_SETWIZBUTTONS message</span></span>

<span data-ttu-id="29615-106">Aktiviert oder deaktiviert die Schaltflächen " **zurück**", " **weiter**" und " **Fertig** stellen" in einem Assistenten.</span><span class="sxs-lookup"><span data-stu-id="29615-106">Enables or disables the **Back**, **Next**, and **Finish** buttons in a wizard.</span></span> <span data-ttu-id="29615-107">Sie können die Nachricht auch mit dem propsheet-Makro für das ""- [**\_ /twizbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) -Makro veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="29615-107">You can also use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to post the message.</span></span>

## <a name="parameters"></a><span data-ttu-id="29615-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29615-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29615-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29615-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29615-110">Legen Sie diesen Parameter auf pswizbf \_ elevationrequired fest, um das Symbol mit erhöhten Rechten auf den in *LPARAM* angegebenen Schaltflächen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="29615-110">Set this parameter to PSWIZBF\_ELEVATIONREQUIRED to display the elevated icon on the buttons specified in *lParam*.</span></span> <span data-ttu-id="29615-111">Das Symbol für erhöhte Rechte (oder das UAC-Schild Symbol) gibt an, dass die Eingabeaufforderung für erhöhte Rechte verwendet wird, um den Benutzer zur Genehmigung bzw</span><span class="sxs-lookup"><span data-stu-id="29615-111">The elevated icon (or UAC shield icon) indicates that the elevation prompt will be used to prompt the user for approval or credentials.</span></span> <span data-ttu-id="29615-112">Weitere Informationen finden Sie unter [Entwerfen von UAC-Anwendungen für Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="29615-112">For more information, see [Designing UAC Applications for Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="29615-113">Das Anzeigen des UAC-Schild Symbols wird nur in den aerowizard (PSH \_ aerowizard) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29615-113">Displaying the UAC shield icon is only supported in AeroWizards (PSH\_AEROWIZARD).</span></span>

 

</dd> <dt>

<span data-ttu-id="29615-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29615-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29615-115">Ein Wert, der angibt, welche Eigenschaften Blatt Schaltflächen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="29615-115">Value that specifies which property sheet buttons are enabled.</span></span> <span data-ttu-id="29615-116">Sie können eines oder mehrere der folgenden Flags kombinieren.</span><span class="sxs-lookup"><span data-stu-id="29615-116">You can combine one or more of the following flags.</span></span>



| <span data-ttu-id="29615-117">Wert</span><span class="sxs-lookup"><span data-stu-id="29615-117">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="29615-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="29615-118">Meaning</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="29615-119"><dt>**pswizb \_ zurück**</dt></span><span class="sxs-lookup"><span data-stu-id="29615-119"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="29615-120">Aktiviert die Schaltfläche " **zurück** ".</span><span class="sxs-lookup"><span data-stu-id="29615-120">Enables the **Back** button.</span></span> <span data-ttu-id="29615-121">Wenn dieses Flag nicht festgelegt ist, wird die Schaltfläche " **zurück** " als deaktiviert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29615-121">If this flag is not set, the **Back** button is displayed as disabled.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="29615-122"><dt>**pswizb \_ disabledfinish**</dt></span><span class="sxs-lookup"><span data-stu-id="29615-122"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="29615-123">Zeigt die Schaltfläche **Fertig** stellen deaktiviert an.</span><span class="sxs-lookup"><span data-stu-id="29615-123">Displays a disabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="29615-124"><dt>**pswizb- \_ Fertigstellen**</dt></span><span class="sxs-lookup"><span data-stu-id="29615-124"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="29615-125">Zeigt die Schaltfläche **Fertig** stellen aktiviert an.</span><span class="sxs-lookup"><span data-stu-id="29615-125">Displays an enabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="29615-126"><dt>**pswizb \_ als nächstes**</dt></span><span class="sxs-lookup"><span data-stu-id="29615-126"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="29615-127">Hiermit wird die Schaltfläche **Weiter** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="29615-127">Enables the **Next** button.</span></span> <span data-ttu-id="29615-128">Wenn dieses Flag nicht festgelegt ist, wird die Schaltfläche **weiter** als deaktiviert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29615-128">If this flag is not set, the **Next** button is displayed as disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29615-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29615-129">Return value</span></span>

<span data-ttu-id="29615-130">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="29615-130">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29615-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29615-131">Remarks</span></span>

<span data-ttu-id="29615-132">Wenn Ihr Benachrichtigungs Handler [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) verwendet, um eine PSM-Nachricht mit dem Wert " **\_ pingzbuttons** " zu senden, führen Sie nichts aus, das den Fokus des Fensters auf den Fenster Fokus auswirkt</span><span class="sxs-lookup"><span data-stu-id="29615-132">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SETWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="29615-133">Wenn Sie z. b. [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) sofort nach dem Verwenden von **PostMessage** zum Senden von PSM-Setup Schaltflächen abrufen, erhält das Meldungs Feld den Fokus. **\_**</span><span class="sxs-lookup"><span data-stu-id="29615-133">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SETWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="29615-134">Da bereitgestellte Nachrichten erst übermittelt werden, wenn Sie den Anfang der Nachrichten Warteschlange erreichen, wird die PSM-Nachricht "Setup **\_ Buttons** " erst übermittelt, wenn der Fokus auf das Meldungs Feld verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="29615-134">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SETWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="29615-135">Folglich kann das Eigenschaften Blatt den Fokus nicht ordnungsgemäß für die Schaltflächen festlegen.</span><span class="sxs-lookup"><span data-stu-id="29615-135">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

<span data-ttu-id="29615-136">Wenn Sie die PSM- \_ Nachricht "setwizbuttons" während der Behandlung der Benachrichtigung " [PSN \_ SETACTIVE](psn-setactive.md) " senden, verwenden Sie die Funktion " [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) " anstelle der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="29615-136">If you send the PSM\_SETWIZBUTTONS message during your handling of the [PSN\_SETACTIVE](psn-setactive.md) notification, use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function rather than the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="29615-137">Andernfalls werden die Schaltflächen vom System nicht ordnungsgemäß aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="29615-137">Otherwise, the system will not update the buttons properly.</span></span> <span data-ttu-id="29615-138">Wenn Sie die Nachricht mit dem propsheet-""-"" \* [**\_ twizbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) "-Makro senden, wird Sie gepostet.</span><span class="sxs-lookup"><span data-stu-id="29615-138">If you use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="29615-139">Zu einem beliebigen Zeitpunkt können Sie **SendMessage** zum Senden von **PSM- \_** Setup Schaltflächen verwenden.</span><span class="sxs-lookup"><span data-stu-id="29615-139">At any other time, you can use **SendMessage** to send **PSM\_SETWIZBUTTONS**.</span></span>

<span data-ttu-id="29615-140">Assistenten zeigen unter jeder Seite entweder drei oder vier Schaltflächen an.</span><span class="sxs-lookup"><span data-stu-id="29615-140">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="29615-141">Diese Meldung wird verwendet, um anzugeben, welche Schaltflächen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="29615-141">This message is used to specify which buttons are enabled.</span></span> <span data-ttu-id="29615-142">Assistenten werden normalerweise **zurück**, **Abbrechen** und entweder eine Schaltfläche " **weiter** " oder " **Fertig** stellen" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29615-142">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="29615-143">Sie aktivieren in der Regel nur die Schaltfläche " **weiter** " für die Willkommensseite, " **Next** " und " **Back** " für innere Seiten und " **zurück** " und " **Fertig** " für die Seite</span><span class="sxs-lookup"><span data-stu-id="29615-143">You typically enable only the **Next** button for the welcome page, **Next** and **Back** for interior pages, and **Back** and **Finish** for the completion page.</span></span> <span data-ttu-id="29615-144">Die Schaltfläche **Abbrechen** ist immer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="29615-144">The **Cancel** button is always enabled.</span></span> <span data-ttu-id="29615-145">Normalerweise wird die Schaltfläche "weiter" durch das Festlegen von "pswizb \_ Finish" oder "pswizb \_ disabledfinish" durch eine Schaltfläche  </span><span class="sxs-lookup"><span data-stu-id="29615-145">Normally, setting PSWIZB\_FINISH or PSWIZB\_DISABLEDFINISH replaces the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="29615-146">Wenn Sie die Schaltflächen **weiter** und **Fertig** stellen gleichzeitig anzeigen möchten, legen \_ Sie beim Erstellen des Assistenten das Flag PSH wizardhasfinish im **dwFlags** -Member der [**propsheeder**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) -Struktur des Assistenten fest.</span><span class="sxs-lookup"><span data-stu-id="29615-146">To display **Next** and **Finish** buttons simultaneously, set the PSH\_WIZARDHASFINISH flag in the **dwFlags** member of the wizard's [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="29615-147">Auf jeder Seite werden dann alle vier Schaltflächen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29615-147">Every page will then display all four buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="29615-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29615-148">Requirements</span></span>



| <span data-ttu-id="29615-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29615-149">Requirement</span></span> | <span data-ttu-id="29615-150">Wert</span><span class="sxs-lookup"><span data-stu-id="29615-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29615-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29615-151">Minimum supported client</span></span><br/> | <span data-ttu-id="29615-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29615-152">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="29615-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29615-153">Minimum supported server</span></span><br/> | <span data-ttu-id="29615-154">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29615-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="29615-155">Header</span><span class="sxs-lookup"><span data-stu-id="29615-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="29615-156"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="29615-156"><dt>Prsht.h</dt></span></span> </dl> |



 

