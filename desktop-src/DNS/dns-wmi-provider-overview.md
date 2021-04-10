---
title: DNS WMI-Anbieter (Übersicht)
description: Ein Anbieter ist ein Architektur Element von Windows-Verwaltungsinstrumentation (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Domain Name System, WMI-Anbieter, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036833"
---
# <a name="dns-wmi-provider-overview"></a>DNS WMI-Anbieter (Übersicht)

Ein Anbieter ist ein Architektur Element von *Windows-Verwaltungsinstrumentation (WMI)*. WMI definiert eine einheitliche Architektur zum beschreiben, zugreifen auf und Instrumentieren von Objekten. Ein Teil dieser Architektur ist eine große Datenbank von WMI-Klassen, die zum Ausführen von Remote Verwaltungsaufgaben für bestimmte Objekte verwendet werden.

WMI-Anbieter fungieren als Vermittler zwischen WMI und einem oder mehreren verwalteten Objekten. Wenn WMI eine Anforderung von einer Verwaltungs Anwendung für Daten empfängt, die nicht im CIM-Repository verfügbar sind, oder für Benachrichtigungen von Ereignissen, die von WMI nicht unterstützt werden, wird die Anforderung an einen Anbieter weitergeleitet. Anbieter stellen Daten und Ereignisbenachrichtigungen für verwaltete Objekte bereit, die für die jeweilige Domäne spezifisch sind. Ein Anbieter erweitert das WMI-Schema der Klassen, damit WMI mit neuen Objekttypen arbeiten kann. Der DNS-WMI-Anbieter definiert Klassen zum Abfragen und Konfigurieren eines DNS-Servers sowie die zugehörigen DNS-Zonen und DNS-Einträge.

Der DNS-WMI-Anbieter macht für Clients eine Reihe von DNS-Objekten verfügbar, einschließlich DNS-Server, DNS-Domäne und DNS-RR-Objekten. Über diese Objekte können Clients DNS-Verwaltungsaktivitäten durchführen.

Mit dem DNS-WMI-Anbieter können Sie eigene Tools erstellen, um die meisten Verwaltungsaufgaben für DNS-Server auszuführen. Beispielsweise können Sie Zonen und Datensätze erstellen, löschen und anzeigen. Server-und Zonen Eigenschaften zurücksetzen; und führen routinemäßige Verwaltungsvorgänge aus, z. b. das Aktualisieren der Zone, das erneute Laden der Zone, das Aktualisieren der Zone, das Zurückschreiben der Zone in eine Datei oder Active Directory, das Anhalten und Fortsetzen der Zone, das Löschen des Caches, das Beenden und Starten des DNS-Dienstes und das Anzeigen von Statistiken.

Der DNS-WMI-Anbieter verfügt über eine Reihe eindeutiger Verhalten, die in anderen Anbietern nicht gefunden wurden. Klassen Details finden Sie in der [DNS-WMI-Anbieter Referenz](dns-wmi-provider-reference.md) .

 

 




