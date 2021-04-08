---
description: ICE35 überprüft, ob Komponenten, die in einer CAB-Datei gespeicherte komprimierte Dateien enthalten, nicht aus der Quelle ausgeführt werden. Bei Windows Installer 2,0 oder höher wurde diese Einschränkung entfernt.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960038"
---
# <a name="ice35"></a><span data-ttu-id="d38bc-104">ICE35</span><span class="sxs-lookup"><span data-stu-id="d38bc-104">ICE35</span></span>

<span data-ttu-id="d38bc-105">ICE35 überprüft, ob Komponenten, die in einer CAB- [Datei](cabinet-files.md) gespeicherte komprimierte Dateien enthalten, nicht aus der Quelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d38bc-105">ICE35 validates that components containing compressed files stored in a [cabinet file](cabinet-files.md) are not set to run from source.</span></span> <span data-ttu-id="d38bc-106">Bei Windows Installer 2,0 oder höher wurde diese Einschränkung entfernt.</span><span class="sxs-lookup"><span data-stu-id="d38bc-106">With Windows Installer 2.0 or later, this restriction has been removed.</span></span>

<span data-ttu-id="d38bc-107">ICE35 fragt die CAB-Spalte der [Medien Tabelle](media-table.md) ab, um zu bestimmen, welche Dateien komprimiert und in einer CAB-Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d38bc-107">ICE35 queries the Cabinet column of the [Media table](media-table.md) to determine which files are compressed and stored in a cabinet file.</span></span> <span data-ttu-id="d38bc-108">Die [Dateitabelle](file-table.md) wird abgefragt, um zu bestimmen, welche Komponenten diese Dateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="d38bc-108">It queries the [File table](file-table.md) to determine which components contain these files.</span></span> <span data-ttu-id="d38bc-109">Zum Schluss überprüft er die [Komponenten Tabelle](component-table.md) , um zu bestimmen, ob die Bits aus der Quelle in der Spalte Attribute festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="d38bc-109">Finally, it checks the [Component table](component-table.md) to determine whether the run-from-source bits are set in the Attributes column.</span></span>

## <a name="result"></a><span data-ttu-id="d38bc-110">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="d38bc-110">Result</span></span>

<span data-ttu-id="d38bc-111">ICE35 gibt eine Fehlermeldung aus, wenn eine komprimierte Datei in einer CAB-Datei gespeichert ist, die zu einer Komponente gehört, in der das Bit msidbcomponentattributessourceonly in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d38bc-111">ICE35 posts an error message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesSourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="d38bc-112">Bei Windows Installer 2,0 oder höher wird dies von einem Fehler in eine Warnmeldung geändert.</span><span class="sxs-lookup"><span data-stu-id="d38bc-112">With Windows Installer 2.0 or later, this is changed from an error to a warning message.</span></span> <span data-ttu-id="d38bc-113">Ein Paket, das nur Windows Installer 2,0 und höher unterstützt, verfügt über die PID- \_ Eigenschaft PageCount des Datenstroms für die Zusammenfassung, die auf einen Wert von mindestens 200 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d38bc-113">A package that supports only Windows Installer 2.0 and later has the PID\_PAGECOUNT property of the Summary Information Stream set to a value of at least 200.</span></span>

<span data-ttu-id="d38bc-114">ICE35 gibt eine Warnmeldung aus, wenn eine komprimierte Datei in einer CAB-Datei gespeichert ist, die zu einer Komponente gehört, in der die Spalte Attribute der [Komponenten Tabelle](component-table.md)in der Spalte Attribute festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d38bc-114">ICE35 posts warning message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesOptional bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="d38bc-115">Diese Warnmeldung wurde mit Windows Installer 2,0 und höher entfernt.</span><span class="sxs-lookup"><span data-stu-id="d38bc-115">This warning message has been removed with Windows Installer 2.0 and later.</span></span>

<span data-ttu-id="d38bc-116">Wenn sich mehrere Dateien in einer-Komponente in einer CAB-Datei befinden, meldet ICE35 Fehler für jede Datei, für die das Run From Source-Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d38bc-116">If multiple files in a component are in a cabinet file, ICE35 reports errors for each file that has the run from source bit set.</span></span>

## <a name="example"></a><span data-ttu-id="d38bc-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d38bc-117">Example</span></span>

<span data-ttu-id="d38bc-118">ICE35 meldet die folgenden Fehler und Warnungen für das Beispiel, das unter Verwendung einer früheren Version als Windows Installer Version 2,0 angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d38bc-118">ICE35 reports the following errors and warnings for the example shown using a version earlier than Windows Installer version 2.0.</span></span>



