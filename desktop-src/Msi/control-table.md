---
description: Die Steuerelement Tabelle definiert die Steuerelemente, die in jedem Dialogfeld angezeigt werden.
ms.assetid: cbe7acd6-b916-45f3-b694-d2345c5a892a
title: Steuerungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ced41fcaf020a043962b16cf12d9c339901b415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217358"
---
# <a name="control-table"></a>Steuerungs Tabelle

Die Steuerelement Tabelle definiert die Steuerelemente, die in jedem Dialogfeld angezeigt werden.

Die Steuerelement Tabelle weist die folgenden Spalten auf.



| Spalte        | Typ                               | Schlüssel | Nullwerte zulässig |
|---------------|------------------------------------|-----|----------|
| Dialog\_      | [Bezeichner](identifier.md)       | J   | N        |
| Control       | [Bezeichner](identifier.md)       | J   | N        |
| type          | [Bezeichner](identifier.md)       | N   | N        |
| X             | [Integer](integer.md)             | N   | N        |
| J             | [Integer](integer.md)             | N   | N        |
| Breite         | [Integer](integer.md)             | N   | N        |
| Höhe        | [Integer](integer.md)             | N   | N        |
| Attribute    | [Doubleiteger](doubleinteger.md) | N   | J        |
| Eigenschaft      | [Bezeichner](identifier.md)       | N   | J        |
| Text          | [Großformatige](formatted.md)         | N   | J        |
| Nächstes Steuerelement \_ | [Bezeichner](identifier.md)       | N   | J        |
| Hilfe          | [Text](text.md)                   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_
</dt> <dd>

Externer Schlüssel für die erste Spalte der [Dialogfeld Tabelle](dialog-table.md), der Name des Dialog Felds.

</dd> <dt>

<span id="Control"></span><span id="control"></span><span id="CONTROL"></span>Steuerelement
</dt> <dd>

Der Name des Steuer Elements. Dieser Name muss in einem Dialogfeld eindeutig sein, kann aber in anderen Dialogfeldern wiederholt werden. Die Steuerelement Spalte in Kombination mit der Dialog Feld \_ Spalte bildet den Primärschlüssel für diese Tabelle.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte
</dt> <dd>

Der Typ des Steuerelements. Eine Liste der Steuerelement Typen finden Sie unter Steuer [Elemente](controls.md).

</dd> <dt>

<span id="X"></span><span id="x"></span>Stuben
</dt> <dd>

Die horizontale Koordinate der oberen linken Ecke der rechteckigen Begrenzung des Steuer Elements. Dabei muss es sich um eine nicht negative Zahl handeln. Siehe [Positions Steuerungs Attribut](position-control-attribute.md).

</dd> <dt>

<span id="Y"></span><span id="y"></span>Teenie
</dt> <dd>

Vertikale Koordinate der oberen linken Ecke der rechteckigen Begrenzung des Steuer Elements. Dabei muss es sich um eine nicht negative Zahl handeln. Siehe [Positions Steuerungs Attribut](position-control-attribute.md).

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Breite
</dt> <dd>

Breite der rechteckigen Begrenzung des Steuer Elements. Dabei muss es sich um eine nicht negative Zahl handeln. Siehe [Positions Steuerungs Attribut](position-control-attribute.md).

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Flugh
</dt> <dd>

Höhe der rechteckigen Begrenzung des Steuer Elements. Dabei muss es sich um eine nicht negative Zahl handeln. Siehe [Positions Steuerungs Attribut](position-control-attribute.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Ein 32-Bit-Wort, das die Bitflags angibt, die auf dieses Steuerelement angewendet werden sollen. Dies muss eine nicht negative Zahl sein, und die zulässigen Werte hängen von der Art des Steuer Elements ab. Eine Liste aller Steuerelement Attribute und den Wert, der in dieses Feld eingegeben werden soll, finden Sie unter [Steuerelement Attribute](control-attributes.md).

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Der Name einer definierten Eigenschaft, die mit diesem Steuerelement verknüpft werden soll. Options Felder, Listenfelder und Kombinations Feld Werte werden in eine Gruppe eingebunden, indem Sie mit derselben Eigenschaft verknüpft werden. Diese Spalte ist für aktive Steuerelemente erforderlich.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Eine lokalisierbare Zeichenfolge, die zum Festlegen des anfänglichen Texts in einem-Steuerelement verwendet wird. Die Zeichenfolge kann auch eingebettete Eigenschaften enthalten. Die Syntax einer formatierten Zeichenfolge, die Eigenschaften enthält, finden Sie unter der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion. Geben Sie die Größe, die Schriftart und die Farbe des Texts an, indem Sie die Text Zeichenfolge mit { \\ Style} vorangestellt wird, wobei Style ein Textformat ist, das in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)erstellt wird. Die Text Zeichenfolge wird abgeschnitten, wenn Sie zu lang ist, um auf das Steuerelement zu passen. Die Text Zeichenfolge ist möglicherweise leer.

