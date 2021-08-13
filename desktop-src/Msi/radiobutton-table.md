---
description: Optionsfelder werden nicht als einzelne Steuerelemente behandelt, sind aber Teil einer Optionsfeldgruppe, die als RadioButtonGroup-Steuerelement fungiert. In der RadioButton-Tabelle werden die Schaltflächen für alle Gruppen aufgeführt.
ms.assetid: 7f8f278a-a737-4116-9938-2850dbb611fa
title: RadioButton-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc91ece6b5c71cd6ba46143f33e49b90b0278139d194a218a2fddb797bb55a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381050"
---
# <a name="radiobutton-table"></a>RadioButton-Tabelle

Optionsfelder werden nicht als einzelne Steuerelemente behandelt, sind aber Teil einer Optionsfeldgruppe, die als [RadioButtonGroup-Steuerelement fungiert.](radiobuttongroup-control.md) In der RadioButton-Tabelle werden die Schaltflächen für alle Gruppen aufgeführt.

Die RadioButton-Tabelle enthält die folgenden Spalten.



| Spalte   | Typ                         | Key | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Identifier](identifier.md) | J   | N        |
| Auftrag    | [Integer](integer.md)       | J   | N        |
| Wert    | [Formatiert](formatted.md)   | N   | N        |
| X        | [Integer](integer.md)       | N   | N        |
| J        | [Integer](integer.md)       | N   | N        |
| Breite    | [Integer](integer.md)       | N   | N        |
| Höhe   | [Integer](integer.md)       | N   | N        |
| Text     | [Formatiert](formatted.md)   | N   | J        |
| Hilfe     | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Optionsfeld gebunden werden soll. Alle Schaltflächen, die an dieselbe Eigenschaft gebunden sind, werden Teil derselben Gruppe.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Bestellung
</dt> <dd>

Eine positive ganze Zahl, die verwendet wird, um die Reihenfolge der Elemente innerhalb einer Liste zu bestimmen. Die ganzen Zahlen müssen nicht aufeinanderfolgende sein.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die dieser Schaltfläche zugeordnete Wertzeichenfolge. Wenn Sie die Schaltfläche auswählen, wird die zugeordnete Eigenschaft auf diesen Wert fest.

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Die horizontale Koordinate innerhalb der Gruppe der oberen linken Ecke des umgebundenen Rechtecks des Optionsfelds. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Die vertikale Koordinate innerhalb der Gruppe der oberen linken Ecke des umgebundenen Rechtecks des Optionsfelds. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Breite
</dt> <dd>

Die Breite der Schaltfläche. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Höhe
</dt> <dd>

Die Höhe der Schaltfläche. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Der lokalisierbare, sichtbare Titel, der dem Optionsfeld zugewiesen werden soll. Wenn der Text zu lang ist, um auf das Steuerelement zu passen, wird er abgeschnitten. Wenn die Schaltfläche ein Symbol oder eine Bitmap anzeigt, enthält diese Spalte den Namen des Bilds, bei dem es sich um einen Schlüssel in der [Binärtabelle handelt.](binary-table.md) Es gibt keine Möglichkeit, sowohl ein Bild als auch Text auf einer Schaltfläche zu zeigen.

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Hilfe
</dt> <dd>

Die mit der Schaltfläche verwendeten Hilfezeichenfolgen. Der Text ist optional und lokalisierbar. Die Zeichenfolge ist in zwei Teile unterteilt, die durch ein Zeichen ( ) getrennt \| sind. Der erste Teil der Zeichenfolge wird als QuickInfo-Text verwendet. Dieser Text wird von Sprachlesebildschirmen für Steuerelemente angezeigt, die ein Bild enthalten. Der zweite Teil wird für kontextorientierte Hilfe verwendet, obwohl die kontextorientierte Hilfe noch nicht implementiert wurde. Das Trennzeichen ist auch dann erforderlich, wenn nur eine der beiden Arten von Text vorhanden ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die ganzzahligen Werte für x, y, width und height befinden sich in den [Installationseinheiten,](installer-units.md)nicht in Dialogeinheiten. Eine Installationseinheit entspricht der Zwölftelhöhe des 10-Punkt-MS Sans Serif-Schriftgrads. Die Koordinaten für die Steuerelemente sind relativ zum Schild.

Die Koordinaten der Schaltflächen werden relativ zur Gruppe angegeben. Wenn die Koordinaten der Gruppe geändert werden, bleiben die Schaltflächen innerhalb der Gruppe an der gleichen relativen Position zueinander.

Der Inhalt der Felder Value und Text wird beim Erstellen des Steuerelements von der [**MsiFormatRecord-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) formatiert. Daher können sie jeden Ausdruck enthalten, den die **MsiFormatRecord-Funktion** interpretieren kann. Die Formatierung erfolgt nur, wenn das Steuerelement erstellt wird, und wird nicht aktualisiert, wenn eine eigenschaft, die am Ausdruck beteiligt ist, während der Lebensdauer des Steuerelements geändert wird.

Jedes RadioButtonGroup-Steuerelement ist einer -Eigenschaft zugeordnet. Der Standardwert für diese Eigenschaft muss in der [Property-Tabelle initialisiert werden.](property-table.md) Innerhalb jeder in der RadioButton-Tabelle angegebenen RadioButtonGroup kann ein Optionsfeld mit einem Wert im Feld Wert angezeigt werden, der dem Standardwert für diese Eigenschaft entspricht. Dies ist die Standardschaltfläche für das RadioButtonGroup-Steuerelement. Die Standardschaltfläche wird anfänglich als im -Steuerelement ausgewählt angezeigt.

Beachten Sie, dass der Benutzer den Fokus nicht in einem Dialogfeld ändern kann, indem er die TAB-TASTE auf ein RadioButtonGroup-Steuerelement drückt, bis eine der Schaltflächen in der Gruppe ausgewählt wurde. Um den Fokus durch Drücken der TAB-TASTE auf diese Schaltflächengruppe zu verschieben, geben Sie eine der Schaltflächen als Standardschaltfläche für die Gruppe an.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE34](ice34.md)  
[ICE46](ice46.md)  
</dl>

 

 



