---
title: MENUITEM-Anweisung
description: Definiert ein Menüelement.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- MENUITEM-Anweisung Menus and Other Resources
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45bca50025e1c9136c22166d6d3f758c5c9b5819a9328d33d375195285f1d4f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092190"
---
# <a name="menuitem-statement"></a>MENUITEM-Anweisung

Definiert ein Menüelement.

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Der Name des Menüelements.

Die Zeichenfolge kann die Escapezeichen **\\ t** und **\\ enthalten.** Das **\\ t-Zeichen** fügt eine Registerkarte in die Zeichenfolge ein und wird verwendet, um Text in Spalten auszurichten. Tabstoppzeichen sollten nur in Menüs und nicht in Menüleisten verwendet werden. (Informationen zu Menüs finden Sie unter [**POPUP-Ressource**](popup-resource.md).) Das **\\ Zeichen** richtet den gesamten darauf folgenden Text direkt in die Menüleiste oder das Popupmenü aus.

</dd> <dt>

<span id="result"></span><span id="RESULT"></span>*Ergebnis*
</dt> <dd>

Eine Zahl, die das Ergebnis angibt, das generiert wird, wenn der Benutzer das Menüelement auswählt. Dieser Parameter akzeptiert einen ganzzahligen Wert. Menüelementergebnisse sind immer ganze Zahlen. Wenn der Benutzer auf den Namen des Menüelements klickt, wird das Ergebnis an das Fenster gesendet, das das Menü besitzt.

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*Optionsliste*
</dt> <dd>

Die Darstellung des Menüelements. Dieser optionale Parameter verwendet eine oder mehrere der folgenden neu definierten Menüoptionen, getrennt durch Kommas oder Leerzeichen.



| Option           | BESCHREIBUNG                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Überprüft**      | Neben dem Menüelement befindet sich ein Häkchen.                                                                                                                                |
| **Grau**       | Das Menüelement ist anfänglich inaktiv und wird im Menü grau oder in einer aufgeblendeten Schattierung der Menütextfarbe angezeigt. Diese Option kann nicht mit der **Option INACTIVE** verwendet werden. |
| **Hilfe**         | Identifiziert ein Hilfeelement. Diese Option hat keine Auswirkungen auf die Darstellung des Menüelements.                                                                                 |
| **Inaktiv**     | Menüelement wird angezeigt, kann aber nicht ausgewählt werden. Diese Option kann nicht mit der **GRAYED-Option** verwendet werden.                                                              |
| **MENUBARBREAK** | Identisch mit **MENUBREAK,** mit der Ausnahme, dass für Popupmenüs die neue Spalte von der alten Spalte mit einer vertikalen Linie getrennt wird.                                             |
| **MENUBREAK**    | Platziert das Menüelement in einer neuen Zeile für statische Menüleistenelemente. Bei Menüs wird das Menüelement in eine neue Spalte ohne Trennlinie zwischen den Spalten platziert.           |



 

</dd> <dt>

<span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM-TRENNZEICHEN**
</dt> <dd>

Das **MENUITEM SEPARATOR-Formular** der **MENUITEM-Anweisung** erstellt ein inaktives Menüelement, das als Trennleiste zwischen zwei aktiven Menüelementen in einem Menü dient.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **MENUITEM-** und **MENUITEM SEPARATOR-Anweisungen** veranschaulicht:

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Menü**](menu-resource.md)
</dt> <dt>

[**Popup**](popup-resource.md)
</dt> </dl>

 

 




