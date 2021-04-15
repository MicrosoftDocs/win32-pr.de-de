---
title: Kompilieren von Menü Band Markup
description: Damit das Windows-Menüband-Framework die Menüband-Markup Datei verwendet, muss die Markup Datei in eine Ressourcen Datei im Binärformat kompiliert werden.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Windows-Menüband, Kompilieren von Markup
- Menüband, Kompilieren von Markup
- Windows-Multifunktionsleiste, compilerworkflow
- Multifunktionsleiste, compilerworkflow
- Windows-Menüband, UI-Befehls Compiler (UICC.exe)
- Multifunktionsleiste, UI-Befehls Compiler (UICC.exe)
- UI-Befehls Compiler (UICC.exe)
- UICC.exe (UI-Befehls Compiler)
- Kompilieren von Windows-Menü Band Markup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515950"
---
# <a name="compiling-ribbon-markup"></a><span data-ttu-id="9c655-112">Kompilieren von Menü Band Markup</span><span class="sxs-lookup"><span data-stu-id="9c655-112">Compiling Ribbon Markup</span></span>

<span data-ttu-id="9c655-113">Damit das Windows-Menüband-Framework die [Menüband-Markup](windowsribbon-schema.md) Datei verwendet, muss die Markup Datei in eine Ressourcen Datei im Binärformat kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="9c655-113">For the Windows Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="9c655-114">Ein dedizierter Markup Compiler, der UI-Befehls Compiler (UICC), ist zu diesem Zweck im Windows Software Development Kit (SDK) (7,0 oder höher) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c655-114">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="9c655-115">Zusätzlich zum Kompilieren der Binärversion des Markups generiert das UICC eine ID-Definitions Header Datei (. h), die alle Markup Elemente für die Menüband-Host Anwendung und eine Ressourcen Datei (. RC) verfügbar macht, mit der Bild-und Zeichen folgen Ressourcen zur Buildzeit mit der Host Anwendung verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="9c655-115">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

