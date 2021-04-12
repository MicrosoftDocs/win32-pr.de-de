---
description: ICE69 prüft, ob alle Teil Zeichenfolgen der Form, die \[ \] innerhalb einer formatierten Zeichenfolge $componentkey, keine Querverweis Komponenten sind.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217654"
---
# <a name="ice69"></a><span data-ttu-id="e89f8-103">ICE69</span><span class="sxs-lookup"><span data-stu-id="e89f8-103">ICE69</span></span>

<span data-ttu-id="e89f8-104">ICE69 prüft, ob alle Teil Zeichenfolgen der Form, die \[ \] innerhalb einer [formatierten](formatted.md) Zeichenfolge $componentkey, keine Querverweis Komponenten sind.</span><span class="sxs-lookup"><span data-stu-id="e89f8-104">ICE69 checks that all substrings of the form \[$componentkey\] within a [formatted](formatted.md) string do not cross-reference components.</span></span> <span data-ttu-id="e89f8-105">Ein Komponenten übergreifender Verweis tritt \[ auf, wenn die $componentkey- \] Eigenschaft einer formatierten Zeichenfolge auf eine andere Komponente als die in der Komponenten \_ Spalte der Tabellen gespeicherte Komponente verweist.</span><span class="sxs-lookup"><span data-stu-id="e89f8-105">A cross-component reference occurs when the \[$componentkey\] property of a formatted string refers to a component other than the component stored in the Component\_ column of your tables.</span></span>

<span data-ttu-id="e89f8-106">Probleme mit der Komponenten übergreifenden Referenzierung ergeben sich aus der Art und Weise, wie [formatierte](formatted.md) Zeichen folgen ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="e89f8-106">Problems with cross-component referencing arise from the way [formatted](formatted.md) strings are evaluated.</span></span> <span data-ttu-id="e89f8-107">Wenn die Komponente, auf die mit der \[ $componentkey \] -Eigenschaft verwiesen wird, bereits installiert ist und während der aktuellen Installation nicht geändert wird (z. b. Wenn Sie neu installiert, in die Quelle verschoben wird usw.), wird der Ausdruck \[ $componentkey \] NULL ausgewertet, da der Aktionszustand der Komponente in \[ $componentkey \] NULL ist.</span><span class="sxs-lookup"><span data-stu-id="e89f8-107">If the component referenced with the \[$componentkey\] property is already installed and is not being changed during the current installation (for example, being reinstalled, moved to source, and so forth), the expression \[$componentkey\] evaluates to null, because the action state of the component in \[$componentkey\] is null.</span></span> <span data-ttu-id="e89f8-108">Ähnliche Probleme können während des Aktualisierungs-und Reparatur Vorgangs auftreten.</span><span class="sxs-lookup"><span data-stu-id="e89f8-108">Similar problems can occur during upgrade and repair operations.</span></span>

## <a name="result"></a><span data-ttu-id="e89f8-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="e89f8-109">Result</span></span>

