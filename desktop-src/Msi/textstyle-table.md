---
description: In der Tabelle TextStyle werden verschiedene Schriftschnitte aufgeführt, die in Steuerelementen mit Text verwendet werden.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: TextStyle-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f8a5b3141314722bc5b92e34ea214fa8e1505babfbc8b7f942899e6c6779c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623488"
---
# <a name="textstyle-table"></a>TextStyle-Tabelle

In der Tabelle TextStyle werden verschiedene Schriftschnitte aufgeführt, die in Steuerelementen mit Text verwendet werden.

Die TextStyle-Tabelle enthält die folgenden Spalten.



| Spalte    | Typ                               | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------------|-----|----------|
| TextStyle | [Identifier](identifier.md)       | J   | N        |
| GesichtsName  | [Text](text.md)                   | N   | N        |
| Size      | [Integer](integer.md)             | N   | N        |
| Color     | [DoubleInteger](doubleinteger.md) | N   | J        |
| StyleBits | [Integer](integer.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle
</dt> <dd>

Diese Spalte ist der Name des Schriftschnitts. Dieser Name kann in die Textzeichenfolge eingebettet werden, um eine Stiländerung anzugeben. Beachten Sie, dass der in diesem Feld verwendete Schriftartstilname nicht mit den folgenden Zeichen enden darf: \_ UL. Weitere Informationen [finden Sie unter Hinzufügen von Steuerelementen und Text.](adding-controls-and-text.md)

</dd> <dt>

<span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName
</dt> <dd>

Eine Zeichenfolge, die den Namen der Schriftart angibt. Die Zeichenfolge darf nicht länger als 31 Zeichen sein.

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>Größe
</dt> <dd>

Der in Punkten gemessene Schriftgrad. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="Color"></span><span id="color"></span><span id="COLOR"></span>Farbe
</dt> <dd>

Diese Spalte gibt die Textfarbe an, die von einem [Textsteuerfeld angezeigt wird.](text-control.md) Alle anderen Steuerelementtypen verwenden immer die Standardtextfarbe. Der in dieser Spalte enthaltene Wert sollte mit der folgenden Formel berechnet werden: 65536 blau + 256 grün + rot, wobei Rot, Grün und Blau jeweils im Bereich von \* \* 0 bis 255 liegen. Der Wert darf den Wert 16777215, der der Wert für Weiß ist, nicht überschreiten. Der Wert ist 0 für Schwarz, 255 für Rot, 65280 für Grün, 16711680 blau und 8421504 grau. Wenn Sie das Feld leer lassen, wird die Standardfarbe angegeben.

Platzieren Sie transparente [Textsteuerelemente nicht](text-control.md) über farbigen Bitmaps. Der Text ist möglicherweise nicht sichtbar, wenn der Benutzer das Anzeigefarbschema ändert. Beispielsweise kann Text unsichtbar werden, wenn der Benutzer den Parameter für hohen Kontrast für die Barrierefreiheit festgibt.

</dd> <dt>

<span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits
</dt> <dd>

Eine Kombination von Bits, die die Formatierung für den Text angibt.

Die einzelnen Stilbits verfügen über die folgenden Werte.



| Konstante                             | Hexadezimal | Decimal | Style      |
|--------------------------------------|-------------|---------|------------|
| **msidbTextStyleStyleBitsBold**      | 0x001       | 1       | Fett       |
| **msidbTextStyleStyleBitsItalic**    | 0x002       | 2       | Kursiv     |
| **msidbTextStyleStyleBitsUnderline** | 0x004       | 4       | Underline  |
| **msidbTextStyleStyleBitsStrike**    | 0x008       | 8       | Ausschlagen |



 

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE31](ice31.md)  
[ICE45](ice45.md)  
</dl>

 

 



