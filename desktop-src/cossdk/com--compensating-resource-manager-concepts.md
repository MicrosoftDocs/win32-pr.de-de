---
description: Sie können COM+ Compensating Resource Manager (CRM) verwenden, um Anwendungsressourcen einfach und schnell in Microsoft Distributed Transaction Coordinator (DTC)-Transaktionen zu integrieren.
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: COM+ Compensating Resource Manager Concepts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b546f10e9a99f827c512e6dd7662ead05476774f7ff8dc32c40fa123b0ffe272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047628"
---
# <a name="com-compensating-resource-manager-concepts"></a>COM+ Compensating Resource Manager Concepts

Sie können COM+ Compensating Resource Manager (CRM) verwenden, um Anwendungsressourcen einfach und schnell in Microsoft Distributed Transaction Coordinator (DTC)-Transaktionen zu integrieren. Ihre Anwendungsressourcen können über das Ergebnis einer Transaktion abstimmen und eine endgültige Benachrichtigung über das Ergebnis erhalten. Ein dauerhaftes Protokoll wird generiert, damit Ihre Anwendungsressourcen Datensätze schreiben können, die Fehler überstehen, und crm stellt diese Protokolldatei wieder auf, wenn die Anwendung neu gestartet wird.

Ein CRM besteht aus den folgenden beiden Komponenten:

-   CRM-Worker. Diese Komponente führt die Hauptarbeit des spezifischen CRM aus und implementiert eine schnittstelle, die für die aufgabe spezifisch ist, die sie ausführen muss. Die CRM-Infrastruktur stellt eine Schnittstelle für den CRM-Worker bereit, über die der CRM-Worker Datensätze in eine dauerhafte Protokolldatei auf dem Datenträger schreiben kann. Der CRM-Worker muss Datensätze in das Protokoll schreiben und dauerhaft machen, bevor er seine Arbeit ausführt, damit bei einem Absturz die Wiederherstellung ordnungsgemäß erfolgen kann. Der CRM-Worker erfordert immer eine Transaktion.
-   CRM-Kompensator. Diese Komponente wird nach Abschluss der Transaktion von der CRM-Infrastruktur erstellt. Es implementiert eine definierte Schnittstelle, über die die CRM-Infrastruktur Benachrichtigungen über den Abschluss der Transaktion und die Protokolldatensätze, die zuvor vom CRM-Worker geschrieben wurden, übergeben kann.

Ein COM+-CRM bietet Atomarität mit Transaktionsbenachrichtigungen und Dauerhaftigkeit mit dem CRM-Protokoll, bietet jedoch keine Isolation von Ressourcen. In einer Multithreadumgebung liegt es in der Verantwortung des CRM-Entwicklers, sicherzustellen, dass der Zugriff auf Ressourcen , entweder durch mehrere CRM-Mitarbeiter oder externe Anwendungen, während einer Transaktion serialisiert wird.

Nachdem die Transaktion die Vorbereitungsphase bestanden hat, können crm compensator und CRM Workers gleichzeitig ausgeführt werden. Es ist möglich, dass die CRM Worker-Komponente einer neuen Transaktion aktiv wird, während der CRM-Kompensator einer vorherigen Transaktion die vorherige Transaktion noch verarbeitet.

Bei Fehlern vor der Wiederherstellung der CRM-Serveranwendung sollte eine unterbrochene Transaktion als aktiv und nicht abgeschlossen betrachtet werden. Externe Prozesse sollten nicht auf die Ressourcen zugreifen können, die von dieser bestimmten Transaktion vor der Wiederherstellung des CRM-Serverprozesses geändert wurden.

Das CRM definiert drei Schnittstellentypen für die grundlegenden CRM-Funktionen:

-   [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) wird auf dem CRM-Clerk implementiert und vom CRM-Worker verwendet, um Protokolldatensätze in das Protokoll zu schreiben. Sie kann auch vom CRM-Kompensator verwendet werden.
-   [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) und [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) werden auf dem CRM-Kompensator implementiert. Diese Schnittstellen werden verwendet, um Transaktionsergebnisbenachrichtigungen und die zugehörigen Protokolldatensätze an den CRM-Kompensator zu senden. Normalerweise implementiert der CRM-Kompensator nur eine dieser Schnittstellen, je nachdem, ob unstrukturierte oder strukturierte Protokolldatensätze erforderlich sind. *Strukturierte Protokolldatensätze* sind datensätze, die als Sammlung von Varianten erstellt werden und in der Regel von Microsoft-Visual Basic. *Unstrukturierte Protokolldatensätze* sind nur ein Bytepuffer und werden in der Regel von Microsoft Visual C++. Ein CRM-Kompensator kann beide Kompensatorschnittstellen implementieren. es wird jedoch immer nur eine nach der anderen verwendet, um Protokolldatensätze zu liefern.
-   Die COM+-CRM-Überwachungsschnittstellen werden zum Überwachen der CRMs innerhalb einer bestimmten Serveranwendung verwendet. Ausführliche Informationen zu den Überwachungsschnittstellen finden Sie unter [COM+ CRM-Überwachungsschnittstellen.](com--crm-monitoring-interfaces.md)

Die folgenden Themen in diesem Abschnitt enthalten weitere Details zum COM+-CRM-Dienst:

-   [Sicherheitsüberlegungen zu COM+ CRM](com--crm-security-considerations.md)
-   [COM+-CRM-Betriebsvorgang](com--crm-operating-process.md)
-   [COM+-CRM- Start und -Wiederherstellung](com--crm-startup-and-recovery.md)
-   [Verwenden von COM+ CRM in einer Clusterumgebung](using-the-com--crm-in-a-cluster-environment.md)
-   [Fehlerbehandlung in COM+ CRM](error-handling-in-the-com--crm.md)
-   [COM+-CRM-Einstellungen](com--crm-registry-settings.md)
-   [Problembehandlung für COM+ CRM](troubleshooting-the-com--crm.md)
-   [Entwurfsvorschläge für die Entwicklung eines COM+-CRM](design-suggestions-for-developing-a-com--crm.md)
-   [COM+-CRM-Überwachungsschnittstellen](com--crm-monitoring-interfaces.md)
-   [COM+-CRM-Schnittstellen](com--crm-interfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Compensating Resource Manager Tasks](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



