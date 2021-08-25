---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player Onlineshops,subgenre.csv
- Onlineshops,subgenre.csv
- Geben Sie 1 Onlineshops ein, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10242e955423d75174d04899285dcd3dc20ea2ea4a761d2ab3ba53561c4d41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122940"
---
# <a name="subgenrecsv"></a>subgenre.csv

Diese Datei enthält einen Eintrag für jedes im Katalog dargestellte Untergenre. Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben sind. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird. Sie verweist nicht auf den Datentyp des Inhalts. Wenn z. B. Integer in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen ganzen Zahl darstellt.



| Feld             | Erforderlich | Format                                                                                            | Beschreibung                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SubGenreID        | Ja      | Nicht negative ganze Zahl.                                                                             | Untergenrebezeichner (ID), innerhalb subgenre.csv eindeutig. Bis zu 1.024 Untergenres sind zulässig.                                                                   |
| SubGenreTitle     | Ja      | Unicode-Zeichenfolge. Beispiel: Intelligent Intelligent Musik (IDM)<br/>                                  | Anzeigename der Unterkategorie.                                                                                                                                    |
| SubGenreSubtitle  | Nein       | Unicode-Zeichenfolge. Beispiel: Neue, percussive elektronische Musik, die nicht ganz rein ist.<br/> | Beschreiben Sie die Bedeutung des Anzeigenamens der Unterkategorie. Sollte weniger als 64 Zeichen lang sein.                                                                     |
| FeedsAreAvailable | Ja      | Boolean.Format: \[ 0 \| 1\]<br/> Beispiel: 0<br/>                                         | Gibt an, ob "Radioplay" durch Springen zu einem Feed möglich ist.                                                                                          |
| Verknüpfte \_ GenreID   | Ja      | Nicht negative ganze Zahl (GenreID). Beispiel: 12<br/>                                             | Die GenreID des übergeordneten Genres. Nur ein übergeordnetes Element ist zulässig.                                                                                              |
| SortOrderRank     | Ja      | Nicht negative ganze Zahl. Beispiel: 23<br/>                                                       | Eine im Idealfall eindeutige Rangfolge, die zum Sortieren von Untergenres in der Benutzeroberfläche verwendet wird. Wenn das übergeordnete Genre über 10 Untergenres verfügt, kann dies eine ganze Zahl zwischen 1 und 10 sein. |



 

 

 





