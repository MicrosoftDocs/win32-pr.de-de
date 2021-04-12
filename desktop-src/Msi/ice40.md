---
description: ICE40 führt verschiedene Überprüfungen durch.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131872"
---
# <a name="ice40"></a><span data-ttu-id="39d03-103">ICE40</span><span class="sxs-lookup"><span data-stu-id="39d03-103">ICE40</span></span>

<span data-ttu-id="39d03-104">ICE40 führt verschiedene Überprüfungen durch.</span><span class="sxs-lookup"><span data-stu-id="39d03-104">ICE40 does miscellaneous validation.</span></span>

## <a name="result"></a><span data-ttu-id="39d03-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="39d03-105">Result</span></span>

<span data-ttu-id="39d03-106">ICE40 gibt Warnungen zu folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="39d03-106">ICE40 posts warnings on the following:</span></span>

-   <span data-ttu-id="39d03-107">Die Eigenschaft " [**REINSTALLMODE**](reinstallmode.md) " wurde überschrieben.</span><span class="sxs-lookup"><span data-stu-id="39d03-107">The [**REINSTALLMODE**](reinstallmode.md) property has been overridden.</span></span>
-   <span data-ttu-id="39d03-108">Die [removeinifile-Tabelle](removeinifile-table.md) enthält einen DELETE-tageintrag ohne Wert.</span><span class="sxs-lookup"><span data-stu-id="39d03-108">The [RemoveIniFile table](removeinifile-table.md) has a Delete Tag entry with no value.</span></span>
-   <span data-ttu-id="39d03-109">In der MSI-Datei fehlt die [Fehler Tabelle](error-table.md) , und die [**Zusammenfassungs Eigenschaft der Seitenanzahl**](page-count-summary.md) ist kleiner oder gleich 100.</span><span class="sxs-lookup"><span data-stu-id="39d03-109">The .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <span data-ttu-id="39d03-110">Diese Ice-Warnung ist veraltet, da Windows Installer nicht erfordert, dass das Paket eine Fehler Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="39d03-110">This ICE warning is obsolete because Windows Installer does not require the package to have an Error table.</span></span> <span data-ttu-id="39d03-111">Fehlermeldungen können mit Msimsg.dll abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="39d03-111">Error messages can be retrieved using Msimsg.dll.</span></span>

## <a name="example"></a><span data-ttu-id="39d03-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="39d03-112">Example</span></span>

[<span data-ttu-id="39d03-113">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="39d03-113">Property Table</span></span>](property-table.md)



| <span data-ttu-id="39d03-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39d03-114">Property</span></span>                               | <span data-ttu-id="39d03-115">Wert</span><span class="sxs-lookup"><span data-stu-id="39d03-115">Value</span></span> |
|----------------------------------------|-------|
| [<span data-ttu-id="39d03-116">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="39d03-116">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="39d03-117">A</span><span class="sxs-lookup"><span data-stu-id="39d03-117">A</span></span>     |



 

[<span data-ttu-id="39d03-118">Removeinifile-Tabelle</span><span class="sxs-lookup"><span data-stu-id="39d03-118">RemoveIniFile Table</span></span>](removeinifile-table.md)



| <span data-ttu-id="39d03-119">Removeinifile</span><span class="sxs-lookup"><span data-stu-id="39d03-119">RemoveIniFile</span></span>                          | <span data-ttu-id="39d03-120">Aktion</span><span class="sxs-lookup"><span data-stu-id="39d03-120">Action</span></span> | <span data-ttu-id="39d03-121">Wert</span><span class="sxs-lookup"><span data-stu-id="39d03-121">Value</span></span> |
|----------------------------------------|--------|-------|
| [<span data-ttu-id="39d03-122">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="39d03-122">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="39d03-123">4</span><span class="sxs-lookup"><span data-stu-id="39d03-123">4</span></span>      |       |



 

## <a name="results"></a><span data-ttu-id="39d03-124">Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="39d03-124">Results</span></span>

<span data-ttu-id="39d03-125">ICE40 würde die folgenden Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="39d03-125">ICE40 would report the following errors.</span></span>



| <span data-ttu-id="39d03-126">ICE40-Fehler</span><span class="sxs-lookup"><span data-stu-id="39d03-126">ICE40 error</span></span>                                                                                           | <span data-ttu-id="39d03-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39d03-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d03-128">[**REINSTALLMODE**](reinstallmode.md) ist in der Eigenschaften Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="39d03-128">[**REINSTALLMODE**](reinstallmode.md) is defined in the Property table.</span></span> <span data-ttu-id="39d03-129">Dies kann zu Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="39d03-129">This may cause difficulties.</span></span> | <span data-ttu-id="39d03-130">Das Definieren der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft in der MSI-Datei kann zu unerwartetem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="39d03-130">Defining the [**REINSTALLMODE**](reinstallmode.md) property in .msi file can lead to unexpected behavior.</span></span> <span data-ttu-id="39d03-131">Legen Sie diese Eigenschaft nicht fest, um diesen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="39d03-131">To fix this error, do not define this property.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="39d03-132">Der removeinifile-Eintrag Remove1 muss über einen Wert verfügen, da die Aktion "Delete Tag" (4) ist.</span><span class="sxs-lookup"><span data-stu-id="39d03-132">RemoveIniFile entry Remove1 must have a value, because the Action is "Delete Tag" (4).</span></span>                | <span data-ttu-id="39d03-133">In der removeinifile-Spalte der [removeinifile-Tabelle](removeinifile-table.md) ist eine DELETE-tagaktion vorhanden, ohne dass ein zu löschende Tag in der Spalte Wert angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="39d03-133">There is a Delete Tag action in the in the RemoveIniFile column of the [RemoveIniFile table](removeinifile-table.md) without specifying a tag to delete in the Value column.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="39d03-134">Fehler Tabelle fehlt.</span><span class="sxs-lookup"><span data-stu-id="39d03-134">Error Table is missing.</span></span> <span data-ttu-id="39d03-135">Nur numerische Fehlermeldungen werden generiert.</span><span class="sxs-lookup"><span data-stu-id="39d03-135">Only numerical error messages will be generated.</span></span>                              | <span data-ttu-id="39d03-136">Diese Ice-Warnung ist veraltet, da Windows Installer nicht erfordert, dass das Paket eine [Fehler Tabelle](error-table.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="39d03-136">This ICE warning is obsolete because Windows Installer does not require the package to have an [Error table](error-table.md).</span></span> <span data-ttu-id="39d03-137">Fehlermeldungen können mit Msimsg.dll abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="39d03-137">Error messages can be retrieved using Msimsg.dll.</span></span><br/> <span data-ttu-id="39d03-138">Diese Warnung bedeutet, dass in der MSI-Datei die [Fehler Tabelle](error-table.md) fehlt und die [**Zusammenfassungs Eigenschaft der Seitenanzahl**](page-count-summary.md) kleiner oder gleich 100 ist.</span><span class="sxs-lookup"><span data-stu-id="39d03-138">This warning means that the .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <br/> <span data-ttu-id="39d03-139">Um diesen Fehler zu beheben, verwenden Sie eine aktuelle Version der Windows Installer, oder fügen Sie dem Installationspaket eine Fehler Tabelle hinzu, und erstellen Sie Formatierungs Vorlagen in der Meldungs Spalte für Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="39d03-139">To fix this error, use a current version of the Windows Installer, or add an Error table to the installation package and author formatting templates in the Message column for error messages.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="39d03-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39d03-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39d03-141">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="39d03-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




