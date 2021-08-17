---
description: COM+-CRM- Start und -Wiederherstellung
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: COM+-CRM- Start und -Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f65b8b1e32f2b587f7c288c6c5147ef30148360e89fc0a04ac952c8630076e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129192"
---
# <a name="com-crm-startup-and-recovery"></a>COM+-CRM- Start und -Wiederherstellung

Wenn für eine  Serveranwendung das Kontrollkästchen Kompensierende Ressourcen-Manager aktivieren aktiviert ist  (mithilfe des Komponentendienste-Verwaltungstools auf der Registerkarte Erweitert der Eigenschaftenseite der COM+-Anwendung), erstellt sie beim ersten Start eine CRM-Protokolldatei, die von allen CRMs in diesem Serveranwendungsprozess verwendet werden kann. (Ausführliche Anweisungen zum Konfigurieren des CRM finden Sie unter [Configuring COM+ CRM Components](configuring-com--crm-components.md).)

Der Name der CRM-Protokolldatei, die für die Serveranwendung erstellt wurde, basiert auf der AppId (einer GUID) der Serveranwendung, und die CRM-Protokolldatei wird im gleichen Verzeichnis wie die DTC-Protokolldatei gespeichert (normalerweise Ihr Verzeichnis %SystemRoot% \\ winnt \\ system32 \\ DtcLog). CRM-Protokolldateien haben die Erweiterung .crmlog.

> [!Note]  
> Es kann erforderlich sein, den Standardspeicherort einer CRM-Protokolldatei aus Leistungsgründen (um die DTC-Protokolldatei auf einem anderen Datenträger als die CRM-Protokolldatei zu speichern) oder möglicherweise aufgrund der Verwendung des CRM in einer Clusterumgebung zu ändern. Der Speicherort der CRM-Protokolldateien kann mit dem COM+-Verwaltungs-SDK geändert werden. Der Eigenschaftenname ist CRMLogFile und im [**Sammlungsobjekt Applications**](applications.md) vorhanden.

 

Wenn eine Serveranwendung (die CRM-fähig ist) gestartet wird und ermittelt, dass bereits eine CRM-Protokolldatei für diese Serveranwendung vorhanden ist, wird die Wiederherstellung für diese CRM-Protokolldatei ausgeführt. *Bei der* Wiederherstellung werden alle Transaktionen abgeschlossen, die durch einen Fehler unterbrochen wurden. Die CRM-Infrastruktur liest die CRM-Protokolldatei für alle Transaktionen, die nicht vollständig abgeschlossen wurden. Wenn eine gefunden wird, kontaktiert sie den DTC, um das Transaktionsergebnis zu bestimmen. Anschließend wird der CRM-Kompensator erstellt und die Commit- oder Abbruchbenachrichtigungen nach Bedarf zusammen mit den zugeordneten Protokolldatensätzen übergibt.

Vorbereitungsbenachrichtigungen werden während der Wiederherstellung nicht vom CRM-Kompensator empfangen. Der CRM-Kompensator verfügt über ein Flag, um zu unterscheiden, ob er während des normalen Betriebs oder während der Wiederherstellung aufgerufen wird.

Die Wiederherstellung findet in der Regel nur dann nicht vervollständigte Transaktionen, wenn die Serveranwendung aufgrund eines Absturzes des Serveranwendungsprozesses oder eines Computerabsturzes nicht normal heruntergefahren wurde. Wenn die Serveranwendung normal heruntergefahren werden darf, entweder aufgrund des Leerlauf-Time outs oder des manuellen Herunterfahrens über das Verwaltungstool der Komponentendienste, wird die Protokolldatei bereinigt.

Das Starten einer CRM-Serveranwendung für die Wiederherstellung wird nicht automatisch initiiert. Es muss eine externe Aktion ausgeführt werden, um die CRM-Serveranwendung zu starten, bei der eine Wiederherstellung erforderlich ist. In der Regel würde dies das Erstellen einer Komponente in dieser Serveranwendung sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Compensating Resource Manager Concepts](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[COM+-CRM-Betriebsvorgang](com--crm-operating-process.md)
</dt> </dl>

 

 