-   [<span data-ttu-id="9c655-116">Compilerworkflow</span><span class="sxs-lookup"><span data-stu-id="9c655-116">Compiler Workflow</span></span>](#compiler-workflow)
-   [<span data-ttu-id="9c655-117">Befehlszeilen Syntax</span><span class="sxs-lookup"><span data-stu-id="9c655-117">Command-Line Syntax</span></span>](#command-line-syntax)
    -   [<span data-ttu-id="9c655-118">Argumente und Optionen</span><span class="sxs-lookup"><span data-stu-id="9c655-118">Arguments and Options</span></span>](#arguments-and-options)
    -   [<span data-ttu-id="9c655-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9c655-119">Example</span></span>](#example)
-   [<span data-ttu-id="9c655-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c655-120">Related topics</span></span>](#related-topics)

## <a name="compiler-workflow"></a><span data-ttu-id="9c655-121">Compilerworkflow</span><span class="sxs-lookup"><span data-stu-id="9c655-121">Compiler Workflow</span></span>

<span data-ttu-id="9c655-122">Der Workflow des Menüband-Markup Compilers ist im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9c655-122">The workflow of the Ribbon markup compiler is illustrated in the following diagram.</span></span>

![Diagramm mit dem Workflow für den Menüband-Markup Compiler.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a><span data-ttu-id="9c655-124">Befehlszeilensyntax</span><span class="sxs-lookup"><span data-stu-id="9c655-124">Command-Line Syntax</span></span>

<span data-ttu-id="9c655-125">Das folgende Beispiel zeigt die Befehlszeilen Syntax für den Menüband-Markup Compiler.</span><span class="sxs-lookup"><span data-stu-id="9c655-125">The command-line syntax for the Ribbon markup compiler is shown in the following example.</span></span>


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a><span data-ttu-id="9c655-126">Argumente und Optionen</span><span class="sxs-lookup"><span data-stu-id="9c655-126">Arguments and Options</span></span>

<span data-ttu-id="9c655-127">Die Argumente und Optionen für dieses Tool werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9c655-127">The arguments and options for this tool are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="9c655-128">Die aufgelisteten Befehlszeilenoptionen müssen in der angegebenen Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9c655-128">The command-line options listed must be specified in the order given.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c655-129">Option</span><span class="sxs-lookup"><span data-stu-id="9c655-129">Option</span></span></th>
<th><span data-ttu-id="9c655-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c655-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c655-131">/Header<headerFile></span><span class="sxs-lookup"><span data-stu-id="9c655-131">/header:<headerFile></span></span></td>
<td><span data-ttu-id="9c655-132">Generieren Sie eine Header Datei mit <headerFile> dem Namen, die die Markup Befehls-ID-Ressourcen Symbole enthält.</span><span class="sxs-lookup"><span data-stu-id="9c655-132">Generate a header file called <headerFile> that contains the markup Command ID resource symbols.</span></span> <span data-ttu-id="9c655-133">Wenn der Wert nicht weggelassen wird, wird keine Header Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="9c655-133">If omitted, a header file is not generated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c655-134">/res<resourceFile></span><span class="sxs-lookup"><span data-stu-id="9c655-134">/res:<resourceFile></span></span></td>
<td><span data-ttu-id="9c655-135">Generieren Sie eine Ressourcen Datei <resourceFile> mit dem Namen, die alle Bild-und Zeichen folgen Ressourcen, die binäre Markup Datei und die Header Datei zur Buildzeit mit der Host Anwendung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9c655-135">Generate a resource file called <resourceFile> that links all image and string resources, the binary markup file, and the header file to the host application at build time.</span></span> <span data-ttu-id="9c655-136">Wenn der Wert nicht weggelassen wird, wird keine Ressourcen Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="9c655-136">If omitted, a resource file is not generated.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c655-137">/Name<ribbonName></span><span class="sxs-lookup"><span data-stu-id="9c655-137">/name:<ribbonName></span></span></td>
<td><span data-ttu-id="9c655-138">Der Ressourcen Name für die binäre Markup Datei, die in protokolliert wird <resourceFile> .</span><span class="sxs-lookup"><span data-stu-id="9c655-138">The resource name for the binary markup file that is logged in the <resourceFile>.</span></span> <span data-ttu-id="9c655-139">Der Standardwert ist APPLICATION_RIBBON.</span><span class="sxs-lookup"><span data-stu-id="9c655-139">The default is APPLICATION_RIBBON.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c655-140">/W{0\1\2}</span><span class="sxs-lookup"><span data-stu-id="9c655-140">/W{0\1\2}</span></span></td>
<td><span data-ttu-id="9c655-141">Filtern Sie die Ereignismeldungen basierend auf dem Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="9c655-141">Filter the event messages based on severity.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c655-142">0</span><span class="sxs-lookup"><span data-stu-id="9c655-142">0</span></span><br/></td>
<td><span data-ttu-id="9c655-143">Nur Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="9c655-143">Error messages only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c655-144">1</span><span class="sxs-lookup"><span data-stu-id="9c655-144">1</span></span><br/></td>
<td><span data-ttu-id="9c655-145">Nur Fehler-und Warnmeldungen.</span><span class="sxs-lookup"><span data-stu-id="9c655-145">Error and Warning messages only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c655-146"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="9c655-146"><strong>2</strong></span></span><br/></td>
<td><span data-ttu-id="9c655-147">Standard.</span><span class="sxs-lookup"><span data-stu-id="9c655-147">Default.</span></span> <br/> <span data-ttu-id="9c655-148">Fehler-, Warn-und Informationsmeldungen.</span><span class="sxs-lookup"><span data-stu-id="9c655-148">Error, Warning, and Informational messages.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a><span data-ttu-id="9c655-149">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9c655-149">Example</span></span>

<span data-ttu-id="9c655-150">Im folgenden Beispiel wird veranschaulicht, wie der multifunktionsleistenmarkup-Compiler verwendet wird, um einen typischen Satz von Ressourcen Dateien für eine Multifunktionsleistenanwendung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9c655-150">The following example demonstrates how to use the Ribbon markup compiler to generate a typical set of resource files for a Ribbon application.</span></span>

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a><span data-ttu-id="9c655-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c655-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c655-152">Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup</span><span class="sxs-lookup"><span data-stu-id="9c655-152">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="9c655-153">Erstellen einer Menü Bandanwendung</span><span class="sxs-lookup"><span data-stu-id="9c655-153">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





