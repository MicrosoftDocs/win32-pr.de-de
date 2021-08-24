---
description: In der TABELLE BBControl sind die Steuerelemente aufgeführt, die auf jedem Schild angezeigt werden sollen.
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: BBControl-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70198167c866195204ec6cbcf644b92f3489a4ff44e14e719efbf5c6647e30c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754370"
---
# <a name="bbcontrol-table"></a>BBControl-Tabelle

In der TABELLE BBControl sind die Steuerelemente aufgeführt, die auf jedem Schild angezeigt werden sollen.

Die BBControl-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                               | Key | Nullwerte zulässig |
|-------------|------------------------------------|-----|----------|
| Billboard\_ | [Identifier](identifier.md)       | J   | N        |
| BBControl   | [Identifier](identifier.md)       | J   | N        |
| type        | [Identifier](identifier.md)       | N   | N        |
| X           | [Integer](integer.md)             | N   | N        |
| J           | [Integer](integer.md)             | N   | N        |
| Breite       | [Integer](integer.md)             | N   | N        |
| Höhe      | [Integer](integer.md)             | N   | N        |
| Attribute  | [DoubleInteger](doubleinteger.md) | N   | J        |
| Text        | [Text](text.md)                   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Billboard_"></span><span id="billboard_"></span><span id="BILLBOARD_"></span>Billboard\_
</dt> <dd>

Name des Schilds.

Externer Schlüssel zu Spalte 1 der [Tabelle "Der Tabellenname".](billboard-table.md)

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>BBControl
</dt> <dd>

Name des Steuerelements. Dieser Name muss innerhalb eines Schilds eindeutig sein, kann aber auf verschiedenen Tafeln wiederholt werden. Diese Spalte bildet in Kombination mit der Spalte \_ "Spaltenname" den Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Typ
</dt> <dd>

Der Typ des Steuerelements. Nur statische Steuerelemente, z. B. [ein Text-,](text-control.md) [Bitmap-,](bitmap-control.md) [Symbol-](icon-control.md)oder benutzerdefiniertes Steuerelement, können auf einer Leiste platziert werden. Eine vollständige Liste der Steuerelemente finden Sie im [Abschnitt Steuerelemente.](controls.md)

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Horizontale Koordinate der oberen linken Ecke der rechteckigen Begrenzung des Steuerelements. Die Einheiten sind [Installationseinheiten.](installer-units.md) Diese Koordinate wird relativ zum Steuerungssteuerfeld und nicht relativ zum Dialog gemessen. Verwenden Sie nur nicht negative Zahlen.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Vertikale Koordinate der oberen linken Ecke der rechteckigen Begrenzung des Steuerelements. Die Einheiten sind [Installationseinheiten.](installer-units.md) Diese Koordinate wird relativ zum Steuerungssteuerfeld und nicht relativ zum Dialog gemessen. Diese Zahl darf nicht negativ sein.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Breite
</dt> <dd>

Breite der rechteckigen Begrenzung des Steuerelements. Die Einheiten sind [Installationseinheiten.](installer-units.md) Diese Zahl darf nicht negativ sein.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Höhe
</dt> <dd>

Höhe der rechteckigen Begrenzung des Steuerelements. Die Einheiten sind [Installationseinheiten.](installer-units.md) Diese Zahl darf nicht negativ sein.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Ein 32-Bit-Wort, das die Attributflags an gibt, die auf dieses Steuerelement angewendet werden sollen. Diese Zahl muss nicht negativ sein und ein Attribut für ein statisches Steuerelement angeben, das für die Platzierung auf einem Schild gültig ist. Informationen zu den numerischen Werten, die in dieses Feld eingegeben werden sollen, finden Sie im jeweiligen Attribut unter [Steuerelementattribute.](control-attributes.md)

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Diese Spalte enthält eine lokalisierbare Zeichenfolge, mit der der ursprüngliche Text im Steuerelement festgelegt wird, wenn das Steuerelement Text anzeigt. Die Zeichenfolge wird abgeschnitten, wenn der Text zu lang ist, um auf das Steuerelement zu passen. Diese Spalte enthält einen Schlüssel in der [Binärtabelle,](binary-table.md) wenn das Steuerelement eine Pushschaltfläche oder ein Kontrollkästchen mit einem Symbol oder einer Bitmap ist. Es ist nicht möglich, sowohl Text als auch ein Bild auf derselben Schaltfläche zu zeigen. Diese Spalte bleibt möglicherweise leer.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die ganzzahligen Werte für x, y, width und height befinden sich in den [Installationseinheiten,](installer-units.md)nicht in Dialogeinheiten. Eine Installationseinheit entspricht der Zwölftelhöhe des 10-Punkt-MS Sans Serif-Schriftgrads. Die Koordinaten für die Steuerelemente sind relativ zum Steuerelement des Steuerelements , nicht zum Dialogfeld.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE95](ice95.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
</dt> </dl>

 

 



