---
title: Erstellen einer Skin-Definitionsdatei
description: Erstellen einer Skin-Definitionsdatei
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Windows Media Player Mobile Skins, Skin-Definitions Dateien
- Skins, Skin-Definitions Dateien
- Dateien für Skins, Skin-Definition
- Skin-Definitions Dateien, erstellen
- Erstellen von Skins, Informationen zu
- Erstellen von Skins, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711723"
---
# <a name="creating-a-skin-definition-file"></a><span data-ttu-id="9d372-109">Erstellen einer Skin-Definitionsdatei</span><span class="sxs-lookup"><span data-stu-id="9d372-109">Creating a Skin Definition File</span></span>

<span data-ttu-id="9d372-110">Eine Skin-Definitionsdatei ist eine Textdatei, die eine Skin und alle zusammengesetzten Teile definiert.</span><span class="sxs-lookup"><span data-stu-id="9d372-110">A skin definition file is a text file that defines a skin and all its composite parts.</span></span> <span data-ttu-id="9d372-111">Die Dateinamenerweiterung muss. SKN lauten.</span><span class="sxs-lookup"><span data-stu-id="9d372-111">The file name extension must be .skn.</span></span>

<span data-ttu-id="9d372-112">Jede Skin-Definitionsdatei muss mit der folgenden Zeile beginnen, in der die Versionsnummer der Skin-Datei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9d372-112">Every skin definition file must start with the following line, which specifies the skin file version number.</span></span> <span data-ttu-id="9d372-113">In der folgenden Tabelle werden die Windows Media Player-Versionen und die Codezeile angezeigt, die zur Identifizierung der einzelnen in einer Skin-Definitionsdatei verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9d372-113">The following table shows Windows Media Player versions and the code line that should be used to identify each in a skin definition file.</span></span> <span data-ttu-id="9d372-114">Obwohl einige der Zahlen in den Codezeilen nicht Ihren Erwartungen entsprechen, sind Sie richtig, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d372-114">Although some of the numbers in the code lines are not what you would expect, they are correct as shown in the following table.</span></span>



