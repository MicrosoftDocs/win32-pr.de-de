---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Windows Media Player Online Stores genre.csv
- Online Stores, genre.csv
- Geben Sie 1 Online Stores, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947926"
---
# <a name="genrecsv"></a>genre.csv

Diese Datei enthält einen Eintrag für jedes Genre, das im Katalog dargestellt wird. Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

Alle Felder in genre.csv sind erforderlich.

In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird. Er verweist nicht auf den Datentyp des Inhalts. Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.



| Feld             | Format                                                    | BESCHREIBUNG                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Genre- \_ ID         | Nicht negative ganze Zahl. Beispiel: 22<br/>               | Der Genre Bezeichner, der innerhalb genre.csv eindeutig ist. Muss kleiner als 2 ^ 32 sein. Maximal 64 Genres sind möglich.                                             |
| Genretitle        | Unicode-Zeichenfolge. Beispiel: Rock<br/>                   | Genre Anzeige Name.                                                                                                                                |
| Feedsareavailable | Boolescher Wert. Format: \[ 0 \| 1\]<br/> Beispiel: 0<br/> | Gibt an, ob "Radio Play"-Verhalten durch springen zu einem Feed möglich ist.                                                                          |
| Hascomposer       | Boolescher Wert. Format: \[ 0 \| 1\]<br/> Beispiel: 1<br/> | True, wenn dieses Genre Composer-Informationen im Katalog speichern soll. Wenn nicht festgelegt, werden die Ersteller-Informationen ignoriert und nicht in den Katalog kompiliert. |



 

 

 





