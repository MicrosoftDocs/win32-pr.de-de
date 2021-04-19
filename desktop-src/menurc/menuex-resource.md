---
title: Menuex-Ressource
description: Definiert den Inhalt einer Menü Ressource. | Menuex-Ressource
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menuex-Ressourcen Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363100"
---
# <a name="menuex-resource"></a><span data-ttu-id="91c32-105">Menuex-Ressource</span><span class="sxs-lookup"><span data-stu-id="91c32-105">MENUEX resource</span></span>

<span data-ttu-id="91c32-106">Definiert den Inhalt einer Menü Ressource.</span><span class="sxs-lookup"><span data-stu-id="91c32-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="91c32-107">Eine Menü Ressource ist eine Auflistung von Informationen, die das Aussehen und die Funktion eines Anwendungs Menüs definiert.</span><span class="sxs-lookup"><span data-stu-id="91c32-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="91c32-108">Ein Menü ist ein spezielles Eingabe Tool, mit dem ein Benutzer Befehle auswählen und Untermenüs aus einer Liste von Menü Elementen öffnen kann.</span><span class="sxs-lookup"><span data-stu-id="91c32-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span> <span data-ttu-id="91c32-109">Außerdem wird Folgendes definiert:</span><span class="sxs-lookup"><span data-stu-id="91c32-109">It also defines the following:</span></span>

