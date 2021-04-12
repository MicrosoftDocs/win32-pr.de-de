---
description: ICE19 überprüft, ob angekündigte Komponenten auf eine Datei in der KEYPATH-Spalte der Component-Tabelle verweisen und ob eine angekündigte Verknüpfung auf ein Verzeichnis in dieser Spalte verweist.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216745"
---
# <a name="ice19"></a><span data-ttu-id="a6adb-103">ICE19</span><span class="sxs-lookup"><span data-stu-id="a6adb-103">ICE19</span></span>

<span data-ttu-id="a6adb-104">ICE19 überprüft, ob angekündigte Komponenten auf eine Datei in der KEYPATH-Spalte der [Component-Tabelle](component-table.md) verweisen und ob eine angekündigte Verknüpfung auf ein Verzeichnis in dieser Spalte verweist.</span><span class="sxs-lookup"><span data-stu-id="a6adb-104">ICE19 validates that advertised components reference a file in the KeyPath column of the [Component table](component-table.md) and that an advertised shortcut references a directory in this column.</span></span>

<span data-ttu-id="a6adb-105">ICE19 überprüft, ob angekündigte Komponenten oder Verknüpfungen über eine ComponentID verfügen.</span><span class="sxs-lookup"><span data-stu-id="a6adb-105">ICE19 validates that advertised components or shortcuts have a ComponentId.</span></span> <span data-ttu-id="a6adb-106">Komponenten in der [PublishComponent-Tabelle](publishcomponent-table.md), die nicht in einer anderen Tabelle angekündigt werden, werden nur geprüft, um festzustellen, ob Sie über eine ComponentID verfügen.</span><span class="sxs-lookup"><span data-stu-id="a6adb-106">Components in the [PublishComponent table](publishcomponent-table.md), which are not advertised in another table, are only checked to see whether they have a ComponentId.</span></span>

## <a name="result"></a><span data-ttu-id="a6adb-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="a6adb-107">Result</span></span>

<span data-ttu-id="a6adb-108">ICE19 gibt eine Fehlermeldung aus, wenn die KEYPATH-Spalte der Component-Tabelle nicht auf eine Datei im Fall einer angekündigten Komponente oder eines Verzeichnisses im Fall einer angekündigten Verknüpfung verweist.</span><span class="sxs-lookup"><span data-stu-id="a6adb-108">ICE19 posts an error message if the KeyPath column of the Component table does not reference a file in the case of an advertised component or a directory in the case of an advertised shortcut.</span></span> <span data-ttu-id="a6adb-109">ICE19 gibt eine Fehlermeldung aus, wenn angekündigte Komponenten oder Verknüpfungen nicht über eine ComponentID verfügen.</span><span class="sxs-lookup"><span data-stu-id="a6adb-109">ICE19 posts an error message if any advertised components or shortcuts do not have a ComponentId.</span></span>

## <a name="example"></a><span data-ttu-id="a6adb-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a6adb-110">Example</span></span>

<span data-ttu-id="a6adb-111">ICE19 gibt die folgenden Fehlermeldungen für das gezeigte Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="a6adb-111">ICE19 posts the following error messages for the example shown:</span></span>

-   <span data-ttu-id="a6adb-112">Die Erweiterungs-FLP verweist auf die Komponente Comp1, die in der [Komponenten Tabelle](component-table.md)nicht über eine ComponentID verfügt.</span><span class="sxs-lookup"><span data-stu-id="a6adb-112">Extension flp references the component Comp1 which does not have a ComponentId specified in the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="a6adb-113">Die Erweiterungs-exe verweist auf die Komponente Comp4, die auf ein Verzeichnis als KEYPATH verweist.</span><span class="sxs-lookup"><span data-stu-id="a6adb-113">Extension exe references the component Comp4 which references a directory as its KeyPath.</span></span> <span data-ttu-id="a6adb-114">Der KEYPATH ist in der Komponenten Tabelle NULL.</span><span class="sxs-lookup"><span data-stu-id="a6adb-114">The KeyPath is Null in the Component table.</span></span>
-   <span data-ttu-id="a6adb-115">Verknüpfung Shortcut2 verweist auf die Komponente Comp3, die auf einen Registrierungs Eintrag als Schlüssel Pfad verweist.</span><span class="sxs-lookup"><span data-stu-id="a6adb-115">Shortcut Shortcut2 references the component Comp3 which references a Registry entry as the key path.</span></span> <span data-ttu-id="a6adb-116">Der Wert der Spalte Attribute in der Komponenten Tabelle ist 4.</span><span class="sxs-lookup"><span data-stu-id="a6adb-116">The value of the Attributes column in the Component table is 4.</span></span>

