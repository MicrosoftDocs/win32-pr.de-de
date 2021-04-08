---
description: Dieses Thema enthält Informationen zur Programmierung. In der folgenden Liste finden Sie einige Programmiertipps, die Ihnen beim Schreiben eines Parsers helfen.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Überlegungen zur Programmierung (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213104060f7dd3c6b6dbe56d22044508e0878c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756216"
---
# <a name="programming-considerations-network-monitor"></a>Überlegungen zur Programmierung (Netzwerkmonitor)

Dieses Thema enthält Informationen zur Programmierung. In der folgenden Liste finden Sie einige Programmiertipps, die Ihnen beim Schreiben eines Parsers helfen.



|                                                 |                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatisches Installieren des Parsers                     | Implementieren Sie die [**parserautoinstallinfo**](parserautoinstallinfo.md) -Funktion, um den Parser automatisch zu installieren und die zugehörigen ini-Dateien zu aktualisieren. Wenn Sie den Parser manuell installieren, müssen Sie alle zugeordneten ini-Dateien manuell aktualisieren.                                                                                                                                                          |
| Eigenschaften des Protokoll Protokolls                     | Implementieren Sie die [**attachproperties**](attachproperties.md) -Funktion, um die Protokoll Eigenschaften zu analysieren. Vermeiden Sie die Verwendung der Funktion " [**attachpropertyinstanceex**](attachpropertyinstanceex.md) ", wenn Sie eine Eigenschaften Instanz anfügen, und verwenden Sie Sie nur für nicht Byte ausgerichtete Daten oder Daten, die decodiert werden müssen. Das Anfügen von Eigenschaften bezieht sich auf die Zuordnung einer Eigenschaften Instanz zu einer bestimmten Position in einer Erfassung. |
| Unterteilen von Protokollen, die zwischen Frames aufgeteilt sind | Angenommen, jedes Protokoll ist innerhalb eines Frames fertiggestellt, und es wird davon ausgegangen, dass der Benutzer das Protokoll COALESCE-Tool aufruft, um die Teile in einem Protokoll zu kombinieren. Schauen Sie sich beim Testen eines Protokolls nicht wieder einen vorherigen Frame an, und vermeiden Sie es, ein Protokoll zu rekonstruieren, das zwischen Frames aufgeteilt ist.                                                                                              |
| Formatieren der angezeigten Daten                       | Rufen Sie die [**formatpropertyinstance**](formatpropertyinstance.md) -Funktion auf, um den generischen Formatierer zum Formatieren der Daten zu verwenden, die im Detailbereich der Netzwerkmonitor Benutzeroberfläche angezeigt werden. Vermeiden Sie das Schreiben eines benutzerdefinierten Formatierers für UI-Anzeigedaten. Sie können jedoch einen benutzerdefinierten Formatierer zum Erstellen einer [*Zusammenfassungs Eigenschaften*](s.md) Zeile für das Protokoll, das Sie untersuchen, erstellen.            |
| Verwenden von cczuweisung                                   | Verwenden Sie ccalloc, wenn Netzwerkmonitor Daten auf Erfassungs Basis zuordnen möchten. Netzwerkmonitor gibt nicht die Reihenfolge an, in der Frames den Parser aufruft.                                                                                                                                                                                                                                                |
| Zustands lose Beibehaltung eines Parsers                      | Der parservorgang bleibt zustandslos, denn wenn Netzwerkmonitor eine Erfassung analysiert, übergibt er die Frames nicht in einer bestimmten Reihenfolge an den Parser. Aus diesem Grund wird empfohlen, dass Sie keine globalen Daten beibehalten.                                                                                                                                                                                      |



 

 

 



