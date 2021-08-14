---
description: COM+-CRM-Betriebsvorgang
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: COM+-CRM-Betriebsvorgang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d294d60429faeaad7a4d58808760ecd327bcaff252f2b71070c6605f5327ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308129"
---
# <a name="com-crm-operating-process"></a>COM+-CRM-Betriebsvorgang

Im normalen Betrieb würde eine Anwendungskomponente, die in einem Serveranwendungsprozess ausgeführt wird, ein COM+-CRM verwenden, indem ein CRM-Worker erstellt wird. Der CRM-Worker implementiert eine COM-Schnittstelle speziell für die Aufgabe, die er ausführen soll. Die Anwendungskomponente muss unter einer Transaktion ausgeführt werden, damit der CRM-Worker die Transaktion der Anwendungskomponente erbt. CRM-Mitarbeiter erfordern immer eine Transaktion.

Für den Zugriff auf COM+ CRM erhält der CRM-Worker zunächst die [**ICrmLogControl-Schnittstelle,**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) die es dem CRM-Worker ermöglicht, Datensätze in das dauerhafte Protokoll zu schreiben. Der CRM-Worker erhält diese Schnittstelle, indem er eine CRM-Clerkkomponente erstellt.

Als Nächstes muss der CRM-Worker dem CRM-Clerk den Namen des CRM-Kompensators mitteilen, den er verwenden möchte. Hierzu wird die [**ICrmLogControl::RegisterCompensator-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) aufruft. Nachdem diese Methode aufgerufen wurde, wird der CRM-Kompensator von der CRM-Infrastruktur erstellt, wenn die Transaktion abgeschlossen ist.

Nachdem der CRM-Worker seinen CRM-Kompensator registriert hat, kann er mithilfe von [**ICrmLogControl Datensätze**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)in das CRM-Protokoll schreiben. Der CRM-Worker muss *vorausschreiben.* Das heißt, er muss einen Datensatz in das Protokoll schreiben, der eine Aktion beschreibt, bevor sie die Aktion tatsächlich ausführt, falls unmittelbar nach Abschluss der Aktion ein Absturz auftritt. Ohne diese Write-Ahead-Protokolldatensätze gibt es keine Möglichkeit, die Aktion zu korrigieren.

Außerdem bedeutet Write-Ahead, dass der CRM-Kompensator, bei dem es sich um die Komponente handelt, die die Protokolldatensätze bei der Wiederherstellung empfängt, den Fall behandeln muss, in dem die Protokolldatensätze geschrieben wurden, die Aktion jedoch nicht tatsächlich erfolgt ist. Aktionen des CRM-Kompensators müssen *idempotent sein.* Das heißt, sie sollten mehr als einmal ausgeführt werden können, sollten aber zu demselben Ergebnis führen. Das Festlegen eines Kontostands auf den Wert von 100 USD ist beispielsweise eine idempotente Aktion. Das Hinzufügen von 100 USD zum Kontostand ist nicht der Wert.

Die [**ICrmLogControl-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) stellt die folgenden beiden Methoden zum Schreiben von Protokolldatensätzen bereit:

-   [**WriteLogRecordVariants wird**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) zum Schreiben eines strukturierten Protokolldatensatz verwendet, der als Sammlung von Varianten erstellt wird. Sie dient hauptsächlich zur Verwendung bei der Entwicklung von CRMs in Microsoft Visual Basic.
-   [**WriteLogRecord**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) wird zum Schreiben eines unstrukturierten Protokolldatensatz als BLOBs von Bytes verwendet. Sie dient hauptsächlich zur Verwendung bei der Entwicklung von CRMs in Microsoft Visual C++. Da Datensatzstrukturen in C häufig aus einem Satz von Headern und Feldern besteht, die im Arbeitsspeicher verteilt sein können, implementiert die **WriteLogRecord-Methode** eine Gather-Funktion, die das Kopieren von Daten reduziert.

