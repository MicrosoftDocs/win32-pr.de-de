---
description: Dieses Thema enthält Programmierinformationen. In der folgenden Liste sind einige Programmiertipps aufgeführt, mit denen Sie einen Parser schreiben können.
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: Überlegungen zur Programmierung (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b9f840abd40a9fd2946c3fe9face5a3c0cb47dca03c14b1c8e399d0855ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778540"
---
# <a name="programming-considerations-network-monitor"></a>Überlegungen zur Programmierung (Netzwerkmonitor)

Dieses Thema enthält Programmierinformationen. In der folgenden Liste sind einige Programmiertipps aufgeführt, mit denen Sie einen Parser schreiben können.



| Tipp                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatische Installation des Parsers                     | Implementieren Sie die [**ParserAutoInstallInfo-Funktion,**](parserautoinstallinfo.md) um den Parser automatisch zu installieren und die zugeordneten INI-Dateien zu aktualisieren. Wenn Sie den Parser manuell installieren, müssen Sie alle zugeordneten INI-Dateien manuell aktualisieren.                                                                                                                                                          |
| Analysieren von Protokolleigenschaften                     | Implementieren Sie die [**AttachProperties-Funktion,**](attachproperties.md) um die Protokolleigenschaften zu analysieren. Vermeiden Sie die Verwendung der [**AttachPropertyInstanceEx-Funktion,**](attachpropertyinstanceex.md) wenn Sie eine Eigenschaftsinstanz anfügen, und verwenden Sie sie nur für Nicht-Byte-ausgerichtete Daten oder Daten, die decodiert werden müssen. Das Anfügen von Eigenschaften bezieht sich auf das Zuordnen einer Eigenschafteninstanz zu einem bestimmten Speicherort in einer Erfassung. |
| Analysieren von Protokollen, die auf Frames aufgeteilt sind | Angenommen, jeder Teil des Protokolls ist innerhalb eines Rahmens abgeschlossen, und es wird davon ausgegangen, dass der Benutzer das Tool Protocol Coalesce aufruft, um die Teile in einem Protokoll zu kombinieren. Sehen Sie sich beim Analysieren eines Protokolls keinen vorherigen Frame an, und vermeiden Sie den Versuch, ein Protokoll zu rekonstruieren, das zwischen Frames aufgeteilt ist.                                                                                              |
| Formatieren der angezeigten Daten                       | Rufen Sie die [**FormatPropertyInstance-Funktion**](formatpropertyinstance.md) auf, um das generische Formatierungsformat zum Formatieren der Daten zu verwenden, die im Detailbereich der Netzwerkmonitor Ui angezeigt werden. Vermeiden Sie das Schreiben eines benutzerdefinierten Formatierungsformatierers für Benutzeroberflächenanzeigedaten. Sie können jedoch einen benutzerdefinierten Formatierungsdienst aufrufen, um eine [*Zusammenfassungseigenschaftszeile*](s.md) für das Protokoll zu erstellen, das Sie analysieren.            |
| Verwenden von CCAlloc                                   | Verwenden Sie CCAlloc, wenn Netzwerkmonitor Daten pro Erfassung zuordnen möchten. Netzwerkmonitor gibt nicht die Reihenfolge an, in der Frames den Parser aufrufen.                                                                                                                                                                                                                                                |
| Zustandsloses Parser                      | Lassen Sie den Parservorgang zustandslos, da Netzwerkmonitor eine Erfassung nicht in einer bestimmten Reihenfolge an den Parser übergibt. Aus diesem Grund wird empfohlen, globale Daten nicht beizubehalten.                                                                                                                                                                                      |



 

 

 



