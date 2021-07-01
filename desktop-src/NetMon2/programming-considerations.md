---
description: Dieses Thema enthält Programmierinformationen. In der folgenden Liste sind einige Programmiertipps aufgeführt, mit deren Hilfe Sie einen Parser schreiben können.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Überlegungen zur Programmierung (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2deb53a27d8abda4f45663b65fb922600a5b5386
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120225"
---
# <a name="programming-considerations-network-monitor"></a>Überlegungen zur Programmierung (Netzwerkmonitor)

Dieses Thema enthält Programmierinformationen. In der folgenden Liste sind einige Programmiertipps aufgeführt, mit deren Hilfe Sie einen Parser schreiben können.



| Tipp                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatische Installation des Parsers                     | Implementieren Sie [**die ParserAutoInstallInfo-Funktion,**](parserautoinstallinfo.md) um ihren Parser automatisch zu installieren und die zugeordneten INI-Dateien zu aktualisieren. Wenn Sie den Parser manuell installieren, müssen Sie alle zugeordneten INI-Dateien manuell aktualisieren.                                                                                                                                                          |
| Analyseprotokolleigenschaften                     | Implementieren Sie [**die AttachProperties-Funktion,**](attachproperties.md) um die Protokolleigenschaften zu analysieren. Vermeiden Sie die [**Verwendung der AttachPropertyInstanceEx-Funktion,**](attachpropertyinstanceex.md) wenn Sie eine Eigenschafteninstanz anfügen, und verwenden Sie sie nur für Nicht-Byte-ausgerichtete Daten oder Daten, die decodiert werden müssen. Das Anfügen von Eigenschaften bezieht sich auf das Zuordnen einer Eigenschafteninstanz zu einer bestimmten Position in einer Erfassung. |
| Analyseprotokolle, die auf Frames aufgeteilt sind | Angenommen, jeder Teil des Protokolls ist innerhalb eines Frames vollständig, und es wird davon ausgegangen, dass der Benutzer das Tool Protocol Coalesce aufruft, um die Teile in einem Protokoll zu kombinieren. Sehen Sie sich bei der Analyse eines Protokolls keinen vorherigen Frame an, und versuchen Sie nicht, ein Protokoll zu rekonstruieren, das auf Frames aufgeteilt ist.                                                                                              |
| Formatieren der angezeigten Daten                       | Rufen Sie [**die FormatPropertyInstance-Funktion**](formatpropertyinstance.md) auf, um den generischen Formatierungser zum Formatieren der Daten zu verwenden, die im Detailbereich der benutzeroberfläche Netzwerkmonitor werden. Vermeiden Sie das Schreiben eines benutzerdefinierten Formatierungsformatters für Anzeigedaten der Benutzeroberfläche. Sie können jedoch einen benutzerdefinierten Formatierungssteuerwert aufrufen, um eine [](s.md) Zusammenfassungseigenschaftszeile für das Protokoll zu erstellen, das Sie analysen.            |
| Verwenden von CCAlloc                                   | Verwenden Sie CCAlloc, wenn Netzwerkmonitor daten auf Erfassungsbasis zuordnen möchten. Netzwerkmonitor gibt nicht die Reihenfolge an, in der Frames den Parser aufrufen.                                                                                                                                                                                                                                                |
| Zustandsloses Halten eines Parsers                      | Lassen Sie den Parservorgang zustandslos, da Netzwerkmonitor eine Erfassung analysiert, die Frames nicht in einer bestimmten Reihenfolge an den Parser übergeben. Aus diesem Grund wird empfohlen, globale Daten nicht zu speichern.                                                                                                                                                                                      |



 

 

 