<span data-ttu-id="a6adb-117">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="a6adb-117">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="a6adb-118">Komponente</span><span class="sxs-lookup"><span data-stu-id="a6adb-118">Component</span></span> | <span data-ttu-id="a6adb-119">ComponentID</span><span class="sxs-lookup"><span data-stu-id="a6adb-119">ComponentId</span></span>                            | <span data-ttu-id="a6adb-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="a6adb-120">Attributes</span></span> | <span data-ttu-id="a6adb-121">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="a6adb-121">KeyPath</span></span> |
|-----------|----------------------------------------|------------|---------|
| <span data-ttu-id="a6adb-122">Comp1</span><span class="sxs-lookup"><span data-stu-id="a6adb-122">Comp1</span></span>     | <span data-ttu-id="a6adb-123">Null</span><span class="sxs-lookup"><span data-stu-id="a6adb-123">Null</span></span>                                   | <span data-ttu-id="a6adb-124">0</span><span class="sxs-lookup"><span data-stu-id="a6adb-124">0</span></span>          | <span data-ttu-id="a6adb-125">Datei1</span><span class="sxs-lookup"><span data-stu-id="a6adb-125">File1</span></span>   |
| <span data-ttu-id="a6adb-126">Comp2</span><span class="sxs-lookup"><span data-stu-id="a6adb-126">Comp2</span></span>     | {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="a6adb-127">0</span><span class="sxs-lookup"><span data-stu-id="a6adb-127">0</span></span>          | <span data-ttu-id="a6adb-128">Datei2</span><span class="sxs-lookup"><span data-stu-id="a6adb-128">File2</span></span>   |
| <span data-ttu-id="a6adb-129">Comp3</span><span class="sxs-lookup"><span data-stu-id="a6adb-129">Comp3</span></span>     | {00000003-0003-0000-0000-624474736554} | <span data-ttu-id="a6adb-130">4</span><span class="sxs-lookup"><span data-stu-id="a6adb-130">4</span></span>          | <span data-ttu-id="a6adb-131">Reg3</span><span class="sxs-lookup"><span data-stu-id="a6adb-131">Reg3</span></span>    |
| <span data-ttu-id="a6adb-132">Comp4</span><span class="sxs-lookup"><span data-stu-id="a6adb-132">Comp4</span></span>     | {00000004-0003-0000-0000-624474736554} | <span data-ttu-id="a6adb-133">0</span><span class="sxs-lookup"><span data-stu-id="a6adb-133">0</span></span>          | <span data-ttu-id="a6adb-134">Null</span><span class="sxs-lookup"><span data-stu-id="a6adb-134">Null</span></span>    |



 

<span data-ttu-id="a6adb-135">[Erweiterungs Tabelle](extension-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="a6adb-135">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="a6adb-136">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="a6adb-136">Extension</span></span> | <span data-ttu-id="a6adb-137">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="a6adb-137">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="a6adb-138">FLP</span><span class="sxs-lookup"><span data-stu-id="a6adb-138">flp</span></span>       | <span data-ttu-id="a6adb-139">Comp1</span><span class="sxs-lookup"><span data-stu-id="a6adb-139">Comp1</span></span>       |
| <span data-ttu-id="a6adb-140">TST</span><span class="sxs-lookup"><span data-stu-id="a6adb-140">tst</span></span>       | <span data-ttu-id="a6adb-141">Comp2</span><span class="sxs-lookup"><span data-stu-id="a6adb-141">Comp2</span></span>       |
| <span data-ttu-id="a6adb-142">exe</span><span class="sxs-lookup"><span data-stu-id="a6adb-142">exe</span></span>       | <span data-ttu-id="a6adb-143">Comp4</span><span class="sxs-lookup"><span data-stu-id="a6adb-143">Comp4</span></span>       |



 

<span data-ttu-id="a6adb-144">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="a6adb-144">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="a6adb-145">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="a6adb-145">Shortcut</span></span>  | <span data-ttu-id="a6adb-146">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="a6adb-146">Component\_</span></span> | <span data-ttu-id="a6adb-147">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="a6adb-147">Feature\_</span></span>      |
|-----------|-------------|----------------|
| <span data-ttu-id="a6adb-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="a6adb-148">Shortcut1</span></span> | <span data-ttu-id="a6adb-149">Comp4</span><span class="sxs-lookup"><span data-stu-id="a6adb-149">Comp4</span></span>       | <span data-ttu-id="a6adb-150">Productfeature</span><span class="sxs-lookup"><span data-stu-id="a6adb-150">ProductFeature</span></span> |
| <span data-ttu-id="a6adb-151">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="a6adb-151">Shortcut2</span></span> | <span data-ttu-id="a6adb-152">Comp3</span><span class="sxs-lookup"><span data-stu-id="a6adb-152">Comp3</span></span>       | <span data-ttu-id="a6adb-153">Productfeature</span><span class="sxs-lookup"><span data-stu-id="a6adb-153">ProductFeature</span></span> |



 

<span data-ttu-id="a6adb-154">[Funktions Tabelle](feature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="a6adb-154">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="a6adb-155">Funktion</span><span class="sxs-lookup"><span data-stu-id="a6adb-155">Feature</span></span>        |
|----------------|
| <span data-ttu-id="a6adb-156">Productfeature</span><span class="sxs-lookup"><span data-stu-id="a6adb-156">ProductFeature</span></span> |



 

> [!Note]  
> <span data-ttu-id="a6adb-157">Wenn die Erweiterungs-FLP und die exe-Datei beide auf dieselbe Komponente verweisen, muss die exe-oder der com-Server, die Sie öffnet, identisch sein.</span><span class="sxs-lookup"><span data-stu-id="a6adb-157">If the extension flp and exe both reference the same component, the EXE or COM server that opens them must be the same.</span></span> <span data-ttu-id="a6adb-158">Diese exe-Datei ist normalerweise der KEYPATH für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="a6adb-158">This EXE is normally the KeyPath for the Component.</span></span> <span data-ttu-id="a6adb-159">Für Office können das Erweiterungs Dokument und XLS nicht auf dieselbe Komponente verweisen, da dieselbe exe nicht beide Erweiterungen öffnet.</span><span class="sxs-lookup"><span data-stu-id="a6adb-159">For OFFICE, the extensions doc and xls cannot reference the same component because the same EXE does not open both extensions.</span></span> <span data-ttu-id="a6adb-160">Sie müssen winword.exe, um doc-Erweiterungen zu öffnen, und Sie benötigen excel.exe, um XLS-Erweiterungen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a6adb-160">You need winword.exe to open doc extensions and you need excel.exe to open xls extensions.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a6adb-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6adb-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6adb-162">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="a6adb-162">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