| <span data-ttu-id="d38bc-119">ICE35-Fehler</span><span class="sxs-lookup"><span data-stu-id="d38bc-119">ICE35 Error</span></span>                                                                                                | <span data-ttu-id="d38bc-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d38bc-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38bc-121">Fehler: die Komponente Component3 kann nicht nur aus der Quelle ausgeführt werden, da die zugehörige Mitglieds Datei "Datei3" komprimiert ist.</span><span class="sxs-lookup"><span data-stu-id="d38bc-121">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="d38bc-122">Es gibt eine komprimierte Datei, die in einer CAB-Datei gespeichert ist, und diese Datei gehört zu einer Komponente, in der das sourceOnly-Bit in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d38bc-122">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="d38bc-123">Um diesen Fehler zu beheben, ändern Sie die unteren 2 Bits des Component2's Attribute-Werts in "00", d. h. nur lokal, oder entfernen Sie datei4 aus der CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="d38bc-123">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="d38bc-124">Fehler: die Komponente Component3 kann nicht nur aus der Quelle ausgeführt werden, da die zugehörige Mitglieds Datei "Datei3" komprimiert ist.</span><span class="sxs-lookup"><span data-stu-id="d38bc-124">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="d38bc-125">Es gibt eine komprimierte Datei, die in einer CAB-Datei gespeichert ist, und diese Datei gehört zu einer Komponente, in der das sourceOnly-Bit in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d38bc-125">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="d38bc-126">Da die Dateien in einer Komponente nicht alle aus denselben Medien stammen müssen, meldet ICE35 Fehler für jede Datei in der Komponente, die sich in einer CAB-Datei befindet.</span><span class="sxs-lookup"><span data-stu-id="d38bc-126">Because the files in a component do not all have to originate from the same media, ICE35 reports errors for each file in the component that is in a cabinet.</span></span><br/> <span data-ttu-id="d38bc-127">Um diesen Fehler zu beheben, ändern Sie die unteren 2 Bits des Component2's Attribute-Werts in "00", d. h. nur lokal, oder entfernen Sie datei4 aus der CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="d38bc-127">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/> |



 