Eine besondere Erstellung der [formatierten](formatted.md) Text Zeichenfolge in diesem Feld ist erforderlich, wenn der Text durch ein [Text Steuer](text-control.md) Element angezeigt werden soll, das sich in einem Dialogfeld befindet, das das trackdiskpace-Attribut aufweist. Dies ist der Fall, der durch das Dialogfeld Format von [trackdiskspace](trackdiskspace-dialog-style-bit.md) angegeben wird, das in den Attributen der [Dialogfeld Tabelle](dialog-table.md)angezeigt wird. Wenn in diesem Fall die formatierte Zeichenfolge in der Text-Spalte der Steuerelement Tabelle mit "" beginnt \[ und mit "" endet, \] müssen Sie am Ende der Zeichenfolge ein Leerzeichen hinzufügen. Wenn dlgtextfont z. b. eine Eigenschaft ist, die auf "{ \\ dlgfontbold}" festgelegt wird, erfordert die formatierte Zeichenfolge " \[ dlgtextfont \] MyText \[ ProductName \] " den Platz am Ende nach der schließenden Klammer. Dieser zusätzliche Speicherplatz ist erforderlich, damit das Installationsprogramm den Text im Text Steuerelement korrekt anzeigt.

Sie können eine kurze beschreibende Text Zeichenfolge für die Steuerelemente " [volumecostlist](volumecostlist-control.md)", " [ListView](listview-control.md)", " [directerylist](directorylist-control.md)" und " [SelectionTree](selectiontree-control.md)" eingeben. Dieser Text wird dem Benutzer nicht angezeigt, kann aber von den Bildschirmlesern als Beschreibung des Steuer Elements gelesen werden.

Siehe auch [Barrierefreiheit](accessibility.md).

</dd> <dt>

<span id="Control_Next"></span><span id="control_next"></span><span id="CONTROL_NEXT"></span>Nächstes Steuerelement \_
</dt> <dd>

Der Name eines anderen Steuer Elements im gleichen Dialogfeld und ein externer Schlüssel zur zweiten Spalte der Steuerelement Tabelle. Wenn sich der Fokus im Dialogfeld auf dem Steuerelement in der Steuerelement Spalte befindet, wird beim Drücken der Tab-Taste der Fokus auf das Steuerelement verschoben, das in der nächsten Spalte des Steuer Elements aufgeführt ist \_ . Daher wird diese Spalte verwendet, um die Aktivier Reihenfolge der Steuerelemente im Dialogfeld anzugeben. Die Links zwischen den Steuerelementen müssen einen geschlossenen Durchlauf bilden. Einige Steuerelemente, wie z. b. statische Text Steuerelemente, können vom-Schleifen Bereich ausgelassen werden. In diesem Fall bleibt dieses Feld möglicherweise leer.

Siehe auch [Barrierefreiheit](accessibility.md).

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Hilfe
</dt> <dd>

Optionale, lokalisierbare Text Zeichenfolgen, die mit der Schaltfläche Hilfe verwendet werden. Die Zeichenfolge wird durch ein Trennzeichen () in zwei Teile aufgeteilt \| . Der erste Teil der Zeichenfolge wird als QuickInfo-Text verwendet. Dieser Text wird von Bildschirmlesern für Steuerelemente verwendet, die ein Bild enthalten. Der zweite Teil der Zeichenfolge ist für die zukünftige Verwendung reserviert. Das Trennzeichen ist auch dann erforderlich, wenn nur eine der beiden Arten von Text vorhanden ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die ganzzahligen Werte für x, y, Width und Height befinden sich in den [Installations Einheiten](installer-units.md)und nicht in den Dialog Einheiten. Eine installereinheit ist gleich 1-zwölfte Höhe des 10-Punkt-MS Sans Serif-Schrift Grads. Die Koordinaten für die Steuerelemente sind relativ zum Billboard.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE31](ice31.md)  
[ICE32](ice32.md)  
[ICE34](ice34.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE95](ice95.md)  
</dl>

 

 



