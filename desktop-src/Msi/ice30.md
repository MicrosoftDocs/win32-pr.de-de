---
description: ICE30 überprüft, ob die Installation von Komponenten, die dieselbe Datei enthalten, die Datei nie mehrmals im gleichen Verzeichnis installiert.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360648"
---
# <a name="ice30"></a><span data-ttu-id="8ceac-103">ICE30</span><span class="sxs-lookup"><span data-stu-id="8ceac-103">ICE30</span></span>

<span data-ttu-id="8ceac-104">ICE30 überprüft, ob die Installation von Komponenten, die dieselbe Datei enthalten, die Datei nie mehrmals im gleichen Verzeichnis installiert.</span><span class="sxs-lookup"><span data-stu-id="8ceac-104">ICE30 validates that the installation of components containing the same file never installs the file more than once in the same directory.</span></span>

<span data-ttu-id="8ceac-105">ICE30 wechselt zu jeder Komponente in der [Komponenten Tabelle](component-table.md) und bestimmt dann das Zielverzeichnis der Komponente aus der [Verzeichnis Tabelle](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ceac-105">ICE30 goes to every component in the [Component table](component-table.md) and then determines the component's target directory from the [Directory table](directory-table.md).</span></span> <span data-ttu-id="8ceac-106">Anschließend wird überprüft, welche dieser Komponenten in demselben Zielverzeichnis installiert werden.</span><span class="sxs-lookup"><span data-stu-id="8ceac-106">It then checks to see which of these components install to the same target directory.</span></span> <span data-ttu-id="8ceac-107">Schließlich wird anhand der [Dateitabelle](file-table.md) überprüft, ob keine der Dateien in diesen Komponenten denselben Namen hat.</span><span class="sxs-lookup"><span data-stu-id="8ceac-107">Finally, it uses the [File table](file-table.md) to verify that none of the files in these components have the same name.</span></span>

<span data-ttu-id="8ceac-108">ICE30 prüft sowohl lange Dateinamen (LFN) als auch kurze Dateinamen (SFN).</span><span class="sxs-lookup"><span data-stu-id="8ceac-108">ICE30 checks both long file names (LFN) and short file names (SFN).</span></span>

<span data-ttu-id="8ceac-109">ICE30 wertet keine Eigenschaften in der Auflösung von Verzeichnissen aus, da sich diese Eigenschaften zur Laufzeit ändern und das Verzeichnis Auflösungs Schema ändern können.</span><span class="sxs-lookup"><span data-stu-id="8ceac-109">ICE30 does not evaluate properties in the resolution of directories because these properties can change at runtime and alter the directory resolution scheme.</span></span> <span data-ttu-id="8ceac-110">Dies bedeutet, dass ICE30 Datei Kollisionen aufgrund von Verzeichnissen mit derselben Eigenschaft in ihren Pfaden erkennen kann, jedoch keine Konflikte erkennt, die sich aus zwei Eigenschaften mit demselben Wert ergeben.</span><span class="sxs-lookup"><span data-stu-id="8ceac-110">This means ICE30 can detect file collisions due to directories with the same property in their paths, but does not detect collisions resulting from two properties having the same value.</span></span>

## <a name="result"></a><span data-ttu-id="8ceac-111">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="8ceac-111">Result</span></span>

<span data-ttu-id="8ceac-112">ICE30 gibt eine Fehlermeldung für jedes Paar von Komponenten aus, die dieselbe Datei im selben Verzeichnis installiert.</span><span class="sxs-lookup"><span data-stu-id="8ceac-112">ICE30 posts an error message for each pair of components that installs the same file to the same directory.</span></span>

## <a name="example"></a><span data-ttu-id="8ceac-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8ceac-113">Example</span></span>

<span data-ttu-id="8ceac-114">Im gezeigten Beispiel werden die folgenden Fehler zweimal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ceac-114">The example shown returns each of the following errors twice.</span></span>



| <span data-ttu-id="8ceac-115">ICE30-Fehler oder-Warnung</span><span class="sxs-lookup"><span data-stu-id="8ceac-115">ICE30 error or warning</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="8ceac-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ceac-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ceac-117">Fehler: die Zieldatei "Infodatei. 1st" wird \\ von zwei verschiedenen Komponenten auf einem SFN-System in "TARGETDIR Product" installiert: "Component1" und "Component2".</span><span class="sxs-lookup"><span data-stu-id="8ceac-117">ERROR: The target file 'README.1st' is installed in 'TARGETDIR\\PRODUCT' by two different components on an SFN system: 'Component1' and 'Component2'.</span></span> <span data-ttu-id="8ceac-118">Dadurch wird die Komponenten Verweis Zählung unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="8ceac-118">This breaks component reference counting.</span></span>                                                                                           | <span data-ttu-id="8ceac-119">Component1 und Component2 verfügen beide über eine Datei mit dem Namen "reademe. 1st".</span><span class="sxs-lookup"><span data-stu-id="8ceac-119">Component1 and Component2 both have a file named 'READEME.1st'.</span></span> <span data-ttu-id="8ceac-120">Wenn Sie kurze Dateinamen verwenden, installiert das Installationsprogramm sowohl dir1 als auch dir2 im gleichen Verzeichnis, TARGETDIR \\ Product.</span><span class="sxs-lookup"><span data-stu-id="8ceac-120">When using short file names, the installer installs both Dir1 and Dir2 to the same directory, TARGETDIR\\PRODUCT.</span></span><br/> <span data-ttu-id="8ceac-121">ICE30 generiert zwei Fehler, eine für jede Datei.</span><span class="sxs-lookup"><span data-stu-id="8ceac-121">ICE30 generate two errors, one for each file.</span></span> <span data-ttu-id="8ceac-122">In einer Erstellungs Umgebung, in der Fehlerspeicher Orte angezeigt werden, liegt der erste Fehler bei einem Datei Eintrag in der [Dateitabelle](file-table.md)und der zweite am Speicherort der anderen Datei.</span><span class="sxs-lookup"><span data-stu-id="8ceac-122">In an authoring environment that displays error locations, the first error is at one file's entry in the [File Table](file-table.md), and the second at the location of the other file.</span></span><br/> |
| <span data-ttu-id="8ceac-123">Fehler: die Installation einer conditionalized-Komponente würde bewirken, dass die Zieldatei "infome. 1st" in "TARGETDIR \\ Common Tools" von zwei verschiedenen Komponenten auf einem LFN-System installiert wird: "Component3" und "Component4".</span><span class="sxs-lookup"><span data-stu-id="8ceac-123">ERROR: Installation of a conditionalized component would cause the target file 'README.1st' to be installed in 'TARGETDIR\\COMMON TOOLS' by two different components on an LFN system: 'Component3' and 'Component4'.</span></span> <span data-ttu-id="8ceac-124">Dadurch wird die Anzahl der Komponenten Verweise nicht mehr berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="8ceac-124">This would break component reference counting.</span></span>                      | <span data-ttu-id="8ceac-125">Component4 verfügt über einen Eintrag in der Condition-Spalte der [Component-Tabelle](component-table.md) und Component3 nicht.</span><span class="sxs-lookup"><span data-stu-id="8ceac-125">Component4 has an entry in the Condition column of the [Component table](component-table.md) and Component3 does not.</span></span> <span data-ttu-id="8ceac-126">Wenn [**VersionNT**](versionnt.md) den Wert true aufweist, wird Component4 installiert, und es gibt einen Konflikt mit der Info. 1. wird immer von Component3 installiert.</span><span class="sxs-lookup"><span data-stu-id="8ceac-126">If [**VersionNT**](versionnt.md) is True, Component4 is installed, and there a collision with the Readme.1st always installed by Component3.</span></span><br/> <span data-ttu-id="8ceac-127">ICE30 generiert 4 Fehler, ein paar für SFN, eines für LFN.</span><span class="sxs-lookup"><span data-stu-id="8ceac-127">ICE30 generates 4 errors, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |
| <span data-ttu-id="8ceac-128">Warnung: die Zieldatei "Infodatei. 1st" kann in "TARGETDIR \\ Common Tools" durch zwei unterschiedliche conditionalisierte Komponenten auf einem SFN-System installiert werden: "Component4" und "Component5".</span><span class="sxs-lookup"><span data-stu-id="8ceac-128">WARNING: The target file 'README.1st' might be installed in 'TARGETDIR\\COMMON TOOLS' by two different conditionalized components on an SFN system: 'Component4' and 'Component5'.</span></span> <span data-ttu-id="8ceac-129">Wenn die Bedingungen sich nicht gegenseitig ausschließen, wird das Komponenten Verweis-System unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="8ceac-129">If the conditions are not mutually exclusive, this will break the component reference counting system.</span></span> | <span data-ttu-id="8ceac-130">Da "Component4" und "Component5" in der Spalte "Bedingung" der [Komponenten Tabelle](component-table.md) Einträge enthalten, tritt möglicherweise keine Datei Kollision auf.</span><span class="sxs-lookup"><span data-stu-id="8ceac-130">Because Component4 and Component5 both have entries in the Condition column of the [Component table](component-table.md) this file collision may not occur.</span></span> <span data-ttu-id="8ceac-131">ICE30 gibt nur dann eine Warnung aus, wenn die Bedingungen zum Zeitpunkt der Installation bestimmt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8ceac-131">ICE30 only posts a warning because the conditions must be determined at the time of the installation.</span></span><br/> <span data-ttu-id="8ceac-132">ICE30 generiert 4 Warnungen, ein paar für SFN, eines für LFN.</span><span class="sxs-lookup"><span data-stu-id="8ceac-132">ICE30 generates 4 warnings, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |



 

<span data-ttu-id="8ceac-133">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="8ceac-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="8ceac-134">Komponente</span><span class="sxs-lookup"><span data-stu-id="8ceac-134">Component</span></span>  | <span data-ttu-id="8ceac-135">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8ceac-135">Directory</span></span> | <span data-ttu-id="8ceac-136">Bedingung</span><span class="sxs-lookup"><span data-stu-id="8ceac-136">Condition</span></span> |
|------------|-----------|-----------|
| <span data-ttu-id="8ceac-137">Component1</span><span class="sxs-lookup"><span data-stu-id="8ceac-137">Component1</span></span> | <span data-ttu-id="8ceac-138">Dir1</span><span class="sxs-lookup"><span data-stu-id="8ceac-138">Dir1</span></span>      |           |
| <span data-ttu-id="8ceac-139">Component2</span><span class="sxs-lookup"><span data-stu-id="8ceac-139">Component2</span></span> | <span data-ttu-id="8ceac-140">Dir2</span><span class="sxs-lookup"><span data-stu-id="8ceac-140">Dir2</span></span>      |           |
| <span data-ttu-id="8ceac-141">Component3</span><span class="sxs-lookup"><span data-stu-id="8ceac-141">Component3</span></span> | <span data-ttu-id="8ceac-142">Dir3</span><span class="sxs-lookup"><span data-stu-id="8ceac-142">Dir3</span></span>      |           |
| <span data-ttu-id="8ceac-143">Component4</span><span class="sxs-lookup"><span data-stu-id="8ceac-143">Component4</span></span> | <span data-ttu-id="8ceac-144">Dir3</span><span class="sxs-lookup"><span data-stu-id="8ceac-144">Dir3</span></span>      | <span data-ttu-id="8ceac-145">VersionNT</span><span class="sxs-lookup"><span data-stu-id="8ceac-145">VersionNT</span></span> |
| <span data-ttu-id="8ceac-146">Component5</span><span class="sxs-lookup"><span data-stu-id="8ceac-146">Component5</span></span> | <span data-ttu-id="8ceac-147">Dir3</span><span class="sxs-lookup"><span data-stu-id="8ceac-147">Dir3</span></span>      | <span data-ttu-id="8ceac-148">Version9X</span><span class="sxs-lookup"><span data-stu-id="8ceac-148">Version9X</span></span> |



 

[<span data-ttu-id="8ceac-149">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="8ceac-149">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="8ceac-150">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8ceac-150">Directory</span></span> | <span data-ttu-id="8ceac-151">Übergeordnetes \_ Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8ceac-151">Parent\_Directory</span></span> | <span data-ttu-id="8ceac-152">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="8ceac-152">DefaultDir</span></span>                    |
|-----------|-------------------|-------------------------------|
| <span data-ttu-id="8ceac-153">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="8ceac-153">SOURCEDIR</span></span> |                   | <span data-ttu-id="8ceac-154">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="8ceac-154">TARGETDIR</span></span>                     |
| <span data-ttu-id="8ceac-155">Dir1</span><span class="sxs-lookup"><span data-stu-id="8ceac-155">Dir1</span></span>      | <span data-ttu-id="8ceac-156">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="8ceac-156">SOURCEDIR</span></span>         | <span data-ttu-id="8ceac-157">Product \| Component1 Product:.</span><span class="sxs-lookup"><span data-stu-id="8ceac-157">Product\|Component1 Product:.</span></span> |
| <span data-ttu-id="8ceac-158">Dir2</span><span class="sxs-lookup"><span data-stu-id="8ceac-158">Dir2</span></span>      | <span data-ttu-id="8ceac-159">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="8ceac-159">SOURCEDIR</span></span>         | <span data-ttu-id="8ceac-160">Produkt:.</span><span class="sxs-lookup"><span data-stu-id="8ceac-160">Product:.</span></span>                     |
| <span data-ttu-id="8ceac-161">Dir3</span><span class="sxs-lookup"><span data-stu-id="8ceac-161">Dir3</span></span>      | <span data-ttu-id="8ceac-162">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="8ceac-162">SOURCEDIR</span></span>         | <span data-ttu-id="8ceac-163">Gängige gängige \| Tools:</span><span class="sxs-lookup"><span data-stu-id="8ceac-163">Common\|Common Tools:</span></span>         |



 

<span data-ttu-id="8ceac-164">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="8ceac-164">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="8ceac-165">File</span><span class="sxs-lookup"><span data-stu-id="8ceac-165">File</span></span>  | <span data-ttu-id="8ceac-166">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="8ceac-166">Component\_</span></span> | <span data-ttu-id="8ceac-167">FileName</span><span class="sxs-lookup"><span data-stu-id="8ceac-167">FileName</span></span>   |
|-------|-------------|------------|
| <span data-ttu-id="8ceac-168">Datei1</span><span class="sxs-lookup"><span data-stu-id="8ceac-168">File1</span></span> | <span data-ttu-id="8ceac-169">Component1</span><span class="sxs-lookup"><span data-stu-id="8ceac-169">Component1</span></span>  | <span data-ttu-id="8ceac-170">Info. 1.</span><span class="sxs-lookup"><span data-stu-id="8ceac-170">README.1st</span></span> |
| <span data-ttu-id="8ceac-171">Datei2</span><span class="sxs-lookup"><span data-stu-id="8ceac-171">File2</span></span> | <span data-ttu-id="8ceac-172">Component2</span><span class="sxs-lookup"><span data-stu-id="8ceac-172">Component2</span></span>  | <span data-ttu-id="8ceac-173">Info. 1.</span><span class="sxs-lookup"><span data-stu-id="8ceac-173">README.1st</span></span> |
| <span data-ttu-id="8ceac-174">Datei3</span><span class="sxs-lookup"><span data-stu-id="8ceac-174">File3</span></span> | <span data-ttu-id="8ceac-175">Component3</span><span class="sxs-lookup"><span data-stu-id="8ceac-175">Component3</span></span>  | <span data-ttu-id="8ceac-176">Info. 1.</span><span class="sxs-lookup"><span data-stu-id="8ceac-176">README.1st</span></span> |
| <span data-ttu-id="8ceac-177">Datei4</span><span class="sxs-lookup"><span data-stu-id="8ceac-177">File4</span></span> | <span data-ttu-id="8ceac-178">Component4</span><span class="sxs-lookup"><span data-stu-id="8ceac-178">Component4</span></span>  | <span data-ttu-id="8ceac-179">Info. 1.</span><span class="sxs-lookup"><span data-stu-id="8ceac-179">README.1st</span></span> |
| <span data-ttu-id="8ceac-180">Datei5</span><span class="sxs-lookup"><span data-stu-id="8ceac-180">File5</span></span> | <span data-ttu-id="8ceac-181">Component5</span><span class="sxs-lookup"><span data-stu-id="8ceac-181">Component5</span></span>  | <span data-ttu-id="8ceac-182">Info. 1.</span><span class="sxs-lookup"><span data-stu-id="8ceac-182">README.1st</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8ceac-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8ceac-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ceac-184">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="8ceac-184">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




