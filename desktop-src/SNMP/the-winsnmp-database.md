---
title: Die WinSNMP-Datenbank
description: Die Microsoft WinSNMP-Implementierung verwaltet einen Speicher von administrativen Informationen in einer-Datenbank.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471093"
---
# <a name="the-winsnmp-database"></a>Die WinSNMP-Datenbank

Die Microsoft WinSNMP-Implementierung verwaltet einen Speicher von administrativen Informationen in einer-Datenbank. Die-Datenbank enthält die folgenden Informationen:

-   Netzwerk-und Versions Eigenschaften.

    Die-Implementierung verwendet diese Eigenschaften, um zu bestimmen, welches Netzwerk Transportprotokoll und welches SNMP-Versions Framework zum Durchführen von Übertragungsanforderungen verwendet werden sollen. Weitere Informationen finden Sie unter Informationen [zu SNMP-Versionen](about-snmp-versions.md).

-   Der Entitäts-und Kontext Übersetzungsmodus.

    Die-Implementierung verwendet diesen Modus, um benutzerfreundliche Namen für SNMP-Entitäten und-Kontexte zu interpretieren. Weitere Informationen finden Sie unter [Festlegen des Entitäts-und Kontext Übersetzungsmodus](setting-the-entity-and-context-translation-mode.md).

-   Neuübertragungs Richtlinien Einstellung.

    Die-Implementierung verwendet diese Einstellung, um zu bestimmen, ob Sie die Richtlinie zur erneuten Übertragung der Anwendung ausführen soll. Die-Implementierung speichert einen Timeout Wert und eine Wiederholungs Anzahl für jede Ziel Entität. Weitere Informationen finden Sie unter Informationen [zur erneuten Übertragung](about-retransmission.md) und zur [Verwaltung der Richtlinie für die Neuübertragung](managing-the-retransmission-policy.md).

 

 




