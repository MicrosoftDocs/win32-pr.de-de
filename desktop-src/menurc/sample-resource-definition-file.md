---
title: Beispieldatei Resource-Definition Beispieldatei
description: Beispielskriptdatei, die die Ressourcen für eine Anwendung namens Shapes definiert.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141258148b4e7a21d625a44b7f03d5e383c318d10447e050891f32b397c4283d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226000"
---
# <a name="sample-resource-definition-file"></a>Beispieldatei Resource-Definition Beispieldatei

Das folgende Beispiel zeigt eine Skriptdatei, die die Ressourcen für eine Anwendung namens Shapes definiert:

``` syntax
#include "shapes.h"

ShapesCursor  CURSOR  SHAPES.CUR
ShapesIcon    ICON    SHAPES.ICO

ShapesMenu MENU
{
    POPUP "&Shape"
    {
        MENUITEM "&Clear", ID_CLEAR
        MENUITEM "&Rectangle", ID_RECT
        MENUITEM "&Triangle", ID_TRIANGLE
        MENUITEM "&Star", ID_STAR
        MENUITEM "&Ellipse", ID_ELLIPSE
    }
}
```

Die [**CURSOR-Anweisung**](cursor-resource.md) benennt die Cursorressource ShapesCursor der Anwendung und gibt die Cursordatei SHAPES an. CUR, das das Bild für diesen Cursor enthält.

Die [**ICON-Anweisung**](icon-resource.md) benennt die Symbolressource ShapesIcon der Anwendung und gibt die Symboldatei SHAPES an. ICO, das das Bild für dieses Symbol enthält.

Die [**MENU-Anweisung**](menu-resource.md) definiert ein Anwendungsmenü namens **ShapesMenu,** ein Popupmenü mit fünf Menüelementen.

Der Text der Menüdefinition, eingeschlossen in geschweifte Klammern oder die **Schlüsselwörter BEGIN** und **END,** gibt jedes Menüelement und den Menübezeichner an, der zurückgegeben wird, wenn der Benutzer dieses Element auswählt. Beispielsweise gibt das erste Element im **Menü,** Löschen, die Menübezeichner-ID CLEAR zurück, wenn der Benutzer \_ sie auswählt. Die Menübezeichner werden in der Anwendungsheaderdatei SHAPES.H definiert.

 

 




