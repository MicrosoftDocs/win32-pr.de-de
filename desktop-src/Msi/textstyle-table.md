---
description: In der TextStyle-Tabelle werden verschiedene Schriftart Stile aufgelistet, die in Steuerelementen mit Text verwendet werden
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: TextStyle-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959072"
---
# <a name="textstyle-table"></a>TextStyle-Tabelle

In der TextStyle-Tabelle werden verschiedene Schriftart Stile aufgelistet, die in Steuerelementen mit Text verwendet werden

Die TextStyle-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                               | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------------|-----|----------|
| Textart | [Bezeichner](identifier.md)       | J   | N        |
| Fakename  | [Text](text.md)                   | N   | N        |
| Size      | [Integer](integer.md)             | N   | N        |
| Color     | [Doubleiteger](doubleinteger.md) | N   | J        |
| Stylebits | [Integer](integer.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>Textart
</dt> <dd>

Diese Spalte ist der Name des Schriftart Stils. Dieser Name kann in die Text Zeichenfolge eingebettet werden, um eine Formatänderung anzugeben. Beachten Sie, dass der Name des Schriftart Stils, der in diesem Feld verwendet wird, nicht auf die folgenden Zeichen enden muss: \_ UL. Siehe [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md).

</dd> <dt>

<span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>Fakename
</dt> <dd>

Eine Zeichenfolge, die den Namen der Schriftart angibt. Die Zeichenfolge darf höchstens 31 Zeichen lang sein.

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>Größe
</dt> <dd>

Der Schrift Grad, der in Punkten gemessen wird. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="Color"></span><span id="color"></span><span id="COLOR"></span>Farbe
</dt> <dd>

Diese Spalte gibt die Textfarbe an, die von einem [Text Steuer](text-control.md)Element angezeigt wird. Alle anderen Steuerelement Typen verwenden immer die Standard Textfarbe. Der in dieser Spalte eingegebene Wert sollte mithilfe der folgenden Formel berechnet werden: 65536 \* Blue + 256 \* Green + Red, wobei rot, grün und blau jeweils im Bereich 0-255 angezeigt werden. Der Wert darf nicht größer als 16777215 sein. Dies ist der Wert für weiß. Der Wert ist 0 für schwarz, 255 für Rot, 65280 für Grün, 16711680 für blau und 8421504 für grau. Wenn das Feld leer gelassen wird, wird die Standardfarbe angegeben.

Platzieren Sie keine transparenten [Text Steuerelemente](text-control.md) oberhalb von farbigen Bitmaps. Der Text ist möglicherweise nicht sichtbar, wenn der Benutzer das Anzeige Farbschema ändert. Beispielsweise kann Text unsichtbar werden, wenn der Benutzer den hohen Kontrast Parameter für Barrierefreiheit festlegt.

</dd> <dt>

<span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>Stylebits
</dt> <dd>

Eine Kombination von Bits, die die Formatierung für den Text angibt.

Die einzelnen stilbits weisen die folgenden Werte auf.



| Konstante                             | Hexadezimal | Decimal | Stil      |
|--------------------------------------|-------------|---------|------------|
| **msidbtextstylestylebisibold**      | 0x001       | 1       | Fett       |
| **msidbtextstylestylebitsitalic**    | 0x002       | 2       | Kursiv     |
| **msidbtextstylestylebider-Unterstreichung** | 0x004       | 4       | Underline  |
| **msidbtextstylestylebisid**    | 0x008       | 8       | Streiken |



 

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE31](ice31.md)  
[ICE45](ice45.md)  
</dl>

 

 



