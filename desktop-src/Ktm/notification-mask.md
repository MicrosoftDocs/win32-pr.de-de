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
# <a name="notification_mask"></a>Benachrichtigungs \_ Maske

Listet die verschiedenen Benachrichtigungs Typen auf, die von einer Eintragung empfangen werden können.

<dl> <dt>

<span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_Benachrichtigungs \_ Maske für Transaktion**
</dt> <dd> <dl> <dt>

0x3fffffff
</dt> <dt>



Eine Maske, die alle gültigen Bits für eine Transaktions Benachrichtigung angibt.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**\_ \_ vorab Vorbereitung der Transaktions Benachrichtigung**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Diese Benachrichtigung wird aufgerufen, nachdem ein Client [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) aufgerufen hat und entweder kein Ressourcen-Manager (RM) ein Einphasencommit unterstützt oder ein übergeordneter Transaktions-Manager (TM) [**preprepareeintragung**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)aufruft. Diese Benachrichtigung wird vom RMS empfangen, was darauf hinweist, dass alle Aufgaben abgeschlossen werden können, die dazu führen können, dass sich andere RMS in eine Transaktion eintragen müssen, z. b. das Leeren des Caches. Nach Abschluss dieser Vorgänge muss der RM [**prepreparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)aufruft. Um diese Benachrichtigung zu erhalten, muss der RM auch **Transaktionen \_ Benachrichtigen \_ vorbereiten** und Commit für die **Transaktions \_ Benachrichtigung \_** unterstützen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**Vorbereiten der Transaktions \_ Benachrichtigung \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Diese Benachrichtigung wird aufgerufen, nachdem die Verarbeitung der **\_ \_ vorab Vorbereitung der Transaktions Benachrichtigung** abgeschlossen ist. Es signalisiert dem RM, dass alle dieser Eintragung zugeordneten Aufgaben abgeschlossen werden, damit sichergestellt werden kann, dass ein Commit-Vorgang erfolgreich ausgeführt werden kann und ein Abbruch Vorgang erfolgreich ausgeführt werden kann. Der Großteil der Arbeit für eine Transaktion erfolgt in der Regel während der Vorbereitungsphase. Bei Durable RMS müssen Sie Ihren Zustand vor dem Aufrufen der [**preparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) -Funktion protokollieren. Dies ist die letzte Chance für den RM, dass ein Rollback für die Transaktion ausgeführt wird.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**Commit für Transaktions \_ Benachrichtigung \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Diese Benachrichtigung signalisiert dem RM, alle dieser Eintragung zugeordneten Aufgaben abzuschließen. In der Regel gibt der RM alle Sperren frei und gibt alle Informationen frei, die für das Rollback der Transaktion erforderlich sind. Der RM muss reagieren, indem er die [**commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) -Funktion aufgerufen, wenn er diese Vorgänge abgeschlossen hat.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**\_Rollback für Transaktions Benachrichtigung \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Diese Benachrichtigung signalisiert dem RM, dass sämtliche Aufgaben rückgängig gemacht werden, die der Transaktion zugeordnet ist.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**\_vorab Vorbereitung der Transaktions Benachrichtigung \_ \_ abgeschlossen**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein vorvorbereitungs Vorgang erfolgreich abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**Vorbereitung der Transaktions \_ Benachrichtigung \_ \_ abgeschlossen**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Vorbereitungs Vorgang erfolgreich abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**Commit für Transaktions \_ Benachrichtigung \_ \_ abgeschlossen**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Commit-Vorgang erfolgreich abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**\_Rollback für Transaktions Benachrichtigung \_ \_ abgeschlossen**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass ein Rollback-Vorgang erfolgreich abgeschlossen wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_ \_ Wiederherstellung von Transaktions Benachrichtigungen**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Diese Benachrichtigung signalisiert RMS, dass Sie Ihren Zustand wiederherstellen sollten, da ein Transaktions Ergebnis erneut zugestellt werden muss. Dies ist beispielsweise der Fall, wenn eine RM wieder hergestellt wird und Transaktionen unsicher sind. Diese Benachrichtigung wird übermittelt, sobald der Status "unsicher" aufgelöst wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**\_ \_ Einzelphasen- \_ \_ Commit für Transaktion Benachrichtigen**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Diese Benachrichtigung signalisiert dem RM, den Vorgang abzuschließen und einen Commit für die Transaktion auszuführen, ohne ein Zweiphasencommit-Protokoll zu verwenden. Wenn der RM einen zweiphasigen Vorgang verwenden möchte, muss er durch Aufrufen der [**singlephasereject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) -Funktion Antworten.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_ \_ Delegierter Commit für Transaktions Benachrichtigung \_**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



KTM signalisiert dem übergeordneten TM, einen Commitvorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**Wiederherstellungs Abfrage zur Transaktions \_ Benachrichtigung \_ \_**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



KTM signalisiert dem übergeordneten TM, den Status einer unsicheren Transaktion abzufragen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**\_ \_ vorvorbereiten der Enlist für Transaktionen Benachrichtigen \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Diese Benachrichtigung signalisiert dem übergeordneten TM, dass Benachrichtigungen vor dem Vorbereiten der angegebenen Eintragung zugestellt werden müssen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ Letzte \_ Wiederherstellung der Transaktions Benachrichtigung**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Diese Benachrichtigung zeigt an, dass der Wiederherstellungs Vorgang für diesen RM beendet wurde.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**\_inzweifel hafte Transaktions Benachrichtigung \_**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Die angegebene Transaktion befindet sich in einem zweifelhaften Zustand. Der RM empfängt diese Benachrichtigung während Wiederherstellungs Vorgängen, wenn eine Transaktion vorbereitet wurde, aber es ist kein übergeordneter Transaktions-Manager (TM) verfügbar. Wenn eine Transaktion z. b. einen Remote-TM umfasst und dieser Knoten nicht verfügbar ist, der Knoten nicht verfügbar ist oder der lokale [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) Dienst nicht verfügbar ist, ist der Transaktionsstatus unsicher.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**\_ \_ TM Online Transaktion \_ Benachrichtigen**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Der TM ist online und akzeptiert Anforderungen.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**Ergebnis der Transaktions \_ Benachrichtigungs \_ Anforderung \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Signalisiert RMS, dass Ergebnisinformationen verfügbar sind und eine Anforderung für diese Informationen erfolgen soll.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_Commit für transaktionsbenachrichtigungs \_ \_ Abschluss**
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
| Header<br/>                   | <dl> <dt>Ktmtypes. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> <dt>

[Kerneltransaktions-Manager-Konstanten](kernel-transaction-manager-constants.md)
</dt> <dt>

[**"Kreateeintragung"**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[**Commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[**Getnotificationresourcemanager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[**Getnotificationresourcemanagerasync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[**Preparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[**Singlephasereject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[**Transaktions \_ Benachrichtigung**](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

