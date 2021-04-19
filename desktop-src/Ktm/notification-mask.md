---
description: Listet die verschiedenen Benachrichtigungs Typen auf, die von einer Eintragung empfangen werden können.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (ktmtypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360674"
---
# <a name="notification_mask"></a><span data-ttu-id="92bb8-103">Benachrichtigungs \_ Maske</span><span class="sxs-lookup"><span data-stu-id="92bb8-103">NOTIFICATION\_MASK</span></span>

<span data-ttu-id="92bb8-104">Listet die verschiedenen Benachrichtigungs Typen auf, die von einer Eintragung empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="92bb8-104">Lists the different types of notifications that can be received by an enlistment.</span></span>

<dl> <dt>

<span data-ttu-id="92bb8-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_Benachrichtigungs \_ Maske für Transaktion**</span><span class="sxs-lookup"><span data-stu-id="92bb8-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**TRANSACTION\_NOTIFY\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-106">0x3fffffff</span><span class="sxs-lookup"><span data-stu-id="92bb8-106">0x3FFFFFFF</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-107">Eine Maske, die alle gültigen Bits für eine Transaktions Benachrichtigung angibt.</span><span class="sxs-lookup"><span data-stu-id="92bb8-107">A mask that indicates all valid bits for a transaction notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**\_ \_ vorab Vorbereitung der Transaktions Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="92bb8-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**TRANSACTION\_NOTIFY\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="92bb8-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-110">Diese Benachrichtigung wird aufgerufen, nachdem ein Client [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) aufgerufen hat und entweder kein Ressourcen-Manager (RM) ein Einphasencommit unterstützt oder ein übergeordneter Transaktions-Manager (TM) [**preprepareeintragung**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)aufruft.</span><span class="sxs-lookup"><span data-stu-id="92bb8-110">This notification is called after a client calls [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) and either no resource manager (RM) supports single-phase commit or a superior transaction manager (TM) calls [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span></span> <span data-ttu-id="92bb8-111">Diese Benachrichtigung wird vom RMS empfangen, was darauf hinweist, dass alle Aufgaben abgeschlossen werden können, die dazu führen können, dass sich andere RMS in eine Transaktion eintragen müssen, z. b. das Leeren des Caches.</span><span class="sxs-lookup"><span data-stu-id="92bb8-111">This notification is received by the RMs indicating that they should complete any work that could cause other RMs to need to enlist in a transaction, such as flushing its cache.</span></span> <span data-ttu-id="92bb8-112">Nach Abschluss dieser Vorgänge muss der RM [**prepreparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)aufruft.</span><span class="sxs-lookup"><span data-stu-id="92bb8-112">After completing these operations the RM must call [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span></span> <span data-ttu-id="92bb8-113">Um diese Benachrichtigung zu erhalten, muss der RM auch **Transaktionen \_ Benachrichtigen \_ vorbereiten** und Commit für die **Transaktions \_ Benachrichtigung \_** unterstützen.</span><span class="sxs-lookup"><span data-stu-id="92bb8-113">To receive this notification the RM must also support **TRANSACTION\_NOTIFY\_PREPARE** and **TRANSACTION\_NOTIFY\_COMMIT**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**Vorbereiten der Transaktions \_ Benachrichtigung \_**</span><span class="sxs-lookup"><span data-stu-id="92bb8-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**TRANSACTION\_NOTIFY\_PREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="92bb8-115">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-116">Diese Benachrichtigung wird aufgerufen, nachdem die Verarbeitung der **\_ \_ vorab Vorbereitung der Transaktions Benachrichtigung** abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="92bb8-116">This notification is called after the **TRANSACTION\_NOTIFY\_PREPREPARE** processing is complete.</span></span> <span data-ttu-id="92bb8-117">Es signalisiert dem RM, dass alle dieser Eintragung zugeordneten Aufgaben abgeschlossen werden, damit sichergestellt werden kann, dass ein Commit-Vorgang erfolgreich ausgeführt werden kann und ein Abbruch Vorgang erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="92bb8-117">It signals the RM to complete all the work that is associated with this enlistment so that it can guarantee that a commit operation could succeed and an abort operation could also succeed.</span></span> <span data-ttu-id="92bb8-118">Der Großteil der Arbeit für eine Transaktion erfolgt in der Regel während der Vorbereitungsphase.</span><span class="sxs-lookup"><span data-stu-id="92bb8-118">Typically, the bulk of the work for a transaction is done during the prepare phase.</span></span> <span data-ttu-id="92bb8-119">Bei Durable RMS müssen Sie Ihren Zustand vor dem Aufrufen der [**preparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) -Funktion protokollieren.</span><span class="sxs-lookup"><span data-stu-id="92bb8-119">For durable RMs, they must log their state prior to calling the [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) function.</span></span> <span data-ttu-id="92bb8-120">Dies ist die letzte Chance für den RM, dass ein Rollback für die Transaktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92bb8-120">This is the last chance for the RM to request that the transaction be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**Commit für Transaktions \_ Benachrichtigung \_**</span><span class="sxs-lookup"><span data-stu-id="92bb8-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION\_NOTIFY\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="92bb8-122">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-123">Diese Benachrichtigung signalisiert dem RM, alle dieser Eintragung zugeordneten Aufgaben abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="92bb8-123">This notification signals the RM to complete all the work that is associated with this enlistment.</span></span> <span data-ttu-id="92bb8-124">In der Regel gibt der RM alle Sperren frei und gibt alle Informationen frei, die für das Rollback der Transaktion erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="92bb8-124">Typically, the RM releases any locks, releases any information necessary to roll back the transaction.</span></span> <span data-ttu-id="92bb8-125">Der RM muss reagieren, indem er die [**commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) -Funktion aufgerufen, wenn er diese Vorgänge abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="92bb8-125">The RM must respond by calling the [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) function when it has finished these operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**\_Rollback für Transaktions Benachrichtigung \_**</span><span class="sxs-lookup"><span data-stu-id="92bb8-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION\_NOTIFY\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-127">0x00000008</span><span class="sxs-lookup"><span data-stu-id="92bb8-127">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-128">Diese Benachrichtigung signalisiert dem RM, dass sämtliche Aufgaben rückgängig gemacht werden, die der Transaktion zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92bb8-128">This notification signals the RM to undo all the work it has done that is associated with the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**\_vorab Vorbereitung der Transaktions Benachrichtigung \_ \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="92bb8-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-130">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92bb8-130">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-131">Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein vorvorbereitungs Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="92bb8-131">This notification signals to the superior TM that a pre-prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**Vorbereitung der Transaktions \_ Benachrichtigung \_ \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="92bb8-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-133">0x00000020</span><span class="sxs-lookup"><span data-stu-id="92bb8-133">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-134">Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Vorbereitungs Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="92bb8-134">This notification signals to the superior TM that a prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**Commit für Transaktions \_ Benachrichtigung \_ \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="92bb8-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION\_NOTIFY\_COMMIT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-136">0x00000040</span><span class="sxs-lookup"><span data-stu-id="92bb8-136">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-137">Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Commit-Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="92bb8-137">This notification signals to the superior TM that a commit operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**\_Rollback für Transaktions Benachrichtigung \_ \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="92bb8-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**TRANSACTION\_NOTIFY\_ROLLBACK\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="92bb8-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-140">Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Rollback-Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="92bb8-140">This notification signals to the superior TM that a rollback operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_ \_ Wiederherstellung von Transaktions Benachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="92bb8-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACTION\_NOTIFY\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="92bb8-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-143">Diese Benachrichtigung signalisiert RMS, dass Sie Ihren Zustand wiederherstellen sollten, da ein Transaktions Ergebnis erneut zugestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="92bb8-143">This notification signals to RMs that they should recover their state because a transaction outcome must be redelivered.</span></span> <span data-ttu-id="92bb8-144">Dies ist beispielsweise der Fall, wenn eine RM wieder hergestellt wird und Transaktionen unsicher sind.</span><span class="sxs-lookup"><span data-stu-id="92bb8-144">For example, when an RM is recovered, and when there are transactions left in-doubt.</span></span> <span data-ttu-id="92bb8-145">Diese Benachrichtigung wird übermittelt, sobald der Status "unsicher" aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="92bb8-145">This notification is delivered once the in-doubt state is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**\_ \_ Einzelphasen- \_ \_ Commit für Transaktion Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="92bb8-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION\_NOTIFY\_SINGLE\_PHASE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-147">0x00000200</span><span class="sxs-lookup"><span data-stu-id="92bb8-147">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-148">Diese Benachrichtigung signalisiert dem RM, den Vorgang abzuschließen und einen Commit für die Transaktion auszuführen, ohne ein Zweiphasencommit-Protokoll zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="92bb8-148">This notification signals the RM to complete and commit the transaction without using a two-phase commit protocol.</span></span> <span data-ttu-id="92bb8-149">Wenn der RM einen zweiphasigen Vorgang verwenden möchte, muss er durch Aufrufen der [**singlephasereject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) -Funktion Antworten.</span><span class="sxs-lookup"><span data-stu-id="92bb8-149">If the RM wants to use a two-phase operation, it must respond by calling the [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_ \_ Delegierter Commit für Transaktions Benachrichtigung \_**</span><span class="sxs-lookup"><span data-stu-id="92bb8-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION\_NOTIFY\_DELEGATE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-151">0x00000400</span><span class="sxs-lookup"><span data-stu-id="92bb8-151">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-152">KTM signalisiert dem übergeordneten TM, einen Commitvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="92bb8-152">KTM is signaling to the superior TM to perform a commit operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**Wiederherstellungs Abfrage zur Transaktions \_ Benachrichtigung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92bb8-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**TRANSACTION\_NOTIFY\_RECOVER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-154">0x00000800</span><span class="sxs-lookup"><span data-stu-id="92bb8-154">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-155">KTM signalisiert dem übergeordneten TM, den Status einer unsicheren Transaktion abzufragen.</span><span class="sxs-lookup"><span data-stu-id="92bb8-155">KTM is signaling to the superior TM to query the status of an in-doubt transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**\_ \_ vorvorbereiten der Enlist für Transaktionen Benachrichtigen \_**</span><span class="sxs-lookup"><span data-stu-id="92bb8-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION\_NOTIFY\_ENLIST\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-157">0x00001000</span><span class="sxs-lookup"><span data-stu-id="92bb8-157">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-158">Diese Benachrichtigung signalisiert dem übergeordneten TM, dass Benachrichtigungen vor dem Vorbereiten der angegebenen Eintragung zugestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="92bb8-158">This notification signals to the superior TM that pre-prepare notifications must be delivered on the specified enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ Letzte \_ Wiederherstellung der Transaktions Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="92bb8-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION\_NOTIFY\_LAST\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="92bb8-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-161">Diese Benachrichtigung zeigt an, dass der Wiederherstellungs Vorgang für diesen RM beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="92bb8-161">This notification indicates that the recovery operation is complete for this RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**\_inzweifel hafte Transaktions Benachrichtigung \_**</span><span class="sxs-lookup"><span data-stu-id="92bb8-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**TRANSACTION\_NOTIFY\_INDOUBT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-163">0x00004000</span><span class="sxs-lookup"><span data-stu-id="92bb8-163">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-164">Die angegebene Transaktion befindet sich in einem zweifelhaften Zustand.</span><span class="sxs-lookup"><span data-stu-id="92bb8-164">The specified transaction is in an in-doubt state.</span></span> <span data-ttu-id="92bb8-165">Der RM empfängt diese Benachrichtigung während Wiederherstellungs Vorgängen, wenn eine Transaktion vorbereitet wurde, aber es ist kein übergeordneter Transaktions-Manager (TM) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92bb8-165">The RM receives this notification during recovery operations when a transaction has been prepared, but there is no superior transaction manager (TM) available.</span></span> <span data-ttu-id="92bb8-166">Wenn eine Transaktion z. b. einen Remote-TM umfasst und dieser Knoten nicht verfügbar ist, der Knoten nicht verfügbar ist oder der lokale [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) Dienst nicht verfügbar ist, ist der Transaktionsstatus unsicher.</span><span class="sxs-lookup"><span data-stu-id="92bb8-166">For example, when a transaction involves a remote TM and that node is unavailable, its node is unavailable, or the local [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) service is unavailable, the transaction state is in-doubt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**\_ \_ TM Online Transaktion \_ Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="92bb8-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACTION\_NOTIFY\_TM\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-168">0x02000000</span><span class="sxs-lookup"><span data-stu-id="92bb8-168">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-169">Der TM ist online und akzeptiert Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="92bb8-169">The TM is online and accepting requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**Ergebnis der Transaktions \_ Benachrichtigungs \_ Anforderung \_**</span><span class="sxs-lookup"><span data-stu-id="92bb8-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**TRANSACTION\_NOTIFY\_REQUEST\_OUTCOME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-171">0x20000000</span><span class="sxs-lookup"><span data-stu-id="92bb8-171">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-172">Signalisiert RMS, dass Ergebnisinformationen verfügbar sind und eine Anforderung für diese Informationen erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="92bb8-172">Signals to RMs that there is outcome information available, and that a request for that information should be made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92bb8-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_Commit für transaktionsbenachrichtigungs \_ \_ Abschluss**</span><span class="sxs-lookup"><span data-stu-id="92bb8-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION\_NOTIFY\_COMMIT\_FINALIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92bb8-174">0x40000000</span><span class="sxs-lookup"><span data-stu-id="92bb8-174">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="92bb8-175">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="92bb8-175">Reserved.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92bb8-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92bb8-176">Requirements</span></span>



| <span data-ttu-id="92bb8-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92bb8-177">Requirement</span></span> | <span data-ttu-id="92bb8-178">Wert</span><span class="sxs-lookup"><span data-stu-id="92bb8-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92bb8-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92bb8-179">Minimum supported client</span></span><br/> | <span data-ttu-id="92bb8-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92bb8-180">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="92bb8-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92bb8-181">Minimum supported server</span></span><br/> | <span data-ttu-id="92bb8-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92bb8-182">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="92bb8-183">Header</span><span class="sxs-lookup"><span data-stu-id="92bb8-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="92bb8-184"><dt>Ktmtypes. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92bb8-184"><dt>KtmTypes.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92bb8-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92bb8-185">See also</span></span>

<dl> <dt>

<span data-ttu-id="92bb8-186">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="92bb8-186">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="92bb8-187">Kerneltransaktions-Manager-Konstanten</span><span class="sxs-lookup"><span data-stu-id="92bb8-187">Kernel Transaction Manager Constants</span></span>](kernel-transaction-manager-constants.md)
</dt> <dt>

[<span data-ttu-id="92bb8-188">**"Kreateeintragung"**</span><span class="sxs-lookup"><span data-stu-id="92bb8-188">**CreateEnlistment**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[<span data-ttu-id="92bb8-189">**Commitcomplete**</span><span class="sxs-lookup"><span data-stu-id="92bb8-189">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[<span data-ttu-id="92bb8-190">**Getnotificationresourcemanager**</span><span class="sxs-lookup"><span data-stu-id="92bb8-190">**GetNotificationResourceManager**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[<span data-ttu-id="92bb8-191">**Getnotificationresourcemanagerasync**</span><span class="sxs-lookup"><span data-stu-id="92bb8-191">**GetNotificationResourceManagerAsync**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[<span data-ttu-id="92bb8-192">**Preparecomplete**</span><span class="sxs-lookup"><span data-stu-id="92bb8-192">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[<span data-ttu-id="92bb8-193">**Singlephasereject**</span><span class="sxs-lookup"><span data-stu-id="92bb8-193">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[<span data-ttu-id="92bb8-194">**Transaktions \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="92bb8-194">**TRANSACTION\_NOTIFICATION**</span></span>](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