<span data-ttu-id="d38bc-128">[Medien Tabelle](media-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d38bc-128">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="d38bc-129">DiskID</span><span class="sxs-lookup"><span data-stu-id="d38bc-129">DiskID</span></span> | <span data-ttu-id="d38bc-130">LastSequence</span><span class="sxs-lookup"><span data-stu-id="d38bc-130">LastSequence</span></span> | <span data-ttu-id="d38bc-131">KEs</span><span class="sxs-lookup"><span data-stu-id="d38bc-131">Cabinet</span></span>   |
|--------|--------------|-----------|
| <span data-ttu-id="d38bc-132">1</span><span class="sxs-lookup"><span data-stu-id="d38bc-132">1</span></span>      | <span data-ttu-id="d38bc-133">2</span><span class="sxs-lookup"><span data-stu-id="d38bc-133">2</span></span>            |           |
| <span data-ttu-id="d38bc-134">2</span><span class="sxs-lookup"><span data-stu-id="d38bc-134">2</span></span>      | <span data-ttu-id="d38bc-135">4</span><span class="sxs-lookup"><span data-stu-id="d38bc-135">4</span></span>            | <span data-ttu-id="d38bc-136">One.cab</span><span class="sxs-lookup"><span data-stu-id="d38bc-136">One.cab</span></span>   |
| <span data-ttu-id="d38bc-137">3</span><span class="sxs-lookup"><span data-stu-id="d38bc-137">3</span></span>      | <span data-ttu-id="d38bc-138">5</span><span class="sxs-lookup"><span data-stu-id="d38bc-138">5</span></span>            | <span data-ttu-id="d38bc-139">\#Two.cab</span><span class="sxs-lookup"><span data-stu-id="d38bc-139">\#Two.cab</span></span> |



 

<span data-ttu-id="d38bc-140">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d38bc-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="d38bc-141">File</span><span class="sxs-lookup"><span data-stu-id="d38bc-141">File</span></span>  | <span data-ttu-id="d38bc-142">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="d38bc-142">Component\_</span></span> | <span data-ttu-id="d38bc-143">Sequenz</span><span class="sxs-lookup"><span data-stu-id="d38bc-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="d38bc-144">Datei1</span><span class="sxs-lookup"><span data-stu-id="d38bc-144">File1</span></span> | <span data-ttu-id="d38bc-145">Component1</span><span class="sxs-lookup"><span data-stu-id="d38bc-145">Component1</span></span>  | <span data-ttu-id="d38bc-146">1</span><span class="sxs-lookup"><span data-stu-id="d38bc-146">1</span></span>        |
| <span data-ttu-id="d38bc-147">Datei2</span><span class="sxs-lookup"><span data-stu-id="d38bc-147">File2</span></span> | <span data-ttu-id="d38bc-148">Component2</span><span class="sxs-lookup"><span data-stu-id="d38bc-148">Component2</span></span>  | <span data-ttu-id="d38bc-149">2</span><span class="sxs-lookup"><span data-stu-id="d38bc-149">2</span></span>        |
| <span data-ttu-id="d38bc-150">Datei3</span><span class="sxs-lookup"><span data-stu-id="d38bc-150">File3</span></span> | <span data-ttu-id="d38bc-151">Component2</span><span class="sxs-lookup"><span data-stu-id="d38bc-151">Component2</span></span>  | <span data-ttu-id="d38bc-152">3</span><span class="sxs-lookup"><span data-stu-id="d38bc-152">3</span></span>        |
| <span data-ttu-id="d38bc-153">Datei4</span><span class="sxs-lookup"><span data-stu-id="d38bc-153">File4</span></span> | <span data-ttu-id="d38bc-154">Component3</span><span class="sxs-lookup"><span data-stu-id="d38bc-154">Component3</span></span>  | <span data-ttu-id="d38bc-155">4</span><span class="sxs-lookup"><span data-stu-id="d38bc-155">4</span></span>        |
| <span data-ttu-id="d38bc-156">Datei5</span><span class="sxs-lookup"><span data-stu-id="d38bc-156">File5</span></span> | <span data-ttu-id="d38bc-157">Component3</span><span class="sxs-lookup"><span data-stu-id="d38bc-157">Component3</span></span>  | <span data-ttu-id="d38bc-158">5</span><span class="sxs-lookup"><span data-stu-id="d38bc-158">5</span></span>        |



 

<span data-ttu-id="d38bc-159">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d38bc-159">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="d38bc-160">Komponente</span><span class="sxs-lookup"><span data-stu-id="d38bc-160">Component</span></span>  | <span data-ttu-id="d38bc-161">Attribute</span><span class="sxs-lookup"><span data-stu-id="d38bc-161">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="d38bc-162">Component1</span><span class="sxs-lookup"><span data-stu-id="d38bc-162">Component1</span></span> | <span data-ttu-id="d38bc-163">0</span><span class="sxs-lookup"><span data-stu-id="d38bc-163">0</span></span>          |
| <span data-ttu-id="d38bc-164">Component2</span><span class="sxs-lookup"><span data-stu-id="d38bc-164">Component2</span></span> | <span data-ttu-id="d38bc-165">2</span><span class="sxs-lookup"><span data-stu-id="d38bc-165">2</span></span>          |
| <span data-ttu-id="d38bc-166">Component3</span><span class="sxs-lookup"><span data-stu-id="d38bc-166">Component3</span></span> | <span data-ttu-id="d38bc-167">1</span><span class="sxs-lookup"><span data-stu-id="d38bc-167">1</span></span>          |



 

<span data-ttu-id="d38bc-168">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d38bc-168">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="d38bc-169">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="d38bc-169">Shortcut</span></span>  | <span data-ttu-id="d38bc-170">Symbol\_</span><span class="sxs-lookup"><span data-stu-id="d38bc-170">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="d38bc-171">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="d38bc-171">Shortcut1</span></span> | <span data-ttu-id="d38bc-172">Icon2</span><span class="sxs-lookup"><span data-stu-id="d38bc-172">Icon2</span></span>  |



 

<span data-ttu-id="d38bc-173">Beachten Sie, dass Dateien auch als komprimiert gekennzeichnet werden können, indem Sie die Eigenschaft " [**Zusammenfassung der Wort Zählung**](word-count-summary.md) " des [Zusammenfassungs Datenstroms](summary-information-stream.md)verwenden</span><span class="sxs-lookup"><span data-stu-id="d38bc-173">Note that files can also be marked as compressed using the [**Word Count Summary**](word-count-summary.md) Property of the [Summary Information stream](summary-information-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d38bc-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d38bc-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d38bc-175">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="d38bc-175">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




