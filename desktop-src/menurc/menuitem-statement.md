---
title: MenuItem-Anweisung
description: Definiert ein Menü Element.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- MenuItem-Anweisungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339032"
---
# <a name="menuitem-statement"></a>MenuItem-Anweisung

Definiert ein Menü Element.

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Der Name des Menüelements.

Die **\\ Zeichenfolge kann** die Escapezeichen **\\ t** und enthalten. Das Zeichen **\\ t** fügt eine Registerkarte in die Zeichenfolge ein und wird zum Ausrichten von Text in Spalten verwendet. Tabstopp Zeichen sollten nur in Menüs und nicht in Menüleisten verwendet werden. (Informationen zu Menüs finden Sie unter [**Popup-Ressource**](popup-resource.md).) Das **\\ a** -Zeichen richtet den gesamten Text, der ihm folgt, direkt auf die Menüleiste oder das Popup Menü aus.

</dd> <dt>

<span id="result"></span><span id="RESULT"></span>*Dadurch*
</dt> <dd>

Eine Zahl, die das Ergebnis angibt, das generiert wird, wenn der Benutzer das Menü Element auswählt. Dieser Parameter nimmt einen ganzzahligen Wert an. Menü Element Ergebnisse sind immer ganze Zahlen. Wenn der Benutzer auf den Menü Elementnamen klickt, wird das Ergebnis an das Fenster gesendet, das das Menü besitzt.

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

Die Darstellung des Menü Elements. Dieser optionale Parameter übernimmt eine oder mehrere der folgenden neu definierten Menü Optionen, die durch Kommas oder Leerzeichen getrennt sind.



| Option           | BESCHREIBUNG                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Über**      | Das Menü Element enthält ein Häkchen daneben.                                                                                                                                |
| **Abgeblendet**       | Das Menü Element ist anfänglich inaktiv und wird im Menü grau oder in einem hellen Farbton der Menü Text Farbe angezeigt. Diese Option kann nicht mit der **inaktiven** Option verwendet werden. |
| **Hilfe**         | Identifiziert ein Hilfe Element. Diese Option hat keine Auswirkung auf die Darstellung des Menü Elements.                                                                                 |
| **VSTE**     | Das Menü Element wird angezeigt, es kann jedoch nicht ausgewählt werden. Diese Option kann nicht mit der Option **grau** verwendet werden.                                                              |
| **Menubarbreak** | Identisch mit **menubreak** , mit der Ausnahme, dass bei Popup Menüs die neue Spalte von der alten Spalte mit einer vertikalen Linie getrennt wird.                                             |
| **Menubreak**    | Platziert das Menü Element für statische Menüleisten Elemente in einer neuen Zeile. Für Menüs wird das Menü Element in einer neuen Spalte ohne Trennlinie zwischen den Spalten platziert.           |



 

</dd> <dt>

<span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MenuItem-Trennzeichen**
</dt> <dd>

Mit dem **MenuItem-Trenn** Zeichen Formular der **MenuItem** -Anweisung wird ein inaktives Menü Element erstellt, das als Trennleiste zwischen zwei aktiven Menü Elementen in einem Menü fungiert.

</dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht die Verwendung der **MenuItem** -und **MenuItem-Trenn** Zeichen Anweisungen:

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Stehen**](menu-resource.md)
</dt> <dt>

[**Up**](popup-resource.md)
</dt> </dl>

 

 




