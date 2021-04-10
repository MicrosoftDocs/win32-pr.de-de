---
description: Windows Installer Entwickler die Richtlinien in diesem Thema verwenden können, um Windows Installer Pakete zu erstellen, die Assemblys enthalten.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Hinzufügen von Assemblys zu Paketen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215727"
---
# <a name="adding-assemblies-to-a-package"></a><span data-ttu-id="b5711-103">Hinzufügen von Assemblys zu Paketen</span><span class="sxs-lookup"><span data-stu-id="b5711-103">Adding Assemblies to a Package</span></span>

<span data-ttu-id="b5711-104">Windows Installer Entwickler die Richtlinien in diesem Thema verwenden können, um Windows Installer Pakete zu erstellen, die Assemblys enthalten.</span><span class="sxs-lookup"><span data-stu-id="b5711-104">Windows Installer developers can use the guidelines in this topic to author Windows Installer packages that contain assemblies.</span></span>

<span data-ttu-id="b5711-105">Die folgenden Richtlinien gelten für Win32-Assemblys und Assemblys, die die Common Language Runtime des Microsoft .NET Frameworks verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5711-105">The following guidelines apply to Win32 assemblies, and assemblies that the common language runtime of the Microsoft .NET Framework uses.</span></span>

-   <span data-ttu-id="b5711-106">Eine Windows Installer Komponente sollte nicht mehr als eine Assembly enthalten.</span><span class="sxs-lookup"><span data-stu-id="b5711-106">A Windows Installer component should contain no more than one assembly.</span></span>
-   <span data-ttu-id="b5711-107">Alle Dateien in der Assembly sollten sich in einer einzelnen Komponente befinden.</span><span class="sxs-lookup"><span data-stu-id="b5711-107">All of the files in the assembly should be in a single component.</span></span>
-   <span data-ttu-id="b5711-108">Jede Komponente, die eine Assembly enthält, muss über einen Eintrag in der [MsiAssembly](msiassembly-table.md) -Tabelle verfügen.</span><span class="sxs-lookup"><span data-stu-id="b5711-108">Each component that contains an assembly should have an entry in the [MsiAssembly](msiassembly-table.md) table.</span></span>
-   <span data-ttu-id="b5711-109">Der Name der starken Assemblycaches der einzelnen Assemblys sollte in der [MsiAssemblyName](msiassemblyname-table.md) -Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5711-109">The strong assembly cache name of each assembly should be authored into the [MsiAssemblyName](msiassemblyname-table.md) table.</span></span>
-   <span data-ttu-id="b5711-110">Verwenden Sie die [Registrierungs](registry-table.md) Tabelle anstelle der [Klassen](class-table.md) Tabelle, wenn Sie COM-Interop für eine Assembly registrieren.</span><span class="sxs-lookup"><span data-stu-id="b5711-110">Use the [Registry](registry-table.md) table instead of the [Class](class-table.md) table when you register COM Interop for an assembly.</span></span>
-   <span data-ttu-id="b5711-111">Assemblys mit demselben starken Namen sind dieselbe Assembly.</span><span class="sxs-lookup"><span data-stu-id="b5711-111">Assemblies that have the same strong name are the same assembly.</span></span> <span data-ttu-id="b5711-112">Wenn dieselbe Assembly von verschiedenen Anwendungen installiert wird, sollten die Komponenten, die die Assembly enthalten, den gleichen Wert für die ComponentID in Ihren [Komponenten](component-table.md) Tabellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5711-112">When the same assembly is installed by different applications, the components that contain the assembly should use the same value for the ComponentId in their [Component](component-table.md) tables.</span></span>

> [!Note]  
> <span data-ttu-id="b5711-113">Produktankündigungen identifizieren Assemblys, die von verschiedenen Anwendungen installiert und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b5711-113">Product advertisements identify assemblies that can be installed and used by different applications.</span></span> <span data-ttu-id="b5711-114">Produktankündigungen identifizieren keine privaten Assemblys.</span><span class="sxs-lookup"><span data-stu-id="b5711-114">Product advertisements do not identify private assemblies.</span></span>

 

## <a name="adding-win32-assemblies"></a><span data-ttu-id="b5711-115">Win32-Assemblys</span><span class="sxs-lookup"><span data-stu-id="b5711-115">Adding Win32 Assemblies</span></span>

<span data-ttu-id="b5711-116">Beachten Sie beim Einschließen von Win32-Assemblys die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="b5711-116">Use the following guidelines when you include Win32 assemblies:</span></span>

-   <span data-ttu-id="b5711-117">Der KEYPATH-Wert in der [Komponenten](component-table.md) Tabelle für eine Komponente, die eine Win32-Assembly enthält, darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b5711-117">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly should not be Null.</span></span>
-   <span data-ttu-id="b5711-118">Der KEYPATH-Wert in der [Komponenten](component-table.md) Tabelle für eine Komponente, die eine Win32-Richtlinienassembly enthält, sollte die Manifest-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="b5711-118">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 policy assembly should be the manifest file.</span></span>
-   <span data-ttu-id="b5711-119">Der KEYPATH-Wert in der [Komponenten](component-table.md) Tabelle für eine Komponente, die eine Win32-Assembly enthält, bei der es sich nicht um eine Richtlinienassembly handelt, sollte nicht die Manifestressource oder die Katalog Datei sein</span><span class="sxs-lookup"><span data-stu-id="b5711-119">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly, that is not a policy assembly, should not be the manifest file or catalog file.</span></span> <span data-ttu-id="b5711-120">Dies sollte eine andere Datei in der Assembly sein.</span><span class="sxs-lookup"><span data-stu-id="b5711-120">It should be a different file in the assembly.</span></span>
-   <span data-ttu-id="b5711-121">Fügen Sie der [MsiAssemblyName](msiassemblyname-table.md) -Tabelle für jedes Name-Wert-Paar, das im Abschnitt " **assemblyIdentity" des Win32-Assemblymanifests** aufgeführt ist, eine Zeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5711-121">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each name and value pair that are listed in the **assemblyIdentity** section of the Win32 assembly's manifest.</span></span>