<span data-ttu-id="e89f8-110">ICE69 gibt einen Fehler zurück, wenn eine \[ $componentkey \] Teil Zeichenfolge innerhalb einer [formatierten](formatted.md) Zeichenfolge Querverweise auf eine Komponente eines anderen Features durchführt.</span><span class="sxs-lookup"><span data-stu-id="e89f8-110">ICE69 returns an error if a \[$componentkey\] substring within a [formatted](formatted.md) string cross-references a component in another feature.</span></span> <span data-ttu-id="e89f8-111">ICE69 gibt eine Warnung zurück, wenn eine \[ $componentkey \] Teil Zeichenfolge innerhalb einer formatierten Zeichenfolge Querverweise auf eine Komponente in derselben Funktion durchführt.</span><span class="sxs-lookup"><span data-stu-id="e89f8-111">ICE69 returns a warning if a \[$componentkey\] substring within a formatted string cross-references a component in the same feature.</span></span> <span data-ttu-id="e89f8-112">(Die Tabelle " [FeatureComponents](featurecomponents-table.md) " wird verwendet, um diese Zuordnung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e89f8-112">(The [FeatureComponents](featurecomponents-table.md) table is used to determine this mapping.</span></span> <span data-ttu-id="e89f8-113">Es muss der gleichen Funktion für die Warnung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="e89f8-113">It must map to the same feature for the warning.</span></span> <span data-ttu-id="e89f8-114">Verweise auf Komponenten in übergeordneten Funktionen oder Verweise auf Komponenten in untergeordneten Funktionen werden als Fehler betrachtet.)</span><span class="sxs-lookup"><span data-stu-id="e89f8-114">Referencing components in parent features or referencing components in child features is considered to be an error.)</span></span>

<span data-ttu-id="e89f8-115">ICE69 meldet einen Fehler, wenn die \[ \# \] Teil Zeichenfolge von filekey innerhalb einer [formatierten](formatted.md) Zeichenfolge auf eine Datei verweist, die nicht in der [Datei](file-table.md) Tabelle als zur selben Komponente gehörend angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e89f8-115">ICE69 reports an error if the \[\#FileKey\] substring within a [formatted](formatted.md) string references a file which is not specified in the [File](file-table.md) table as belonging to the same component.</span></span>

## <a name="example"></a><span data-ttu-id="e89f8-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e89f8-116">Example</span></span>

<span data-ttu-id="e89f8-117">ICE69 meldet Folgendes für die gezeigten Beispiele.</span><span class="sxs-lookup"><span data-stu-id="e89f8-117">ICE69 reports the following for the examples shown.</span></span>

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

<span data-ttu-id="e89f8-118">Um diesen Fehler zu beheben, führen Sie keine Querverweise für Komponenten aus.</span><span class="sxs-lookup"><span data-stu-id="e89f8-118">To fix this error, do not cross-reference components.</span></span> <span data-ttu-id="e89f8-119">Ändern \[ Sie die $componentkey so, dass \] Sie der Komponente der Verknüpfung entspricht.</span><span class="sxs-lookup"><span data-stu-id="e89f8-119">Change the \[$componentkey\] to match the component of the shortcut.</span></span>

<span data-ttu-id="e89f8-120">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e89f8-120">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="e89f8-121">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="e89f8-121">Shortcut</span></span>  | <span data-ttu-id="e89f8-122">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="e89f8-122">Component\_</span></span> | <span data-ttu-id="e89f8-123">Argument</span><span class="sxs-lookup"><span data-stu-id="e89f8-123">Argument</span></span>     |
|-----------|-------------|--------------|
| <span data-ttu-id="e89f8-124">Test</span><span class="sxs-lookup"><span data-stu-id="e89f8-124">Test</span></span>      | <span data-ttu-id="e89f8-125">QuickTest</span><span class="sxs-lookup"><span data-stu-id="e89f8-125">QuickTest</span></span>   | <span data-ttu-id="e89f8-126">-v \[ $Test\]</span><span class="sxs-lookup"><span data-stu-id="e89f8-126">-v \[$Test\]</span></span> |
| <span data-ttu-id="e89f8-127">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="e89f8-127">Shortcut2</span></span> | <span data-ttu-id="e89f8-128">QuickTest</span><span class="sxs-lookup"><span data-stu-id="e89f8-128">QuickTest</span></span>   | <span data-ttu-id="e89f8-129">\[$Test 2\]</span><span class="sxs-lookup"><span data-stu-id="e89f8-129">\[$Test2\]</span></span>   |



 

<span data-ttu-id="e89f8-130">Die [Verb](verb-table.md) -und [Erweiterungs](extension-table.md) Tabellen sind Sonderfälle, in denen die Verb-Tabelle auf eine Erweiterung verweist, die zu einer Komponente gehört.</span><span class="sxs-lookup"><span data-stu-id="e89f8-130">The [Verb](verb-table.md) and [Extension](extension-table.md) tables are special cases in that the Verb table references an extension that belongs to a component.</span></span> <span data-ttu-id="e89f8-131">Eine Erweiterung kann jedoch mehreren Komponenten angehören, da der Primärschlüssel für die Erweiterungs Tabelle aus der Erweiterung und den Komponenten \_ Spalten besteht.</span><span class="sxs-lookup"><span data-stu-id="e89f8-131">An Extension, however, can belong to multiple components because the primary key for the extension table is made up of the Extension and Component\_ columns.</span></span> <span data-ttu-id="e89f8-132">Sie können logisch folgende Situation haben:</span><span class="sxs-lookup"><span data-stu-id="e89f8-132">You can logically have the following situation.</span></span>

<span data-ttu-id="e89f8-133">[Verb Tabelle](verb-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e89f8-133">[Verb Table](verb-table.md) (partial)</span></span>



| <span data-ttu-id="e89f8-134">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="e89f8-134">Extension</span></span> | <span data-ttu-id="e89f8-135">Verb\_</span><span class="sxs-lookup"><span data-stu-id="e89f8-135">Verb\_</span></span> | <span data-ttu-id="e89f8-136">Argument</span><span class="sxs-lookup"><span data-stu-id="e89f8-136">Argument</span></span>                |
|-----------|--------|-------------------------|
| <span data-ttu-id="e89f8-137">TST</span><span class="sxs-lookup"><span data-stu-id="e89f8-137">tst</span></span>       | <span data-ttu-id="e89f8-138">open</span><span class="sxs-lookup"><span data-stu-id="e89f8-138">open</span></span>   | <span data-ttu-id="e89f8-139">-v \[ $COMP 1 \] \[ $COMP 2\]</span><span class="sxs-lookup"><span data-stu-id="e89f8-139">-v \[$comp1\]\[$comp2\]</span></span> |



 

<span data-ttu-id="e89f8-140">[Erweiterungs Tabelle](extension-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e89f8-140">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="e89f8-141">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="e89f8-141">Extension</span></span> | <span data-ttu-id="e89f8-142">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="e89f8-142">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="e89f8-143">TST</span><span class="sxs-lookup"><span data-stu-id="e89f8-143">tst</span></span>       | <span data-ttu-id="e89f8-144">comp1</span><span class="sxs-lookup"><span data-stu-id="e89f8-144">comp1</span></span>       |
| <span data-ttu-id="e89f8-145">TST</span><span class="sxs-lookup"><span data-stu-id="e89f8-145">tst</span></span>       | <span data-ttu-id="e89f8-146">comp2</span><span class="sxs-lookup"><span data-stu-id="e89f8-146">comp2</span></span>       |



 

[<span data-ttu-id="e89f8-147">FeatureComponents-Tabelle</span><span class="sxs-lookup"><span data-stu-id="e89f8-147">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="e89f8-148">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="e89f8-148">Feature\_</span></span> | <span data-ttu-id="e89f8-149">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="e89f8-149">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="e89f8-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="e89f8-150">Feature1</span></span>  | <span data-ttu-id="e89f8-151">QuickTest</span><span class="sxs-lookup"><span data-stu-id="e89f8-151">QuickTest</span></span>   |
| <span data-ttu-id="e89f8-152">Feature1</span><span class="sxs-lookup"><span data-stu-id="e89f8-152">Feature1</span></span>  | <span data-ttu-id="e89f8-153">Test</span><span class="sxs-lookup"><span data-stu-id="e89f8-153">Test</span></span>        |
| <span data-ttu-id="e89f8-154">Feature2</span><span class="sxs-lookup"><span data-stu-id="e89f8-154">Feature2</span></span>  | <span data-ttu-id="e89f8-155">Test2</span><span class="sxs-lookup"><span data-stu-id="e89f8-155">Test2</span></span>       |



 

<span data-ttu-id="e89f8-156">In diesem Fall müssen Sie sicherstellen, dass mindestens eine der \[ $componentkey \] Eigenschaften einen nicht-NULL-Wert ergibt.</span><span class="sxs-lookup"><span data-stu-id="e89f8-156">In this case, you must ensure that at least one of the \[$componentkey\] properties evaluates to a non-null value.</span></span> <span data-ttu-id="e89f8-157">Jede \[ $componentkey \] Eigenschaft in der Argument-Spalte der Verb-Tabelle ( \[ $COMP 1 \] und \[ $COMP 2 \] im obigen Beispiel) muss jedoch auf eine mögliche Komponente verweisen, die in der dem Verb zugeordneten Erweiterung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e89f8-157">However, every \[$componentkey\] property in the Argument column of the Verb table (\[$comp1\] and \[$comp2\] in the above example) must reference a possible component included with the extension associated with the verb.</span></span> <span data-ttu-id="e89f8-158">Ein Verweis wie \[ $Comp 3 \] würde zu einer Warnung aus ICE69 führen.</span><span class="sxs-lookup"><span data-stu-id="e89f8-158">A reference like \[$comp3\] would result in a warning from ICE69.</span></span>

<span data-ttu-id="e89f8-159">Die [AppID-Tabelle](appid-table.md) hat eine ähnliche Situation wie die Verb Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e89f8-159">The [AppId table](appid-table.md) has a similar situation to the Verb table.</span></span> <span data-ttu-id="e89f8-160">Die [Klassen Tabelle](class-table.md) wird als Komponenten Verweis verwendet.</span><span class="sxs-lookup"><span data-stu-id="e89f8-160">It uses the [Class table](class-table.md) for its component reference.</span></span> <span data-ttu-id="e89f8-161">In diesem Fall wird die AppID-Tabelle auf die gleiche Weise überprüft wie die Verb-Extension Validierung (jetzt AppID-Class).</span><span class="sxs-lookup"><span data-stu-id="e89f8-161">In this case, the AppId table is validated in the same way as the Verb-Extension validation (now AppId-Class).</span></span>

<span data-ttu-id="e89f8-162">Die Argument-Spalte der Klassen Tabelle wird wie die [Verknüpfung](shortcut-table.md), die [Registrierung](registry-table.md)und ähnliche Tabellen überprüft.</span><span class="sxs-lookup"><span data-stu-id="e89f8-162">The Class table's Argument column is validated like the [Shortcut](shortcut-table.md), [Registry](registry-table.md), and similar tables.</span></span>

## <a name="table-used-during-execution-only-if-found"></a><span data-ttu-id="e89f8-163">Während der Ausführung verwendete Tabelle (nur, wenn Sie gefunden wurde)</span><span class="sxs-lookup"><span data-stu-id="e89f8-163">Table used during execution (only if found)</span></span>

[<span data-ttu-id="e89f8-164">INIFILE</span><span class="sxs-lookup"><span data-stu-id="e89f8-164">IniFile</span></span>](inifile-table.md)

[<span data-ttu-id="e89f8-165">Removeinifile</span><span class="sxs-lookup"><span data-stu-id="e89f8-165">RemoveIniFile</span></span>](removeinifile-table.md)

[<span data-ttu-id="e89f8-166">Registrierung</span><span class="sxs-lookup"><span data-stu-id="e89f8-166">Registry</span></span>](registry-table.md)

[<span data-ttu-id="e89f8-167">Removeregistry</span><span class="sxs-lookup"><span data-stu-id="e89f8-167">RemoveRegistry</span></span>](removeregistry-table.md)

[<span data-ttu-id="e89f8-168">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="e89f8-168">ServiceControl</span></span>](servicecontrol-table.md)

[<span data-ttu-id="e89f8-169">Serviceingestall</span><span class="sxs-lookup"><span data-stu-id="e89f8-169">ServiceInstall</span></span>](serviceinstall-table.md)

[<span data-ttu-id="e89f8-170">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="e89f8-170">Shortcut</span></span>](shortcut-table.md)

[<span data-ttu-id="e89f8-171">Verb</span><span class="sxs-lookup"><span data-stu-id="e89f8-171">Verb</span></span>](verb-table.md)

[<span data-ttu-id="e89f8-172">Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e89f8-172">Extension</span></span>](extension-table.md)

[<span data-ttu-id="e89f8-173">Klasse</span><span class="sxs-lookup"><span data-stu-id="e89f8-173">Class</span></span>](class-table.md)

[<span data-ttu-id="e89f8-174">AppId</span><span class="sxs-lookup"><span data-stu-id="e89f8-174">AppId</span></span>](appid-table.md)

[<span data-ttu-id="e89f8-175">Umgebung</span><span class="sxs-lookup"><span data-stu-id="e89f8-175">Environment</span></span>](environment-table.md)

## <a name="related-topics"></a><span data-ttu-id="e89f8-176">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e89f8-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e89f8-177">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="e89f8-177">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



