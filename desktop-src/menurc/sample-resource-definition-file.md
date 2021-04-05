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
# <a name="sample-resource-definition-file"></a><span data-ttu-id="a4991-103">Beispiel Resource-Definition Datei</span><span class="sxs-lookup"><span data-stu-id="a4991-103">Sample Resource-Definition File</span></span>

<span data-ttu-id="a4991-104">Das folgende Beispiel zeigt eine Skriptdatei, die die Ressourcen für eine Anwendung mit dem Namen "Shapes" definiert:</span><span class="sxs-lookup"><span data-stu-id="a4991-104">The following example shows a script file that defines the resources for an application named Shapes:</span></span>

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

<span data-ttu-id="a4991-105">Die [**Cursor**](cursor-resource.md) Anweisung benennt den Cursor Ressourcen-shapescursor der Anwendung und gibt die Cursor Datei Formen an. Cur, die das Bild für diesen Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="a4991-105">The [**CURSOR**](cursor-resource.md) statement names the application's cursor resource ShapesCursor and specifies the cursor file SHAPES.CUR, which contains the image for that cursor.</span></span>

<span data-ttu-id="a4991-106">Die [**Symbol**](icon-resource.md) -Anweisung benennt die Symbol Ressource shapesicon der Anwendung und gibt die Symbol Datei Formen an. ICO, das das Bild für das Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="a4991-106">The [**ICON**](icon-resource.md) statement names the application's icon resource ShapesIcon and specifies the icon file SHAPES.ICO, which contains the image for that icon.</span></span>

<span data-ttu-id="a4991-107">Die [**Menu**](menu-resource.md) -Anweisung definiert ein Anwendungsmenü mit dem Namen **shapesmenu**, einem Popupmenü mit fünf Menü Elementen.</span><span class="sxs-lookup"><span data-stu-id="a4991-107">The [**MENU**](menu-resource.md) statement defines an application menu named **ShapesMenu**, a pop-up menu with five menu items.</span></span>

<span data-ttu-id="a4991-108">Der Text der Menü Definition, der durch geschweifte Klammern eingeschlossen ist, oder die **anfangs** -und **endschlüsselwörter** gibt jedes Menü Element und den Menü Bezeichner an, der zurückgegeben wird, wenn der Benutzer das Element auswählt.</span><span class="sxs-lookup"><span data-stu-id="a4991-108">The body of the menu definition, enclosed by the curly braces, or the **BEGIN** and **END** keywords, specifies each menu item and the menu identifier that is returned when the user selects that item.</span></span> <span data-ttu-id="a4991-109">Beispielsweise gibt das erste Element im Menü **Clear** die menübezeichnerkennung Clear zurück, \_ Wenn der Benutzer es auswählt.</span><span class="sxs-lookup"><span data-stu-id="a4991-109">For example, the first item on the menu, **Clear**, returns the menu identifier ID\_CLEAR when the user selects it.</span></span> <span data-ttu-id="a4991-110">Die Menü Bezeichner werden in der Anwendungs Header Datei Shapes. H definiert.</span><span class="sxs-lookup"><span data-stu-id="a4991-110">The menu identifiers are defined in the application header file, SHAPES.H.</span></span>

 

 




