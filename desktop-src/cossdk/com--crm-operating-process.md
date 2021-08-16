---
description: COM+ CRM-Betriebsprozess
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: COM+ CRM-Betriebsprozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d294d60429faeaad7a4d58808760ecd327bcaff252f2b71070c6605f5327ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308129"
---
# <a name="com-crm-operating-process"></a>COM+ CRM-Betriebsprozess

Im normalen Betrieb würde eine Anwendungskomponente, die in einem Serveranwendungsprozess ausgeführt wird, ein COM+-CRM verwenden, indem ein CRM-Worker erstellt wird. Der CRM-Worker implementiert eine COM-Schnittstelle, die für die Aufgabe spezifisch ist, die er ausführen soll. Die Anwendungskomponente muss unter einer Transaktion ausgeführt werden, damit der CRM-Worker die Transaktion der Anwendungskomponente erbt. CRM-Worker erfordern immer eine Transaktion.

Um auf COM+ CRM zuzugreifen, ruft der CRM-Worker zuerst die [**ICrmLogControl-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) ab, die es dem CRM-Worker ermöglicht, Datensätze in das dauerhafte Protokoll zu schreiben. Der CRM-Worker erhält diese Schnittstelle, indem er eine CRM-Clerkkomponente erstellt.

Als Nächstes muss der CRM-Worker dem CRM-Clerk den Namen des CRM-Kompensators mitteilen, den er verwenden möchte. Hierzu wird die [**ICrmLogControl::RegisterCompensator-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) aufgerufen. Nachdem diese Methode aufgerufen wurde, wird der CRM-Kompensator von der CRM-Infrastruktur erstellt, wenn die Transaktion abgeschlossen ist.

Nachdem der CRM-Worker den CRM-Kompensator registriert hat, kann er mithilfe von [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)Datensätze in das CRM-Protokoll schreiben. Der CRM-Worker muss *schreiben.* Das heißt, er muss einen Datensatz in das Protokoll schreiben, der eine Aktion beschreibt, bevor die Aktion tatsächlich ausgeführt wird, falls unmittelbar nach Abschluss der Aktion ein Absturz auftritt. Ohne diese Write-Ahead-Protokolldatensätze gibt es keine Möglichkeit, die Aktion zu korrigieren.

Außerdem bedeutet Write Ahead, dass der CRM-Kompensator, bei dem es sich um die Komponente handelt, die die Protokolldatensätze bei der Wiederherstellung empfängt, den Fall behandeln muss, in dem die Protokolldatensätze geschrieben wurden, aber die Aktion nicht tatsächlich durchgeführt wurde. Aktionen des CRM-Kompensators müssen *idempotent* sein. Das heißt, sie sollten mehr als einmal ausgeführt werden können, aber zu demselben Ergebnis führen. Das Festlegen eines Kontosaldos auf den Wert von 100 USD ist beispielsweise eine idempotente Aktion. Das Hinzufügen von 100 US-Dollar zum Kontostand ist nicht der Richtige.

Die [**ICrmLogControl-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) stellt die folgenden beiden Methoden zum Schreiben von Protokolldatensätzen bereit:

-   [**WriteLogRecordVariants**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) wird zum Schreiben eines strukturierten Protokolldatensatzes verwendet, der als Sammlung von Varianten erstellt wird. Sie ist in erster Linie für die Entwicklung von CRMs in Microsoft Visual Basic vorgesehen.
-   [**WriteLogRecord**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) wird zum Schreiben eines unstrukturierten Protokolldatensatzes als BLOBs von Bytes verwendet. Sie ist in erster Linie für die Entwicklung von CRMs in Microsoft Visual C++ vorgesehen. Da Datensatzstrukturen in C häufig aus einem Satz von Headern und Feldern bestehen, die möglicherweise im Arbeitsspeicher verteilt sind, implementiert die **WriteLogRecord-Methode** eine Erfassungsfunktion, die das Kopieren von Daten reduziert.

