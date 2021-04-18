---
description: In diesem Abschnitt werden die XML-Typen beschrieben, die von der Journal Leser Komponente verwendet werden.
ms.assetid: 08b45fe0-a505-4cc0-9791-764a87e8f1eb
title: Namespace Typen für Journal Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e8e3d812eea879ca9dd31680aa2834d6dfe50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216404"
---
# <a name="journal-reader-namespace-types"></a>Namespace Typen für Journal Reader

In diesem Abschnitt werden die XML-Typen beschrieben, die von der Journal Leser Komponente verwendet werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| type                                                                                  | BESCHREIBUNG                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComplexType "Alternative ListType"**](alternateslisttype-complex-type.md)             | Definiert den Typ, der die Liste der Erkennungs Alternativen für ein frei Hand Wort enthält.<br/>                                                                                                                  |
| [**ComplexType für backgroundimagetype**](backgroundimagetype-complex-type.md)           | Definiert den Typ, der Informationen über das Hintergrundbild enthält, das von der Journal Notiz verwendet wird (sofern vorhanden).<br/>                                                                                                |
| [**ComplexType für BackgroundType**](backgroundtype-complex-type.md)                     | Definiert den Typ, der die Hintergrundinformationen für die Journal Notiz enthält.<br/>                                                                                                                     |
| [**ComplexType für baselinetype**](baselinetype-complex-type.md)                         | Definiert den Typ, der Informationen über die Baseline eines Absatzes enthält.<br/>                                                                                                                       |
| [Boundstype attributeGroup](boundstype-attributegroup.md)                            | Definiert eine Attribut Gruppe, die von einer Vielzahl von Elementen in einer Journal-XML-Datei verwendet wird.<br/>                                                                                                             |
| [**ColorType simpleType**](colortype-simple-type.md)                                 | Definiert den Typ, der verwendet wird, um gültige Werte für die Farbe bestimmter Elemente in einer Journal-XML-Datei anzugeben.<br/>                                                                                      |
| [Gruppe "contentgroup"](contentgroup-group.md)                                          | Definiert den Typ, der einen Satz gruppierter Inhalte in einer Journal Notiz enthält.<br/>                                                                                                                          |
| [**ComplexType für ContentType**](contenttype-complex-type.md)                           | Definiert den Typ, der eine Form von Inhalt in einer Journal-XML-Datei enthält.<br/>                                                                                                                      |
| [**Contenttypetype simpleType**](contenttypetype-simple-type.md)                     | Definiert den Typ, der gültige Werte für das **Type** -Attribut des [Inhalts Element- \[ Journal \] Readers](content-element--journal-reader.md)definiert.<br/>                                             |
| [**ComplexType für drawingtype**](drawingtype-complex-type.md)                           | Definiert den Typ, der frei Hand Eingaben enthält, die von der Journal Analyse-Engine als [Zeichnungs Element](drawing-element.md) klassifiziert wurden (im Gegensatz zu einem [InkWord-Element](inkword-element.md)).<br/>  |
| [**ComplexType "FlagType"**](flagtype-complex-type.md)                                 | Definiert den Typ, der das codierte binäre Image und Positionsinformationen für ein in einem Journal Dokument eingebettetes Flag enthält.<br/>                                                                         |
| [**ComplexType "groupnodetype"**](groupnodetype-complex-type.md)                       | Definiert den Typ, der einen Satz gruppierter Inhalte in einer Journal Notiz enthält.<br/>                                                                                                                          |
| [**ComplexType "horizontaltype"**](horizontaltype-complex-type.md)                     | Definiert den Typ, der Informationen zu horizontalen Linien enthält, die von dem Schreib Fach in einem Journal Hinweis verwendet werden.<br/>                                                                                         |
| [**ImageType complexType**](imagetype-complex-type.md)                               | Definiert den Typ, der die binären Informationen für ein Bild in einer Journal Notiz enthält. Siehe auch [**backgroundimagetype complexType**](backgroundimagetype-complex-type.md).<br/>                     |
| [**ComplexType "inkwordtype"**](inkwordtype-complex-type.md)                           | Definiert den Typ, der die frei Hand Daten, die Alternativen und das Vertrauen für frei Hand Inhalte enthält, bei denen es sich um ein [InkWord-Element](inkword-element.md) handelt (im Gegensatz zu einem [Zeichnungs Element](drawing-element.md)).<br/> |
| [**ComplexType für journalpagetype**](journalpagetype-complex-type.md)                   | Definiert den Typ, der eine einzelne Seite in einer Journal Notiz enthält.<br/>                                                                                                                                |
| [**ComplexType für linelayouttype**](linelayouttype-complex-type.md)                     | Definiert den Typ, der Informationen zu den Zeilen enthält, die im Schreibweise eines bestimmten Journal Hinweises verwendet werden.<br/>                                                                                      |
| [**Linelayoutstyletype simpleType**](linelayoutstyletype-simple-type.md)             | Definiert die gültigen Werte für das **Style** -Attribut des [linelayout-Elements](linelayout-element.md).<br/>                                                                                           |
| [**ComplexType für LineType**](linetype-complex-type.md)                                 | Definiert den Typ, der eine Textzeile enthält.<br/>                                                                                                                                                 |
| [**ComplexType ' margintype '**](margintype-complex-type.md)                             | Definiert den Typ, der die Details zu allen Rändern in der Journal Notiz enthält, z. b. Stil, Farbe und Position.<br/>                                                                               |
| [**Margintypetype simpleType**](margintypetype-simple-type.md)                       | Definiert den Typ, der gültige Werte für das **Type** -Attribut für das [Margin-Element](margin-element.md)enthält.<br/>                                                                                |
| [**ComplexType-Datentyp**](paragraphtype-complex-type.md)                       | Definiert den Typ, der einen Absatz in einer Journal Notiz enthält.<br/>                                                                                                                                          |
| [**ComplexType "paragphlinemetricstype"**](paragraphlinemetricstype-complex-type.md) | Definiert den Typ, der Informationen über die linienmetriken eines Absatzes enthält, z. b. die Baseline.<br/>                                                                                             |
| [**ComplexType für reflowtype**](reflowtype-complex-type.md)                             | Definiert den Typ, der angibt, dass die Gruppe weitergeleitet wurde.<br/>                                                                                                                                        |
| [**ComplexType "scalartransformtype"**](scalartransformtype-complex-type.md)           | Definiert den Typ, der die Informationen zu jeder auf Freihand angewendeten Transformation enthält.<br/>                                                                                                                |
| [**ComplexType "stationerytype"**](stationerytype-complex-type.md)                     | Definiert den Typ, der die von der Journal Notiz verwendeten Schreibweise enthält.<br/>                                                                                                                             |
| [**ComplexType für TextType**](texttype-complex-type.md)                                 | Definiert den Typ, der den Textwert in einem [Inhalts Element- \[ Journal \] Reader](content-element--journal-reader.md)enthält.<br/>                                                                       |
| [**ComplexType für titleareatype**](titleareatype-complex-type.md)                       | Definiert den Typ, der Positions-und Begrenzungen-Informationen für den Titel in einer Journal Notiz enthält.<br/>                                                                                                     |
| [**ComplexType für titleinfotype**](titleinfotype-complex-type.md)                       | Definiert den Typ, der Informationen über den Titel in einer Journal Notiz enthält.<br/>                                                                                                                       |
| [**ComplexType für titletype**](titletype-complex-type.md)                               | Definiert den Typ, der Titelinformationen für die Journal Notiz enthält.<br/>                                                                                                                              |
| [**ComplexType ' verticaltype '**](verticaltype-complex-type.md)                         | Definiert den Typ, der Details zu den vertikalen Linien enthält, die in der Schreibweise eines Journal Notiz Blatts verwendet werden.<br/>                                                                                                |



 

 

 




