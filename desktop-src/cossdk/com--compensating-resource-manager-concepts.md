---
description: Sie können das com+-kompensierende Ressourcen-Manager (CRM) verwenden, um Anwendungs Ressourcen einfach und schnell in Microsoft Distributed Transaction Coordinator (DTC)-Transaktionen zu integrieren.
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: Kompensierende com+-Ressourcen-Manager Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14206a54ffcb4f7e06ddf7362736a722393b0791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958359"
---
# <a name="com-compensating-resource-manager-concepts"></a>Kompensierende com+-Ressourcen-Manager Konzepte

Sie können das com+-kompensierende Ressourcen-Manager (CRM) verwenden, um Anwendungs Ressourcen einfach und schnell in Microsoft Distributed Transaction Coordinator (DTC)-Transaktionen zu integrieren. Ihre Anwendungs Ressourcen können über das Ergebnis einer Transaktion abstimmen und können eine abschließende Benachrichtigung über das Ergebnis erhalten. Ein dauerhaftes Protokoll wird generiert, damit Ihre Anwendungs Ressourcen Datensätze schreiben können, die Fehler überstehen, und das CRM diese Protokolldatei wiederherstellt, wenn die Anwendung neu gestartet wird.

Ein CRM besteht aus den folgenden zwei Komponenten:

-   CRM-Worker. Diese Komponente führt die Hauptarbeit des jeweiligen CRM durch und implementiert eine Schnittstelle, die für die Aufgabe spezifisch ist, die Sie ausführen muss. Die CRM-Infrastruktur stellt eine Schnittstelle für den CRM-Worker bereit, über den der CRM-Worker Datensätze in eine permanente Protokolldatei auf dem Datenträger schreiben kann. Der CRM-Worker muss Datensätze in das Protokoll schreiben und Sie dauerhaft machen, bevor er seine Arbeit durchführt, sodass die Wiederherstellung bei Auftreten eines Absturzes ordnungsgemäß durchgeführt werden kann. Der CRM-Worker benötigt immer eine Transaktion.
-   CRM-kompenator. Diese Komponente wird nach Abschluss der Transaktion von der CRM-Infrastruktur erstellt. Es implementiert eine definierte Schnittstelle, mit der die CRM-Infrastruktur Benachrichtigungen über den Abschluss der Transaktion und die Protokolldaten Sätze, die zuvor vom CRM-Worker geschrieben wurden, übergeben kann.

Ein com+-CRM bietet Atomizität bei Transaktions Benachrichtigungen und Beständigkeit mit dem CRM-Protokoll, bietet aber keine Isolation von Ressourcen. In einer Multithreadumgebung liegt es in der Verantwortung des CRM-Entwicklers, sicherzustellen, dass der Zugriff auf Ressourcen von mehreren CRM-Workern oder externen Anwendungen während einer Transaktion serialisiert wird.

Nachdem die Transaktion die Vorbereitungsphase überschritten hat, können CRM-kompenatormitarbeiter und CRM-Worker gleichzeitig ausgeführt werden. Es ist möglich, dass die CRM-Worker-Komponente einer neuen Transaktion aktiv wird, während der CRM-Compensator einer vorherigen Transaktion noch die vorherige Transaktion verarbeitet.

Bei Fehlern vor der Wiederherstellung der CRM-Serveranwendung sollte eine unterbrochene Transaktion als aktiv betrachtet und nicht abgeschlossen werden. Externe Prozesse sollten vor der Wiederherstellung des CRM-Server Prozesses nicht auf die Ressourcen zugreifen können, die von dieser speziellen Transaktion geändert wurden.

Das CRM definiert drei Schnittstellentypen für die grundlegenden CRM-Funktionen:

-   [**Icrmlogcontrol**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) ist auf dem CRM Clerk implementiert und wird vom CRM-Worker verwendet, um Protokolldaten Sätze in das Protokoll zu schreiben. Sie kann auch vom CRM-kompenator verwendet werden.
-   [**Icrmcompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) und [**icrmcompensatorvarianten**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) werden auf dem CRM-kompenator implementiert. Diese Schnittstellen werden verwendet, um Transaktions Ergebnis Benachrichtigungen und die zugehörigen Protokolldaten Sätze an den CRM-kompenerer zu übermitteln. Normalerweise implementiert der CRM-Compensator nur eine dieser Schnittstellen, je nachdem, ob er unstrukturierte oder strukturierte Protokolldaten Sätze erforderte. *Strukturierte Protokolldaten Sätze* sind solche, die als eine Sammlung von Varianten erstellt werden und in der Regel von Microsoft Visual Basic verwendet werden. *Unstrukturierte Protokolldaten Sätze* sind nur ein Puffer von Bytes und werden in der Regel von Microsoft Visual C++ verwendet. Ein CRM-Kompensator kann beide kompenatorschnittstellen implementieren. für die Bereitstellung von Protokolldaten Sätzen wird jedoch immer nur jeweils ein verwendet.
-   Die com+-CRM-Überwachungsschnittstellen werden zum Überwachen der CRMs innerhalb einer bestimmten Serveranwendung verwendet. Ausführliche Informationen zu den Überwachungsschnittstellen finden Sie unter [com+ CRM-Überwachungsschnittstellen](com--crm-monitoring-interfaces.md).

Die folgenden Themen in diesem Abschnitt enthalten weitere Details zum com+ CRM-Dienst:

-   [Com+ CRM-Sicherheitsüberlegungen](com--crm-security-considerations.md)
-   [Com+-CRM-Betriebs Prozess](com--crm-operating-process.md)
-   [Com+-CRM-Start und-Wiederherstellung](com--crm-startup-and-recovery.md)
-   [Verwenden des com+-CRM in einer Cluster Umgebung](using-the-com--crm-in-a-cluster-environment.md)
-   [Fehlerbehandlung in com+ CRM](error-handling-in-the-com--crm.md)
-   [Com+ CRM-Registrierungs Einstellungen](com--crm-registry-settings.md)
-   [Problembehandlung bei com+ CRM](troubleshooting-the-com--crm.md)
-   [Entwurfsvorschläge für die Entwicklung eines com+ CRM](design-suggestions-for-developing-a-com--crm.md)
-   [Com+ CRM-Überwachungsschnittstellen](com--crm-monitoring-interfaces.md)
-   [Com+ CRM-Schnittstellen](com--crm-interfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Aufgaben](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