> [!Note]  
> Sie sollten keine Benutzerzeigertypen innerhalb von Datenstrukturen in einem Protokolldatensatz verwenden. Zeiger sind während der Wiederherstellungsphase nicht mehr gültig, da der CRM-Kompensator in einem anderen Prozess als der CRM-Worker ausgeführt wird, der den Protokolldatensatz geschrieben hat. Das Einschließen von Zeigertypen in einen Protokolldatensatz kann dazu führen, dass eine Anwendung während der Wiederherstellung abstürzt oder sich selbst beschädigt.

 

Beide Schreibmethoden schreiben einen Protokolldatensatz auf den Datenträger, garantieren jedoch nicht die Dauerhaftigkeit des Datensatzes. Auch wenn verzögerte Schreibvorgänge vor dem Erzwingen des Datenträgers akkumuliert werden können, kann die Leistung verbessert werden. Sie können jedoch stattdessen die [**ICrmLogControl::ForceLog-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) verwenden, um sicherzustellen, dass alle vom CRM ausgeführten Schreibvorgänge dauerhaft auf dem Datenträger gespeichert werden, was für die Wiederherstellung von Fehlern wichtig ist.

Wenn der CRM-Worker mit seinen Aktionen fertig ist und das Schreiben und Erzwingen von Datensätzen in das Protokoll abgeschlossen hat, muss [**er ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)freigeben. Wenn die Transaktion abgeschlossen ist (in der Regel aufgrund der Anwendungskomponente, die [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) oder [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)aufruft), erstellt die CRM-Infrastruktur die CRM-Kompensierungskomponente, die entweder die [**ICrmCompensator-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) oder die [**ICrmCompensatorVariants-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) implementiert. Diese Schnittstellen werden verwendet, um die unstrukturierten (Visual C++) oder strukturierten Datensätze (Visual Basic) zusammen mit den Transaktionsergebnisbenachrichtigungen an den CRM-Kompensator zu übergeben.

Der CRM-Kompensator wird zuerst über die Vorbereitungsphase des Transaktionsabschlusses benachrichtigt und kann entweder mit Ja oder Nein für die Vorbereitungsanforderung abstimmen. Wenn der CRM-Kompensator nein stimmt, erhält er keine weiteren Abbruchbenachrichtigungen. Wenn sie ja zur Vorbereitungsanforderung stimmt, empfängt sie entweder die Commit- oder Abbruchbenachrichtigungen. Im Fall eines Clientabbruchs werden keine Vorbereitungsbenachrichtigungen empfangen, sondern nur Abbruchbenachrichtigungen. Der CRM-Kompensator muss darauf vorbereitet sein, all diese Fälle zu verarbeiten, und er muss auch den Fall behandeln, in dem keine Protokolldatensätze erfolgreich vom CRM-Worker geschrieben wurden. Der CRM-Kompensator darf nicht davon ausgehen, dass dieselbe CRM-Kompensatorinstanz sowohl die Benachrichtigungen der Phase 1 (Vorbereitung) als auch der Phase 2 (Commit oder Abbruch) empfängt, da diese durch die Wiederherstellung unterbrochen werden können.

In der Regel verwendet ein CRM-Kompensator die Abbruchbenachrichtigung, um die vom CRM-Worker ausgeführte Aktion umzukehren. Der CRM-Worker kann einen Zustand verfügbar lassen, falls er seine Aktion umkehren muss. Dieser Zustand kann vollständig in den Protokolldatensätzen enthalten sein. Andernfalls muss der CRM-Kompensator diesen Zustand bereinigen, wenn für die Transaktion ein Commit ausgeführt wird. Dies ist der Grund, warum der CRM-Kompensator die Commitbenachrichtigung empfängt. Der CRM-Kompensator wird nicht unter einer DTC-Transaktion ausgeführt.

Der CRM-Kompensator kann bei Bedarf neue Datensätze protokollieren, indem [**er ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)verwendet, das beim Erstellen empfangen wird. Sowohl der CRM-Worker als auch der CRM-Kompensator können auch den letzten Protokolldatensatz vergessen, den sie geschrieben haben. Dies kann erforderlich sein, um eine unnötige Wiederherstellung zu vermeiden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Compensating Resource Manager Concepts](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[COM+ CRM-Start und -Wiederherstellung](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