| <span data-ttu-id="9d372-115">Windows Media Player-Version</span><span class="sxs-lookup"><span data-stu-id="9d372-115">Windows Media Player version</span></span> | <span data-ttu-id="9d372-116">Erste Zeile der Skin-Definitionsdatei</span><span class="sxs-lookup"><span data-stu-id="9d372-116">First line of skin definition file</span></span> |
|------------------------------|------------------------------------|
| <span data-ttu-id="9d372-117">1.01.1</span><span class="sxs-lookup"><span data-stu-id="9d372-117">1.01.1</span></span><br/>            | <span data-ttu-id="9d372-118">\[Pocket WMP-Skin-Datei v 1.0\]</span><span class="sxs-lookup"><span data-stu-id="9d372-118">\[Pocket WMP Skin File v1.0\]</span></span>      |
| <span data-ttu-id="9d372-119">1.2</span><span class="sxs-lookup"><span data-stu-id="9d372-119">1.2</span></span>                          | <span data-ttu-id="9d372-120">\[Pocket WMP-Skin-Datei v 1.2\]</span><span class="sxs-lookup"><span data-stu-id="9d372-120">\[Pocket WMP Skin File v1.2\]</span></span>      |
| <span data-ttu-id="9d372-121">7.0</span><span class="sxs-lookup"><span data-stu-id="9d372-121">7.0</span></span>                          | <span data-ttu-id="9d372-122">\[Pocket WMP-Skin-Datei v 2.0\]</span><span class="sxs-lookup"><span data-stu-id="9d372-122">\[Pocket WMP Skin File v2.0\]</span></span>      |
| <span data-ttu-id="9d372-123">7.1</span><span class="sxs-lookup"><span data-stu-id="9d372-123">7.1</span></span>                          | <span data-ttu-id="9d372-124">\[Pocket WMP-Skin-Datei v 8.0\]</span><span class="sxs-lookup"><span data-stu-id="9d372-124">\[Pocket WMP Skin File v8.0\]</span></span>      |
| <span data-ttu-id="9d372-125">9-Serie</span><span class="sxs-lookup"><span data-stu-id="9d372-125">9 Series</span></span>                     | <span data-ttu-id="9d372-126">\[Pocket WMP-Skin-Datei v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="9d372-126">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="9d372-127">Windows 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="9d372-127">10 Mobile</span></span>                    | <span data-ttu-id="9d372-128">\[Pocket WMP-Skin-Datei v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="9d372-128">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="9d372-129">10,1 Mobile</span><span class="sxs-lookup"><span data-stu-id="9d372-129">10.1 Mobile</span></span>                  | <span data-ttu-id="9d372-130">\[Pocket WMP-Skin-Datei v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="9d372-130">\[Pocket WMP Skin File v9.0.1\]</span></span>    |



 

<span data-ttu-id="9d372-131">Die Versionsnummer 9.0.1 ist für Skins vorgesehen, die speziell für Windows Media Player 9-Serie oder höher erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9d372-131">The version number 9.0.1 is for skins created specifically for Windows Media Player 9 Series or later.</span></span> <span data-ttu-id="9d372-132">Skins mit einer früheren Versionsnummer werden von Windows Media Player 9 oder höher als Hochformat, 96 dpi-pro-Zoll-Skins (dpi) geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9d372-132">Skins having an earlier version number are opened by Windows Media Player 9 Series or later as portrait mode, 96 dots per inch (DPI) skins.</span></span>

<span data-ttu-id="9d372-133">Die Skin-Definitionsdatei besteht aus mehreren Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="9d372-133">The skin definition file consists of several sections.</span></span> <span data-ttu-id="9d372-134">Jeder Abschnitt definiert einen bestimmten Bereich der Skin.</span><span class="sxs-lookup"><span data-stu-id="9d372-134">Each section defines a particular area of the skin.</span></span> <span data-ttu-id="9d372-135">Die Abschnitte müssen in der folgenden Reihenfolge platziert werden:</span><span class="sxs-lookup"><span data-stu-id="9d372-135">The sections must be placed in the following order:</span></span>

1.  <span data-ttu-id="9d372-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d372-136">Description</span></span>
2.  <span data-ttu-id="9d372-137">Bitmaps</span><span class="sxs-lookup"><span data-stu-id="9d372-137">Bitmaps</span></span>
3.  <span data-ttu-id="9d372-138">Video</span><span class="sxs-lookup"><span data-stu-id="9d372-138">Video</span></span>
4.  <span data-ttu-id="9d372-139">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="9d372-139">Buttons</span></span>
5.  <span data-ttu-id="9d372-140">Status</span><span class="sxs-lookup"><span data-stu-id="9d372-140">Status</span></span>
6.  <span data-ttu-id="9d372-141">Text</span><span class="sxs-lookup"><span data-stu-id="9d372-141">Text</span></span>
7.  <span data-ttu-id="9d372-142">Marquee</span><span class="sxs-lookup"><span data-stu-id="9d372-142">Marquee</span></span>
8.  <span data-ttu-id="9d372-143">Trackbars</span><span class="sxs-lookup"><span data-stu-id="9d372-143">Trackbars</span></span>

<span data-ttu-id="9d372-144">Jeder Abschnitt beginnt mit dem Namen des Abschnitts in eckigen Klammern, z. b.:</span><span class="sxs-lookup"><span data-stu-id="9d372-144">Each section starts with the name of the section in square brackets, for example:</span></span>


```C++
[ Bitmaps ]

```



> [!Note]  
> <span data-ttu-id="9d372-145">Ihre Skin-Definitionsdatei wird nicht ordnungsgemäß analysiert, es sei denn, Sie fügen Leerzeichen zwischen den eckigen Klammern und dem Namen des Abschnitts ein.</span><span class="sxs-lookup"><span data-stu-id="9d372-145">Your skin definition file will not be parsed correctly unless you include spaces between the brackets and the name of the section.</span></span>

 

<span data-ttu-id="9d372-146">Anschließend werden in einer oder mehreren Zeilen einzelne Bilder, Schaltflächen usw. definiert.</span><span class="sxs-lookup"><span data-stu-id="9d372-146">Then, one or more lines define individual images, buttons, and so on.</span></span> <span data-ttu-id="9d372-147">Ein Bitmaps-Abschnitt könnte beispielsweise Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="9d372-147">For example, a Bitmaps section might include the following:</span></span>


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="9d372-148">Es ist nicht notwendig, die Werte in Spalten auszureihen, aber der Code wird leichter lesbar.</span><span class="sxs-lookup"><span data-stu-id="9d372-148">It is not necessary to line up the values in columns, but it will help your code to be more readable.</span></span> <span data-ttu-id="9d372-149">Weitere Informationen zu den einzelnen Abschnitten der Skin-Definitionsdatei finden Sie in der [Skin-Referenz](skin-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9d372-149">For more details about each section of the skin definition file, see the [Skin Reference](skin-reference.md).</span></span>

> [!Note]  
> <span data-ttu-id="9d372-150">Verwenden Sie Tabstopps nicht an einer beliebigen Stelle in der Datei. Verwenden Sie stattdessen zusätzliche Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="9d372-150">Do not use tabs anywhere in the file; use extra spaces instead.</span></span> <span data-ttu-id="9d372-151">Dies ist sehr wichtig, da das Drücken der Tab-Taste beim Schreiben oder Bearbeiten der Skin-Definitionsdatei dazu führt, dass die gesamte Skin ausfällt.</span><span class="sxs-lookup"><span data-stu-id="9d372-151">This is very important, because pressing the TAB key while writing or editing your skin definition file will cause the entire skin to fail.</span></span> <span data-ttu-id="9d372-152">Jede Zeile muss fertig sein und kann nicht auf eine zweite Zeile fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="9d372-152">Each line must be complete and cannot continue onto a second line.</span></span> <span data-ttu-id="9d372-153">Außerdem sind die Bereiche "Region" und "Super" für Skins veraltet, die mit Windows Media Player 10 Mobile oder höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d372-153">Also, the Region and Super values are deprecated for skins used with Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9d372-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d372-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d372-155">**Skin-Definitionsdatei**</span><span class="sxs-lookup"><span data-stu-id="9d372-155">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 





