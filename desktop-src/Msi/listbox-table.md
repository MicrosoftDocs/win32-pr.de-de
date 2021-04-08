---
description: Die Zeilen eines Listen Felds werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil eines Listen Felds, das als Steuerelement fungiert. Die ListBox-Tabelle definiert die Werte für alle Listenfelder.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: ListBox-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960036"
---
# <a name="listbox-table"></a>ListBox-Tabelle

Die Zeilen eines Listen Felds werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil eines Listen Felds, das als Steuerelement fungiert. Die ListBox-Tabelle definiert die Werte für alle Listenfelder.

Die ListBox-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Bezeichner](identifier.md) | J   | N        |
| Auftrag    | [Integer](integer.md)       | J   | N        |
| Wert    | [Großformatige](formatted.md)   | N   | N        |
| Text     | [Großformatige](formatted.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Element gebunden werden soll. Alle Elemente, die an dieselbe Eigenschaft gebunden sind, werden Teil desselben Listen Felds.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge
</dt> <dd>

Eine positive ganze Zahl, die verwendet wird, um die Reihenfolge der Elemente zu bestimmen, die in einem einzelnen Listenfeld angezeigt werden. Wenn das Listenfeld als sortiert definiert ist, sollten alle Elemente über einen Bestellwert verfügen. Die ganzen Zahlen müssen nicht aufeinander folgen. Wenn das Listenfeld als nicht geordnet definiert ist, wird diese Spalte ignoriert.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die diesem Element zugeordnete Wert Zeichenfolge. Durch Auswählen der Zeile wird die zugehörige Eigenschaft auf diesen Wert festgelegt.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Der lokalisierbare, sichtbare Text, der dem Element zugewiesen werden soll. Wenn dieser Eintrag oder die gesamte Spalte fehlt, wird der Text standardmäßig auf den entsprechenden Eintrag in value eingestellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das Steuerelement erstellt wird, werden die Inhalte der Werte und Text Felder von der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion formatiert und können daher jeden beliebigen Ausdruck enthalten, der von der **msiformatrecord** -Funktion interpretiert werden kann. Die Formatierung erfolgt nur, wenn das Steuerelement erstellt wird, und es wird nicht aktualisiert, wenn eine Eigenschaft, die an dem Ausdruck beteiligt ist, während der Lebensdauer des Steuer Elements geändert wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE46](ice46.md)  
</dl>

 

 



