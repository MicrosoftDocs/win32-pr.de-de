---
description: Mehrere Registrierungs Einstellungen sind verfügbar, um das CRM-Verhalten zur Unterstützung bei der Problembehandlung und Entwicklung zu ändern.
ms.assetid: c4e68451-fb8a-45b5-9968-7d5a6418dfe8
title: Com+ CRM-Registrierungs Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0ea4ec245ab55b73c79660973824fcf33c6c2b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860868"
---
# <a name="com-crm-registry-settings"></a>Com+ CRM-Registrierungs Einstellungen

Mehrere Registrierungs Einstellungen sind verfügbar, um das CRM-Verhalten zur Unterstützung bei der Problembehandlung und Entwicklung zu ändern. Alle diese Registrierungs Einstellungen, die in der folgenden Tabelle aufgelistet und beschrieben werden, sind optional. für den normalen Betrieb von CRM sind keine erforderlich.

Alle CRM-Registrierungs Einstellungen befinden sich unter **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ COM3 \\ CRM**. Erstellen Sie den **CRM** -Schlüssel unter dem Schlüssel **COM3** , sofern er nicht bereits vorhanden ist.



| CRM-Registrierungs Einstellungen                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VTRACE1**<br/>                 | REG \_ DWORD-Wert. Wenn Sie diesen Wert auf einen anderen Wert als Null festlegen, werden Debug-Ablauf Verfolgungs Meldungen bei Warnungen oder Fehlern aktiviert. Diese Meldungen können im Ausgabefenster des Debuggers angezeigt werden. Dieser Wert sollte nur für die Entwicklung und nicht während der normalen Bereitstellung festgelegt werden. Dieser Wert wird gelesen, wenn eine CRM-Serveranwendung gestartet wird.<br/>                                                                                                                                                                                                                                                   |
| **Ignorecompensatorerrors**<br/> | REG \_ DWORD-Wert. Wenn dieser Wert auf einen anderen Wert als NULL festgelegt wird, kann die CRM-Infrastruktur alle von CRM-Kompensatoren zurückgegebenen Fehler ignorieren. Wenn die Wiederherstellung aufgrund eines Fehlers von einem CRM-kompenator fehlschlägt, kann durch Festlegen dieses Werts die Wiederherstellung abgeschlossen werden. Dieser Wert wird gelesen, wenn eine CRM-Serveranwendung gestartet wird.<br/>                                                                                                                                                                                                                                           |
| **Checkpointintervalinsec**<br/> | REG \_ DWORD-Wert. Dies ist das Prüf Punkt Intervall in Sekunden. Das Standard Prüf Punkt Intervall beträgt 30 Sekunden. Prüfpunkte werden verwendet, um Speicherplatz aus der CRM-Protokolldatei freizugeben. Das Erhöhen des Prüf Punkt Intervalls kann die Leistung erhöhen, aber auf Kosten einer erhöhten Wiederherstellungszeit und einer größeren CRM-Protokolldatei. Dieser Wert wird gelesen, wenn eine CRM-Serveranwendung gestartet wird.<br/>                                                                                                                                                                                                  |
| **Initizugfilesizin KB**<br/>  | REG \_ DWORD-Wert. Dies ist die anfängliche CRM-Protokolldatei Größe in Kilobyte. Die standardmäßige CRM-Protokolldatei Größe beträgt 1024 KB (1 MB). Die CRM-Protokolldatei wird automatisch erweitert, um die für Sie erzwungene Transaktions Last zu erfüllen. Wenn jedoch hohe Lasten zu erwarten sind, kann es erforderlich sein, diesen Wert zu erhöhen. Dieser Wert wird gelesen, wenn eine CRM-aktivierte COM+-Serveranwendung gestartet wird, aber wenn die CRM-Protokolldatei bereits für eine CRM-Serveranwendung vorhanden ist, wird dieser Wert für die Serveranwendung ignoriert.<br/>                                                                               |
| **Wiederherabtraceaktivierte**<br/>    | REG \_ DWORD-Wert. Wenn Sie diesen Wert auf einen anderen Wert als Null festlegen, wird eine Wiederherstellungs Ablauf Verfolgung aktiviert Die Wiederherstellungs Ablauf Verfolgung ist eine Textdatei mit dem gleichen Namen wie die CRM-Protokolldatei und der folgenden zusätzlichen Erweiterung: .recoverytrace.txt. <br/> Diese Datei befindet sich im gleichen Verzeichnis wie die CRM-Protokolldatei. Die Wiederherstellungs Ablauf Verfolgung bietet bei der Wiederherstellung eine Ablauf Verfolgung der CRM-Aktivität, die für die Problem Diagnose verwendet werden kann. Dieser Wert wird gelesen, wenn eine CRM-Serveranwendung gestartet wird. Allerdings wird für jede CRM-Serveranwendung eine eindeutige Ablauf Verfolgungs Datei für die Wiederherstellung erstellt.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 




