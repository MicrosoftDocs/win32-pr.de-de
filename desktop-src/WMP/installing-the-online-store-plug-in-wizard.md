---
title: Installieren des Online Store-Plug-in-Assistenten
description: Installieren des Online Store-Plug-in-Assistenten
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 1 Online Stores, Plug-ins
- Windows Media Player Online Stores, Plug-in-Assistent
- Online Stores, Plug-in-Assistent
- Typ 1 Online Stores, Plug-in-Assistent
- Windows Media Player Online Stores, Assistent zum Installieren von Plug-ins
- Online Stores, Assistent zum Installieren von Plug-ins
- Typ 1 Online Stores, Assistent zum Installieren von Plug-ins
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 1 Online Stores
- Plug-ins, Installieren des Plug-in-Assistenten
- Plug-ins, Plug-in-Assistent
- Windows Media Player-Plug-ins, geben Sie 1 Online Stores ein.
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, Installieren des Plug-in-Assistenten
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Assistent zum Installieren von Plug-ins
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037077"
---
# <a name="installing-the-online-store-plug-in-wizard"></a><span data-ttu-id="dbe15-124">Installieren des Online Store-Plug-in-Assistenten</span><span class="sxs-lookup"><span data-stu-id="dbe15-124">Installing the Online Store Plug-in Wizard</span></span>

<span data-ttu-id="dbe15-125">Zum Einrichten der Entwicklungsumgebung für das Erstellen von 1-Online Store-Plug-Ins müssen Sie Folgendes installieren:</span><span class="sxs-lookup"><span data-stu-id="dbe15-125">To set up your development environment for creating type 1 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="dbe15-126">Microsoft Visual Studio 2005 oder höher</span><span class="sxs-lookup"><span data-stu-id="dbe15-126">Microsoft Visual Studio 2005 or later</span></span>
-   <span data-ttu-id="dbe15-127">Windows Media Player 11 oder höher</span><span class="sxs-lookup"><span data-stu-id="dbe15-127">Windows Media Player 11 or later</span></span>
-   <span data-ttu-id="dbe15-128">Windows SDK, einschließlich des Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="dbe15-128">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="dbe15-129">Plug-in-Assistent für Online Store</span><span class="sxs-lookup"><span data-stu-id="dbe15-129">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="dbe15-130">Installieren des Assistenten</span><span class="sxs-lookup"><span data-stu-id="dbe15-130">Installing the Wizard</span></span>

<span data-ttu-id="dbe15-131">Führen Sie die folgenden Schritte aus, um den Online-Store-Plug-in-Assistenten in Visual Studio zu installieren.</span><span class="sxs-lookup"><span data-stu-id="dbe15-131">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="dbe15-132">Suchen Sie den Ordner, in dem Sie den Windows SDK installiert haben.</span><span class="sxs-lookup"><span data-stu-id="dbe15-132">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="dbe15-133">Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und navigieren Sie zu Samples \\ Multimedia \\ WMP- \\ Assistenten \\ Dienste.</span><span class="sxs-lookup"><span data-stu-id="dbe15-133">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="dbe15-134">Suchen Sie die folgenden drei Dateien:</span><span class="sxs-lookup"><span data-stu-id="dbe15-134">Locate the following three files:</span></span>
    -   <span data-ttu-id="dbe15-135">wmpservices. VSZ</span><span class="sxs-lookup"><span data-stu-id="dbe15-135">wmpservices.vsz</span></span>
    -   <span data-ttu-id="dbe15-136">wmpservices. vsdir</span><span class="sxs-lookup"><span data-stu-id="dbe15-136">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="dbe15-137">wmpservices. ico</span><span class="sxs-lookup"><span data-stu-id="dbe15-137">wmpservices.ico</span></span>
3.  <span data-ttu-id="dbe15-138">Bearbeiten Sie die Datei wmpservices. vsz mithilfe eines Text-Editors, z. b. Notepad.</span><span class="sxs-lookup"><span data-stu-id="dbe15-138">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="dbe15-139">Suchen Sie die folgende Zeile:</span><span class="sxs-lookup"><span data-stu-id="dbe15-139">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="dbe15-140">Wechseln `<VsWizardEngine version goes here>` Sie abhängig von der installierten Version von Visual Studio zu einem der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="dbe15-140">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="dbe15-141">Wert</span><span class="sxs-lookup"><span data-stu-id="dbe15-141">Value</span></span>              | <span data-ttu-id="dbe15-142">Visual Studio-Version</span><span class="sxs-lookup"><span data-stu-id="dbe15-142">Visual Studio version</span></span> |
    |--------------------|-----------------------|
    | <span data-ttu-id="dbe15-143">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="dbe15-143">VsWizardEngine.8.0</span></span> | <span data-ttu-id="dbe15-144">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="dbe15-144">Visual Studio 2005</span></span>    |
    | <span data-ttu-id="dbe15-145">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="dbe15-145">VsWizardEngine.9.0</span></span> | <span data-ttu-id="dbe15-146">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="dbe15-146">Visual Studio 2008</span></span>    |

    

     

    <span data-ttu-id="dbe15-147">Suchen Sie die folgende Zeile:</span><span class="sxs-lookup"><span data-stu-id="dbe15-147">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="dbe15-148">Wechseln `<path to wmpservices directory goes here>` Sie zu dem Pfad, in dem sich die Assistenten Dateien befinden.</span><span class="sxs-lookup"><span data-stu-id="dbe15-148">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="dbe15-149">Nehmen Sie beispielsweise an, Sie verfügen über Visual Studio 2008, und ihre Assistenten Dateien finden Sie hier: C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WMP Wizard \\ \\ Services.</span><span class="sxs-lookup"><span data-stu-id="dbe15-149">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="dbe15-150">Die Datei "wmpservices. VSZ" würde dann wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="dbe15-150">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="dbe15-151">Suchen Sie den Ordner, in dem Sie Visual Studio installiert haben.</span><span class="sxs-lookup"><span data-stu-id="dbe15-151">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="dbe15-152">Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und suchen Sie einen Ordner mit dem Namen vcprojects.</span><span class="sxs-lookup"><span data-stu-id="dbe15-152">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="dbe15-153">Kopieren Sie die drei in Schritt 2 aufgeführten Dateien in den Ordner vcprojects.</span><span class="sxs-lookup"><span data-stu-id="dbe15-153">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="dbe15-154">Der Assistent ist jetzt installiert.</span><span class="sxs-lookup"><span data-stu-id="dbe15-154">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbe15-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dbe15-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbe15-156">Entwickeln des Plug-Ins für einen Typ-1-Online Shop</span><span class="sxs-lookup"><span data-stu-id="dbe15-156">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




