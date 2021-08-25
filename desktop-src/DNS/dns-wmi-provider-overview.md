---
title: Übersicht über den DNS-WMI-Anbieter
description: Ein Anbieter ist ein Architekturelement der Windows Management Instrumentation (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Domain Name System, WMI-Anbieter, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44103edba64a1f572beef9cff9b8aeb31f02344f172f42b2a7378a6fbf3677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913160"
---
# <a name="dns-wmi-provider-overview"></a>Übersicht über den DNS-WMI-Anbieter

Ein Anbieter ist ein Architekturelement von *Windows Management Instrumentation (WMI).* WMI definiert eine einheitliche Architektur zum Beschreiben, Zugreifen auf und Instrumentieren von Objekten. Teil dieser Architektur ist eine große Datenbank mit WMI-Klassen, die zum Ausführen von Remoteverwaltungsaufgaben für bestimmte Objekte verwendet werden.

WMI-Anbieter fungieren als Vermittler zwischen WMI und mindestens einem verwalteten Objekt. Wenn WMI eine Anforderung von einer Verwaltungsanwendung für Daten empfängt, die nicht aus dem CIM-Repository verfügbar sind, oder für Benachrichtigungen über Ereignisse, die von WMI nicht unterstützt werden, wird die Anforderung an einen Anbieter weitergeleitet. Anbieter stellen Daten und Ereignisbenachrichtigungen für verwaltete Objekte bereit, die für die jeweilige Domäne spezifisch sind. Ein Anbieter erweitert das WMI-Schema von Klassen, damit WMI mit neuen Objekttypen arbeiten kann. Der DNS-WMI-Anbieter definiert Klassen zum Abfragen und Konfigurieren eines DNS-Servers sowie die zugehörigen DNS-Zonen und DNS-Einträge.

Der DNS-WMI-Anbieter macht eine Reihe von DNS-Objekten für Clients verfügbar, einschließlich DNS-Server, DNS-Domäne und DNS-RR-Objekten. Über diese Objekte können Clients DNS-Verwaltungsaktivitäten ausführen.

Mithilfe des DNS-WMI-Anbieters können Sie eigene Tools erstellen, um die meisten DNS-Serververwaltungsaufgaben auszuführen. Beispielsweise können Sie Zonen und Datensätze erstellen, löschen und anzeigen. Zurücksetzen von Server- und Zoneneigenschaften; und führen Routinemäßige Verwaltungsvorgänge aus, z. B. Aktualisieren der Zone, erneutes Laden der Zone, Aktualisieren der Zone, Zurückschreiben der Zone in eine Datei oder Active Directory, Anhalten und Fortsetzen der Zone, Löschen des Caches, Beenden und Starten des DNS-Diensts und Anzeigen von Statistiken.

Der DNS-WMI-Anbieter verfügt über eine Reihe eindeutiger Verhaltensweisen, die in anderen Anbietern nicht gefunden werden. Klassendetails finden Sie in der [DNS-WMI-Anbieterreferenz.](dns-wmi-provider-reference.md)

 

 




