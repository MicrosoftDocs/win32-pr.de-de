---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player Online Stores subgenre.csv
- Online Stores, subgenre.csv
- Geben Sie 1 Online Stores, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341471"
---
# <a name="subgenrecsv"></a>subgenre.csv

Diese Datei enthält einen Eintrag für jedes unter Genre, das im Katalog dargestellt wird. Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird. Er verweist nicht auf den Datentyp des Inhalts. Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.



| Feld             | Erforderlich | Format                                                                                            | BESCHREIBUNG                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Subgenreid        | Ja      | Nicht negative ganze Zahl.                                                                             | Der in subgenre.csv eindeutige Subgenre Bezeichner (ID). Bis zu 1024 Subgenres sind zulässig.                                                                   |
| Subgenretitle     | Ja      | Unicode-Zeichenfolge. Beispiel: Intelligent Dance Music (IDM)<br/>                                  | Der Anzeige Name des Subgenres.                                                                                                                                    |
| Subgenreuntertitel  | Nein       | Unicode-Zeichenfolge. Beispiel: neue, perkussive Elektronische Musik, die nicht ganz rein Techno ist.<br/> | Beschreibt die Bedeutung des Anzeige namens des unter Genres. Sollte kleiner als 64 Zeichen sein.                                                                     |
| Feedsareavailable | Ja      | Boolescher Wert. Format: \[ 0 \| 1\]<br/> Beispiel: 0<br/>                                         | Gibt an, ob "Radio Play" durch springen zu einem Feed möglich ist.                                                                                          |
| Verknüpfte \_ GenreID   | Ja      | Nicht negative Ganzzahl (GenreID). Beispiel: 12<br/>                                             | Der GenreID des übergeordneten Genres. Es ist nur ein übergeordnetes Element zulässig.                                                                                              |
| Sorrenderrank     | Ja      | Nicht negative ganze Zahl. Beispiel: 23<br/>                                                       | Eine Rangfolge, die im Idealfall eindeutig ist, wird zum Sortieren von unter Genres in der Benutzeroberfläche verwendet. Wenn das übergeordnete Genre 10 unter Genres hat, kann dies eine ganze Zahl zwischen 1 und 10 sein. |



 

 

 





