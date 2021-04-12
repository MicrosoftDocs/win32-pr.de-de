---
title: Verweis auf Windows Media-Metadateielemente
description: Verweis auf Windows Media-Metadateielemente
ms.assetid: 6f85e488-53f6-4fb0-ba48-55c3d7e59f1c
keywords:
- Windows Media-Metadateien, Referenz
- Metadatendateien, Referenz
- Referenz für Windows Media-Metadatendateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20e024c97e9bf8d0f8877eb3f68002702cc1a76f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388462"
---
# <a name="windows-media-metafile-elements-reference"></a>Verweis auf Windows Media-Metadateielemente

Dieser Abschnitt enthält die Referenz Dokumentation für alle Windows Media-Metadatei-Elemente für Client seitige Anwendungen. Verweis Einträge enthalten Definitionen der Elemente, ihrer Attribute und Werte sowie spezielle Bedingungen im Zusammenhang mit den einzelnen Elementen.

Die folgenden Metadatei-Elemente werden für Client seitige Anwendungen unterstützt.



| Element                                           | BESCHREIBUNG                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Kter](abstract-element.md)                  | Enthält Text, der den zugeordneten **ASX**, das **Banner** oder das **Einstiegs** Element beschreibt.                                 |
| [ASX](asx-element.md)                            | Definiert eine Datei als Windows Media-Metadatendatei.                                                                            |
| [Schrift](author-element.md)                      | Enthält den Namen des Autors eines Medienclips oder einer Windows Media-Metadatendatei.                                           |
| [Flagge](banner-element.md)                      | Gibt eine URL für eine Grafik an, die im Anzeigebereich von Windows-Media Player angezeigt wird.                               |
| [Sock](base-element.md)                          | Gibt eine Zeichenfolge an, die an den Anfang der an Windows Media Player gesendeten URLs angehängt wird.                                 |
| [Kommentare](comments.md)                          | Gibt die XML-Syntax für Kommentare an ( <!--...--> ).                                                            |
| [Copyright](copyright-element.md)                | Enthält die Copyright Informationen für ein **ASX** -oder **Entry** -Element.                                                |
| [DURATION](duration-element.md)                  | Gibt die Zeitspanne an, in der Windows Media Player einen Stream rendert.                                                    |
| [Endmarker](endmarker-element.md)                | Gibt einen Marker an, bei dem Windows Media Player das Rendern des Streams beendet.                                           |
| [Ein](entry-element.md)                        | Gibt den Pfad für einen Medien Clip an.                                                                                   |
| [ENTRYREF](entryref-element.md)                  | Links zu den **Eintrags** Elementen in einer externen Windows Media-Metadatei mit der Erweiterung. ASX,. Wax,. wvx oder. wmx. |
| [Veranstalter](event-element.md)                        | Definiert ein Verhalten oder eine Aktion, die von Windows Media Player ausgeführt wird, wenn ein Skript Befehl, der als Ereignis bezeichnet wird, empfangen wird.      |
| [LogURL](logurl-element.md)                      | Weist Windows Media Player an, beliebige Protokolldaten an die angegebene URL zu senden.                                            |
| [Morumfo](moreinfo-element.md)                  | Gibt eine URL für eine Website, eine e-Mail-Adresse oder einen Skript Befehl an, die einer Show, einem Clip oder einem Banner zugeordnet ist.               |
| [PARAM](param-element.md)                        | Gibt den Wert eines benutzerdefinierten Parameters an, der einer Wiedergabeliste oder einem Element einer Wiedergabeliste zugeordnet ist.                      |
| [Previewduration](previewduration-element.md)    | Gibt die Zeitspanne an, für die ein Clip im Vorschaumodus wiedergegeben wird.                                                         |
| [Atur](ref-element.md)                            | Gibt eine URL für einen Inhalt digitaler Medien an.                                                                  |
| [Wiederholung](repeat-element.md)                      | Gibt an, wie oft Windows Media Player ein oder mehrere **Entry** -oder **ENTRYREF** -Elemente wiederholt.             |
| [Skin (veraltet)](skin-element--deprecated.md) | Gibt eine URL zu einer eingebetteten Skin an.                                                                                   |
| [Startmarker](startmarker-element.md)            | Gibt einen Marker an, bei dem Windows-Media Player mit dem Rendern des Streams beginnt.                                          |
| [StartTime](starttime-element.md)                | Gibt einen Zeitpunkt an, zu dem Windows-Media Player mit dem Rendern des Streams beginnen soll.                                        |
| [Tel](title-element--metafile.md)              | Enthält den Titel eines **ASX** -oder **Entry** -Elements.                                                                 |



 

 

 




