---
title: Datenbank des RPC-namens Dienstanbieter
description: Ein Namensdienst ist ein Dienst, der-Objekten Namen zuordnet und in der Regel die (Name, Object)-Paare in einer Datenbank verwaltet.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Name Service Database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471421"
---
# <a name="the-rpc-name-service-database"></a>Datenbank des RPC-namens Dienstanbieter

Ein Namensdienst ist ein Dienst, der-Objekten Namen zuordnet und in der Regel die (Name, Object)-Paare in einer Datenbank verwaltet. Im Allgemeinen ist der Name ein logischer Name, den Benutzer leicht merken und verwenden können. Beispielsweise kann ein Benutzer mit einem Namensdienst den logischen Namen "Laser Printer" verwenden. Der Namensdienst ordnet diesen Namen dem vom Druckserver verwendeten Netzwerk spezifischen Namen zu.

Um eine vereinfachte Erläuterung zu verwenden, ordnet der RPC-Namensdienst einem Bindungs handle einen Namen zu und verwaltet die Zuordnungen (Name, Bindungs handle) in der Datenbank des RPC-namens Dienstanbieter. Der RPC-Namensdienst ermöglicht es Client Anwendungen, anstelle einer bestimmten Protokoll Sequenz und Netzwerkadresse einen logischen Namen zu verwenden. Die Verwendung des logischen Namens erleichtert Netzwerkadministratoren die Installation und Konfiguration der verteilten Anwendung.

Ein RPC Name Service-Datenbankeintrag weist eines der folgenden Attribute auf: **Server**, **Gruppe** oder **Profil**. In der Microsoft-Implementierung können Einträge nur ein Attribut aufweisen, sodass diese Einträge auch als Server Einträge, Gruppen Einträge und Profil Einträge bezeichnet werden.

Der Server Eintrag besteht aus den Schnittstellen-UUIDs, den Objekt-UUIDs (erforderlich, wenn der Server mehrere Einstiegspunkte implementiert), der Netzwerkadresse, der Protokoll Sequenz und sämtlicher Endpunkt Informationen, die bekannten Endpunkten zugeordnet sind. Wenn ein dynamischer Endpunkt verwendet wird, werden die Endpunkt Informationen in der Datenbank der Endpunkt Zuordnung und nicht in der Name Service-Datenbank gespeichert, und der Endpunkt wird wie jeder andere dynamische Endpunkt aufgelöst. Server Einträge werden von Funktionen verwaltet, die mit dem Präfix "rpcnsbinding" beginnen.

Der Gruppen Eintrag kann Server Einträge oder andere Gruppen Einträge enthalten. Gruppen Einträge werden von Funktionen verwaltet, die mit dem Präfix "rpcnsgroup" beginnen.

Der Profil Eintrag kann Profil-, Gruppen-oder Server Einträge enthalten. Profil Einträge werden von den Funktionen verwaltet, die mit dem Präfix "rpcnsprofile" beginnen.

Dieser Abschnitt enthält eine Übersicht über die Name Service-Datenbank in den folgenden Themen:

-   [Richtlinien für die Namensdienst Anwendung](name-service-application-guidelines.md)
-   [Übersicht über den Eintrag "Name Service"](an-overview-of-the-name-service-entry.md)
-   [Kriterien für Namensdienst Einträge](criteria-for-name-service-entries.md)
-   [Bereinigung der Namensdienst Einträge](name-service-entry-cleanup.md)
-   [Was geschieht während einer Abfrage?](what-happens-during-a-query.md)
-   [Verwenden von Microsoft Locator](using-microsoft-locator.md)
-   [Verwenden des Zellen Verzeichnis Dienstanbieter (CDs)](using-the-cell-directory-service-cds-.md)
-   [Namens Syntax](name-syntax.md)

 

 




