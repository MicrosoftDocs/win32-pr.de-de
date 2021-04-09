---
description: Datensätze sind eine Möglichkeit für die Kommunikation zwischen Knoten in einem Diagramm oder Mitgliedern einer Gruppe.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Datensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960262"
---
# <a name="records"></a>Datensätze

Datensätze sind eine Möglichkeit für die Kommunikation zwischen Knoten in einem Diagramm oder Mitgliedern einer Gruppe. Ein Datensatz besteht aus den folgenden zwei Teilen:

-   Datensatz-Header
-   Spezifischer undurchsichtiger Dateninhalt

Der-Header enthält Informationen zum Datensatz, einschließlich der Version, des Erstellers und der Art der Daten, die veröffentlicht werden. Der Header enthält auch ein XML-Attribut Feld, das Anwendungen das Hinzufügen von Name-Wert-Attributen, die die Daten beschreiben, sowie das effiziente Durchsuchen der datensatzdatenbank nach bestimmten Datensätzen ermöglicht, die zuvor veröffentlicht wurden. Der Inhalt ist die Anwendungs definierte Daten, die für die Peer Infrastruktur nicht transparent sind.

Wenn ein Datensatz veröffentlicht wird, werden er (sowohl Header als auch Daten) im Diagramm oder in der Gruppe überflutet. Synchronisierte Peers erhalten diese Daten und speichern Sie in einer lokalen Datenbank. Nicht synchronisierte und Offline-Peers erhalten die Daten beim nächsten Herstellen einer Verbindung und Synchronisieren mit dem Peer Diagramm oder der Gruppe.

Weitere Informationen zum Arbeiten mit Datensätzen finden Sie in den folgenden Themen:

-   [Daten Satz Abhängigkeiten](record-dependencies.md)
-   [Daten Satz Verwaltung](record-management.md)
-   [Attribut Schema aufzeichnen](record-attribute-schema.md)
-   [Suchabfrage Format aufzeichnen](record-search-query-format.md)

 

 