-   <span data-ttu-id="91c32-110">Hilfe Bezeichner in Menüs.</span><span class="sxs-lookup"><span data-stu-id="91c32-110">Help identifiers on menus.</span></span>
-   <span data-ttu-id="91c32-111">Bezeichner in Menüs.</span><span class="sxs-lookup"><span data-stu-id="91c32-111">Identifiers on menus.</span></span>
-   <span data-ttu-id="91c32-112">Verwendung der **MFT \_ \** _-Typflags und _*MFS \_ \*\*_ -Statusflags.</span><span class="sxs-lookup"><span data-stu-id="91c32-112">Use of the **MFT\_\** _ type flags and _*MFS\_\*\*_ state flags.</span></span> <span data-ttu-id="91c32-113">Weitere Informationen zu diesen Flags finden Sie in der [_ *menuiteminfo* \*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="91c32-113">For more information on these flags, see the [_ *MENUITEMINFO*\*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a><span data-ttu-id="91c32-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="91c32-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c32-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span><span class="sxs-lookup"><span data-stu-id="91c32-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span></span>
</dt> <dd>

<span data-ttu-id="91c32-116">Definiert ein Menü Element.</span><span class="sxs-lookup"><span data-stu-id="91c32-116">Defines a menu item.</span></span>

<dl> <dt>

<span data-ttu-id="91c32-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*ItemText*</span><span class="sxs-lookup"><span data-stu-id="91c32-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-118">Zeichenfolge, die den Text für das Menü Element enthält.</span><span class="sxs-lookup"><span data-stu-id="91c32-118">String containing the text for the menu item.</span></span> <span data-ttu-id="91c32-119">Weitere Informationen finden Sie unter [**MenuItem**](menuitem-statement.md).</span><span class="sxs-lookup"><span data-stu-id="91c32-119">For more information, see [**MENUITEM**](menuitem-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91c32-120"><span id="id"></span><span id="ID"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="91c32-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-121">Numerischer Ausdruck, der den Bezeichner des Menü Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="91c32-121">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="91c32-122"><span id="type"></span><span id="TYPE"></span>*Sorte*</span><span class="sxs-lookup"><span data-stu-id="91c32-122"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-123">Numerischer Ausdruck, der den Typ des Menü Elements angibt, für das die vordefinierten MFT- \_ \* Typwerte verwendet werden sollen. Fügen Sie die folgende Anweisung in die RC-Datei ein:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="91c32-123">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="91c32-124"><span id="state"></span><span id="STATE"></span>*Land*</span><span class="sxs-lookup"><span data-stu-id="91c32-124"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-125">Numerischer Ausdruck, der den Zustand des Menü Elements angibt, in dem die vordefinierten MFS- \_ \* Zustands Werte verwendet werden sollen. Fügen Sie die folgende Anweisung in den ein. RC-Datei:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="91c32-125">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="91c32-126"><span id="POPUP"></span><span id="popup"></span>[**Up**](popup-resource.md)</span><span class="sxs-lookup"><span data-stu-id="91c32-126"><span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)</span></span>
</dt> <dd>

<span data-ttu-id="91c32-127">Definiert ein Menü Element, das über ein zugeordnetes Untermenü verfügt.</span><span class="sxs-lookup"><span data-stu-id="91c32-127">Defines a menu item that has a submenu associated with it.</span></span>

<dl> <dt>

<span data-ttu-id="91c32-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*ItemText*</span><span class="sxs-lookup"><span data-stu-id="91c32-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-129">Zeichenfolge, die den Text für das Menü Element enthält.</span><span class="sxs-lookup"><span data-stu-id="91c32-129">String containing the text for the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="91c32-130"><span id="id"></span><span id="ID"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="91c32-130"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-131">Numerischer Ausdruck, der den Bezeichner des Menü Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="91c32-131">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="91c32-132"><span id="type"></span><span id="TYPE"></span>*Sorte*</span><span class="sxs-lookup"><span data-stu-id="91c32-132"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-133">Numerischer Ausdruck, der den Typ des Menü Elements angibt, für das die vordefinierten MFT- \_ \* Typwerte verwendet werden sollen. Fügen Sie die folgende Anweisung in ihr ein. RC-Datei:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="91c32-133">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="91c32-134"><span id="state"></span><span id="STATE"></span>*Land*</span><span class="sxs-lookup"><span data-stu-id="91c32-134"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-135">Numerischer Ausdruck, der den Zustand des Menü Elements angibt, in dem die vordefinierten MFS- \_ \* Zustands Werte verwendet werden sollen. Fügen Sie die folgende Anweisung in die RC-Datei ein:`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="91c32-135">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="91c32-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*</span><span class="sxs-lookup"><span data-stu-id="91c32-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-137">Numerischer Ausdruck, der den Bezeichner angibt, mit dem das Menü während der [**WM- \_ Hilfe**](../shell/wm-help.md) Verarbeitung identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="91c32-137">Numeric expression indicating the identifier used to identify the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="91c32-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupbody*</span><span class="sxs-lookup"><span data-stu-id="91c32-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span></span>
</dt> <dd>

<span data-ttu-id="91c32-139">Enthält eine beliebige Kombination der [**MenuItem**](menuitem-statement.md) -und [**Popup**](popup-resource.md) -Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="91c32-139">Contains any combination of the [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statements.</span></span>

</dd> </dl>

<span data-ttu-id="91c32-140">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91c32-140">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="91c32-141">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="91c32-141">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91c32-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91c32-142">Remarks</span></span>

<span data-ttu-id="91c32-143">Die gültigen arithmetischen und booleschen Vorgänge, die in einem der numerischen Ausdrücke in den Anweisungen von **menuex** enthalten sein können, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="91c32-143">The valid arithmetic and Boolean operations that can be contained in any of the numeric expressions in the statements of **MENUEX** are as follows:</span></span>

-   <span data-ttu-id="91c32-144">Hinzufügen ("+")</span><span class="sxs-lookup"><span data-stu-id="91c32-144">Add ('+')</span></span>
-   <span data-ttu-id="91c32-145">Subtraktion ("-")</span><span class="sxs-lookup"><span data-stu-id="91c32-145">Subtract ('-')</span></span>
-   <span data-ttu-id="91c32-146">Unäres Minuszeichen ("-")</span><span class="sxs-lookup"><span data-stu-id="91c32-146">Unary minus ('-')</span></span>
-   <span data-ttu-id="91c32-147">Unärer Not (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="91c32-147">Unary NOT ('~')</span></span>
-   <span data-ttu-id="91c32-148">Und (' & ')</span><span class="sxs-lookup"><span data-stu-id="91c32-148">AND ('&')</span></span>
-   <span data-ttu-id="91c32-149">Oder (' \| ')</span><span class="sxs-lookup"><span data-stu-id="91c32-149">OR ('\|')</span></span>

## <a name="see-also"></a><span data-ttu-id="91c32-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91c32-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c32-151">Verwenden von Menüs</span><span class="sxs-lookup"><span data-stu-id="91c32-151">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="91c32-152">**Accelerators**</span><span class="sxs-lookup"><span data-stu-id="91c32-152">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="91c32-153">**Charakteristik**</span><span class="sxs-lookup"><span data-stu-id="91c32-153">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="91c32-154">**Dialog**</span><span class="sxs-lookup"><span data-stu-id="91c32-154">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="91c32-155">**Kurse**</span><span class="sxs-lookup"><span data-stu-id="91c32-155">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="91c32-156">**Stehen**</span><span class="sxs-lookup"><span data-stu-id="91c32-156">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="91c32-157">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="91c32-157">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="91c32-158">**Up**</span><span class="sxs-lookup"><span data-stu-id="91c32-158">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="91c32-159">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="91c32-159">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="91c32-160">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="91c32-160">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="91c32-161">**Version**</span><span class="sxs-lookup"><span data-stu-id="91c32-161">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
