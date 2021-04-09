---
title: Einbetten des Windows Media Player-Steuer Elements in ein benutzerdefiniertes Programm
description: Einbetten des Windows Media Player-Steuer Elements in ein benutzerdefiniertes Programm
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- einbetten, benutzerdefinierte Programme
- benutzerdefiniertes programmieren
- einbetten, Visual Basic basierte Programme
- Visual Basic basierte Programm Einbettung
- einbetten, Manuelles Verwenden von com-Methoden
- manuelle Einbettung mithilfe von com-Methoden
- einbetten, C++-Programme
- C++-Programm Einbettung
- einbetten, Visual Studio-Programme
- Visual Studio, Programm Einbettung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036738"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a><span data-ttu-id="40c88-120">Einbetten des Windows Media Player-Steuer Elements in ein benutzerdefiniertes Programm</span><span class="sxs-lookup"><span data-stu-id="40c88-120">Embedding the Windows Media Player Control in a Custom Program</span></span>

<span data-ttu-id="40c88-121">Da das Windows Media Player ActiveX-Steuerelement auf der com-Technologie (Microsoft Component Object Model) basiert, können Sie es in Programme einbetten, die mit vielen verschiedenen Programmiersprachen geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="40c88-121">Because the Windows Media Player ActiveX control is based on Microsoft Component Object Model (COM) technology, you can embed it in programs written with many different programming languages.</span></span> <span data-ttu-id="40c88-122">Das Windows Media Player-Steuerelement stellt eine einfache Möglichkeit dar, einem beliebigen Programm ausgereifte Funktionen für digitale Medien hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="40c88-122">The Windows Media Player control represents an easy way to add sophisticated digital media functionality to any program.</span></span>

<span data-ttu-id="40c88-123">In Microsoft Visual Basic können Sie das Steuerelement der Toolbox für Steuerelemente hinzufügen, es auf einem Formular platzieren und die Steuerelement Eigenschaften im Eigenschaften Fenster anpassen.</span><span class="sxs-lookup"><span data-stu-id="40c88-123">In Microsoft Visual Basic, you can add the control to the control toolbox, place it on a form, and adjust the control properties in the properties window.</span></span> <span data-ttu-id="40c88-124">Wenn Sie eine benutzerdefinierte Benutzeroberfläche erstellen möchten, können Sie Befehls Schaltflächen im Formular platzieren und Code hinzufügen, der das Windows Media Player-Steuerelement verwaltet.</span><span class="sxs-lookup"><span data-stu-id="40c88-124">If you want a custom user interface, you can place command buttons on the form and add code that manages the Windows Media Player control.</span></span> <span data-ttu-id="40c88-125">Das Einbetten des Steuer Elements in ein Visual Basic basiertes Programm ähnelt dem Einbetten in ein Office-Dokument und dem Programmieren mit VBA.</span><span class="sxs-lookup"><span data-stu-id="40c88-125">Embedding the control in a Visual Basic-based program is very similar to embedding it in an Office document and programming it with VBA.</span></span>

<span data-ttu-id="40c88-126">Alternativ können Sie das Steuerelement manuell mithilfe von com-Methoden einbetten, um das Steuerelement zu instanziieren und auf die COM-Schnittstellen zuzugreifen, die in der [Objektmodell Referenz für C++](object-model-reference-for-c.md)</span><span class="sxs-lookup"><span data-stu-id="40c88-126">Alternately, you can embed the control manually using COM methods to instantiate the control and access the COM interfaces documented in [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

<span data-ttu-id="40c88-127">Wenn Sie das Windows Media Player-Steuerelement in ein C++-Programm einbetten, haben Sie die Möglichkeit, COM-Schnittstellen zu implementieren, mit denen das Steuerelement im Remote Modus ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="40c88-127">When you embed the Windows Media Player control in a C++ program, you have the option of implementing COM interfaces that allow the control to run in remote mode.</span></span> <span data-ttu-id="40c88-128">Dies bedeutet, dass das eingebettete Steuerelement dieselbe Wiedergabe-Engine wie der vollständige Modus des Players nutzt und dass Benutzer zwischen dem vollständigen und dem angedockten Zustand hin-und herwechseln können, ohne die Wiedergabe digitaler Medien zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="40c88-128">This means that the embedded control shares the same playback engine as the full mode of the Player, and users can switch back and forth between the full mode and the docked state without interrupting digital media playback.</span></span> <span data-ttu-id="40c88-129">Sie können auch steuern, was in den verschiedenen Bereichen des vollmodusplayers angezeigt wird, wenn die Benutzer in den nicht angedockten Zustand wechseln.</span><span class="sxs-lookup"><span data-stu-id="40c88-129">You can also control what is displayed in the various panes of the full mode Player when your users switch to the undocked state.</span></span>

<span data-ttu-id="40c88-130">Mit C++ Einbettungen haben Sie auch die Möglichkeit, eine Skin-Definitionsdatei auf das eingebettete Player-Steuerelement anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="40c88-130">With C++ embedding, you also have the option of applying a skin definition file to the embedded Player control.</span></span> <span data-ttu-id="40c88-131">Dies ist eine einfache Möglichkeit zum Erstellen von einfachem Benutzeroberflächen Code, den Sie separat von Ihrem Hauptprogramm Code verwalten können.</span><span class="sxs-lookup"><span data-stu-id="40c88-131">This is an easy way to create lightweight user interface code that you can maintain separately from your main program code.</span></span>

<span data-ttu-id="40c88-132">Microsoft Visual Studio unterstützt das Einbetten von ActiveX-Steuerelementen, einschließlich des Windows Media Player Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="40c88-132">Microsoft Visual Studio supports embedding ActiveX controls, including the Windows Media Player control.</span></span> <span data-ttu-id="40c88-133">Wenn Sie sich dafür entscheiden, erstellt Visual Studio eine neue Alternative Interoperabilitäts-Assembly (Interop), um die Interoperabilität zwischen dem .NET Framework und dem Windows Media Player-Steuerelement zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="40c88-133">When you choose to do this, Visual Studio creates a new alternate interoperability (interop) assembly to manage interoperability between the .NET Framework and the Windows Media Player control.</span></span> <span data-ttu-id="40c88-134">Visual Studio verwendet das .NET Framework tlbimp.exe Tool, um die Interop-Assembly zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="40c88-134">Visual Studio uses the .NET Framework tlbimp.exe tool to create the interop assembly.</span></span> <span data-ttu-id="40c88-135">Dies bedeutet, dass die Signaturen, die bei Verwendung der IntelliSense-Funktion in Visual Studio angezeigt werden, Semantik verwenden, die von der aktuellen Version von Tlbimp bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="40c88-135">This means that the signatures displayed when using the IntelliSense feature in Visual Studio use semantics determined by the current version of tlbimp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40c88-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40c88-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40c88-137">**Einbetten des Windows Media Player-Steuer Elements**</span><span class="sxs-lookup"><span data-stu-id="40c88-137">**Embedding the Windows Media Player Control**</span></span>](embedding-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="40c88-138">**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**</span><span class="sxs-lookup"><span data-stu-id="40c88-138">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[<span data-ttu-id="40c88-139">**Verwenden des Windows Media Player-Steuer Elements in einer .NET Framework-Lösung**</span><span class="sxs-lookup"><span data-stu-id="40c88-139">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="40c88-140">**Verwenden des Windows Media Player-Steuer Elements mit Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="40c88-140">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




