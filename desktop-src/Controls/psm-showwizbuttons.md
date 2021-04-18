---
title: PSM_SHOWWIZBUTTONS Meldung (prsht. h)
description: Blendet Schaltflächen in einem Assistenten ein oder aus. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ showwitzbuttons-Makros senden.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- Windows-Steuerelemente für PSM_SHOWWIZBUTTONS Meldung
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337496"
---
# <a name="psm_showwizbuttons-message"></a><span data-ttu-id="02ac6-105">PSM- \_ showwizbuttons-Meldung</span><span class="sxs-lookup"><span data-stu-id="02ac6-105">PSM\_SHOWWIZBUTTONS message</span></span>

<span data-ttu-id="02ac6-106">Blendet Schaltflächen in einem Assistenten ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="02ac6-106">Shows or hides buttons in a wizard.</span></span> <span data-ttu-id="02ac6-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet- \_ showwitzbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="02ac6-107">You can send this message explicitly or by using the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="02ac6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02ac6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ac6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02ac6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02ac6-110">Einer oder mehrere der folgenden Werte, die angeben, welche Eigenschaften Blatt Schaltflächen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="02ac6-110">One or more of the following values that specify which property sheet buttons are to be shown.</span></span> <span data-ttu-id="02ac6-111">Wenn ein Schaltflächen Wert sowohl in diesem Parameter als auch in *LPARAM* enthalten ist, wird er angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02ac6-111">If a button value is included in both this parameter and *lParam*, it is shown.</span></span>



| <span data-ttu-id="02ac6-112">Wert</span><span class="sxs-lookup"><span data-stu-id="02ac6-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="02ac6-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="02ac6-113">Meaning</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="02ac6-114"><dt>**pswizb \_ zurück**</dt></span><span class="sxs-lookup"><span data-stu-id="02ac6-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="02ac6-115">Die Schaltfläche " **zurück** ".</span><span class="sxs-lookup"><span data-stu-id="02ac6-115">The **Back** button.</span></span><br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="02ac6-116"><dt>**pswizb- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="02ac6-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="02ac6-117">Die Schaltfläche " **Abbrechen** ".</span><span class="sxs-lookup"><span data-stu-id="02ac6-117">The **Cancel** button.</span></span><br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="02ac6-118"><dt>**pswizb \_ disabledfinish**</dt></span><span class="sxs-lookup"><span data-stu-id="02ac6-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="02ac6-119">Die Schaltfläche **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="02ac6-119">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="02ac6-120"><dt>**pswizb- \_ Fertigstellen**</dt></span><span class="sxs-lookup"><span data-stu-id="02ac6-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="02ac6-121">Die Schaltfläche **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="02ac6-121">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="02ac6-122"><dt>**pswizb \_ als nächstes**</dt></span><span class="sxs-lookup"><span data-stu-id="02ac6-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="02ac6-123">Die Schaltfläche **weiter** .</span><span class="sxs-lookup"><span data-stu-id="02ac6-123">The **Next** button.</span></span><br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <span data-ttu-id="02ac6-124"><dt>**pswizb- \_ Anzeige**</dt></span><span class="sxs-lookup"><span data-stu-id="02ac6-124"><dt>**PSWIZB\_SHOW**</dt></span></span> </dl>                               | <span data-ttu-id="02ac6-125">Legen Sie nur dieses Flag (definiert als null) fest, um alle in *LPARAM* angegebenen Schaltflächen auszublenden.</span><span class="sxs-lookup"><span data-stu-id="02ac6-125">Set only this flag (defined as zero) to hide all buttons specified in *lParam*.</span></span><br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <span data-ttu-id="02ac6-126"><dt>**pswizb- \_ Wiederherstellung**</dt></span><span class="sxs-lookup"><span data-stu-id="02ac6-126"><dt>**PSWIZB\_RESTORE**</dt></span></span> </dl>                      | <span data-ttu-id="02ac6-127">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="02ac6-127">Not implemented.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="02ac6-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02ac6-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02ac6-129">Mindestens einer der in *wParam* verwendeten Werte, der angibt, welche Schaltflächen von diesem-Befehl betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="02ac6-129">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="02ac6-130">Wenn ein Schaltflächen Wert in diesem Parameter, aber nicht in *wParam* angezeigt wird, wird die Schaltfläche ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="02ac6-130">If a button value appears in this parameter but not in *wParam*, the button is hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02ac6-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02ac6-131">Return value</span></span>

<span data-ttu-id="02ac6-132">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="02ac6-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02ac6-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02ac6-133">Remarks</span></span>

