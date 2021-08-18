---
description: Listet die verschiedenen Arten von Benachrichtigungen auf, die von einer Eintragung empfangen werden können.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (KtmTypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17391d2b406b3f7a3ee9a3a868bc1b6734050c787fdbb432785e5be0b917468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146543"
---
# <a name="notification_mask"></a>\_BENACHRICHTIGUNGSMASKE

Listet die verschiedenen Arten von Benachrichtigungen auf, die von einer Eintragung empfangen werden können.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**TRANSACTION \_ NOTIFY \_ MASK**
</dt> <dd> <dl> <dt>

0x3FFFFFFF
</dt> <dt>



Eine Maske, die alle gültigen Bits für eine Transaktionsbenachrichtigung angibt.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**\_ \_ TRANSAKTIONSBENACHRICHTIGUNGSVORBEREITUNG**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Diese Benachrichtigung wird aufgerufen, nachdem ein Client [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) aufgerufen hat und entweder kein Ressourcen-Manager (RM) einphasenbasierte Commits unterstützt oder ein übergeordneter Transaktions-Manager (TM) [**PrePrepareEnlistment aufruft.**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment) Diese Benachrichtigung wird von den RMs empfangen, die angeben, dass sie alle Arbeiten abschließen sollten, die dazu führen können, dass andere RMs sich in eine Transaktion einträgt, z. B. das Leeren des Caches. Nach Abschluss dieser Vorgänge muss der RM [**PrePrepareComplete aufrufen.**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete) Um diese Benachrichtigung zu erhalten, muss DER RM auch **TRANSACTION \_ NOTIFY PREPARE \_ und** **TRANSACTION NOTIFY COMMIT \_ \_ unterstützen.**


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**VORBEREITUNG DER \_ \_ TRANSAKTIONSBENACHRICHTIGUNG**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Diese Benachrichtigung wird aufgerufen, nachdem **die VERARBEITUNG VON TRANSACTION NOTIFY \_ \_ PREPREPARE** abgeschlossen ist. Er signalisiert dem RM, die gesamte Arbeit, die dieser Eintragung zugeordnet ist, zu abschließen, damit sichergestellt werden kann, dass ein Commitvorgang erfolgreich ist und ein Abbruchvorgang ebenfalls erfolgreich ist. In der Regel erfolgt der Großteil der Arbeit für eine Transaktion während der Vorbereitungsphase. Bei dauerhaften RMs müssen sie ihren Status protokollieren, bevor sie die [**PrepareComplete-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) aufrufen. Dies ist die letzte Chance, dass der RM ein Rollback der Transaktion an fordert.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION \_ NOTIFY \_ COMMIT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Diese Benachrichtigung signalisiert dem RM, alle mit dieser Eintragung verbundenen Arbeiten zu abschließen. In der Regel gibt der RM alle Sperren frei und gibt alle Informationen frei, die zum Rollback der Transaktion erforderlich sind. Der RM muss reagieren, indem er die [**CommitComplete-Funktion aufruft,**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) wenn er diese Vorgänge abgeschlossen hat.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**ROLLBACK \_ DER \_ TRANSAKTIONSBENACHRICHTIGUNG**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Diese Benachrichtigung signalisiert dem RM, alle der Transaktion zugeordneten Arbeit rückgängig zu machen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**\_ \_ TRANSAKTIONSBENACHRICHTIGUNGSVORBEREITUNG \_ ABGESCHLOSSEN**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Vorbereitungsvorgang erfolgreich abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION \_ NOTIFY \_ PREPARE \_ COMPLETE**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Vorbereitungsvorgang erfolgreich abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION \_ NOTIFY \_ COMMIT \_ COMPLETE**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Commitvorgang erfolgreich abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**ROLLBACK \_ FÜR \_ TRANSAKTIONSBENACHRICHTIGUNG \_ ABGESCHLOSSEN**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Rollbackvorgang erfolgreich abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACTION \_ NOTIFY \_ RECOVER**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Diese Benachrichtigung signalisiert RMs, dass sie ihren Zustand wiederherstellen sollten, da ein Transaktionsergebnis erneut zugestellt werden muss. Beispielsweise, wenn ein RM wiederhergestellt wird und Transaktionen im Zweifelsfall bestehen. Diese Benachrichtigung wird übermittelt, sobald der zustandsverglichene Zustand aufgelöst wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION \_ NOTIFY \_ SINGLE \_ PHASE \_ COMMIT**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Diese Benachrichtigung signalisiert dem RM, die Transaktion ohne Zweiphasen-Commitprotokoll abzuschließen und zu commiten. Wenn der RM einen zweistufigen Vorgang verwenden möchte, muss er durch Aufrufen der [**SinglePhaseReject-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) antworten.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION \_ NOTIFY \_ DELEGATE \_ COMMIT**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



KTM signalisiert dem übergeordneten TM, einen Commitvorgang durchzuführen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**TRANSACTION \_ NOTIFY \_ RECOVER \_ QUERY**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



KTM signalisiert dem übergeordneten TM, den Status einer im Zweifelsfall transaktion zu fragen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**\_VORBEREITEN DER EINTRAGUNG DER \_ \_ TRANSAKTIONSBENACHRICHTIGUNG**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass vorab vorbereitete Benachrichtigungen bei der angegebenen Eintragung übermittelt werden müssen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**LETZTE \_ WIEDERHERSTELLUNG DER \_ \_ TRANSAKTIONSBENACHRICHTIGUNG**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Diese Benachrichtigung gibt an, dass der Wiederherstellungsvorgang für diesen RM abgeschlossen ist.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**TRANSACTION \_ NOTIFY \_ INDOUBT**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Die angegebene Transaktion befindet sich in einem nicht sicheren Zustand. Der RM empfängt diese Benachrichtigung während Wiederherstellungsvorgängen, wenn eine Transaktion vorbereitet wurde, aber kein übergeordneter Transaktions-Manager (TM) verfügbar ist. Wenn eine Transaktion beispielsweise einen Remote-TM umfasst und dieser Knoten nicht verfügbar ist, sein Knoten nicht verfügbar ist oder der lokale [Distributed Transaction Coordinator-Dienst](/previous-versions/windows/desktop/ms684146(v=vs.85)) nicht verfügbar ist, ist der Transaktionsstatus unsicher.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACTION \_ NOTIFY \_ TM \_ ONLINE**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Der TM ist online und akzeptiert Anforderungen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**\_ \_ TRANSAKTIONSBENACHRICHTIGUNGSANFORDERUNGSERGEBNIS \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Signalisiert RMs, dass Ergebnisinformationen verfügbar sind und dass eine Anforderung für diese Informationen gestellt werden soll.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION \_ NOTIFY \_ COMMIT \_ FINALIZE**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Reserviert.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                            |
| Header<br/>                   | <dl> <dt>KtmTypes.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[KernelTransaktions-Manager-Konstanten](kernel-transaction-manager-constants.md)
</dt> <dt>

[**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[**\_TRANSAKTIONSBENACHRICHTIGUNG**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

