---
description: Übersicht über die Eltern Steuerungs-API
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Übersicht über die Eltern Steuerungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366192"
---
# <a name="parental-controls-api-overview"></a>Übersicht über die Eltern Steuerungs-API

APIs, die für Eltern Steuerelemente verwendet werden, machen die Richtlinien-und EinstellungenEinstellungen sowie die Protokollierungs Funktionalität verfügbar

## <a name="settings"></a>Einstellungen

Es werden zwei öffentliche APIs bereitgestellt:

-   Eine vereinfachte com-basierte API für minimale Konformität (die als Kompatibilitäts-API bezeichnet wird), um zu bestimmen, ob die Protokollierung aktiviert werden soll. Außerdem werden einfache Methoden für Folgendes bereitgestellt:
    -   Das Abrufen des Einschränkungs Zustands für Webeinschränkungen, Zeitlimits, Spiele Einschränkungen und Anwendungs Einschränkungen.
    -   Die ID des aktiven Webinhalts Filters wird abgerufen.
    -   Festlegen, ob die Benutzeroberflächen Elemente des Anbieters auf eine Weise angezeigt werden sollen, die mit dem in einer Domäne verbundenen eingeblendeten ausblenden übereinstimmt.
    -   Der Zeitpunkt der letzten Änderung einer Einstellung für einen Benutzer wird abgerufen.
    -   Abrufen, ob Browser-oder Browser ähnliche Dateidownloads für einen Benutzer blockiert werden müssen, und die Möglichkeit, eine URL anzufordern, die für den Webinhalts Filter dieses Benutzers explizit zulässig ist.
    -   Es wird ermittelt, ob ein bestimmtes Spiel für einen Benutzer blockiert ist.
-   Windows-Verwaltungsinstrumentation (WMI)-API-Zugriff auf einen Eltern Steuerungs Namespace, um vollständigen Schreib-und Lesezugriff auf alle verfügbar gemachten Einstellungen zu erhalten. Mit der Jugendschutz Steuerung wird ein WMI-Anbieter bereitgestellt, um Lese-/Schreibberechtigungen für den zugrunde liegenden Einstellungs Speicher mit ordnungsgemäßer Erzwingung von Berechtigungen für Administratoren und kontrollierte Benutzer

ISVs werden aufgefordert, die Kompatibilitäts-API und ggf. die WMI-API zu verwenden, um die Einschränkungen für die untergeordnete Sicherheit basierend auf der Funktionalität der Anwendung oder Lösung zu steuern.

## <a name="logging"></a>Protokollierung

-   Die Aktivitäts Überwachung von Windows-Standard Ereignissen wird für die Überwachung von Eltern Steuerelementen verwendet. Das Windows Vista-Ereignis Berichterstattungs-und-Ablauf Verfolgungssystem hat gegenüber der früheren etw-Funktionalität (Event Tracing for Windows) eine bessere Leistung erzielt. Eltern Steuerelemente definieren einen eindeutigen Kanal für Ihre Daten in etw.
-   ISVs werden aufgefordert, die Ereignis Veröffentlichungs-API zum Protokollieren von Benutzeraktivitäten zu verwenden, wie im Abschnitt using Jugend Steuerungs-APIs angegeben.

 

 



