---
description: Die Steuertabelle definiert die Steuerelemente, die in jedem Dialogfeld angezeigt werden.
ms.assetid: cbe7acd6-b916-45f3-b694-d2345c5a892a
title: Steuertabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e1832a2cb600e8d7a27b43bc28c94836396d74a50a90b44d0e5013bde973c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638532"
---
# <a name="control-table"></a>Steuertabelle

Die Steuertabelle definiert die Steuerelemente, die in jedem Dialogfeld angezeigt werden.

Die Control-Tabelle enthält die folgenden Spalten.



| Spalte        | Typ                               | Key | Nullwerte zulässig |
|---------------|------------------------------------|-----|----------|
| Dialog\_      | [Identifier](identifier.md)       | J   | N        |
| Control       | [Identifier](identifier.md)       | J   | N        |
| Typ          | [Identifier](identifier.md)       | N   | N        |
| X             | [Integer](integer.md)             | N   | N        |
| J             | [Integer](integer.md)             | N   | N        |
| Breite         | [Integer](integer.md)             | N   | N        |
| Höhe        | [Integer](integer.md)             | N   | N        |
| Attribute    | [DoubleInteger](doubleinteger.md) | N   | J        |
| Eigenschaft      | [Identifier](identifier.md)       | N   | J        |
| Text          | [Formatiert](formatted.md)         | N   | J        |
| Weiter \_ steuern | [Identifier](identifier.md)       | N   | J        |
| Hilfe          | [Text](text.md)                   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogfeld\_
</dt> <dd>

Externer Schlüssel für die erste Spalte der [Tabelle Dialog](dialog-table.md), der Name des Dialogfelds.

</dd> <dt>

<span id="Control"></span><span id="control"></span><span id="CONTROL"></span>Steuerung
</dt> <dd>

Name des Steuerelements. Dieser Name muss innerhalb eines Dialogfelds eindeutig sein, kann aber in verschiedenen Dialogfeldern wiederholt werden. Die Spalte Steuerelement in Kombination mit der Spalte Dialog \_ bildet den Primärschlüssel für diese Tabelle.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Typ
</dt> <dd>

