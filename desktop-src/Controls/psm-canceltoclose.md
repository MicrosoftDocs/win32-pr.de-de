---
title: PSM_CANCELTOCLOSE Meldung (prsht. h)
description: Wird von einer Anwendung gesendet, wenn Sie Änderungen seit der letzten Überprüfung von PSN-Benachrichtigungen durchgeführt hat \_ , die nicht abgebrochen werden können. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ canceldeclose-Makros senden.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- Windows-Steuerelemente für PSM_CANCELTOCLOSE Meldung
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105278"
---
# <a name="psm_canceltoclose-message"></a><span data-ttu-id="47738-105">PSM \_ cancelumclose-Nachricht</span><span class="sxs-lookup"><span data-stu-id="47738-105">PSM\_CANCELTOCLOSE message</span></span>

<span data-ttu-id="47738-106">Wird von einer Anwendung gesendet, wenn Sie Änderungen seit der letzten Überprüfung von [PSN \_ ](psn-apply.md) -Benachrichtigungen durchgeführt hat, die nicht abgebrochen werden können.</span><span class="sxs-lookup"><span data-stu-id="47738-106">Sent by an application when it has performed changes since the most recent [PSN\_APPLY](psn-apply.md) notification that cannot be canceled.</span></span> <span data-ttu-id="47738-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ canceldeclose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="47738-107">You can send this message explicitly or by using the [**PropSheet\_CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="47738-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="47738-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47738-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47738-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47738-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="47738-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="47738-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47738-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47738-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="47738-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47738-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47738-113">Return value</span></span>

<span data-ttu-id="47738-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="47738-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47738-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47738-115">Remarks</span></span>

<span data-ttu-id="47738-116">**PSM \_ Canceldeclose** deaktiviert die Schaltfläche **Abbrechen** und ändert den Text der Schaltfläche **OK** in "Close".</span><span class="sxs-lookup"><span data-stu-id="47738-116">**PSM\_CANCELTOCLOSE** disables the **Cancel** button and changes the text of the **OK** button to "Close".</span></span>

<span data-ttu-id="47738-117">Die meisten Eigenschaften Blätter warten auf das Durchführen von nicht rückgängig zu machenden Änderungen, bis eine Benachrichtigung über das \_</span><span class="sxs-lookup"><span data-stu-id="47738-117">Most property sheets wait to perform irreversible changes until a PSN\_APPLY notification is received.</span></span> <span data-ttu-id="47738-118">In einigen Fällen kann ein Eigenschaften Blatt jedoch nicht rückgängig zu machende Änderungen außerhalb der standardmäßigen "PSN \_ Apply/PSN Reset"- \_ Sequenz vornehmen.</span><span class="sxs-lookup"><span data-stu-id="47738-118">However, in some circumstances, a property sheet may make irreversible changes outside the standard PSN\_APPLY/PSN\_RESET sequence.</span></span> <span data-ttu-id="47738-119">Ein Beispiel hierfür ist ein Eigenschaften Blatt, das eine **Bearbeitungs** Schaltfläche enthält, die zum Anzeigen eines unter Dialogfelds zum Bearbeiten einer Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47738-119">One example is a property sheet that contains an **Edit** button that is used to display a subdialog box for editing a property.</span></span> <span data-ttu-id="47738-120">Wenn der Benutzer auf **OK** klickt, um die Änderung zu übermitteln, verfügt die Seite Eigenschaften Blatt über mehrere Optionen.</span><span class="sxs-lookup"><span data-stu-id="47738-120">When the user clicks **OK** to submit the change, the property sheet page has several options.</span></span>

-   <span data-ttu-id="47738-121">Die Änderungen können aufgezeichnet werden, aber warten Sie, bis Sie eine PSN- \_ Benachrichtigungs Benachrichtigung erhalten, um Sie anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="47738-121">It can record the changes, but wait until it receives a PSN\_APPLY notification to apply them.</span></span> <span data-ttu-id="47738-122">Dies ist der bevorzugte Ansatz.</span><span class="sxs-lookup"><span data-stu-id="47738-122">This is the preferred approach.</span></span>
-   <span data-ttu-id="47738-123">Sie kann die Änderungen sofort nach dem Beenden des unter Dialogfelds anwenden, aber merken Sie sich die ursprünglichen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="47738-123">It can apply the changes immediately after exiting the subdialog box, but remember the original settings.</span></span> <span data-ttu-id="47738-124">Diese Einstellungen können verwendet werden, um den ursprünglichen Status wiederherzustellen, wenn eine \_ Benachrichtigung zum Zurücksetzen von PSN empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="47738-124">Those settings can be used to restore the original state if a PSN\_RESET notification is received.</span></span>
-   <span data-ttu-id="47738-125">Die Änderungen können sofort angewendet werden, und es wird nicht versucht, die ursprünglichen Einstellungen wiederherzustellen, wenn eine Benachrichtigung zum [ \_ Zurücksetzen von PSN](psn-reset.md) empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="47738-125">It can apply the changes immediately and not attempt to restore the original settings when it receives a [PSN\_RESET](psn-reset.md) notification.</span></span> <span data-ttu-id="47738-126">Diese Vorgehensweise wird nicht empfohlen, kann jedoch notwendig sein, wenn die Änderungen zu weitreichend sind, damit die beiden anderen Optionen praktikabel sind.</span><span class="sxs-lookup"><span data-stu-id="47738-126">This approach is not recommended, but may be necessary if the changes are too far-reaching for the other two options to be practical.</span></span>

<span data-ttu-id="47738-127">Bei der dritten Option sollten Anwendungen eine **PSM \_ canceldeclose** -Nachricht an das Eigenschaften Blatt senden.</span><span class="sxs-lookup"><span data-stu-id="47738-127">For the third option, applications should send a **PSM\_CANCELTOCLOSE** message to the property sheet.</span></span> <span data-ttu-id="47738-128">Es zeigt dem Benutzer an, dass die mit dem unter Dialogfeld vorgenommenen Änderungen nicht durch Klicken auf die Schaltfläche **Abbrechen** rückgängig gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="47738-128">It indicates to the user that the changes made with the subdialog box cannot be reversed by clicking the **Cancel** button.</span></span>

> [!Note]  
> <span data-ttu-id="47738-129">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47738-129">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="47738-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47738-130">Requirements</span></span>



| <span data-ttu-id="47738-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47738-131">Requirement</span></span> | <span data-ttu-id="47738-132">Wert</span><span class="sxs-lookup"><span data-stu-id="47738-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47738-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47738-133">Minimum supported client</span></span><br/> | <span data-ttu-id="47738-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47738-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="47738-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47738-135">Minimum supported server</span></span><br/> | <span data-ttu-id="47738-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47738-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="47738-137">Header</span><span class="sxs-lookup"><span data-stu-id="47738-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="47738-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="47738-138"><dt>Prsht.h</dt></span></span> </dl> |



 

 





