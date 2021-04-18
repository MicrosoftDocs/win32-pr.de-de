---
description: Com+-CRM-Start und-Wiederherstellung
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Com+-CRM-Start und-Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345457"
---
# <a name="com-crm-startup-and-recovery"></a>Com+-CRM-Start und-Wiederherstellung

Wenn für eine Serveranwendung das Kontrollkästchen **kompensierende Ressourcen-Manager aktivieren aktiviert** ist (mithilfe des Verwaltungs Programms Komponenten Dienste auf der Registerkarte **erweitert** auf der Eigenschaften Seite der com+-Anwendung), wird beim ersten Start eine CRM-Protokolldatei erstellt, die von allen CRMs in diesem Server Anwendungsprozess verwendet werden kann. (Ausführliche Anweisungen zum Konfigurieren des CRM finden Sie unter [Konfigurieren von com+ CRM-Komponenten](configuring-com--crm-components.md).)

Der Name der CRM-Protokolldatei, die für die Serveranwendung erstellt wurde, basiert auf der APP-ID (GUID) der Serveranwendung, und die CRM-Protokolldatei befindet sich im gleichen Verzeichnis wie die DTC-Protokolldatei (normalerweise das Verzeichnis% systemroot% \\ Winnt \\ system32 \\ dtclog). CRM-Protokolldateien haben die Erweiterung ". crmlog".

> [!Note]  
> Möglicherweise ist es erforderlich, den Standard Speicherort einer CRM-Protokolldatei aufgrund von Leistungsgründen (um die DTC-Protokolldatei auf einem anderen Datenträger als die CRM-Protokolldatei zu speichern) oder möglicherweise aufgrund der Verwendung von CRM in einer Cluster Umgebung zu ändern. Der Speicherort der CRM-Protokolldateien kann mit dem com+-Verwaltungs-SDK geändert werden. Der Eigenschaftsname ist crmlogfile und ist im [**Anwendungs**](applications.md) Sammlungsobjekt vorhanden.

 

Wenn eine Serveranwendung (die CRM-fähig ist) gestartet wird und feststellt, dass bereits eine CRM-Protokolldatei für diese Serveranwendung vorhanden ist, führt Sie eine Wiederherstellung für diese CRM-Protokolldatei aus. Bei der *Wiederherstellung* werden alle Transaktionen abgeschlossen, die durch einen Fehler unterbrochen wurden, und die CRM-Infrastruktur umfasst die CRM-Protokolldatei für Transaktionen, die nicht vollständig abgeschlossen wurden. Wenn eine beliebige gefunden wird, kontaktiert Sie den DTC, um das Transaktions Ergebnis zu ermitteln. Anschließend wird der CRM-Compensator erstellt, und die Commit-oder Abbruch Benachrichtigungen werden zusammen mit den zugehörigen Protokolldaten Sätzen nach Bedarf übergeben.

Vorbereitungs Benachrichtigungen werden während der Wiederherstellung nicht vom CRM-kompenerer empfangen. Der CRM-kompenerer verfügt über ein Flag, um zu unterscheiden, ob es während des normalen Betriebs oder während der Wiederherstellung aufgerufen wird.

Die Wiederherstellung findet in der Regel nur dann nicht abgeschlossene Transaktionen, wenn die Serveranwendung aufgrund eines Absturzes eines Server Anwendungsprozesses oder eines Computer Absturzes nicht ordnungsgemäß heruntergefahren wurde. Wenn die Serveranwendung aufgrund des Leerlauf Timeouts oder durch manuelles Herunterfahren über das Verwaltungs Programmkomponenten Dienste normal heruntergefahren werden darf, ist die Protokolldatei bereinigt.

Das Starten einer CRM-Serveranwendung für die Wiederherstellung wird nicht automatisch initiiert. Zum Starten der CRM-Serveranwendung, bei der eine Wiederherstellung erforderlich ist, müssen einige externe Aktionen durchgeführt werden. In der Regel wird dadurch eine Komponente in dieser Serveranwendung erstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Com+-CRM-Betriebs Prozess](com--crm-operating-process.md)
</dt> </dl>

 

 



