---
description: Die Verknüpfungs Tabelle enthält die Informationen, die die Anwendung benötigt, um Verknüpfungen auf dem Computer des Benutzers zu erstellen.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Verknüpfungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56482f1d2d5521bede54c781c91d2de2bc39e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866283"
---
# <a name="shortcut-table"></a><span data-ttu-id="b02ff-103">Verknüpfungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="b02ff-103">Shortcut Table</span></span>

<span data-ttu-id="b02ff-104">Die Verknüpfungs Tabelle enthält die Informationen, die die Anwendung benötigt, um Verknüpfungen auf dem Computer des Benutzers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b02ff-104">The Shortcut table holds the information the application needs to create shortcuts on the user's computer.</span></span>

<span data-ttu-id="b02ff-105">Die Verknüpfungs Tabelle enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="b02ff-105">The Shortcut table has the following columns.</span></span>



| <span data-ttu-id="b02ff-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="b02ff-106">Column</span></span>                 | <span data-ttu-id="b02ff-107">Typ</span><span class="sxs-lookup"><span data-stu-id="b02ff-107">Type</span></span>                         | <span data-ttu-id="b02ff-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b02ff-108">Key</span></span> | <span data-ttu-id="b02ff-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="b02ff-109">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="b02ff-110">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="b02ff-110">Shortcut</span></span>               | [<span data-ttu-id="b02ff-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b02ff-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b02ff-112">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-112">Y</span></span>   | <span data-ttu-id="b02ff-113">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-113">N</span></span>        |
| <span data-ttu-id="b02ff-114">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="b02ff-114">Directory\_</span></span>            | [<span data-ttu-id="b02ff-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b02ff-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="b02ff-116">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-116">N</span></span>   | <span data-ttu-id="b02ff-117">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-117">N</span></span>        |
| <span data-ttu-id="b02ff-118">Name</span><span class="sxs-lookup"><span data-stu-id="b02ff-118">Name</span></span>                   | [<span data-ttu-id="b02ff-119">Filename</span><span class="sxs-lookup"><span data-stu-id="b02ff-119">Filename</span></span>](filename.md)     | <span data-ttu-id="b02ff-120">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-120">N</span></span>   | <span data-ttu-id="b02ff-121">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-121">N</span></span>        |
| <span data-ttu-id="b02ff-122">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="b02ff-122">Component\_</span></span>            | [<span data-ttu-id="b02ff-123">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b02ff-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="b02ff-124">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-124">N</span></span>   | <span data-ttu-id="b02ff-125">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-125">N</span></span>        |
| <span data-ttu-id="b02ff-126">Ziel</span><span class="sxs-lookup"><span data-stu-id="b02ff-126">Target</span></span>                 | [<span data-ttu-id="b02ff-127">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="b02ff-127">Shortcut</span></span>](shortcut.md)     | <span data-ttu-id="b02ff-128">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-128">N</span></span>   | <span data-ttu-id="b02ff-129">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-129">N</span></span>        |
| <span data-ttu-id="b02ff-130">Argumente</span><span class="sxs-lookup"><span data-stu-id="b02ff-130">Arguments</span></span>              | [<span data-ttu-id="b02ff-131">Großformatige</span><span class="sxs-lookup"><span data-stu-id="b02ff-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b02ff-132">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-132">N</span></span>   | <span data-ttu-id="b02ff-133">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-133">Y</span></span>        |
| <span data-ttu-id="b02ff-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b02ff-134">Description</span></span>            | [<span data-ttu-id="b02ff-135">Text</span><span class="sxs-lookup"><span data-stu-id="b02ff-135">Text</span></span>](text.md)             | <span data-ttu-id="b02ff-136">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-136">N</span></span>   | <span data-ttu-id="b02ff-137">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-137">Y</span></span>        |
| <span data-ttu-id="b02ff-138">Hotkey</span><span class="sxs-lookup"><span data-stu-id="b02ff-138">Hotkey</span></span>                 | [<span data-ttu-id="b02ff-139">Integer</span><span class="sxs-lookup"><span data-stu-id="b02ff-139">Integer</span></span>](integer.md)       | <span data-ttu-id="b02ff-140">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-140">N</span></span>   | <span data-ttu-id="b02ff-141">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-141">Y</span></span>        |
| <span data-ttu-id="b02ff-142">Symbol\_</span><span class="sxs-lookup"><span data-stu-id="b02ff-142">Icon\_</span></span>                 | [<span data-ttu-id="b02ff-143">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b02ff-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="b02ff-144">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-144">N</span></span>   | <span data-ttu-id="b02ff-145">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-145">Y</span></span>        |
| <span data-ttu-id="b02ff-146">IconIndex</span><span class="sxs-lookup"><span data-stu-id="b02ff-146">IconIndex</span></span>              | [<span data-ttu-id="b02ff-147">Integer</span><span class="sxs-lookup"><span data-stu-id="b02ff-147">Integer</span></span>](integer.md)       | <span data-ttu-id="b02ff-148">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-148">N</span></span>   | <span data-ttu-id="b02ff-149">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-149">Y</span></span>        |
| <span data-ttu-id="b02ff-150">ShowCmd</span><span class="sxs-lookup"><span data-stu-id="b02ff-150">ShowCmd</span></span>                | [<span data-ttu-id="b02ff-151">Integer</span><span class="sxs-lookup"><span data-stu-id="b02ff-151">Integer</span></span>](integer.md)       | <span data-ttu-id="b02ff-152">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-152">N</span></span>   | <span data-ttu-id="b02ff-153">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-153">Y</span></span>        |
| <span data-ttu-id="b02ff-154">Wkdir</span><span class="sxs-lookup"><span data-stu-id="b02ff-154">WkDir</span></span>                  | [<span data-ttu-id="b02ff-155">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b02ff-155">Identifier</span></span>](identifier.md) | <span data-ttu-id="b02ff-156">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-156">N</span></span>   | <span data-ttu-id="b02ff-157">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-157">Y</span></span>        |
| <span data-ttu-id="b02ff-158">Displayresourcedll</span><span class="sxs-lookup"><span data-stu-id="b02ff-158">DisplayResourceDLL</span></span>     | [<span data-ttu-id="b02ff-159">Großformatige</span><span class="sxs-lookup"><span data-stu-id="b02ff-159">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b02ff-160">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-160">N</span></span>   | <span data-ttu-id="b02ff-161">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-161">Y</span></span>        |
| <span data-ttu-id="b02ff-162">Displayresourceid</span><span class="sxs-lookup"><span data-stu-id="b02ff-162">DisplayResourceId</span></span>      | [<span data-ttu-id="b02ff-163">Integer</span><span class="sxs-lookup"><span data-stu-id="b02ff-163">Integer</span></span>](integer.md)       | <span data-ttu-id="b02ff-164">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-164">N</span></span>   | <span data-ttu-id="b02ff-165">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-165">Y</span></span>        |
| <span data-ttu-id="b02ff-166">Deskriptionresourcedll</span><span class="sxs-lookup"><span data-stu-id="b02ff-166">DescriptionResourceDLL</span></span> | [<span data-ttu-id="b02ff-167">Großformatige</span><span class="sxs-lookup"><span data-stu-id="b02ff-167">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b02ff-168">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-168">N</span></span>   | <span data-ttu-id="b02ff-169">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-169">Y</span></span>        |
| <span data-ttu-id="b02ff-170">Deskriptionresourceid</span><span class="sxs-lookup"><span data-stu-id="b02ff-170">DescriptionResourceId</span></span>  | [<span data-ttu-id="b02ff-171">Integer</span><span class="sxs-lookup"><span data-stu-id="b02ff-171">Integer</span></span>](integer.md)       | <span data-ttu-id="b02ff-172">N</span><span class="sxs-lookup"><span data-stu-id="b02ff-172">N</span></span>   | <span data-ttu-id="b02ff-173">J</span><span class="sxs-lookup"><span data-stu-id="b02ff-173">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b02ff-174">Spalten</span><span class="sxs-lookup"><span data-stu-id="b02ff-174">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b02ff-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Kontext</span><span class="sxs-lookup"><span data-stu-id="b02ff-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Shortcut</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-176">Der Schlüsselwert für diese Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b02ff-176">The key value for this table.</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="b02ff-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-178">Der externe Schlüssel in die erste Spalte der [Verzeichnis Tabelle](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="b02ff-178">The external key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="b02ff-179">Diese Spalte gibt das Verzeichnis an, in dem die Verknüpfungs Datei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b02ff-179">This column specifies the directory in which the Shortcut file is created.</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="b02ff-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-181">Der lokalisierbare Name der zu erstellenden Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="b02ff-181">The localizable name of the shortcut to be created.</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="b02ff-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-183">Der externe Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b02ff-183">The external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="b02ff-184">Das Installationsprogramm verwendet den Installationsstatus der in dieser Spalte angegebenen Komponente, um zu bestimmen, ob die Verknüpfung erstellt oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b02ff-184">The installer uses the installation state of the component specified in this column to determine whether the shortcut is created or deleted.</span></span> <span data-ttu-id="b02ff-185">Diese Komponente muss über einen gültigen Schlüssel Pfad für die zu installierende Verknüpfung verfügen.</span><span class="sxs-lookup"><span data-stu-id="b02ff-185">This component must have a valid key path for the shortcut to be installed.</span></span> <span data-ttu-id="b02ff-186">Wenn die Ziel Spalte den Namen einer Funktion enthält, ist die von der Verknüpfung gestartete Datei die Schlüsseldatei der in dieser Spalte aufgeführten Komponente.</span><span class="sxs-lookup"><span data-stu-id="b02ff-186">If the Target column contains the name of a feature, the file launched by the shortcut is the key file of the component listed in this column.</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Spar</span><span class="sxs-lookup"><span data-stu-id="b02ff-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-188">Das Verknüpfungs Ziel.</span><span class="sxs-lookup"><span data-stu-id="b02ff-188">The shortcut target.</span></span>

<span data-ttu-id="b02ff-189">Bei einer angekündigten Verknüpfung muss es sich bei dieser Spalte um einen externen Schlüssel in der ersten Spalte der [Funktions Tabelle](feature-table.md)handeln.</span><span class="sxs-lookup"><span data-stu-id="b02ff-189">For an advertised shortcut, this column must be an external key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="b02ff-190">Das Installationsprogramm wertet den Eintrag im Zielfeld als [Bezeichner](identifier.md) aus, und der Eintrag muss ein gültiger Fremdschlüssel in der [Featuretabelle](feature-table.md)sein.</span><span class="sxs-lookup"><span data-stu-id="b02ff-190">The installer evaluates the entry in the Target field as an [Identifier](identifier.md) and the entry must be a valid foreign key into the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="b02ff-191">Die von der Verknüpfung gestartete Datei ist in diesem Fall die Schlüsseldatei der Komponente, die in der Spalte Komponente aufgeführt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="b02ff-191">The file launched by the shortcut in this case is the key file of the component listed in the Component\_ column.</span></span> <span data-ttu-id="b02ff-192">Wenn die Verknüpfung aktiviert ist, überprüft das Installationsprogramm, ob alle Komponenten in der Funktion installiert sind, bevor diese Datei gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b02ff-192">When the shortcut is activated, the installer verifies that all the components in the feature are installed before launching this file.</span></span>

<span data-ttu-id="b02ff-193">Bei einer nicht angekündigten Verknüpfung wertet das Installationsprogramm dieses Feld als [formatierte](formatted.md) Zeichenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="b02ff-193">For a non-advertised shortcut, the installer evaluates this field as a [Formatted](formatted.md) string.</span></span> <span data-ttu-id="b02ff-194">Das Feld muss einen Eigenschafts Bezeichner enthalten, der durch eckige Klammern ( \[ \] ) eingeschlossen ist, die in die Datei oder einen Ordner, auf den die Verknüpfung zeigt, erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="b02ff-194">The field should contains a property identifier enclosed by square brackets (\[ \]), that is expanded into the file or a folder pointed to by the shortcut.</span></span> <span data-ttu-id="b02ff-195">Weitere Informationen finden Sie unter der Aktion "" für " [kreateshortcuts](createshortcuts-action.md)".</span><span class="sxs-lookup"><span data-stu-id="b02ff-195">For more information, see the [CreateShortcuts action](createshortcuts-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentation</span><span class="sxs-lookup"><span data-stu-id="b02ff-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-197">Die Befehlszeilenargumente für die Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="b02ff-197">The command-line arguments for the shortcut.</span></span>

<span data-ttu-id="b02ff-198">Beachten Sie, dass die Auflösung von Eigenschaften im Feld Argumente eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="b02ff-198">Note that the resolution of properties in the Arguments field is limited.</span></span> <span data-ttu-id="b02ff-199">Eine Eigenschaft, die als \[ *Eigenschaft* \] in diesem Feld formatiert ist, kann nur aufgelöst werden, wenn die Eigenschaft bereits über den vorgesehenen Wert verfügt, wenn die Komponente, die die Verknüpfung besitzt, installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b02ff-199">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component that owns the shortcut is installed.</span></span> <span data-ttu-id="b02ff-200">Um beispielsweise den richtigen Wert für das Argument " \[ \#MyDoc.doc\] " aufzulösen, muss der gleiche Prozess die Datei MyDoc.doc und die Komponente, die die Verknüpfung besitzt, installieren.</span><span class="sxs-lookup"><span data-stu-id="b02ff-200">For example, to resolve to the correct value for the argument "\[\#MyDoc.doc\]", the same process must be installing the file MyDoc.doc and the component that owns the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b02ff-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-202">Die lokalisierbare Beschreibung der Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="b02ff-202">The localizable description of the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey</span><span class="sxs-lookup"><span data-stu-id="b02ff-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-204">Der Hotkey für die Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="b02ff-204">The hotkey for the shortcut.</span></span> <span data-ttu-id="b02ff-205">Das nieder wertige Byte enthält den Code des virtuellen Schlüssels für den Schlüssel, und das hochwertige Byte enthält Modifiziererflags.</span><span class="sxs-lookup"><span data-stu-id="b02ff-205">The low-order byte contains the virtual-key code for the key, and the high-order byte contains modifier flags.</span></span> <span data-ttu-id="b02ff-206">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="b02ff-206">This must be a non-negative number.</span></span> <span data-ttu-id="b02ff-207">In der Regel wird empfohlen, diese Option nicht festzulegen, da die Einstellung dieser Option dem Desktop eines Benutzers doppelte Hotkeys hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="b02ff-207">Authors of installation packages are generally recommended not to set this option, because the setting of this option can add duplicate hotkeys to a user's desktop.</span></span> <span data-ttu-id="b02ff-208">Außerdem kann das Zuweisen von Hotkeys zu Verknüpfungen für Benutzer problematisch sein, die Hotkeys für [Barrierefreiheit](accessibility.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="b02ff-208">In addition, the practice of assigning hotkeys to shortcuts can be problematic for users using hotkeys for [accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Angezeigt\_</span><span class="sxs-lookup"><span data-stu-id="b02ff-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-210">Der externe Schlüssel für die Spalte einer der [Symboltabellen](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="b02ff-210">The external key to column one of the [Icon table](icon-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="b02ff-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-212">Der Symbol Index für die Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="b02ff-212">The icon index for the shortcut.</span></span> <span data-ttu-id="b02ff-213">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="b02ff-213">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span><span class="sxs-lookup"><span data-stu-id="b02ff-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-215">Der Show-Befehl für das Anwendungsfenster.</span><span class="sxs-lookup"><span data-stu-id="b02ff-215">The Show command for the application window.</span></span>

<span data-ttu-id="b02ff-216">Die folgenden Werte können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b02ff-216">The following values may be used.</span></span> <span data-ttu-id="b02ff-217">Die Werte sind für die Windows-API-Funktion ShowWindow definiert.</span><span class="sxs-lookup"><span data-stu-id="b02ff-217">The values are as defined for the Windows API function ShowWindow.</span></span>



| <span data-ttu-id="b02ff-218">Wert</span><span class="sxs-lookup"><span data-stu-id="b02ff-218">Value</span></span> | <span data-ttu-id="b02ff-219">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b02ff-219">Meaning</span></span>             |
|-------|---------------------|
| <span data-ttu-id="b02ff-220">1</span><span class="sxs-lookup"><span data-stu-id="b02ff-220">1</span></span>     | <span data-ttu-id="b02ff-221">SW \_ Show normal</span><span class="sxs-lookup"><span data-stu-id="b02ff-221">SW\_SHOWNORMAL</span></span>      |
| <span data-ttu-id="b02ff-222">3</span><span class="sxs-lookup"><span data-stu-id="b02ff-222">3</span></span>     | <span data-ttu-id="b02ff-223">SW \_ showmaximized</span><span class="sxs-lookup"><span data-stu-id="b02ff-223">SW\_SHOWMAXIMIZED</span></span>   |
| <span data-ttu-id="b02ff-224">7</span><span class="sxs-lookup"><span data-stu-id="b02ff-224">7</span></span>     | <span data-ttu-id="b02ff-225">SW \_ showminnoactive</span><span class="sxs-lookup"><span data-stu-id="b02ff-225">SW\_SHOWMINNOACTIVE</span></span> |



 

</dd> <dt>

<span data-ttu-id="b02ff-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>Wkdir</span><span class="sxs-lookup"><span data-stu-id="b02ff-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-227">Der Name der Eigenschaft, die den Pfad des Arbeitsverzeichnisses für die Verknüpfung enthält.</span><span class="sxs-lookup"><span data-stu-id="b02ff-227">The name of the property that has the path of the working directory for the shortcut.</span></span> <span data-ttu-id="b02ff-228">Der Wert kann das Windows-Format verwenden, um auf Umgebungsvariablen zu verweisen, z. b .% User Profile%.</span><span class="sxs-lookup"><span data-stu-id="b02ff-228">The value can use the Windows format to reference environment variables, for example %USERPROFILE%.</span></span> <span data-ttu-id="b02ff-229">Die Verweise werden in einen tatsächlichen Pfad aufgelöst, wenn das Installationsprogramm das Arbeitsverzeichnis auflöst, um die Verknüpfung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b02ff-229">The references are resolved to an actual path when the installer resolves the working directory to create the shortcut.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b02ff-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>Displayresourcedll</span><span class="sxs-lookup"><span data-stu-id="b02ff-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-231">Dieses Feld enthält einen [formatierten](formatted.md) Zeichen folgen Wert für den vollständigen Pfad zur sprach neutralen portablen ausführbaren Datei (LN-Datei), in der die Daten der Ressourcen Konfiguration (RC config) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b02ff-231">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="b02ff-232">Die formatierte Zeichenfolge kann die \[ \# filekey- \] Konvention verwenden.</span><span class="sxs-lookup"><span data-stu-id="b02ff-232">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="b02ff-233">Wenn dieses Feld einen Wert enthält, wird die Spalte Name ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b02ff-233">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="b02ff-234">Wenn dieses Feld leer ist, verwendet das Installationsprogramm den Wert in der Spalte Name.</span><span class="sxs-lookup"><span data-stu-id="b02ff-234">If this field is empty, the installer uses the value in the Name column.</span></span> <span data-ttu-id="b02ff-235">Wenn dieses Feld einen Wert enthält, muss auch das Feld **displayresourceid** einen Wert enthalten, sonst tritt bei der Installation ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b02ff-235">When this field contains a value, the **DisplayResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="b02ff-236">Diese Spalte der Verknüpfungs Tabelle wird nur verwendet, wenn Sie unter Windows Vista oder Windows Server 2008 ausgeführt wird und andernfalls ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="b02ff-236">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="b02ff-237">Diese Spalte ist für Versionen verfügbar, die nicht älter sind als Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="b02ff-237">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="b02ff-238">Weitere Informationen zum Hinzufügen von Verknüpfungen zur Verknüpfungs Tabelle für die Verwendung mit MUI-Ressourcen finden Sie unter [Beispiel für eine MUI-Verknüpfung](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="b02ff-238">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>Displayresourceid</span><span class="sxs-lookup"><span data-stu-id="b02ff-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-240">Der Anzeige Namensindex für die Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="b02ff-240">The display name index for the shortcut.</span></span> <span data-ttu-id="b02ff-241">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="b02ff-241">This must be a non-negative number.</span></span> <span data-ttu-id="b02ff-242">Wenn dieses Feld einen Wert enthält, muss das Feld **displayresourcedll** ebenfalls einen Wert enthalten, da die Installation nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b02ff-242">When this field contains a value, the **DisplayResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="b02ff-243">Diese Spalte der Verknüpfungs Tabelle wird nur verwendet, wenn Sie unter Windows Vista oder Windows Server 2008 ausgeführt wird und andernfalls ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="b02ff-243">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="b02ff-244">Diese Spalte ist für Versionen verfügbar, die nicht älter sind als Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="b02ff-244">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>Deskriptionresourcedll</span><span class="sxs-lookup"><span data-stu-id="b02ff-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-246">Dieses Feld enthält einen [formatierten](formatted.md) Zeichen folgen Wert für den vollständigen Pfad zur sprach neutralen portablen ausführbaren Datei (LN-Datei), in der die Daten der Ressourcen Konfiguration (RC config) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b02ff-246">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="b02ff-247">Die formatierte Zeichenfolge kann die \[ \# filekey- \] Konvention verwenden.</span><span class="sxs-lookup"><span data-stu-id="b02ff-247">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="b02ff-248">Wenn dieses Feld einen Wert enthält, wird die Spalte Name ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b02ff-248">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="b02ff-249">Wenn dieses Feld leer ist, verwendet das Installationsprogramm den Wert in der Spalte Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="b02ff-249">If this field is empty, the installer uses the value in the Description column.</span></span> <span data-ttu-id="b02ff-250">Wenn dieses Feld einen Wert enthält, muss auch das Feld **descriptionresourceid** einen Wert enthalten, sonst tritt bei der Installation ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b02ff-250">When this field contains a value, the **DescriptionResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="b02ff-251">Diese Spalte der Verknüpfungs Tabelle wird nur verwendet, wenn Sie unter Windows Vista oder Windows Server 2008 ausgeführt wird und andernfalls ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="b02ff-251">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="b02ff-252">Diese Spalte ist für Versionen verfügbar, die nicht älter sind als Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="b02ff-252">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="b02ff-253">Weitere Informationen zum Hinzufügen von Verknüpfungen zur Verknüpfungs Tabelle für die Verwendung mit MUI-Ressourcen finden Sie unter [Beispiel für eine MUI-Verknüpfung](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="b02ff-253">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="b02ff-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>Deskriptionresourceid</span><span class="sxs-lookup"><span data-stu-id="b02ff-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span></span>
</dt> <dd>

<span data-ttu-id="b02ff-255">Der Beschreibungs Name Index für die Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="b02ff-255">The description name index for the shortcut.</span></span> <span data-ttu-id="b02ff-256">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="b02ff-256">This must be a non-negative number.</span></span> <span data-ttu-id="b02ff-257">Wenn dieses Feld einen Wert enthält, muss das Feld **descriptionresourcedll** ebenfalls einen Wert enthalten, da die Installation nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b02ff-257">When this field contains a value, the **DescriptionResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="b02ff-258">Diese Spalte der Verknüpfungs Tabelle wird nur verwendet, wenn Sie unter Windows Vista oder Windows Server 2008 ausgeführt wird und andernfalls ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="b02ff-258">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="b02ff-259">Diese Spalte ist für Versionen verfügbar, die nicht älter sind als Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="b02ff-259">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b02ff-260">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b02ff-260">Remarks</span></span>

<span data-ttu-id="b02ff-261">Durch die Aktivierung einer Funktion wird nur dann eine angekündigte Verknüpfung erstellt, wenn die IShellLink-Schnittstelle des Systems die Installation des Installationsprogramm Deskriptors unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b02ff-261">The enabling of a feature creates an advertised shortcut only if the system's IShellLink interface supports installer descriptor resolution.</span></span> <span data-ttu-id="b02ff-262">Dies wird von Microsoft Windows 2000 und Systemen unterstützt, die Microsoft Internet Explorer 4,01 ausführen.</span><span class="sxs-lookup"><span data-stu-id="b02ff-262">This is supported by Microsoft Windows 2000 and systems running Microsoft Internet Explorer 4.01.</span></span> <span data-ttu-id="b02ff-263">Wenn dies nicht unterstützt wird, erstellt das Installationsprogramm bei der Installation der featurekomponente eine nicht angekündigte Verknüpfung, entweder lokal oder über die Quelle auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b02ff-263">If unsupported, the installer creates a non-advertised shortcut upon the installation of the feature's component, either locally or run from source.</span></span>

<span data-ttu-id="b02ff-264">Beachten Sie, dass angekündigte Verknüpfungen immer auf eine bestimmte Anwendung verweisen, die durch einen [**ProductCode**](productcode.md)gekennzeichnet ist und nicht von Anwendungen gemeinsam verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="b02ff-264">Note that advertised shortcuts always point at a particular application, identified by a [**ProductCode**](productcode.md), and should not be shared between applications.</span></span> <span data-ttu-id="b02ff-265">Angekündigte Verknüpfungen funktionieren nur für die zuletzt installierte Anwendung und werden entfernt, wenn diese Anwendung entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b02ff-265">Advertised shortcuts only work for the most recently installed application, and are removed when that application is removed.</span></span>

<span data-ttu-id="b02ff-266">Diese Tabelle wird verwendet, wenn die Aktion " [kreateshortcuts](createshortcuts-action.md) " und die [removeshortcuts-Aktion](removeshortcuts-action.md) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b02ff-266">This table is referred to when the [CreateShortcuts action](createshortcuts-action.md) and the [RemoveShortcuts action](removeshortcuts-action.md) is executed.</span></span>

<span data-ttu-id="b02ff-267">Siehe auch die [**disableadvtverknüpfungs**](disableadvtshortcuts.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b02ff-267">See also the [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="b02ff-268">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="b02ff-268">Validation</span></span>

<dl>

[<span data-ttu-id="b02ff-269">ICE03</span><span class="sxs-lookup"><span data-stu-id="b02ff-269">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b02ff-270">ICE06</span><span class="sxs-lookup"><span data-stu-id="b02ff-270">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b02ff-271">ICE19</span><span class="sxs-lookup"><span data-stu-id="b02ff-271">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="b02ff-272">ICE32</span><span class="sxs-lookup"><span data-stu-id="b02ff-272">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b02ff-273">ICE36</span><span class="sxs-lookup"><span data-stu-id="b02ff-273">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="b02ff-274">ICE46</span><span class="sxs-lookup"><span data-stu-id="b02ff-274">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="b02ff-275">ICE50</span><span class="sxs-lookup"><span data-stu-id="b02ff-275">ICE50</span></span>](ice50.md)  
[<span data-ttu-id="b02ff-276">ICE57</span><span class="sxs-lookup"><span data-stu-id="b02ff-276">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="b02ff-277">ICE59</span><span class="sxs-lookup"><span data-stu-id="b02ff-277">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="b02ff-278">ICE67</span><span class="sxs-lookup"><span data-stu-id="b02ff-278">ICE67</span></span>](ice67.md)  
[<span data-ttu-id="b02ff-279">ICE69</span><span class="sxs-lookup"><span data-stu-id="b02ff-279">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="b02ff-280">ICE80</span><span class="sxs-lookup"><span data-stu-id="b02ff-280">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="b02ff-281">ICE90</span><span class="sxs-lookup"><span data-stu-id="b02ff-281">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="b02ff-282">ICE91</span><span class="sxs-lookup"><span data-stu-id="b02ff-282">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="b02ff-283">ICE94</span><span class="sxs-lookup"><span data-stu-id="b02ff-283">ICE94</span></span>](ice94.md)  
</dl>

 

 



