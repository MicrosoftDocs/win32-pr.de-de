---
description: Com+-CRM-Betriebs Prozess
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: Com+-CRM-Betriebs Prozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39dba3dedcbdefebe0f62144547ebb6985fa51f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861636"
---
# <a name="com-crm-operating-process"></a>Com+-CRM-Betriebs Prozess

Im normalen Betrieb würde eine Anwendungs Komponente, die in einem Server Anwendungsprozess ausgeführt wird, ein com+-CRM verwenden, indem ein CRM-Worker erstellt wird. Der CRM-Worker implementiert eine spezifische com-Schnittstelle für den Task, der durchgeführt werden soll. Die Anwendungs Komponente muss unter einer Transaktion ausgeführt werden, damit der CRM-Worker die Transaktion der Anwendungs Komponente erbt. CRM-Worker benötigen immer eine Transaktion.

Für den Zugriff auf com+ CRM erhält der CRM-Worker zunächst die [**icrmlogcontrol**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) -Schnittstelle, die es dem CRM-Worker ermöglicht, Datensätze in das permanente Protokoll zu schreiben. Der CRM-Worker erhält diese Schnittstelle, indem er eine CRM Clerk-Komponente erstellt.

Als nächstes muss der CRM-Worker dem CRM-Clerk den Namen des CRM-kompenators mitteilen, den er verwenden möchte. Dies erfolgt durch Aufrufen der [**icrmlogcontrol:: RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) -Methode. Nachdem diese Methode aufgerufen wurde, wird der CRM-Compensator von der CRM-Infrastruktur erstellt, wenn die Transaktion abgeschlossen ist.

Nachdem der CRM-Worker seinen CRM-Kompensierungs Dienst registriert hat, kann er mithilfe von [**icrmlogcontrol**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)Datensätze in das CRM-Protokoll schreiben. Der CRM-Worker muss in den *Schreibvorgang schreiben*. Das heißt, es muss einen Datensatz in das Protokoll schreiben, der eine Aktion beschreibt, bevor die Aktion ausgeführt wird, falls ein Absturz unmittelbar nach dem Abschließen der Aktion auftritt. Ohne diese Write-Ahead-Protokolldaten Sätze gibt es keine Möglichkeit, für die Aktion zu korrigieren.

Außerdem bedeutet Write Ahead, dass der CRM-Compensator, der die Komponente ist, die die Protokolldaten Sätze bei der Wiederherstellung empfängt, den Fall behandeln muss, in dem die Protokolldaten Sätze geschrieben wurden, aber die Aktion nicht tatsächlich durchgeführt wurde. Aktionen durch den CRM-kompenerer müssen *idempotent* sein. Das heißt, Sie sollten in der Lage sein, mehrmals ausgeführt zu werden, sollten aber zu demselben Ergebnis führen. Beispielsweise ist das Festlegen eines Konto Ausgleichs auf den Wert $100 eine idempotente Aktion. das Hinzufügen von $100 zum Konto Saldo ist nicht.

Die [**icrmlogcontrol**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) -Schnittstelle stellt die folgenden beiden Methoden zum Schreiben von Protokolldaten Sätzen bereit:

-   [**Writelogrecordvariant**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) wird zum Schreiben eines strukturierten Protokolldaten Satzes verwendet, der als eine Sammlung von Varianten erstellt wurde. Dies ist in erster Linie für die Verwendung bei der Entwicklung von CRMs in Microsoft Visual Basic.
-   [**Writelogrecord**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) wird zum Schreiben eines unstrukturierten Protokolldaten Satzes als blobbyte verwendet. Dies ist in erster Linie für die Verwendung bei der Entwicklung von CRMs in Microsoft Visual C++. Da Datensatzstrukturen in C häufig aus einem Satz von Headern und Feldern bestehen, die möglicherweise im Speicher verstreut sind, implementiert die Methode " **Write telogrecord** " eine Sammel Funktion, die das Kopieren von Daten reduziert.