## <a name="adding-assemblies-used-with-the-net-framework"></a><span data-ttu-id="b5711-122">Hinzufügen von mit dem .NET Framework verwendeten Assemblys</span><span class="sxs-lookup"><span data-stu-id="b5711-122">Adding Assemblies used with the .NET Framework</span></span>

<span data-ttu-id="b5711-123">Verwenden Sie die folgenden Richtlinien, wenn Sie Assemblys einschließen, die die Common Language Runtime des .NET Framework verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5711-123">Use the following guidelines when you include assemblies that the common language runtime of the .NET Framework uses.</span></span>

-   <span data-ttu-id="b5711-124">Der KEYPATH-Wert in der [Komponenten](component-table.md) Tabelle für eine Komponente, die die Assembly enthält, darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b5711-124">The KeyPath value in the [Component](component-table.md) table for a component that contains the assembly should not be Null.</span></span>
-   <span data-ttu-id="b5711-125">Wenn Sie eine vom Common Language Runtime verwendete Assembly in den globalen Assemblycache installieren, muss der Wert in der Datei \_ Anwendungs Spalte der MsiAssembly-Tabelle den Wert NULL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b5711-125">When you install an assembly used by the common language runtime to the global assembly cache, the value in the File\_Application column of the MsiAssembly table must be Null.</span></span>
-   <span data-ttu-id="b5711-126">Fügen Sie der Tabelle [MsiAssemblyName](msiassemblyname-table.md) für jedes Attribut des starken Namens der Assembly eine Zeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5711-126">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each attribute of the assembly's strong name.</span></span> <span data-ttu-id="b5711-127">Alle Assemblys müssen über die Attribute Name, Version und Culture verfügen, die in der Tabelle MsiAssemblyName angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b5711-127">All assemblies must have the Name, Version, and Culture attributes that are specified in the MsiAssemblyName table.</span></span> <span data-ttu-id="b5711-128">Ein PublicKeyToken-Attribut ist für eine globale Assembly erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b5711-128">A publicKeyToken attribute is required for a global assembly.</span></span> <span data-ttu-id="b5711-129">Die folgende Tabelle ist ein Beispiel für die MsiAssemblyName-Tabelle für eine globale Assembly, die von der Common Language Runtime verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5711-129">The following table is an example of the MsiAssemblyName table for a global assembly for use by the common language runtime.</span></span>

[<span data-ttu-id="b5711-130">MsiAssemblyName-Tabelle</span><span class="sxs-lookup"><span data-stu-id="b5711-130">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)



| <span data-ttu-id="b5711-131">Komponente</span><span class="sxs-lookup"><span data-stu-id="b5711-131">Component</span></span>  | <span data-ttu-id="b5711-132">Name</span><span class="sxs-lookup"><span data-stu-id="b5711-132">Name</span></span>           | <span data-ttu-id="b5711-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b5711-133">Value</span></span>            |
|------------|----------------|------------------|
| <span data-ttu-id="b5711-134">Componenta</span><span class="sxs-lookup"><span data-stu-id="b5711-134">ComponentA</span></span> | <span data-ttu-id="b5711-135">Name</span><span class="sxs-lookup"><span data-stu-id="b5711-135">Name</span></span>           | <span data-ttu-id="b5711-136">Einfach</span><span class="sxs-lookup"><span data-stu-id="b5711-136">simple</span></span>           |
| <span data-ttu-id="b5711-137">Componenta</span><span class="sxs-lookup"><span data-stu-id="b5711-137">ComponentA</span></span> | <span data-ttu-id="b5711-138">version</span><span class="sxs-lookup"><span data-stu-id="b5711-138">version</span></span>        | <span data-ttu-id="b5711-139">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="b5711-139">1.0.0.0</span></span>          |
| <span data-ttu-id="b5711-140">Componenta</span><span class="sxs-lookup"><span data-stu-id="b5711-140">ComponentA</span></span> | <span data-ttu-id="b5711-141">Kultur</span><span class="sxs-lookup"><span data-stu-id="b5711-141">Culture</span></span>        | <span data-ttu-id="b5711-142">Neutral</span><span class="sxs-lookup"><span data-stu-id="b5711-142">neutral</span></span>          |
| <span data-ttu-id="b5711-143">Componenta</span><span class="sxs-lookup"><span data-stu-id="b5711-143">ComponentA</span></span> | <span data-ttu-id="b5711-144">PublicKeyToken</span><span class="sxs-lookup"><span data-stu-id="b5711-144">publicKeyToken</span></span> | <span data-ttu-id="b5711-145">9d1ec8380b483-Dienst</span><span class="sxs-lookup"><span data-stu-id="b5711-145">9d1ec8380f483f5a</span></span> |



 

 

 



