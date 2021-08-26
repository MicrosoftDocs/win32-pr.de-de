---
title: POPUP-Ressource
description: Definiert ein Menüelement, das Menüelemente und Untermenüs enthalten kann.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- POPUP-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f134b2d5801bc5003be6f45b42d13f1668c2e684b5f63fe0aed1f2c9c0400860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952340"
---
# <a name="popup-resource"></a>POPUP-Ressource

Definiert ein Menüelement, das Menüelemente und Untermenüs enthalten kann.

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Eine Zeichenfolge, die den Namen des Menüs enthält. Diese Zeichenfolge muss in doppelte Anführungszeichen (**" ) eingeschlossen werden.**

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

Dieser Parameter gibt neu definierte Menüoptionen an, die die Darstellung des Menüelements angeben. Dieser optionale Parameter kann eine oder mehrere der folgenden Parameter sein.



| Option           | BESCHREIBUNG                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Überprüft**      | Neben dem Menüelement steht ein Häkchen. Diese Option ist für ein Menü der obersten Ebene ungültig.                                                                                 |
| **Grau**       | Das Menüelement ist anfänglich inaktiv und wird im Menü in Grau oder einem abgeblendet schattierten Farbton der Menütextfarbe angezeigt. Diese Option kann nicht mit der **Option INACTIVE verwendet** werden. |
| **Hilfe**         | Identifiziert ein Hilfeelement. Das Menüelement befindet sich rechts auf der Menüleiste.                                                                            |
| **Inaktiv**     | Das Menüelement wird angezeigt, kann aber nicht ausgewählt werden. Diese Option kann nicht mit der **GRAYED-Option verwendet** werden.                                                              |
| **MENUBARBREAK** | Identisch mit **MENUBREAK,** mit der Ausnahme, dass bei Popupmenüs die neue Spalte von der alten Spalte durch eine vertikale Linie getrennt wird.                                             |
| **MENUBREAK**    | Platziert das Menüelement in einer neuen Zeile für statische Menüleistenelemente. Bei Menüs wird das Menüelement in eine neue Spalte ohne Trennlinie zwischen den Spalten platziert.           |



 

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **POPUP-Anweisung** veranschaulicht:

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Menü**](menu-resource.md)
</dt> <dt>

[**Menuitem**](menuitem-statement.md)
</dt> </dl>

 

 