> [!Note]  
> Sie sollten keine Zeiger Typen innerhalb von Datenstrukturen in einem Protokolldaten Satz finden. Zeiger sind während der Wiederherstellungs Phase nicht mehr gültig, da der CRM-Compensator in einem anderen Prozess als der CRM-Worker ausgeführt wird, der den Protokolldaten Satz geschrieben hat. Das Einschließen von Zeiger Typen in einen Protokolldaten Satz kann dazu führen, dass eine Anwendung während der Wiederherstellung abstürzt oder beschädigt wird.

 

Beide Schreib Methoden schreiben einen Protokolldaten Satz auf den Datenträger, gewährleisten aber nicht die Dauerhaftigkeit des Datensatzes. Obwohl das Zulassen von verzögerten Schreibvorgängen vor dem erzwingen auf die Festplatte die Leistung verbessern kann, können Sie stattdessen die [**icrmlogcontrol:: ForceLog**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) -Methode verwenden, um sicherzustellen, dass alle vom CRM ausgeführten Schreibvorgänge auf dem Datenträger dauerhaft sind.

Wenn der CRM-Worker mit seinen Aktionen fertig ist und das Schreiben und Erzwingen von Datensätzen im Protokoll abgeschlossen hat, muss er [**icrmlogcontrol**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)freigeben. Wenn die Transaktion abgeschlossen ist (in der Regel aufgrund der Anwendungs Komponente [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) oder [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)), erstellt die CRM-Infrastruktur die CRM-compensatorkomponente, die entweder die [**icrmcompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) -Schnittstelle oder die [**icrmcompensatorvarianten**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) -Schnittstelle implementiert. Diese Schnittstellen werden verwendet, um die unstrukturierten (Visual C++) oder strukturierten (Visual Basic) Datensätze zusammen mit den Transaktions Ergebnis Benachrichtigungen an den CRM-kompenerer zu übergeben.

Der CRM-kompenerer wird zuerst über die Vorbereitungsphase des Transaktions Abschlusses benachrichtigt und kann für die Vorbereitungs Anforderung entweder yes oder No abstimmen. Wenn der CRM-Compensator die Stimme Nein abbricht, empfängt er keine weiteren Abbruch Benachrichtigungen. Wenn ja für die Prepare-Anforderung Stimmen, empfängt es entweder die Commit-oder Abbruch Benachrichtigungen. Bei einem Client Abbruch werden keine Vorbereitungs Benachrichtigungen empfangen, sondern nur Abbruch Benachrichtigungen. Der CRM-kompenerer muss darauf vorbereitet sein, alle diese Fälle zu verarbeiten, und er muss auch den Fall behandeln, in dem keine Protokolldaten Sätze erfolgreich vom CRM-Worker geschrieben wurden. Der CRM-Compensator darf nicht davon ausgehen, dass dieselbe CRM-kompenatorinstanz die Benachrichtigungen Phase 1 (Vorbereitung) und Phase 2 (Commit oder Abbruch) empfängt, da diese durch die Wiederherstellung unterbrochen werden könnten.

In der Regel verwendet ein CRM-Compensator die Abbruch Benachrichtigung, um die vom CRM-Worker ausgeführte Aktion umzukehren. Der CRM-Worker kann einen Zustand verfügbar machen, wenn er seine Aktion umkehren muss. Dieser Zustand ist möglicherweise vollständig in den Protokolldaten Sätzen enthalten. andernfalls muss der CRM-Compensator diesen Zustand bereinigen, wenn für die Transaktion ein Commit ausgeführt wird. Dies ist der Grund, warum der CRM-Compensator die Commit-Benachrichtigung empfängt. Der CRM-kompenerer wird nicht unter einer DTC-Transaktion ausgeführt.

Der CRM-Kompensierungs Dienst kann bei Bedarf neue Datensätze protokollieren, indem er [**icrmlogcontrol**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)verwendet, der während der Erstellung empfangen wird. Der CRM-Worker und der CRM-kompenerer können auch den letzten Protokolldaten Satz vergessen, den Sie geschrieben haben. Dies kann erforderlich sein, um eine unnötige Wiederherstellung zu vermeiden

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Com+-CRM-Start und-Wiederherstellung](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



