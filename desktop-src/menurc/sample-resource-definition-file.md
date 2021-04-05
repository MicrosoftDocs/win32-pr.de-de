---
title: Beispiel Resource-Definition Datei
description: Beispielskript Datei, die die Ressourcen für eine Anwendung namens Shapes definiert.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e6a870b4b63b0e88e5ddcd069e8318e4bdb750
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037303"
---
# <a name="sample-resource-definition-file"></a>Beispiel Resource-Definition Datei

Das folgende Beispiel zeigt eine Skriptdatei, die die Ressourcen für eine Anwendung mit dem Namen "Shapes" definiert:

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

Die [**Cursor**](cursor-resource.md) Anweisung benennt den Cursor Ressourcen-shapescursor der Anwendung und gibt die Cursor Datei Formen an. Cur, die das Bild für diesen Cursor enthält.

Die [**Symbol**](icon-resource.md) -Anweisung benennt die Symbol Ressource shapesicon der Anwendung und gibt die Symbol Datei Formen an. ICO, das das Bild für das Symbol enthält.

Die [**Menu**](menu-resource.md) -Anweisung definiert ein Anwendungsmenü mit dem Namen **shapesmenu**, einem Popupmenü mit fünf Menü Elementen.

Der Text der Menü Definition, der durch geschweifte Klammern eingeschlossen ist, oder die **anfangs** -und **endschlüsselwörter** gibt jedes Menü Element und den Menü Bezeichner an, der zurückgegeben wird, wenn der Benutzer das Element auswählt. Beispielsweise gibt das erste Element im Menü **Clear** die menübezeichnerkennung Clear zurück, \_ Wenn der Benutzer es auswählt. Die Menü Bezeichner werden in der Anwendungs Header Datei Shapes. H definiert.

 

 




