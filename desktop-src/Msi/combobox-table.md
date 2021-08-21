---
description: Die Linien eines Kombinationsfelds werden nicht als einzelne Steuerelemente behandelt. sie sind Teil eines einzelnen Kombinationsfelds, das als Steuerelement fungiert. In dieser Tabelle werden die Werte für jedes Kombinationsfeld aufgeführt.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: ComboBox-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea20677ab6ede02f76a1061d5f715eb0b8d6d87a1744d1eb89b7e0918a018e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380295"
---
# <a name="combobox-table"></a>ComboBox-Tabelle

Die Linien eines Kombinationsfelds werden nicht als einzelne Steuerelemente behandelt. sie sind Teil eines einzelnen Kombinationsfelds, das als Steuerelement fungiert. In dieser Tabelle werden die Werte für jedes Kombinationsfeld aufgeführt.

Die ComboBox-Tabelle enthält die folgenden Spalten.



| Spalte   | Typ                         | Key | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Identifier](identifier.md) | J   | N        |
| Auftrag    | [Integer](integer.md)       | J   | N        |
| Wert    | [Formatiert](formatted.md)   | N   | N        |
| Text     | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Element gebunden werden soll. Alle Elemente, die an dieselbe Eigenschaft gebunden sind, werden Teil desselben Kombinationsfelds.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Bestellung
</dt> <dd>

Eine positive ganze Zahl, die verwendet wird, um die Reihenfolge der Elemente zu bestimmen, die in einer einzelnen Kombinationsfeldliste angezeigt werden. Die ganzen Zahlen müssen nicht aufeinander folgenden sein. Wenn ein Kombinationsfeld als geordnet definiert ist, sollten alle Elemente einen Order-Wert haben. Wenn das Kombinationsfeld als ungeordnet definiert ist, wird diese Spalte ignoriert.

Nur positive Zahlen.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die diesem Element zugeordnete Wertzeichenfolge. Wenn Sie diese Zeile des Kombinationsfelds auswählen, wird die zugeordnete Eigenschaft (in Eigenschaft angegeben) auf diesen Wert festgelegt.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Der sichtbare, lokalisierbare Text, der dem Element zugewiesen werden soll. Wenn dieser Eintrag oder die gesamte Spalte fehlt, wird der Text standardmäßig auf den Eintrag in Value festgelegt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Inhalt der Felder Value und Text wird beim Erstellen des Steuerelements von der [**MsiFormatRecord-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) formatiert. Daher können sie jeden Ausdruck enthalten, den die **MsiFormatRecord-Funktion** interpretieren kann. Die Formatierung erfolgt nur, wenn das Steuerelement erstellt wird, und es wird nicht aktualisiert, wenn eine eigenschaft, die am Ausdruck beteiligt ist, während der Lebensdauer des Steuerelements geändert wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



