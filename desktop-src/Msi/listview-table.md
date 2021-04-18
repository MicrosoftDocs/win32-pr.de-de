---
description: Die Zeilen einer ListView werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil einer ListView, die als Steuerelement fungiert. In der ListView-Tabelle sind die Werte für alle ListViews definiert.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: ListView-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347942"
---
# <a name="listview-table"></a>ListView-Tabelle

Die Zeilen einer ListView werden nicht als einzelne Steuerelemente behandelt, aber Sie sind Teil einer ListView, die als Steuerelement fungiert. In der ListView-Tabelle sind die Werte für alle ListViews definiert.

Die ListView-Tabelle weist die folgenden Spalten auf.



| Spalte   | Typ                         | Schlüssel | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Bezeichner](identifier.md) | J   | N        |
| Auftrag    | [Integer](integer.md)       | J   | N        |
| Wert    | [Großformatige](formatted.md)   | N   | N        |
| Text     | [Großformatige](formatted.md)   | N   | J        |
| Binary\_ | [Bezeichner](identifier.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Element gebunden werden soll. Alle Elemente, die an dieselbe Eigenschaft gebunden sind, werden Teil derselben ListView.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Reihenfolge
</dt> <dd>

Eine positive ganze Zahl, mit der die Reihenfolge der Elemente bestimmt wird, die in einer einzelnen ListView-Liste angezeigt werden. Die ganzen Zahlen müssen nicht aufeinander folgen. Wenn eine ListView als geordnet definiert ist, sollten alle Elemente über einen Bestellwert verfügen. Wenn ListView als nicht geordnet definiert ist, wird diese Spalte ignoriert.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die diesem Element zugeordnete Wert Zeichenfolge. Durch Auswählen der Zeile wird die zugehörige Eigenschaft auf diesen Wert festgelegt.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Der sichtbare, lokalisierbare Text, der dem Element zugewiesen werden soll. Wenn dieser Eintrag oder die gesamte Spalte fehlt, wird der Text standardmäßig auf den entsprechenden Eintrag in value eingestellt.

</dd> <dt>

<span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Ärer\_
</dt> <dd>

Die Bilddaten für das Symbol. Dabei handelt es sich um einen Fremdschlüssel für die [binäre Tabelle](binary-table.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das Steuerelement erstellt wird, werden die Inhalte der Werte und Text Felder von der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion formatiert und können daher jeden beliebigen Ausdruck enthalten, der von der msiformatrecord-Funktion interpretiert werden kann. Die Formatierung erfolgt nur, wenn das Steuerelement erstellt wird, und es wird nicht aktualisiert, wenn eine Eigenschaft, die an dem Ausdruck beteiligt ist, während der Lebensdauer des Steuer Elements geändert wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
</dl>

 

 



