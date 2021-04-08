---
title: E (Menüs und andere Ressourcen)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102750"
---
# <a name="e-menus-and-other-resources"></a><span data-ttu-id="caf98-103">E (Menüs und andere Ressourcen)</span><span class="sxs-lookup"><span data-stu-id="caf98-103">E (Menus and Other Resources)</span></span>

<span data-ttu-id="caf98-104">[a](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="caf98-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="caf98-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Leere Menüs sind nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="caf98-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Empty menus not allowed**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-106">Ein **End** -Schlüsselwort wird angezeigt, bevor beliebige Menü Elemente in der [**Menü**](menu-resource.md) Anweisung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="caf98-106">An **END** keyword appears before any menu items are defined in the [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="caf98-107">Leere Menüs sind vom Microsoft Windows 32 Resource Compiler (RC) nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="caf98-107">Empty menus are not permitted by Microsoft Windows 32 Resource Compiler (RC).</span></span> <span data-ttu-id="caf98-108">Stellen Sie sicher, dass in der **Menü** Anweisung keine öffnenden Anführungszeichen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="caf98-108">Make sure that you do not have any opening quotation marks within the **MENU** statement.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**Ende erwartet in Dialog Feld**</span><span class="sxs-lookup"><span data-stu-id="caf98-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**END expected in Dialog**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-110">Das **End** -Schlüsselwort muss am Ende einer [**Dialog**](dialog-resource.md) Feld Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="caf98-110">The **END** keyword must appear at the end of a [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="caf98-111">Stellen Sie sicher, dass die vorangehende Anweisung keine öffnenden Anführungszeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="caf98-111">Make sure that there are no opening quotation marks left from the preceding statement.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**Ende im Menü erwartet**</span><span class="sxs-lookup"><span data-stu-id="caf98-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END expected in menu**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-113">Das **End** -Schlüsselwort muss am Ende einer [**Menü**](menu-resource.md) Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="caf98-113">The **END** keyword must appear at the end of a [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="caf98-114">Stellen Sie sicher, dass keine übereinstimmenden **Begin** -und **End** -Anweisungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="caf98-114">Make sure that there are no mismatched **BEGIN** and **END** statements.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Fehler bei "kreatingresource-Name".**</span><span class="sxs-lookup"><span data-stu-id="caf98-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Error Creatingresource-name**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-116">Die angegebene binäre Ressource konnte von Microsoft Windows 32 Resource Compiler (RC) nicht erstellt werden. RES-Datei).</span><span class="sxs-lookup"><span data-stu-id="caf98-116">Microsoft Windows 32 Resource Compiler (RC) could not create the specified binary resource (.RES) file.</span></span> <span data-ttu-id="caf98-117">Stellen Sie sicher, dass er nicht auf einem schreibgeschützten Laufwerk erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="caf98-117">Make sure that it is not being created on a read-only drive.</span></span> <span data-ttu-id="caf98-118">Verwenden Sie die Option **/v** , um herauszufinden, ob die Datei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="caf98-118">Use the **/v** option to find out whether the file is being created.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Komma in Zugriffstasten Tabelle erwartet**</span><span class="sxs-lookup"><span data-stu-id="caf98-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Expected Comma in Accelerator Table**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-120">Der Microsoft Windows 32-Ressourcen Compiler (RC) erfordert ein Komma zwischen den Parametern " *Event* " und " *idValue* " in der [**Accelerators**](accelerators-resource.md) -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="caf98-120">Microsoft Windows 32 Resource Compiler (RC) requires a comma between the *event* and *idvalue* parameters in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Name der Steuerelement Klasse erwartet**</span><span class="sxs-lookup"><span data-stu-id="caf98-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Expected control class name**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-122">Der *Class* -Parameter einer [**Control**](control-control.md) -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss einer der folgenden Steuerelement Typen sein: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** oder User-Defined.</span><span class="sxs-lookup"><span data-stu-id="caf98-122">The *class* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement must be one of the following control types: **BUTTON**, [**COMBOBOX**](combobox-control.md), **EDIT**, [**LISTBOX**](listbox-control.md), [**SCROLLBAR**](scrollbar-control.md), **STATIC**, or user-defined.</span></span> <span data-ttu-id="caf98-123">Stellen Sie sicher, dass die-Klasse korrekt geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="caf98-123">Make sure that the class is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Der Name der Schriftart wurde erwartet.**</span><span class="sxs-lookup"><span data-stu-id="caf98-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Expected font face name**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-125">Der *Schriftart-Parameter* der **Font** -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss eine Zeichenfolge sein, die in doppelten Anführungszeichen (") eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="caf98-125">The *typeface* parameter of the **FONT** statement in the [**DIALOG**](dialog-resource.md) statement must be a character string enclosed in double quotation marks (").</span></span> <span data-ttu-id="caf98-126">Dieser Parameter gibt den Namen einer Schriftart an.</span><span class="sxs-lookup"><span data-stu-id="caf98-126">This parameter specifies the name of a font.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Erwarteter ID-Wert für MenuItem.**</span><span class="sxs-lookup"><span data-stu-id="caf98-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Expected ID value for Menuitem**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-128">Die [**Menu**](menu-resource.md) -Anweisung muss eine [**MenuItem**](menuitem-statement.md) -Anweisung enthalten, die entweder eine Ganzzahl oder eine symbolische Konstante im *MENUID* -Parameter aufweist.</span><span class="sxs-lookup"><span data-stu-id="caf98-128">The [**MENU**](menu-resource.md) statement must contain a [**MENUITEM**](menuitem-statement.md) statement, which has either an integer or a symbolic constant in the *MenuID* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Erwartete Menü Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="caf98-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Expected Menu String**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-130">Jede [**MenuItem**](menuitem-statement.md) -und [**Popup**](popup-resource.md) -Anweisung muss einen *Text* Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="caf98-130">Each [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statement must contain a *text* parameter.</span></span> <span data-ttu-id="caf98-131">Dieser Parameter ist eine Zeichenfolge, die in doppelten Anführungszeichen (") eingeschlossen ist, die den Namen des Menü Elements oder Popup Menüs angibt.</span><span class="sxs-lookup"><span data-stu-id="caf98-131">This parameter is a string enclosed in double quotation marks (") that specifies the name of the menu item or pop-up menu.</span></span> <span data-ttu-id="caf98-132">Eine **MENUITEM SEPARATOR** -Anweisung erfordert keine Zeichenfolge in Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="caf98-132">A **MENUITEM SEPARATOR** statement requires no quoted string.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Numerischer Befehls Wert erwartet.**</span><span class="sxs-lookup"><span data-stu-id="caf98-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Expected numeric command value**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-134">Der Microsoft Windows-Ressourcen Compiler (RC) hat einen numerischen *idValue* -Parameter in der [**Accelerators**](accelerators-resource.md) -Anweisung erwartet.</span><span class="sxs-lookup"><span data-stu-id="caf98-134">Microsoft Windows Resource Compiler (RC) was expecting a numeric *idvalue* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span> <span data-ttu-id="caf98-135">Stellen Sie sicher, dass Sie eine [**\# define**](-define.md) -Anweisung verwendet haben, um den Wert anzugeben, und dass die verwendete Konstante korrekt geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="caf98-135">Make sure that you have used a [**\#define**](-define.md) statement to specify the value and that the constant used is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Numerische Konstante in Zeichen folgen Tabelle erwartet**</span><span class="sxs-lookup"><span data-stu-id="caf98-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Expected numeric constant in string table**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-137">Eine in einer [**\# define**](-define.md) -Anweisung definierte numerische Konstante muss direkt auf das **Begin** -Schlüsselwort in einer [**STRINGTABLE**](stringtable-resource.md) -Anweisung folgen.</span><span class="sxs-lookup"><span data-stu-id="caf98-137">A numeric constant, defined in a [**\#define**](-define.md) statement, must immediately follow the **BEGIN** keyword in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Erwartete numerische Punktgröße**</span><span class="sxs-lookup"><span data-stu-id="caf98-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Expected numeric point size**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-139">Der *pointsize* -Parameter der [**Font**](font-statement.md) -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss ein ganzzahliger Wert für die Punktgröße sein.</span><span class="sxs-lookup"><span data-stu-id="caf98-139">The *pointsize* parameter of the [**FONT**](font-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer point-size value.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Numerische Dialog Konstante erwartet**</span><span class="sxs-lookup"><span data-stu-id="caf98-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Expected Numerical Dialog constant**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-141">Eine [**Dialog**](dialog-resource.md) Feld Anweisung erfordert *ganzzahlige* Werte für die Parameter *x*, y, *Width* und *height* .</span><span class="sxs-lookup"><span data-stu-id="caf98-141">A [**DIALOG**](dialog-resource.md) statement requires integer values for the *x*, *y*, *width*, and *height* parameters.</span></span> <span data-ttu-id="caf98-142">Stellen Sie sicher, dass diese Werte, die nach dem **Dialog** Feld Schlüsselwort enthalten sind, nicht negativ sind.</span><span class="sxs-lookup"><span data-stu-id="caf98-142">Make sure that these values, which are included after the **DIALOG** keyword, are not negative.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Erwartete Zeichenfolge in STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="caf98-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Expected String in STRINGTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-144">Nach jedem numerischen *stringID* -Parameter in einer [**STRINGTABLE**](stringtable-resource.md) -Anweisung wird eine Zeichenfolge erwartet.</span><span class="sxs-lookup"><span data-stu-id="caf98-144">A string is expected after each numeric *stringid* parameter in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Erwarteter String-oder Constant Accelerator-Befehl**</span><span class="sxs-lookup"><span data-stu-id="caf98-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Expected String or Constant Accelerator command**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-146">Der Microsoft Windows-Ressourcen Compiler (RC) konnte nicht ermitteln, welcher Schlüssel für die Zugriffstaste eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="caf98-146">Microsoft Windows Resource Compiler (RC) was not able to determine which key was being set up for the accelerator.</span></span> <span data-ttu-id="caf98-147">Der *Ereignis* Parameter in der [**Accelerators**](accelerators-resource.md) -Anweisung ist möglicherweise ungültig.</span><span class="sxs-lookup"><span data-stu-id="caf98-147">The *event* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement might be invalid.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Erwartetes Wert-, Block-oder End-Schlüsselwort.**</span><span class="sxs-lookup"><span data-stu-id="caf98-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Expected VALUE, BLOCK, or END keyword.**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-149">Die [**VERSIONINFO**](versioninfo-resource.md) -Struktur erfordert ein **value**-, **Block**-oder **End** -Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="caf98-149">The [**VERSIONINFO**](versioninfo-resource.md) structure requires a **VALUE**, **BLOCK**, or **END** keyword.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Anzahl für ID wird erwartet.**</span><span class="sxs-lookup"><span data-stu-id="caf98-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Expecting number for ID**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-151">Eine Zahl wird für den *ID* -Parameter einer [**Steuer**](control-control.md) Element Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung erwartet.</span><span class="sxs-lookup"><span data-stu-id="caf98-151">A number is expected for the *id* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="caf98-152">Stellen Sie sicher, dass Sie über eine Zahl oder eine [**\# define**](-define.md) -Anweisung für den Steuerelement Bezeichner verfügen.</span><span class="sxs-lookup"><span data-stu-id="caf98-152">Make sure that you have a number or a [**\#define**](-define.md) statement for the control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Zeichenfolge in Anführungszeichen für Schlüssel erwartet**</span><span class="sxs-lookup"><span data-stu-id="caf98-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Expecting quoted string for key**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-154">Die Schlüssel Zeichenfolge nach dem **Block** -oder **value** -Schlüsselwort sollte in doppelte Anführungszeichen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="caf98-154">The key string following the **BLOCK** or **VALUE** keyword should be enclosed in double quotation marks.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Zeichenfolge in Anführungszeichen in Dialog Klasse erwartet**</span><span class="sxs-lookup"><span data-stu-id="caf98-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Expecting quoted string in dialog class**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-156">Der *Class* -Parameter der [**Class**](class-statement.md) -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss eine ganze Zahl oder eine Zeichenfolge sein, die in doppelten Anführungszeichen (") eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="caf98-156">The *class* parameter of the [**CLASS**](class-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer or a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="caf98-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Zeichenfolge in Anführungszeichen in Dialogfeld Titel erwartet**</span><span class="sxs-lookup"><span data-stu-id="caf98-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Expecting quoted string in dialog title**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-158">Der *CaptionText* -Parameter der [**Caption**](caption-statement.md) -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss eine Zeichenfolge sein, die in doppelten Anführungszeichen (") eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="caf98-158">The *captiontext* parameter of the [**CAPTION**](caption-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be a character string, enclosed in double quotation marks (").</span></span>

</dd> </dl>

 

 