<span data-ttu-id="02ac6-134">Assistenten zeigen unter jeder Seite entweder drei oder vier Schaltflächen an.</span><span class="sxs-lookup"><span data-stu-id="02ac6-134">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="02ac6-135">Diese Meldung wird verwendet, um anzugeben, welche Schaltflächen sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="02ac6-135">This message is used to specify which buttons are visible.</span></span> <span data-ttu-id="02ac6-136">Assistenten werden normalerweise **zurück**, **Abbrechen** und entweder eine Schaltfläche " **weiter** " oder " **Fertig** stellen" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02ac6-136">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="02ac6-137">Die Schaltfläche **Abbrechen** ist immer sichtbar.</span><span class="sxs-lookup"><span data-stu-id="02ac6-137">The **Cancel** button is always visible.</span></span>

<span data-ttu-id="02ac6-138">Legen Sie in der Regel **pswizb- \_ Fertig** stellen oder **pswizb \_ disabledfinish** fest, um die Schaltfläche **weiter** durch die Schaltfläche **Fertig** stellen zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="02ac6-138">Typically, set **PSWIZB\_FINISH** or **PSWIZB\_DISABLEDFINISH** to replace the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="02ac6-139">Wenn Sie die Schaltflächen " **weiter** " und " **Fertig** stellen" gleichzeitig anzeigen möchten, legen Sie beim Erstellen des Assistenten das Flag " **PSH \_ wizardhasfinish** " im **dwFlags** -Member der [**propsheeder**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="02ac6-139">To display **Next** and **Finish** buttons simultaneously, set the **PSH\_WIZARDHASFINISH** flag in the **dwFlags** member of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="02ac6-140">Auf jeder Seite werden dann alle vier Schaltflächen angezeigt: **zurück**, **weiter**, **Abbrechen** und **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="02ac6-140">Every page will then display all four buttons: **Back**, **Next**, **Cancel**, and **Finish**.</span></span>

<span data-ttu-id="02ac6-141">Wenn Sie das [**propsheet- \_ showwitzbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) -Makro verwenden, um diese Nachricht zu senden, wird Sie gepostet.</span><span class="sxs-lookup"><span data-stu-id="02ac6-141">If you use the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="02ac6-142">Zu einem beliebigen Zeitpunkt können Sie [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) verwenden, um **PSM \_ showwitzbuttons** zu senden.</span><span class="sxs-lookup"><span data-stu-id="02ac6-142">At any other time, you can use [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to send **PSM\_SHOWWIZBUTTONS**.</span></span>

<span data-ttu-id="02ac6-143">Wenn Ihr Benachrichtigungs Handler [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) verwendet, um eine **PSM- \_ showwitzbuttons** -Nachricht zu senden, sollten Sie keine Auswirkungen auf den Fenster Fokus haben, bis der Handler zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="02ac6-143">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SHOWWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="02ac6-144">Wenn Sie z. b. [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) sofort nach dem Verwenden von **PostMessage** zum Senden von **PSM- \_ showwitzbuttons** aufzurufen, erhält das Meldungs Feld den Fokus.</span><span class="sxs-lookup"><span data-stu-id="02ac6-144">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SHOWWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="02ac6-145">Da bereitgestellte Nachrichten erst übermittelt werden, wenn Sie den Anfang der Nachrichten Warteschlange erreichen, wird die **PSM- \_ showwitzbuttons** -Nachricht erst zugestellt, wenn der Fokus auf das Meldungs Feld verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="02ac6-145">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SHOWWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="02ac6-146">Folglich kann das Eigenschaften Blatt den Fokus nicht ordnungsgemäß für die Schaltflächen festlegen.</span><span class="sxs-lookup"><span data-stu-id="02ac6-146">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="02ac6-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02ac6-147">Requirements</span></span>



| <span data-ttu-id="02ac6-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02ac6-148">Requirement</span></span> | <span data-ttu-id="02ac6-149">Wert</span><span class="sxs-lookup"><span data-stu-id="02ac6-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02ac6-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02ac6-150">Minimum supported client</span></span><br/> | <span data-ttu-id="02ac6-151">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02ac6-151">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="02ac6-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02ac6-152">Minimum supported server</span></span><br/> | <span data-ttu-id="02ac6-153">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02ac6-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="02ac6-154">Header</span><span class="sxs-lookup"><span data-stu-id="02ac6-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="02ac6-155"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="02ac6-155"><dt>Prsht.h</dt></span></span> </dl> |



 

