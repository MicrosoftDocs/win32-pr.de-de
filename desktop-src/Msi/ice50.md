---
description: ICE50 prüft, ob Verknüpfungs Symbole angegeben werden, damit Sie ordnungsgemäß angezeigt werden und der Erweiterung der Zieldatei entsprechen.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960348"
---
# <a name="ice50"></a><span data-ttu-id="60015-103">ICE50</span><span class="sxs-lookup"><span data-stu-id="60015-103">ICE50</span></span>

<span data-ttu-id="60015-104">ICE50 prüft, ob Verknüpfungs Symbole angegeben werden, damit Sie ordnungsgemäß angezeigt werden und der Erweiterung der Zieldatei entsprechen.</span><span class="sxs-lookup"><span data-stu-id="60015-104">ICE50 checks that shortcut icons are specified to display correctly and match their target file's extension.</span></span>

## <a name="result"></a><span data-ttu-id="60015-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="60015-105">Result</span></span>

<span data-ttu-id="60015-106">ICE50 gibt eine Fehlermeldung aus, wenn die Erweiterung der Symbol-und Zieldateien nicht entspricht.</span><span class="sxs-lookup"><span data-stu-id="60015-106">ICE50 posts an error message if the extension of the icon and target files do not match.</span></span> <span data-ttu-id="60015-107">ICE50 gibt eine Warnung aus, wenn Symbole in Dateien gespeichert werden, die nicht über die Erweiterung ". exe" oder ". ico" verfügen.</span><span class="sxs-lookup"><span data-stu-id="60015-107">ICE50 posts a warning if icons are stored in files that do not have an .exe or .ico extension.</span></span>

## <a name="example"></a><span data-ttu-id="60015-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="60015-108">Example</span></span>

<span data-ttu-id="60015-109">ICE50 meldet den folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="60015-109">ICE50 reports the following error for the example shown.</span></span>



| <span data-ttu-id="60015-110">ICE50-Fehler oder-Warnung</span><span class="sxs-lookup"><span data-stu-id="60015-110">ICE50 error or warning</span></span>                                                                                                              | <span data-ttu-id="60015-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60015-111">Description</span></span>                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60015-112">Die Erweiterung des Symbols ' Icon2. dat ' für die Verknüpfung ' Shortcut2 ' stimmt nicht mit der Erweiterung der Schlüsseldatei für die Komponente ' Component2 ' identisch.</span><span class="sxs-lookup"><span data-stu-id="60015-112">The extension of Icon 'Icon2.dat' for Shortcut 'Shortcut2' does not match the extension of the Key File for component 'Component2'.</span></span> | <span data-ttu-id="60015-113">Wenn die Erweiterungen des Symbols und der Zieldatei nicht stimmen, verfügt die Verknüpfung nicht über das korrekte Kontextmenü, wenn die Komponente angekündigt wird.</span><span class="sxs-lookup"><span data-stu-id="60015-113">If the extensions of the icon and the target file do not match, the shortcut will not have the correct context menu when the component is advertised.</span></span> <span data-ttu-id="60015-114">Benennen Sie das Symbol so um, dass es der Erweiterung der Zieldatei entspricht, um diesen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="60015-114">To fix this error, rename the icon to match the extension of the target file.</span></span><br/> |
| <span data-ttu-id="60015-115">Die Erweiterung des Symbols ' Icon1.bat ' für die Verknüpfung ' Shortcut1 ' ist nicht ' exe ' oder ' ICO '.</span><span class="sxs-lookup"><span data-stu-id="60015-115">The extension of Icon 'Icon1.bat' for Shortcut 'Shortcut1' is not "exe" or "ico".</span></span> <span data-ttu-id="60015-116">Das Symbol wird nicht ordnungsgemäß angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60015-116">The Icon will not be displayed correctly.</span></span>         | <span data-ttu-id="60015-117">Nicht in allen Versionen der Shell werden Symbole korrekt angezeigt, die in Dateien gespeichert sind, die nicht über die Erweiterungen "exe" oder "ico" verfügen.</span><span class="sxs-lookup"><span data-stu-id="60015-117">Not all versions of the shell correctly display icons stored in files that do not have extensions of "exe" or "ico".</span></span> <span data-ttu-id="60015-118">Um diese Warnung zu beheben, benennen Sie das Symbol mit der Erweiterung "exe" oder "ico" um.</span><span class="sxs-lookup"><span data-stu-id="60015-118">To fix this warning, rename the icon have an extension of "exe" or "ico".</span></span><br/>                                      |



 

