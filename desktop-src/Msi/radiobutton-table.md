---
description: Options Felder werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil einer Optionsfeld Gruppe, die als RadioButton Group-Steuerelement fungiert. In der RadioButton-Tabelle sind die Schaltflächen für alle Gruppen aufgeführt.
ms.assetid: 7f8f278a-a737-4116-9938-2850dbb611fa
title: RadioButton-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097f8fbe3081c865e3668631ed0fa9d43a4488cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215902"
---
# <a name="radiobutton-table"></a>RadioButton-Tabelle

Options Felder werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil einer Optionsfeld Gruppe, die als [RadioButton Group-Steuer](radiobuttongroup-control.md)Element fungiert. In der RadioButton-Tabelle sind die Schaltflächen für alle Gruppen aufgeführt.

Die RadioButton-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Bezeichner](identifier.md) | J   | N        |
| Auftrag    | [Integer](integer.md)       | J   | N        |
| Wert    | [Großformatige](formatted.md)   | N   | N        |
| X        | [Integer](integer.md)       | N   | N        |
| J        | [Integer](integer.md)       | N   | N        |
| Breite    | [Integer](integer.md)       | N   | N        |
| Höhe   | [Integer](integer.md)       | N   | N        |
| Text     | [Großformatige](formatted.md)   | N   | J        |
| Hilfe     | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Optionsfeld gebunden werden soll. Alle an dieselbe Eigenschaft gebundenen Schaltflächen werden Teil derselben Gruppe.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge
</dt> <dd>

Eine positive ganze Zahl, die verwendet wird, um die Reihenfolge der Elemente in einer Liste zu bestimmen. Die ganzen Zahlen müssen nicht aufeinander folgen.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die dieser Schaltfläche zugeordnete Wert Zeichenfolge. Wenn Sie die Schaltfläche auswählen, wird die zugehörige-Eigenschaft auf diesen Wert

</dd> <dt>

<span id="X"></span><span id="x"></span>Stuben
</dt> <dd>

Die horizontale Koordinate in der Gruppe der oberen linken Ecke des Begrenzungs Rechtecks des Options Felds. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Teenie
</dt> <dd>

Die vertikale Koordinate in der Gruppe der oberen linken Ecke des Begrenzungs Rechtecks des Options Felds. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Breite
</dt> <dd>

Die Breite der Schaltfläche. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Flugh
</dt> <dd>

Die Höhe der Schaltfläche. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Der lokalisierbare, sichtbare Titel, der dem Optionsfeld zugewiesen werden soll. Wenn der Text für das Steuerelement zu lang ist, wird er abgeschnitten. Wenn die Schaltfläche ein Symbol oder eine Bitmap anzeigt, enthält diese Spalte den Namen des Bilds, bei dem es sich um einen Schlüssel in die [binäre Tabelle](binary-table.md)handelt. Es gibt keine Möglichkeit, ein Bild und Text auf einer Schaltfläche anzuzeigen.

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Hilfe
</dt> <dd>

Die mit der Schaltfläche verwendeten Hilfe Zeichenfolgen. Der Text ist optional und lokalisierbar. Die Zeichenfolge wird in zwei Teile unterteilt, die durch ein Zeichen () getrennt sind \| . Der erste Teil der Zeichenfolge wird als QuickInfo-Text verwendet. Dieser Text wird von Bildschirmlesern für Steuerelemente angezeigt, die ein Bild enthalten. Der zweite Teil wird für die kontextbezogene Hilfe verwendet, obwohl die kontextbezogene Hilfe noch nicht implementiert wurde. Das Trennzeichen ist auch dann erforderlich, wenn nur eine der beiden Arten von Text vorhanden ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die ganzzahligen Werte für x, y, Width und Height befinden sich in den [Installations Einheiten](installer-units.md)und nicht in den Dialog Einheiten. Eine installereinheit ist gleich 1-zwölfte Höhe des 10-Punkt-MS Sans Serif-Schrift Grads. Die Koordinaten für die Steuerelemente sind relativ zum Billboard.

Die Koordinaten der Schaltflächen werden relativ zur Gruppe angegeben. Wenn die Koordinaten der Gruppe geändert werden, bleiben die Schaltflächen innerhalb der Gruppe in der gleichen relativen Position zueinander.

Wenn das Steuerelement erstellt wird, werden die Inhalte der Werte und Text Felder von der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion formatiert und können daher jeden beliebigen Ausdruck enthalten, der von der **msiformatrecord** -Funktion interpretiert werden kann. Die Formatierung erfolgt nur, wenn das Steuerelement erstellt wird, und es wird nicht aktualisiert, wenn eine Eigenschaft, die an dem Ausdruck beteiligt ist, während der Lebensdauer des Steuer Elements geändert wird.

Jedem RadioButton Group-Steuerelement ist eine Eigenschaft zugeordnet. Der Standardwert für diese Eigenschaft muss in der [Eigenschaften Tabelle](property-table.md)initialisiert werden. Innerhalb jeder RadioButton Group, die in der RadioButton-Tabelle angegeben ist, kann ein Optionsfeld mit einem Wert im Feld Wert vorhanden sein, der mit dem Standardwert für diese Eigenschaft übereinstimmt. Dies ist die Standard Schaltfläche für das RadioButton Group-Steuerelement. Die Standard Schaltfläche wird anfänglich im-Steuerelement als ausgewählt angezeigt.

Beachten Sie, dass der Benutzer den Fokus nicht in einem Dialogfeld ändern kann, indem er die Tab-Taste auf ein RadioButton Group-Steuerelement drückt, bis eine der Schaltflächen in der Gruppe ausgewählt wurde. Um den Fokus auf diese Schaltflächen Gruppe durch Drücken der Tab-Taste zu verschieben, geben Sie eine der Schaltflächen als Standard Schaltfläche für die Gruppe an.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE34](ice34.md)  
[ICE46](ice46.md)  
</dl>

 

 



