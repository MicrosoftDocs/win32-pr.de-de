---
title: Popup Ressource
description: Definiert ein Menü Element, das Menü Elemente und Untermenüs enthalten kann.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Popup Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c7a1af3bd8ed9aae8908aa7ff926a3f4799ee5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100946"
---
# <a name="popup-resource"></a>Popup Ressource

Definiert ein Menü Element, das Menü Elemente und Untermenüs enthalten kann.

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Eine Zeichenfolge, die den Namen des Menüs enthält. Diese Zeichenfolge muss in doppelte Anführungszeichen (**"**) eingeschlossen werden.

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

Dieser Parameter gibt neudefinierte Menü Optionen an, die die Darstellung des Menü Elements angeben. Der optionale Parameter kann eine oder mehrere der folgenden sein.



| Option           | BESCHREIBUNG                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Über**      | Das Menü Element enthält ein Häkchen daneben. Diese Option ist für ein Menü der obersten Ebene ungültig.                                                                                 |
| **Abgeblendet**       | Das Menü Element ist anfänglich inaktiv und wird im Menü grau oder in einem hellen Farbton der Menü Text Farbe angezeigt. Diese Option kann nicht mit der **inaktiven** Option verwendet werden. |
| **Hilfe**         | Identifiziert ein Hilfe Element. Das Menü Element wird an der rechten Position in der Menüleiste platziert.                                                                            |
| **VSTE**     | Das Menü Element wird angezeigt, es kann jedoch nicht ausgewählt werden. Diese Option kann nicht mit der Option **grau** verwendet werden.                                                              |
| **Menubarbreak** | Identisch mit **menubreak** , mit der Ausnahme, dass bei Popup Menüs die neue Spalte von der alten Spalte mit einer vertikalen Linie getrennt wird.                                             |
| **Menubreak**    | Platziert das Menü Element für statische Menüleisten Elemente in einer neuen Zeile. Für Menüs wird das Menü Element in einer neuen Spalte ohne Trennlinie zwischen den Spalten platziert.           |



 

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Popup** -Anweisung veranschaulicht:

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

[**Stehen**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> </dl>

 

 




