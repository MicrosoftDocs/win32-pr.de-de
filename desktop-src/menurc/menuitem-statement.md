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
# <a name="menuitem-statement"></a><span data-ttu-id="7286a-104">MenuItem-Anweisung</span><span class="sxs-lookup"><span data-stu-id="7286a-104">MENUITEM statement</span></span>

<span data-ttu-id="7286a-105">Definiert ein Menü Element.</span><span class="sxs-lookup"><span data-stu-id="7286a-105">Defines a menu item.</span></span>

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span data-ttu-id="7286a-106"><span id="text"></span><span id="TEXT"></span>*Text*</span><span class="sxs-lookup"><span data-stu-id="7286a-106"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="7286a-107">Der Name des Menüelements.</span><span class="sxs-lookup"><span data-stu-id="7286a-107">The name of the menu item.</span></span>

<span data-ttu-id="7286a-108">Die **\\ Zeichenfolge kann** die Escapezeichen **\\ t** und enthalten.</span><span class="sxs-lookup"><span data-stu-id="7286a-108">The string can contain the escape characters **\\t** and **\\a**.</span></span> <span data-ttu-id="7286a-109">Das Zeichen **\\ t** fügt eine Registerkarte in die Zeichenfolge ein und wird zum Ausrichten von Text in Spalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="7286a-109">The **\\t** character inserts a tab in the string and is used to align text in columns.</span></span> <span data-ttu-id="7286a-110">Tabstopp Zeichen sollten nur in Menüs und nicht in Menüleisten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7286a-110">Tab characters should be used only in menus, not in menu bars.</span></span> <span data-ttu-id="7286a-111">(Informationen zu Menüs finden Sie unter [**Popup-Ressource**](popup-resource.md).) Das **\\ a** -Zeichen richtet den gesamten Text, der ihm folgt, direkt auf die Menüleiste oder das Popup Menü aus.</span><span class="sxs-lookup"><span data-stu-id="7286a-111">(For information on menus, see [**POPUP Resource**](popup-resource.md).) The **\\a** character aligns all text that follows it flush right to the menu bar or pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="7286a-112"><span id="result"></span><span id="RESULT"></span>*Dadurch*</span><span class="sxs-lookup"><span data-stu-id="7286a-112"><span id="result"></span><span id="RESULT"></span>*result*</span></span>
</dt> <dd>

<span data-ttu-id="7286a-113">Eine Zahl, die das Ergebnis angibt, das generiert wird, wenn der Benutzer das Menü Element auswählt.</span><span class="sxs-lookup"><span data-stu-id="7286a-113">A number that specifies the result generated when the user selects the menu item.</span></span> <span data-ttu-id="7286a-114">Dieser Parameter nimmt einen ganzzahligen Wert an.</span><span class="sxs-lookup"><span data-stu-id="7286a-114">This parameter takes an integer value.</span></span> <span data-ttu-id="7286a-115">Menü Element Ergebnisse sind immer ganze Zahlen. Wenn der Benutzer auf den Menü Elementnamen klickt, wird das Ergebnis an das Fenster gesendet, das das Menü besitzt.</span><span class="sxs-lookup"><span data-stu-id="7286a-115">Menu-item results are always integers; when the user clicks the menu-item name, the result is sent to the window that owns the menu.</span></span>

</dd> <dt>

<span data-ttu-id="7286a-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span><span class="sxs-lookup"><span data-stu-id="7286a-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="7286a-117">Die Darstellung des Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="7286a-117">The appearance of the menu item.</span></span> <span data-ttu-id="7286a-118">Dieser optionale Parameter übernimmt eine oder mehrere der folgenden neu definierten Menü Optionen, die durch Kommas oder Leerzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="7286a-118">This optional parameter takes one or more of the following redefined menu options, separated by commas or spaces.</span></span>



