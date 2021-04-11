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
# <a name="popup-resource"></a><span data-ttu-id="022ec-104">Popup Ressource</span><span class="sxs-lookup"><span data-stu-id="022ec-104">POPUP resource</span></span>

<span data-ttu-id="022ec-105">Definiert ein Menü Element, das Menü Elemente und Untermenüs enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="022ec-105">Defines a menu item that can contain menu items and submenus.</span></span>

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a><span data-ttu-id="022ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="022ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="022ec-107"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="022ec-107"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="022ec-108">Eine Zeichenfolge, die den Namen des Menüs enthält.</span><span class="sxs-lookup"><span data-stu-id="022ec-108">String that contains the name of the menu.</span></span> <span data-ttu-id="022ec-109">Diese Zeichenfolge muss in doppelte Anführungszeichen (**"**) eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="022ec-109">This string must be enclosed in double quotation marks (**"**).</span></span>

</dd> <dt>

<span data-ttu-id="022ec-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span><span class="sxs-lookup"><span data-stu-id="022ec-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="022ec-111">Dieser Parameter gibt neudefinierte Menü Optionen an, die die Darstellung des Menü Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="022ec-111">This parameter specifies redefined menu options that specify the appearance of the menu item.</span></span> <span data-ttu-id="022ec-112">Der optionale Parameter kann eine oder mehrere der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="022ec-112">This optional parameter can be one or more of the following.</span></span>



| <span data-ttu-id="022ec-113">Option</span><span class="sxs-lookup"><span data-stu-id="022ec-113">Option</span></span>           | <span data-ttu-id="022ec-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="022ec-114">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="022ec-115">**Über**</span><span class="sxs-lookup"><span data-stu-id="022ec-115">**CHECKED**</span></span>      | <span data-ttu-id="022ec-116">Das Menü Element enthält ein Häkchen daneben.</span><span class="sxs-lookup"><span data-stu-id="022ec-116">Menu item has a check mark next to it.</span></span> <span data-ttu-id="022ec-117">Diese Option ist für ein Menü der obersten Ebene ungültig.</span><span class="sxs-lookup"><span data-stu-id="022ec-117">This option is not valid for a top-level menu.</span></span>                                                                                 |
| <span data-ttu-id="022ec-118">**Abgeblendet**</span><span class="sxs-lookup"><span data-stu-id="022ec-118">**GRAYED**</span></span>       | <span data-ttu-id="022ec-119">Das Menü Element ist anfänglich inaktiv und wird im Menü grau oder in einem hellen Farbton der Menü Text Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="022ec-119">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="022ec-120">Diese Option kann nicht mit der **inaktiven** Option verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="022ec-120">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="022ec-121">**Hilfe**</span><span class="sxs-lookup"><span data-stu-id="022ec-121">**HELP**</span></span>         | <span data-ttu-id="022ec-122">Identifiziert ein Hilfe Element.</span><span class="sxs-lookup"><span data-stu-id="022ec-122">Identifies a help item.</span></span> <span data-ttu-id="022ec-123">Das Menü Element wird an der rechten Position in der Menüleiste platziert.</span><span class="sxs-lookup"><span data-stu-id="022ec-123">The menu item is place at the right-most position on the menu bar.</span></span>                                                                            |
| <span data-ttu-id="022ec-124">**VSTE**</span><span class="sxs-lookup"><span data-stu-id="022ec-124">**INACTIVE**</span></span>     | <span data-ttu-id="022ec-125">Das Menü Element wird angezeigt, es kann jedoch nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="022ec-125">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="022ec-126">Diese Option kann nicht mit der Option **grau** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="022ec-126">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="022ec-127">**Menubarbreak**</span><span class="sxs-lookup"><span data-stu-id="022ec-127">**MENUBARBREAK**</span></span> | <span data-ttu-id="022ec-128">Identisch mit **menubreak** , mit der Ausnahme, dass bei Popup Menüs die neue Spalte von der alten Spalte mit einer vertikalen Linie getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="022ec-128">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="022ec-129">**Menubreak**</span><span class="sxs-lookup"><span data-stu-id="022ec-129">**MENUBREAK**</span></span>    | <span data-ttu-id="022ec-130">Platziert das Menü Element für statische Menüleisten Elemente in einer neuen Zeile.</span><span class="sxs-lookup"><span data-stu-id="022ec-130">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="022ec-131">Für Menüs wird das Menü Element in einer neuen Spalte ohne Trennlinie zwischen den Spalten platziert.</span><span class="sxs-lookup"><span data-stu-id="022ec-131">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> </dl>

<span data-ttu-id="022ec-132">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="022ec-132">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="022ec-133">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="022ec-133">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="022ec-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="022ec-134">Examples</span></span>

<span data-ttu-id="022ec-135">Im folgenden Beispiel wird die Verwendung der **Popup** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="022ec-135">The following example demonstrates the use of the **POPUP** statement:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="022ec-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="022ec-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022ec-137">**Stehen**</span><span class="sxs-lookup"><span data-stu-id="022ec-137">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="022ec-138">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="022ec-138">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> </dl>

 

 