Der Typ des Steuerelements. Eine Liste der Steuerelementtypen finden Sie unter [Steuerelemente](controls.md).

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Horizontale Koordinate der oberen linken Ecke der rechteckigen Begrenzung des Steuerelements. Dies muss eine nicht negative Zahl sein. Weitere Informationen [finden Sie unter Position Control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Vertikale Koordinate der oberen linken Ecke der rechteckigen Begrenzung des Steuerelements. Dies muss eine nicht negative Zahl sein. Weitere Informationen [finden Sie unter Position Control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Breite
</dt> <dd>

Breite der rechteckigen Begrenzung des Steuerelements. Dies muss eine nicht negative Zahl sein. Weitere Informationen [finden Sie unter Position Control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Höhe
</dt> <dd>

Höhe der rechteckigen Begrenzung des Steuerelements. Dies muss eine nicht negative Zahl sein. Weitere Informationen [finden Sie unter Position Control Attribute](position-control-attribute.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Ein 32-Bit-Wort, das die Bitflags angibt, die auf dieses Steuerelement angewendet werden sollen. Dies muss eine nicht negative Zahl sein, und die zulässigen Werte hängen vom Typ des Steuerelements ab. Eine Liste aller Steuerelementattribute und den Wert, den Sie in dieses Feld eingeben möchten, finden Sie unter [Steuerelementattribute](control-attributes.md).

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Der Name einer definierten Eigenschaft, die mit diesem Steuerelement verknüpft werden soll. Optionsfeld-, Listenfeld- und Kombinationsfeldwerte werden an eine Gruppe gebunden, indem sie mit derselben Eigenschaft verknüpft werden. Diese Spalte ist für aktive Steuerelemente erforderlich.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Eine lokalisierbare Zeichenfolge, die zum Festlegen des ursprünglichen Texts in einem -Steuerelement verwendet wird. Die Zeichenfolge kann auch eingebettete Eigenschaften enthalten. Die Syntax einer formatierten Zeichenfolge, die Eigenschaften enthält, finden Sie in der [**MsiFormatRecord-Funktion.**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) Geben Sie die Größe, Schriftart und Farbe des Texts an, indem Sie der Textzeichenfolge {style} vorangestellt werden, wobei style ein Textformat ist, das in der TextStyle -Spalte der TextStyle-Tabelle erstellt \\ [wurde.](textstyle-table.md) Die Textzeichenfolge wird abgeschnitten, wenn sie zu lang ist, um auf das Steuerelement zu passen. Die Textzeichenfolge ist möglicherweise leer.

Eine spezielle Erstellung der [formatierten](formatted.md) Textzeichenfolge in diesem Feld ist erforderlich, wenn der Text von einem [Text-Steuerelement](text-control.md) angezeigt werden soll, das sich in einem Dialogfeld mit dem TrackDiskpace-Attribut befindet. Dies ist der Fall, der durch [das TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) angegeben wird, das in den Attributen der [Dialogtabelle angezeigt wird.](dialog-table.md) Wenn in diesem Fall die formatierte Zeichenfolge in der Text -Spalte der Control-Tabelle mit " " beginnt und mit " " endet, müssen Sie am Ende der Zeichenfolge ein Leerzeichen \[ \] hinzufügen. Wenn dlgTextFont beispielsweise eine Eigenschaft ist, die auf "{ DlgFontBold}" festgelegt wird, benötigt die formatierte Zeichenfolge \\ \[ DlgTextFont \] MyText ProductName das Leerzeichen am Ende nach der schließenden \[ \] Klammer. Dieser zusätzliche Speicherplatz wird vom Installationsprogramm benötigt, um den Text im Text-Steuerelement ordnungsgemäß anzuzeigen.

Sie können eine kurze beschreibende Textzeichenfolge für [die Steuerelemente VolumeCostList,](volumecostlist-control.md) [ListView,](listview-control.md) [DirectoryList](directorylist-control.md)und [SelectionTree eingeben.](selectiontree-control.md) Dieser Text wird dem Benutzer nicht angezeigt, kann aber von Sprachlesern als Beschreibung des Steuerelements gelesen werden.

Siehe auch [Barrierefreiheit.](accessibility.md)

</dd> <dt>

<span id="Control_Next"></span><span id="control_next"></span><span id="CONTROL_NEXT"></span>Weiter \_ steuern
</dt> <dd>

Der Name eines anderen Steuerelements im gleichen Dialogfeld und ein externer Schlüssel für die zweite Spalte der Control-Tabelle. Wenn sich der Fokus im Dialogfeld auf dem Steuerelement in der Spalte Steuerelement befindet, wird der Fokus durch Drücken der TAB-TASTE auf das Steuerelement in der Spalte Nächstes \_ Steuerelement aufgeführt. Daher wird diese Spalte verwendet, um die Registerkarten reihenfolge der Steuerelemente im Dialogfeld anzugeben. Die Verknüpfungen zwischen den Steuerelementen müssen einen geschlossenen Zyklus bilden. Einige Steuerelemente, z. B. statische Textsteuerelemente, können aus dem Zyklus weggelassen werden. In diesem Fall wird dieses Feld möglicherweise leer gelassen.

Siehe auch [Barrierefreiheit.](accessibility.md)

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Hilfe
</dt> <dd>

Optionale, lokalisierbare Textzeichenfolgen, die mit der Schaltfläche Hilfe verwendet werden. Die Zeichenfolge wird durch ein Trennzeichen ( ) in zwei Teile \| unterteilt. Der erste Teil der Zeichenfolge wird als QuickInfo-Text verwendet. Dieser Text wird von Sprachbildschirmen für Steuerelemente verwendet, die ein Bild enthalten. Der zweite Teil der Zeichenfolge ist für die zukünftige Verwendung reserviert. Das Trennzeichen ist auch dann erforderlich, wenn nur eine der beiden Arten von Text vorhanden ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die ganzzahligen Werte für x, y, width und height befinden sich in den [Installationseinheiten,](installer-units.md)nicht in Dialogeinheiten. Eine Installationseinheit entspricht einem Zwölftel der Höhe des 10-Punkt-MS Sans Serif-Schriftgrads. Koordinaten für die Steuerelemente sind relativ zum Schild.

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

 

 



