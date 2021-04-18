---
description: Die Linien eines Kombinations Felds werden nicht als einzelne Steuerelemente behandelt. Sie sind Teil eines einzelnen Kombinations Felds, das als Steuerelement fungiert. In dieser Tabelle werden die Werte für jedes Kombinations Feld aufgelistet.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: ComboBox-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e209ac8a7c27c36fd5c1bbd3c97822617c48f5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352431"
---
# <a name="combobox-table"></a>ComboBox-Tabelle

Die Linien eines Kombinations Felds werden nicht als einzelne Steuerelemente behandelt. Sie sind Teil eines einzelnen Kombinations Felds, das als Steuerelement fungiert. In dieser Tabelle werden die Werte für jedes Kombinations Feld aufgelistet.

Die ComboBox-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Bezeichner](identifier.md) | J   | N        |
| Auftrag    | [Integer](integer.md)       | J   | N        |
| Wert    | [Großformatige](formatted.md)   | N   | N        |
| Text     | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Element gebunden werden soll. Alle Elemente, die an dieselbe Eigenschaft gebunden sind, werden Teil desselben Kombinations Felds.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge
</dt> <dd>

Eine positive ganze Zahl, die verwendet wird, um die Reihenfolge der Elemente zu bestimmen, die in einer einzelnen Kombinations Feld Liste angezeigt werden. Die ganzen Zahlen müssen nicht aufeinander folgen. Wenn ein Kombinations Feld als sortiert definiert ist, sollten alle Elemente über einen Bestellwert verfügen. Wenn das Kombinations Feld als nicht geordnet definiert ist, wird diese Spalte ignoriert.

Nur positive Zahlen.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die diesem Element zugeordnete Wert Zeichenfolge. Wenn Sie diese Zeile im Kombinations Feld auswählen, wird die zugehörige Eigenschaft (in der-Eigenschaft angegeben) auf diesen Wert festgelegt.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Der sichtbare, lokalisierbare Text, der dem Element zugewiesen werden soll. Wenn dieser Eintrag oder die gesamte Spalte fehlt, wird für den Text standardmäßig der Wert "Value" verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das Steuerelement erstellt wird, werden die Inhalte der Werte und Text Felder von der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion formatiert und können daher jeden beliebigen Ausdruck enthalten, der von der **msiformatrecord** -Funktion interpretiert werden kann. Die Formatierung erfolgt nur, wenn das Steuerelement erstellt wird, und es wird nicht aktualisiert, wenn eine Eigenschaft, die an dem Ausdruck beteiligt ist, während der Lebensdauer des Steuer Elements geändert wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