| <span data-ttu-id="7286a-119">Option</span><span class="sxs-lookup"><span data-stu-id="7286a-119">Option</span></span>           | <span data-ttu-id="7286a-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7286a-120">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7286a-121">**Über**</span><span class="sxs-lookup"><span data-stu-id="7286a-121">**CHECKED**</span></span>      | <span data-ttu-id="7286a-122">Das Menü Element enthält ein Häkchen daneben.</span><span class="sxs-lookup"><span data-stu-id="7286a-122">Menu item has a check mark next to it.</span></span>                                                                                                                                |
| <span data-ttu-id="7286a-123">**Abgeblendet**</span><span class="sxs-lookup"><span data-stu-id="7286a-123">**GRAYED**</span></span>       | <span data-ttu-id="7286a-124">Das Menü Element ist anfänglich inaktiv und wird im Menü grau oder in einem hellen Farbton der Menü Text Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7286a-124">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="7286a-125">Diese Option kann nicht mit der **inaktiven** Option verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7286a-125">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="7286a-126">**Hilfe**</span><span class="sxs-lookup"><span data-stu-id="7286a-126">**HELP**</span></span>         | <span data-ttu-id="7286a-127">Identifiziert ein Hilfe Element.</span><span class="sxs-lookup"><span data-stu-id="7286a-127">Identifies a help item.</span></span> <span data-ttu-id="7286a-128">Diese Option hat keine Auswirkung auf die Darstellung des Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="7286a-128">This option has no effect on the appearance of the menu item.</span></span>                                                                                 |
| <span data-ttu-id="7286a-129">**VSTE**</span><span class="sxs-lookup"><span data-stu-id="7286a-129">**INACTIVE**</span></span>     | <span data-ttu-id="7286a-130">Das Menü Element wird angezeigt, es kann jedoch nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="7286a-130">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="7286a-131">Diese Option kann nicht mit der Option **grau** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7286a-131">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="7286a-132">**Menubarbreak**</span><span class="sxs-lookup"><span data-stu-id="7286a-132">**MENUBARBREAK**</span></span> | <span data-ttu-id="7286a-133">Identisch mit **menubreak** , mit der Ausnahme, dass bei Popup Menüs die neue Spalte von der alten Spalte mit einer vertikalen Linie getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="7286a-133">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="7286a-134">**Menubreak**</span><span class="sxs-lookup"><span data-stu-id="7286a-134">**MENUBREAK**</span></span>    | <span data-ttu-id="7286a-135">Platziert das Menü Element für statische Menüleisten Elemente in einer neuen Zeile.</span><span class="sxs-lookup"><span data-stu-id="7286a-135">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="7286a-136">Für Menüs wird das Menü Element in einer neuen Spalte ohne Trennlinie zwischen den Spalten platziert.</span><span class="sxs-lookup"><span data-stu-id="7286a-136">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="7286a-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MenuItem-Trennzeichen**</span><span class="sxs-lookup"><span data-stu-id="7286a-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM SEPARATOR**</span></span>
</dt> <dd>

<span data-ttu-id="7286a-138">Mit dem **MenuItem-Trenn** Zeichen Formular der **MenuItem** -Anweisung wird ein inaktives Menü Element erstellt, das als Trennleiste zwischen zwei aktiven Menü Elementen in einem Menü fungiert.</span><span class="sxs-lookup"><span data-stu-id="7286a-138">The **MENUITEM SEPARATOR** form of the **MENUITEM** statement creates an inactive menu item that serves as a dividing bar between two active menu items on a menu.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7286a-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7286a-139">Examples</span></span>

<span data-ttu-id="7286a-140">Das folgende Beispiel veranschaulicht die Verwendung der **MenuItem** -und **MenuItem-Trenn** Zeichen Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="7286a-140">The following example demonstrates the use of the **MENUITEM** and **MENUITEM SEPARATOR** statements:</span></span>

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a><span data-ttu-id="7286a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7286a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7286a-142">**Stehen**</span><span class="sxs-lookup"><span data-stu-id="7286a-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="7286a-143">**Up**</span><span class="sxs-lookup"><span data-stu-id="7286a-143">**POPUP**</span></span>](popup-resource.md)
</dt> </dl>

 

 




