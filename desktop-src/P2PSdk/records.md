---
description: Datensätze sind eine Möglichkeit, zwischen Knoten in einem Diagramm oder Mitgliedern in einer Gruppe zu kommunizieren.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Datensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3066bb6d309ce70a790947f002e1a74eb329c862ffcb0ef2c1766ca315323f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675000"
---
# <a name="records"></a>Datensätze

Datensätze sind eine Möglichkeit, zwischen Knoten in einem Diagramm oder Mitgliedern in einer Gruppe zu kommunizieren. Ein Datensatz besteht aus den folgenden beiden Teilen:

-   Datensatzheader
-   Bestimmter nicht transparenter Dateninhalt

Der Header enthält Informationen zum Datensatz, einschließlich Version, Ersteller und Typ der zu veröffentlichenden Daten. Der Header enthält auch ein XML-Attributfeld, mit dem Anwendungen Name-Wert-Attribute hinzufügen können, die die Daten beschreiben, und die Datensatzdatenbank effizient nach bestimmten Datensätzen durchsuchen können, die zuvor veröffentlicht wurden. Der Inhalt sind die anwendungsdefinierten Daten und für die Peerinfrastruktur nicht transparent.

Wenn ein Datensatz veröffentlicht wird, wird er (Header und Daten) im gesamten Diagramm oder in der Gruppe überflutet. Synchronisierte Peers empfangen diese Daten und speichern sie in einer lokalen Datenbank. Nicht synchronisierte und Offline-Peers empfangen die Daten, wenn sie das nächste Mal eine Verbindung mit dem Peerdiagramm oder der Peergruppe herstellen und diese synchronisieren.

Informationen zum Arbeiten mit Datensätzen finden Sie in den folgenden Themen:

-   [Aufzeichnen von Abhängigkeiten](record-dependencies.md)
-   [Datensatzverwaltung](record-management.md)
-   [Datensatzattributschema](record-attribute-schema.md)
-   [Abfrageformat der Datensatzsuche](record-search-query-format.md)

 

 



