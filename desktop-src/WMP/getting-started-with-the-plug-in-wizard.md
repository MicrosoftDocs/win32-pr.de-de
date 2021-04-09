---
title: Einstieg in den Plug-in-Assistenten
description: Einstieg in den Plug-in-Assistenten
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Windows Media Player-Plug-ins, Installieren des Plug-in-Assistenten
- Plug-ins, Installieren des Plug-in-Assistenten
- aufbauen von Plug-ins, Installieren des Plug-in-Assistenten
- Windows Media Player-Plug-in-Assistent, installieren
- Assistent zum Installieren von Plug-ins
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947924"
---
# <a name="getting-started-with-the-plug-in-wizard"></a><span data-ttu-id="62c9a-109">Einstieg in den Plug-in-Assistenten</span><span class="sxs-lookup"><span data-stu-id="62c9a-109">Getting Started with the Plug-in Wizard</span></span>

<span data-ttu-id="62c9a-110">Zum Einrichten der Entwicklungsumgebung für das Erstellen von Windows Media Player-Plug-Ins müssen Sie Folgendes installieren:</span><span class="sxs-lookup"><span data-stu-id="62c9a-110">To set up your development environment for creating Windows Media Player plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="62c9a-111">Microsoft Visual Studio .NET 2003 oder höher</span><span class="sxs-lookup"><span data-stu-id="62c9a-111">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="62c9a-112">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="62c9a-112">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="62c9a-113">Windows SDK, einschließlich des Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="62c9a-113">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="62c9a-114">Windows Media Player-Plug-in-Assistent</span><span class="sxs-lookup"><span data-stu-id="62c9a-114">Windows Media Player Plug-in Wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="62c9a-115">Installieren des Assistenten</span><span class="sxs-lookup"><span data-stu-id="62c9a-115">Installing the Wizard</span></span>

<span data-ttu-id="62c9a-116">Führen Sie die folgenden Schritte aus, um den Assistenten für Windows Media Player-Plug-in zu installieren.</span><span class="sxs-lookup"><span data-stu-id="62c9a-116">Perform the following steps to install the Windows Media Player Plug-in Wizard.</span></span>

1.  <span data-ttu-id="62c9a-117">Suchen Sie den Ordner, in dem Sie den Windows SDK installiert haben.</span><span class="sxs-lookup"><span data-stu-id="62c9a-117">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="62c9a-118">Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und navigieren Sie zu Samples \\ Multimedia \\ WMP- \\ Assistenten \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="62c9a-118">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span>
2.  <span data-ttu-id="62c9a-119">Suchen Sie die folgenden drei Dateien:</span><span class="sxs-lookup"><span data-stu-id="62c9a-119">Locate the following three files:</span></span>
    -   <span data-ttu-id="62c9a-120">wmpwiz. VSZ</span><span class="sxs-lookup"><span data-stu-id="62c9a-120">wmpwiz.vsz</span></span>
    -   <span data-ttu-id="62c9a-121">wmpwiz. vsdir</span><span class="sxs-lookup"><span data-stu-id="62c9a-121">wmpwiz.vsdir</span></span>
    -   <span data-ttu-id="62c9a-122">wmpwiz. ico</span><span class="sxs-lookup"><span data-stu-id="62c9a-122">wmpwiz.ico</span></span>
3.  <span data-ttu-id="62c9a-123">Bearbeiten Sie die Datei wmpwiz. vsz mithilfe eines Text-Editors, z. b. Notepad.</span><span class="sxs-lookup"><span data-stu-id="62c9a-123">Using a text editor, such as Notepad, edit the wmpwiz.vsz file.</span></span>

    <span data-ttu-id="62c9a-124">Suchen Sie die folgende Zeile:</span><span class="sxs-lookup"><span data-stu-id="62c9a-124">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="62c9a-125">Wechseln `<VsWizardEngine version goes here>` Sie abhängig von der installierten Version von Visual Studio zu einem der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="62c9a-125">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="62c9a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="62c9a-126">Value</span></span>              | <span data-ttu-id="62c9a-127">Visual Studio-Version</span><span class="sxs-lookup"><span data-stu-id="62c9a-127">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="62c9a-128">VsWizardEngine. 7.1</span><span class="sxs-lookup"><span data-stu-id="62c9a-128">VsWizardEngine.7.1</span></span> | <span data-ttu-id="62c9a-129">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="62c9a-129">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="62c9a-130">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="62c9a-130">VsWizardEngine.8.0</span></span> | <span data-ttu-id="62c9a-131">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="62c9a-131">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="62c9a-132">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="62c9a-132">VsWizardEngine.9.0</span></span> | <span data-ttu-id="62c9a-133">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="62c9a-133">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="62c9a-134">Suchen Sie die folgende Zeile:</span><span class="sxs-lookup"><span data-stu-id="62c9a-134">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    <span data-ttu-id="62c9a-135">Wechseln `<path to wmpwiz directory goes here>` Sie zu dem Pfad, in dem sich die Assistenten Dateien befinden.</span><span class="sxs-lookup"><span data-stu-id="62c9a-135">Change `<path to wmpwiz directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="62c9a-136">Nehmen Sie beispielsweise an, Sie haben Visual Studio 2008, und ihre Assistenten Dateien sind hier: C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WMP Wizard \\ \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="62c9a-136">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span> <span data-ttu-id="62c9a-137">Die Datei "wmpwiz. VSZ" würde dann wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="62c9a-137">Then your wmpwiz.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="62c9a-138">Suchen Sie den Ordner, in dem Sie Visual Studio installiert haben.</span><span class="sxs-lookup"><span data-stu-id="62c9a-138">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="62c9a-139">Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und suchen Sie einen Ordner mit dem Namen vcprojects.</span><span class="sxs-lookup"><span data-stu-id="62c9a-139">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="62c9a-140">Kopieren Sie die drei in Schritt 2 aufgeführten Dateien in den Ordner vcprojects.</span><span class="sxs-lookup"><span data-stu-id="62c9a-140">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="62c9a-141">Der Assistent ist jetzt installiert.</span><span class="sxs-lookup"><span data-stu-id="62c9a-141">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62c9a-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62c9a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62c9a-143">Aufbauen eines Plug-ins</span><span class="sxs-lookup"><span data-stu-id="62c9a-143">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> <dt>

[<span data-ttu-id="62c9a-144">Verwenden des Plug-in-Assistenten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="62c9a-144">Using the Plug-in Wizard with Visual Studio</span></span>](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