> [!Note]  
> Sie sollten keine Benutzerzeigertypen innerhalb von Datenstrukturen in einem Protokolldatensatz verwenden. Zeiger sind während der Wiederherstellungsphase nicht mehr gültig, da der CRM-Kompensator in einem anderen Prozess ausgeführt wird als der CRM-Worker, der den Protokolldatensatz geschrieben hat. Das Aufnehmen von Zeigertypen in einen Protokolldatensatz kann dazu führen, dass eine Anwendung während der Wiederherstellung abstürzt oder beschädigt wird.

 

Beide Schreibmethoden schreiben einen Protokolldatensatz auf den Datenträger, garantieren jedoch nicht die Dauerhaftigkeit des Datensatzes. Auch wenn verzögerte Schreibvorgänge vor dem Erzwingen auf den Datenträger die Leistung verbessern können, können Sie stattdessen die [**ICrmLogControl::ForceLog-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) verwenden, um zu gewährleisten, dass alle vom CRM durchgeführten Schreibvorgänge dauerhaft auf dem Datenträger gespeichert werden, was für die Wiederherstellung von Fehlern wichtig ist.

Wenn der CRM-Worker seine Aktionen abgeschlossen und das Schreiben und Erzwingen von Datensätzen in das Protokoll abgeschlossen hat, muss [**er ICrmLogControl veröffentlichen.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) Wenn die Transaktion abgeschlossen ist (in der Regel aufgrund der Anwendungskomponente, die [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) oder [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)aufruft), erstellt die CRM-Infrastruktur die CRM-Kompensatorkomponente, die entweder die [**ICrmCompensator-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) oder die [**ICrmCompensatorVariants-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) implementiert. Diese Schnittstellen werden verwendet, um die unstrukturierten (Visual C++) oder strukturierten (Visual Basic)-Datensätze zusammen mit den Transaktionsergebnisbenachrichtigungen an den CRM-Kompensator zu übergeben.

Der CRM-Kompensator wird zuerst über die Vorbereitungsphase des Transaktionsabschlusses benachrichtigt und kann entweder mit Ja oder Nein für die Vorbereitungsanforderung abstimmen. Wenn der CRM-Kompensator mit "Nein" abstimme, erhält er keine weiteren Abbruchbenachrichtigungen. Wenn sie der Vorbereitungsanforderung mit Ja zustimme, empfängt sie entweder die Commit- oder Abbruchbenachrichtigungen. Im Fall eines Clientabbruchs werden keine Vorbereitungsbenachrichtigungen empfangen, sondern nur Benachrichtigungen zum Abbrechen. Der CRM-Kompensator muss darauf vorbereitet sein, all diese Fälle zu verarbeiten, und er muss auch den Fall behandeln, in dem keine Protokolldatensätze erfolgreich vom CRM-Worker geschrieben wurden. Der CRM-Kompensator darf nicht davon ausgehen, dass dieselbe CRM-Kompensatorinstanz sowohl die Benachrichtigungen in Phase 1 (Vorbereitung) als auch in Phase 2 (Commit oder Abbruch) erhält, da diese durch die Wiederherstellung unterbrochen werden könnten.

In der Regel verwendet ein CRM-Kompensator die Abbruchbenachrichtigung, um die Aktion umzukehren, die vom CRM-Worker ausgeführt wurde. Der CRM-Worker kann einen Zustand verfügbar lassen, falls er seine Aktion umkehren muss. Dieser Zustand kann vollständig in den Protokolldatensätzen enthalten sein. Ander denn, der CRM-Kompensator muss diesen Zustand bereinigt, wenn die Transaktion einen Commit ausgeführt. Aus diesem Grund empfängt der CRM-Kompensator die Commitbenachrichtigung. Der CRM-Kompensator wird nicht unter einer DTC-Transaktion ausgeführt.

Der CRM-Kompensator kann bei Bedarf neue Datensätze protokollieren, indem er [**ICrmLogControl verwendet,**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)das beim Erstellen empfangen wird. Sowohl der CRM-Worker als auch der CRM-Kompensator können auch den letzten von ihnen geschriebenen Protokolldatensatz vergessen. Dies kann erforderlich sein, um eine unnötige Wiederherstellung zu vermeiden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Compensating Resource Manager Concepts](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[COM+-CRM- Start und -Wiederherstellung](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



