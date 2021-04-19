---
description: Die Tabelle bbcontrol listet die Steuerelemente auf, die auf jedem Billboard angezeigt werden sollen.
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: Bbcontrol-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfebbdbc474ef88cbf26f34555deb4874840d005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355663"
---
# <a name="bbcontrol-table"></a>Bbcontrol-Tabelle

Die Tabelle bbcontrol listet die Steuerelemente auf, die auf jedem Billboard angezeigt werden sollen.

Die Tabelle "bbcontrol" weist die folgenden Spalten auf.



| Spalte      | Typ                               | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------------|-----|----------|
| Billboard\_ | [Bezeichner](identifier.md)       | J   | N        |
| Bbcontrol   | [Bezeichner](identifier.md)       | J   | N        |
| type        | [Bezeichner](identifier.md)       | N   | N        |
| X           | [Integer](integer.md)             | N   | N        |
| J           | [Integer](integer.md)             | N   | N        |
| Breite       | [Integer](integer.md)             | N   | N        |
| Höhe      | [Integer](integer.md)             | N   | N        |
| Attribute  | [Doubleiteger](doubleinteger.md) | N   | J        |
| Text        | [Text](text.md)                   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Billboard_"></span><span id="billboard_"></span><span id="BILLBOARD_"></span>Billboard\_
</dt> <dd>

Der Name des Billboard.

Externer Schlüssel für Spalte 1 der [Billboard-Tabelle](billboard-table.md).

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>Bbcontrol
</dt> <dd>

Der Name des Steuer Elements. Dieser Name muss innerhalb eines Billboard eindeutig sein, kann jedoch auf unterschiedlichen Plakaten wiederholt werden. Diese Spalte in Kombination mit der \_ Spalte Billboard bildet den Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte
</dt> <dd>

Der Typ des Steuerelements. Nur statische Steuerelemente, z. b. ein [Text](text-control.md), eine [Bitmap](bitmap-control.md), ein [Symbol](icon-control.md)oder ein benutzerdefiniertes Steuerelement, können in einem Billboard abgelegt werden. Eine umfassende Liste der Steuerelemente finden Sie im Abschnitt "Steuer [Elemente](controls.md) ".

</dd> <dt>

<span id="X"></span><span id="x"></span>Stuben
</dt> <dd>

Die horizontale Koordinate der oberen linken Ecke der rechteckigen Begrenzung des Steuer Elements. Die Einheiten sind [Installer-Einheiten](installer-units.md). Diese Koordinate wird relativ zum Billboard-Steuerelement und nicht relativ zum Dialogfeld gemessen. Verwenden Sie nur nicht negative Zahlen.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Teenie
</dt> <dd>

Vertikale Koordinate der oberen linken Ecke der rechteckigen Begrenzung des Steuer Elements. Die Einheiten sind [Installer-Einheiten](installer-units.md). Diese Koordinate wird relativ zum Billboard-Steuerelement und nicht relativ zum Dialogfeld gemessen. Diese Zahl darf nicht negativ sein.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Breite
</dt> <dd>

Breite der rechteckigen Begrenzung des Steuer Elements. Die Einheiten sind [Installer-Einheiten](installer-units.md). Diese Zahl darf nicht negativ sein.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Flugh
</dt> <dd>

Höhe der rechteckigen Begrenzung des Steuer Elements. Die Einheiten sind [Installer-Einheiten](installer-units.md). Diese Zahl darf nicht negativ sein.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Ein 32-Bit-Wort, das die Attributflags angibt, die auf dieses Steuerelement angewendet werden sollen. Diese Zahl darf nicht negativ sein und ein Attribut für ein statisches Steuerelement angeben, das für die Platzierung in einem Billboard gültig ist. Informationen zu den numerischen Werten, die in dieses Feld eingegeben werden sollen, finden Sie unter das Attribut "Attribut" unter " [Steuer Attribute](control-attributes.md)".

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Diese Spalte enthält eine lokalisierbare Zeichenfolge, mit der der anfängliche Text im Steuerelement festgelegt wird, wenn das Steuerelement Text anzeigt. Die Zeichenfolge wird abgeschnitten, wenn der Text zu lang ist, um auf das Steuerelement zu passen. Diese Spalte enthält einen Schlüssel in die [binäre Tabelle](binary-table.md) , wenn das Steuerelement eine pushschaltfläche oder ein Kontrollkästchen ist, das ein Symbol oder eine Bitmap enthält. Es ist nicht möglich, sowohl Text als auch ein Bild auf derselben Schaltfläche anzuzeigen. Diese Spalte kann leer gelassen werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die ganzzahligen Werte für x, y, Width und Height befinden sich in den [Installations Einheiten](installer-units.md)und nicht in den Dialog Einheiten. Eine installereinheit ist gleich 1-zwölfte Höhe des 10-Punkt-MS Sans Serif-Schrift Grads. Die Koordinaten für die Steuerelemente sind relativ zum Billboard-Steuerelement, nicht zum Dialogfeld.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE95](ice95.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Msiseeltexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
</dt> </dl>

 

 



