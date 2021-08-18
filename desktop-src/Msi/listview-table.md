---
description: Die Zeilen einer Listenansicht werden nicht als einzelne Steuerelemente behandelt, sie sind jedoch Teil einer Listenansicht, die als Steuerelement fungiert. Die ListView-Tabelle definiert die Werte für alle Listviews.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: ListView-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a84ebab6c90486283c3dd8d4731cc0b7f3aff11a5459a0e93496bab83d7c277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013078"
---
# <a name="listview-table"></a>ListView-Tabelle

Die Zeilen einer Listenansicht werden nicht als einzelne Steuerelemente behandelt, sie sind jedoch Teil einer Listenansicht, die als Steuerelement fungiert. Die ListView-Tabelle definiert die Werte für alle Listviews.

Die ListView-Tabelle enthält die folgenden Spalten.



| Spalte   | Typ                         | Key | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Identifier](identifier.md) | J   | N        |
| Auftrag    | [Integer](integer.md)       | J   | N        |
| Wert    | [Formatiert](formatted.md)   | N   | N        |
| Text     | [Formatiert](formatted.md)   | N   | J        |
| Binäre\_ | [Identifier](identifier.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Element gebunden werden soll. Alle Elemente, die an dieselbe Eigenschaft gebunden sind, werden Teil derselben Listview.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Bestellung
</dt> <dd>

Eine positive ganze Zahl, die verwendet wird, um die Reihenfolge der Elemente zu bestimmen, die in einer einzelnen Listview-Liste angezeigt werden. Die ganzen Zahlen müssen nicht aufeinander folgenden sein. Wenn eine Listview als geordnet definiert ist, sollten alle Elemente einen Ordering-Wert haben. Wenn die Listview als ungeordnet definiert ist, wird diese Spalte ignoriert.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die diesem Element zugeordnete Wertzeichenfolge. Wenn Sie die Zeile auswählen, wird die zugeordnete Eigenschaft auf diesen Wert fest.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Der sichtbare, lokalisierbare Text, der dem Element zugewiesen werden soll. Wenn dieser Eintrag oder die gesamte Spalte fehlt, wird der Text standardmäßig auf den entsprechenden Eintrag in Value festgelegt.

</dd> <dt>

<span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binäre\_
</dt> <dd>

Die Bilddaten für das Symbol. Dies ist ein Fremdschlüssel für die [Binärtabelle](binary-table.md).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Inhalt der Felder Value und Text wird beim Erstellen des Steuerelements von der [**MsiFormatRecord-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) formatiert. Daher können sie jeden Ausdruck enthalten, den die MsiFormatRecord-Funktion interpretieren kann. Die Formatierung tritt nur auf, wenn das Steuerelement erstellt wird, und wird nicht aktualisiert, wenn eine am Ausdruck beteiligte Eigenschaft während der Lebensdauer des Steuerelements geändert wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
</dl>

 

 



