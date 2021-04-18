---
title: Verwenden des Online Store-Plug-in-Assistenten mit Visual Studio
description: Verwenden des Online Store-Plug-in-Assistenten mit Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 1 Online Stores, Plug-ins
- Windows Media Player Online Stores, Plug-in-Assistent
- Online Stores, Plug-in-Assistent
- Typ 1 Online Stores, Plug-in-Assistent
- Windows Media Player Online Stores, Visual Studio
- Online Stores, Visual Studio
- Typ 1 Online Stores, Visual Studio
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 1 Online Stores
- Plug-ins, Visual Studio
- Plug-ins, Plug-in-Assistent
- Windows Media Player-Plug-ins, geben Sie 1 Online Stores ein.
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, Visual Studio
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Visual Studio, Windows Media Player Online Stores-Assistent
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337557"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="3f485-124">Verwenden des Online Store-Plug-in-Assistenten mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3f485-124">Using the Online Store Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="3f485-125">Nachdem Sie die erforderlichen Komponenten installiert haben, können Sie schnell ein Plug-in erstellen, das als Ausgangspunkt fungiert.</span><span class="sxs-lookup"><span data-stu-id="3f485-125">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="3f485-126">Die folgenden Schritte führen Sie durch:</span><span class="sxs-lookup"><span data-stu-id="3f485-126">The following steps will guide you:</span></span>

1.  <span data-ttu-id="3f485-127">Starten Sie Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3f485-127">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="3f485-128">Zeigen Sie im Menü **Datei** auf **neu** , und klicken Sie dann auf **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="3f485-128">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="3f485-129">Klicken Sie unter **Projekttypen** auf **Visual C++ Projekte**.</span><span class="sxs-lookup"><span data-stu-id="3f485-129">In **Project Types**, click **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="3f485-130">Klicken Sie unter **Vorlagen** auf **Windows Media Player Online Stores Wizard**.</span><span class="sxs-lookup"><span data-stu-id="3f485-130">In **Templates**, click **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="3f485-131">Geben Sie einen Namen für das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="3f485-131">Enter a name for your project.</span></span>
6.  <span data-ttu-id="3f485-132">Geben Sie einen Speicherort für das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="3f485-132">Enter a location for your project.</span></span> <span data-ttu-id="3f485-133">Dies ist der Ordner, in den die Projektdateien kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="3f485-133">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="3f485-134">Klicken Sie auf **OK** , um den Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="3f485-134">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="3f485-135">Wählen Sie **Typ 1 (Deep Integration)** aus, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3f485-135">Select **Type 1 (Deep integration)**, and click **Next**.</span></span>
9.  <span data-ttu-id="3f485-136">Geben Sie einen anzeigen Amen und einen Inhalts Verteiler ein.</span><span class="sxs-lookup"><span data-stu-id="3f485-136">Enter a friendly name and a content distributor.</span></span> <span data-ttu-id="3f485-137">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="3f485-137">Click **Finish**.</span></span>
10. <span data-ttu-id="3f485-138">Verwenden Sie die Visual Studio-Entwicklungsumgebung, um Ihr Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3f485-138">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="3f485-139">In Windows Vista und höher wird das Projekt nicht erfolgreich erstellt, es sei denn, Sie führen Visual Studio mit einem vollen Administrator Zugriffs Token aus.</span><span class="sxs-lookup"><span data-stu-id="3f485-139">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="3f485-140">Klicken Sie mit der rechten Maustaste auf den Namen oder das Symbol von Visual Studio, und klicken Sie auf **als Administrator ausführen**</span><span class="sxs-lookup"><span data-stu-id="3f485-140">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="3f485-141">Bevor Sie versuchen, das Projekt zu erstellen, stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung so konfigurieren, dass Sie auf die Ordner include und lib verweist, in denen Sie die Windows SDK installiert haben.</span><span class="sxs-lookup"><span data-stu-id="3f485-141">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="3f485-142">Der Compiler und Linker benötigen Zugriff auf einige der Dateien in diesen Ordnern.</span><span class="sxs-lookup"><span data-stu-id="3f485-142">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="3f485-143">Wenn Sie das Visual Studio-Registrierungs Dienstprogramm ausgeführt haben, das in der Windows SDK enthalten ist, wurde die Entwicklungsumgebung wahrscheinlich bereits so konfiguriert, dass Sie auf die Ordner Windows SDK include und lib verweist.</span><span class="sxs-lookup"><span data-stu-id="3f485-143">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="3f485-144">Andernfalls müssen Sie Ihre Entwicklungsumgebung manuell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3f485-144">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="3f485-145">Führen Sie die folgenden Schritte aus, um Visual Studio manuell zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3f485-145">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="3f485-146">Klicken Sie **im Menü Extras** auf Optionen.</span><span class="sxs-lookup"><span data-stu-id="3f485-146">On the **Tools** menu, click Options.</span></span>
2.  <span data-ttu-id="3f485-147">Klicken Sie auf **Projekte und Projekt** Mappen und dann auf **VC + +-Verzeichnisse**.</span><span class="sxs-lookup"><span data-stu-id="3f485-147">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="3f485-148">Klicken Sie unter **Verzeichnisse anzeigen für** auf Dateien oder **Bibliotheksdateien** **einschließen** .</span><span class="sxs-lookup"><span data-stu-id="3f485-148">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="3f485-149">Fügen Sie die Verzeichnisse für die erforderlichen Dateien hinzu.</span><span class="sxs-lookup"><span data-stu-id="3f485-149">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f485-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f485-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f485-151">Entwickeln des Plug-Ins für einen Typ-1-Online Shop</span><span class="sxs-lookup"><span data-stu-id="3f485-151">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




