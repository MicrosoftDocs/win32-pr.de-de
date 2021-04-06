---
title: Installieren des Projekt-Assistenten
description: Installieren des Projekt-Assistenten
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 2 Online Stores, Plug-ins
- Windows Media Player Online Stores, Plug-in-Assistent
- Online Stores, Plug-in-Assistent
- Typ 2 Online Stores, Plug-in-Assistent
- Windows Media Player Online Stores, Projekt-Assistent
- Online Stores, Projekt-Assistent
- Typ 2 Online Stores, Projekt-Assistent
- Windows Media Player Online Stores, Assistent zum Installieren von Plug-ins
- Online Stores, Assistent zum Installieren von Plug-ins
- Typ 2 Online Stores, Assistent zum Installieren von Plug-ins
- Windows Media Player Online Stores, Assistent zum Installieren von Projekten
- Online Stores, Assistent zum Installieren von Projekten
- Typ 2 Online Stores, Assistent zum Installieren von Projekten
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 2 Online Stores
- Plug-ins, Installieren des Plug-in-Assistenten
- Plug-ins, Plug-in-Assistent
- Plug-ins, Assistent zum Installieren von Projekten
- Plug-ins, Projekt-Assistent
- Windows Media Player-Plug-ins, Typ 2 Online Stores
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, Installieren des Plug-in-Assistenten
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Windows Media Player-Plug-ins, Assistent zum Installieren von Projekten
- Windows Media Player-Plug-ins, Projekt-Assistent
- Assistent zum Installieren von Plug-ins
- Plug-in-Assistent
- Assistent zum Installieren von Projekten
- Projekt-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711988"
---
# <a name="installing-the-project-wizard"></a><span data-ttu-id="0f51a-136">Installieren des Projekt-Assistenten</span><span class="sxs-lookup"><span data-stu-id="0f51a-136">Installing the Project Wizard</span></span>

<span data-ttu-id="0f51a-137">Zum Einrichten der Entwicklungsumgebung für das Erstellen von Type 2 Online Store-Plug-Ins müssen Sie Folgendes installieren:</span><span class="sxs-lookup"><span data-stu-id="0f51a-137">To set up your development environment for creating type 2 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="0f51a-138">Microsoft Visual Studio .NET 2003 oder höher</span><span class="sxs-lookup"><span data-stu-id="0f51a-138">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="0f51a-139">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0f51a-139">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="0f51a-140">Windows SDK, einschließlich des Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="0f51a-140">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="0f51a-141">Plug-in-Assistent für Online Store</span><span class="sxs-lookup"><span data-stu-id="0f51a-141">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="0f51a-142">Installieren des Assistenten</span><span class="sxs-lookup"><span data-stu-id="0f51a-142">Installing the Wizard</span></span>

<span data-ttu-id="0f51a-143">Führen Sie die folgenden Schritte aus, um den Online-Store-Plug-in-Assistenten in Visual Studio zu installieren.</span><span class="sxs-lookup"><span data-stu-id="0f51a-143">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="0f51a-144">Suchen Sie den Ordner, in dem Sie den Windows SDK installiert haben.</span><span class="sxs-lookup"><span data-stu-id="0f51a-144">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="0f51a-145">Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und navigieren Sie zu Samples \\ Multimedia \\ WMP- \\ Assistenten \\ Dienste.</span><span class="sxs-lookup"><span data-stu-id="0f51a-145">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="0f51a-146">Suchen Sie die folgenden drei Dateien:</span><span class="sxs-lookup"><span data-stu-id="0f51a-146">Locate the following three files:</span></span>
    -   <span data-ttu-id="0f51a-147">wmpservices. VSZ</span><span class="sxs-lookup"><span data-stu-id="0f51a-147">wmpservices.vsz</span></span>
    -   <span data-ttu-id="0f51a-148">wmpservices. vsdir</span><span class="sxs-lookup"><span data-stu-id="0f51a-148">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="0f51a-149">wmpservices. ico</span><span class="sxs-lookup"><span data-stu-id="0f51a-149">wmpservices.ico</span></span>
3.  <span data-ttu-id="0f51a-150">Bearbeiten Sie die Datei wmpservices. vsz mithilfe eines Text-Editors, z. b. Notepad.</span><span class="sxs-lookup"><span data-stu-id="0f51a-150">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="0f51a-151">Suchen Sie die folgende Zeile:</span><span class="sxs-lookup"><span data-stu-id="0f51a-151">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="0f51a-152">Wechseln `<VsWizardEngine version goes here>` Sie abhängig von der installierten Version von Visual Studio zu einem der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="0f51a-152">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="0f51a-153">Wert</span><span class="sxs-lookup"><span data-stu-id="0f51a-153">Value</span></span>              | <span data-ttu-id="0f51a-154">Visual Studio-Version</span><span class="sxs-lookup"><span data-stu-id="0f51a-154">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="0f51a-155">VsWizardEngine. 7.1</span><span class="sxs-lookup"><span data-stu-id="0f51a-155">VsWizardEngine.7.1</span></span> | <span data-ttu-id="0f51a-156">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="0f51a-156">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="0f51a-157">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="0f51a-157">VsWizardEngine.8.0</span></span> | <span data-ttu-id="0f51a-158">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="0f51a-158">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="0f51a-159">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="0f51a-159">VsWizardEngine.9.0</span></span> | <span data-ttu-id="0f51a-160">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="0f51a-160">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="0f51a-161">Suchen Sie die folgende Zeile:</span><span class="sxs-lookup"><span data-stu-id="0f51a-161">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="0f51a-162">Wechseln `<path to wmpservices directory goes here>` Sie zu dem Pfad, in dem sich die Assistenten Dateien befinden.</span><span class="sxs-lookup"><span data-stu-id="0f51a-162">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="0f51a-163">Nehmen Sie beispielsweise an, Sie verfügen über Visual Studio 2008, und ihre Assistenten Dateien finden Sie hier: C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WMP Wizard \\ \\ Services.</span><span class="sxs-lookup"><span data-stu-id="0f51a-163">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="0f51a-164">Die Datei "wmpservices. VSZ" würde dann wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="0f51a-164">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="0f51a-165">Suchen Sie den Ordner, in dem Sie Visual Studio installiert haben.</span><span class="sxs-lookup"><span data-stu-id="0f51a-165">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="0f51a-166">Erweitern Sie den Ordner, um die Unterordner anzuzeigen, und suchen Sie einen Ordner mit dem Namen vcprojects.</span><span class="sxs-lookup"><span data-stu-id="0f51a-166">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="0f51a-167">Kopieren Sie die drei in Schritt 2 aufgeführten Dateien in den Ordner vcprojects.</span><span class="sxs-lookup"><span data-stu-id="0f51a-167">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="0f51a-168">Der Assistent ist jetzt installiert.</span><span class="sxs-lookup"><span data-stu-id="0f51a-168">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f51a-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f51a-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f51a-170">**Entwickeln des Plug-Ins für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="0f51a-170">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




