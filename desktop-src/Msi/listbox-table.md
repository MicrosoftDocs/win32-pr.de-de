---
description: Die Zeilen eines Listenfelds werden nicht als einzelne Steuerelemente behandelt, sie sind jedoch Teil eines Listenfelds, das als Steuerelement fungiert. Die ListBox-Tabelle definiert die Werte für alle Listenfelder.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: ListBox-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8877db002185cd675914eca6d5be38454796c7b50af6a48f88e0e63c10c195
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043190"
---
# <a name="listbox-table"></a>ListBox-Tabelle

Die Zeilen eines Listenfelds werden nicht als einzelne Steuerelemente behandelt, sie sind jedoch Teil eines Listenfelds, das als Steuerelement fungiert. Die ListBox-Tabelle definiert die Werte für alle Listenfelder.

Die ListBox-Tabelle enthält die folgenden Spalten.



| Spalte   | Typ                         | Key | Nullwerte zulässig |
|----------|------------------------------|-----|----------|
| Eigenschaft | [Identifier](identifier.md) | J   | N        |
| Auftrag    | [Integer](integer.md)       | J   | N        |
| Wert    | [Formatiert](formatted.md)   | N   | N        |
| Text     | [Formatiert](formatted.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Eine benannte Eigenschaft, die an dieses Element gebunden werden soll. Alle Elemente, die an dieselbe Eigenschaft gebunden sind, werden Teil desselben Listenfelds.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Bestellung
</dt> <dd>

Eine positive ganze Zahl, die verwendet wird, um die Reihenfolge der Elemente zu bestimmen, die in einem einzelnen Listenfeld angezeigt werden. Wenn das Listenfeld als geordnet definiert ist, sollten alle Elemente einen Order-Wert haben. Die ganzen Zahlen müssen nicht aufeinander folgenden sein. Wenn das Listenfeld als ungeordnet definiert ist, wird diese Spalte ignoriert.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Die diesem Element zugeordnete Wertzeichenfolge. Wenn Sie die Zeile auswählen, wird die zugeordnete Eigenschaft auf diesen Wert fest.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text
</dt> <dd>

Der lokalisierbare, sichtbare Text, der dem Element zugewiesen werden soll. Wenn dieser Eintrag oder die gesamte Spalte fehlt, wird der Text standardmäßig auf den entsprechenden Eintrag in Value festgelegt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Inhalt der Felder Value und Text wird beim Erstellen des Steuerelements von der [**MsiFormatRecord-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) formatiert. Daher können sie jeden Ausdruck enthalten, den die **MsiFormatRecord-Funktion** interpretieren kann. Die Formatierung tritt nur auf, wenn das Steuerelement erstellt wird, und wird nicht aktualisiert, wenn eine am Ausdruck beteiligte Eigenschaft während der Lebensdauer des Steuerelements geändert wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE46](ice46.md)  
</dl>

 

 



