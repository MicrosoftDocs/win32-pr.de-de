---
description: Screenreader-Programme können nur den Text eines RadioButton Group-Steuer Elements lesen, das in der Text-Spalte der RadioButton-Tabelle erstellt wurde.
ms.assetid: 92ad70ec-a3a4-4ea7-8888-40c78d73e58a
title: Hinzufügen von zusätzlichem Text zu Options Feldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e73ac55e300ddee603449e9ea7ce5e10f4e0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959546"
---
# <a name="adding-extra-text-to-radio-buttons"></a>Hinzufügen von zusätzlichem Text zu Options Feldern

Screenreader-Programme können nur den Text eines [RadioButton Group-Steuer Elements](radiobuttongroup-control.md) lesen, das in der Text-Spalte der [RadioButton-Tabelle](radiobutton-table.md)erstellt wurde. Wenn dieser Text eine unzureichende Beschreibung der Options Felder ist, können überlappende [Text Steuerelemente](text-control.md) hinzugefügt werden, um zusätzlichen beschreibenden Text bereitzustellen. Diese Text Steuerelemente sollten sich im Dialogfeld gegenseitig überlappen und in der [ControlCondition-Tabelle](controlcondition-table.md) Bedingungen festgelegt werden, sodass jeweils nur ein Text Steuerelement angezeigt wird. Die Text Steuerelemente dürfen das RadioButton Group-Steuerelement oder andere Steuerelemente im Dialogfeld nicht überlappen, da die Steuerelemente für die Bildschirm Sprachausgabe unsichtbar werden. Wenn der Benutzer mit dem Cursor auf das Text Steuerelement zeigt, liest das Bildschirm Leseprogramm den zusätzlichen Text.

Im folgenden Beispiel enthält das Dialogfeld MySample ein RadioButton Group-Steuerelement mit dem Namen Colors, das zwei Optionen für den Wert der Eigenschaft thecolor enthält. Für jede Auswahl ist ein Text Steuerelement mit einer Bedingung zum Ausblenden oder anzeigen vorhanden, abhängig von der aktuellen Auswahl, die für thecolor ausgewählt ist. In der Eigenschaften Tabelle ist ein ursprünglicher thecolor-Wert definiert. Die Text Steuerelemente haben den zusätzlichen beschreibenden Text, der im Textfeld der RadioButton-Tabelle erstellt wurde. Wenn ein Benutzer den Cursor über das Text Steuerelement im Dialogfeld bewegt, kann die Sprachausgabe die zusätzliche Beschreibung der aktuellen Auswahl lesen.

[Dialog Feld Tabelle](dialog-table.md)



| Dialog   | Hcentering | Vcentering | Breite | Höhe | Attribute | Titel                    | \_Zuerst Steuern | Standard Steuerelement \_ | Abbrechen von Steuerelementen \_ |
|----------|------------|------------|-------|--------|------------|--------------------------|----------------|------------------|-----------------|
| MySample | 50         | 50         | 200   | 180    | 3          | Barrierefreie Options Felder | Farben         | Nächste             |                 |



 

[Steuerungs Tabelle](control-table.md)



| Dialog\_ | Control    | type             | X   | J   | Breite | Höhe | Attribute | Eigenschaft | Text                               | Nächstes Steuerelement \_ | Hilfe |
|----------|------------|------------------|-----|-----|-------|--------|------------|----------|------------------------------------|---------------|------|
| MySample | Farben     | RadioButtonGroup | 2   | 20  | 100   | 50     | 3          | Thecolor |                                    | Nächste          |      |
| MySample | Huwisblue  | Text             | 20  | 80  | 150   | 15     | 2          |          | Es ähnelt dem Himmel an einem klaren Tag. |               |      |
| MySample | Horwisgrün | Text             | 20  | 80  | 150   | 15     | 2          |          | Es ist wie das Gras im Spring.    |               |      |



 

[RadioButton-Tabelle](radiobutton-table.md)



| Eigenschaft | Auftrag | Wert | X   | J   | Breite | Höhe | Text   | Hilfe |
|----------|-------|-------|-----|-----|-------|--------|--------|------|
| Thecolor | 1     | Blau  | 10  | 10  | 80    | 15     | &blau  |      |
| Thecolor | 2     | Grün | 10  | 30  | 80    | 15     | &grün |      |



 

[Eigenschaften Tabelle](property-table.md)



| Eigenschaft | Wert |
|----------|-------|
| Thecolor | Blau  |



 

[ControlCondition-Tabelle](controlcondition-table.md)



| Dialog\_ | Steuerelement\_  | Aktion | Bedingung                 |
|----------|------------|--------|---------------------------|
| MySample | Huwisblue  | Ausblenden   | Thecolor <>  "Blue"  |
| MySample | Huwisblue  | Anzeigen   | Thecolor = "Blue"         |
| MySample | Horwisgrün | Ausblenden   | Thecolor <>  "grün" |
| MySample | Horwisgrün | Anzeigen   | Thecolor = "grün"        |



 

Weitere Informationen finden Sie unter [Barrierefreiheit](accessibility.md).

 

 