<span data-ttu-id="60015-119">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="60015-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="60015-120">File</span><span class="sxs-lookup"><span data-stu-id="60015-120">File</span></span>  | <span data-ttu-id="60015-121">FileName</span><span class="sxs-lookup"><span data-stu-id="60015-121">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="60015-122">Datei1</span><span class="sxs-lookup"><span data-stu-id="60015-122">File1</span></span> | <span data-ttu-id="60015-123">File1.bat</span><span class="sxs-lookup"><span data-stu-id="60015-123">File1.bat</span></span> |
| <span data-ttu-id="60015-124">Datei2</span><span class="sxs-lookup"><span data-stu-id="60015-124">File2</span></span> | <span data-ttu-id="60015-125">File2.pl</span><span class="sxs-lookup"><span data-stu-id="60015-125">File2.pl</span></span>  |



 

<span data-ttu-id="60015-126">[Funktions Tabelle](feature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="60015-126">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="60015-127">Funktion</span><span class="sxs-lookup"><span data-stu-id="60015-127">Feature</span></span>  |
|----------|
| <span data-ttu-id="60015-128">Feature1</span><span class="sxs-lookup"><span data-stu-id="60015-128">Feature1</span></span> |



 

<span data-ttu-id="60015-129">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="60015-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="60015-130">Komponente</span><span class="sxs-lookup"><span data-stu-id="60015-130">Component</span></span>  | <span data-ttu-id="60015-131">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="60015-131">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="60015-132">Component1</span><span class="sxs-lookup"><span data-stu-id="60015-132">Component1</span></span> | <span data-ttu-id="60015-133">Datei1</span><span class="sxs-lookup"><span data-stu-id="60015-133">File1</span></span>   |
| <span data-ttu-id="60015-134">Component2</span><span class="sxs-lookup"><span data-stu-id="60015-134">Component2</span></span> | <span data-ttu-id="60015-135">Datei2</span><span class="sxs-lookup"><span data-stu-id="60015-135">File2</span></span>   |



 

[<span data-ttu-id="60015-136">Symboltabelle</span><span class="sxs-lookup"><span data-stu-id="60015-136">Icon Table</span></span>](icon-table.md)



| <span data-ttu-id="60015-137">Name</span><span class="sxs-lookup"><span data-stu-id="60015-137">Name</span></span>      | <span data-ttu-id="60015-138">Daten</span><span class="sxs-lookup"><span data-stu-id="60015-138">Data</span></span>            |
|-----------|-----------------|
| <span data-ttu-id="60015-139">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="60015-139">Icon1.bat</span></span> | <span data-ttu-id="60015-140">\[Binärdaten\]</span><span class="sxs-lookup"><span data-stu-id="60015-140">\[Binary Data\]</span></span> |
| <span data-ttu-id="60015-141">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="60015-141">Icon2.dat</span></span> | <span data-ttu-id="60015-142">\[Binärdaten\]</span><span class="sxs-lookup"><span data-stu-id="60015-142">\[Binary Data\]</span></span> |



 

<span data-ttu-id="60015-143">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="60015-143">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="60015-144">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="60015-144">Shortcut</span></span>  | <span data-ttu-id="60015-145">Komponente</span><span class="sxs-lookup"><span data-stu-id="60015-145">Component</span></span>  | <span data-ttu-id="60015-146">Ziel</span><span class="sxs-lookup"><span data-stu-id="60015-146">Target</span></span>   | <span data-ttu-id="60015-147">Symbol\_</span><span class="sxs-lookup"><span data-stu-id="60015-147">Icon\_</span></span>    |
|-----------|------------|----------|-----------|
| <span data-ttu-id="60015-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="60015-148">Shortcut1</span></span> | <span data-ttu-id="60015-149">Component1</span><span class="sxs-lookup"><span data-stu-id="60015-149">Component1</span></span> | <span data-ttu-id="60015-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="60015-150">Feature1</span></span> | <span data-ttu-id="60015-151">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="60015-151">Icon1.bat</span></span> |
| <span data-ttu-id="60015-152">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="60015-152">Shortcut2</span></span> | <span data-ttu-id="60015-153">Component2</span><span class="sxs-lookup"><span data-stu-id="60015-153">Component2</span></span> | <span data-ttu-id="60015-154">Feature1</span><span class="sxs-lookup"><span data-stu-id="60015-154">Feature1</span></span> | <span data-ttu-id="60015-155">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="60015-155">Icon2.dat</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="60015-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60015-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60015-157">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="60015-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




