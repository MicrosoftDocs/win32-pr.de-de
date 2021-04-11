---
title: Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm
description: Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm
ms.assetid: 2531ac25-5e9d-462e-a06a-6f81bf4ca33d
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, C++
- Windows Media Player-Objektmodell, C++
- Objektmodell, C++
- Windows Media Player Mobile, C++
- Windows Media Player ActiveX-Steuerelement, C++
- Windows Media Player Mobile ActiveX-Steuerelement, C++
- ActiveX-Steuerelement, C++
- C++-Programm Einbettung
- einbetten, C++-Programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02430dbdaba3bb2e8ea3ca6e46b202a289a096f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207058"
---
# <a name="using-the-windows-media-player-control-in-a-c-program"></a><span data-ttu-id="22a8e-119">Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm</span><span class="sxs-lookup"><span data-stu-id="22a8e-119">Using the Windows Media Player Control in a C++ Program</span></span>

> [!Note]  
> <span data-ttu-id="22a8e-120">Die Verwendung von C++ zum Einbetten des Windows Media Player-Steuer Elements wird für Windows Media Player 9-Serie oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22a8e-120">Using C++ to embed the Windows Media Player control is supported for Windows Media Player 9 Series or later.</span></span>

 

<span data-ttu-id="22a8e-121">Es gibt verschiedene Möglichkeiten, das Windows Media Player-Steuerelement in einem C++-Programm zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="22a8e-121">There are several different ways to use the Windows Media Player control in a C++ program.</span></span> <span data-ttu-id="22a8e-122">Sie können eine Instanz des-Steuer Elements in einer Konsolenanwendung erstellen, oder Sie können das-Steuerelement in eine Windows-Anwendung einbetten.</span><span class="sxs-lookup"><span data-stu-id="22a8e-122">You can create an instance of the control in a console application, or you can embed the control in a Windows application.</span></span> <span data-ttu-id="22a8e-123">Außerdem können Sie Schnittstellen implementieren, die es Ihnen ermöglichen, ein eingebettetes Player-Steuerelement im Remote Modus auszuführen.</span><span class="sxs-lookup"><span data-stu-id="22a8e-123">Also, you can implement interfaces that enable you to run an embedded Player control in remote mode.</span></span> <span data-ttu-id="22a8e-124">Sie können die Benutzeroberfläche eines eingebetteten Steuer Elements anpassen, indem Sie eine Skin-Definitionsdatei anwenden.</span><span class="sxs-lookup"><span data-stu-id="22a8e-124">You can customize the user interface of an embedded control by applying a skin definition file.</span></span>

<span data-ttu-id="22a8e-125">Diese Informationen werden in den folgenden Themen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="22a8e-125">This information is described in the following topics.</span></span>



| <span data-ttu-id="22a8e-126">Thema</span><span class="sxs-lookup"><span data-stu-id="22a8e-126">Topic</span></span>                                                                                                                                      | <span data-ttu-id="22a8e-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22a8e-127">Description</span></span>                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22a8e-128">Verwenden des Windows Media Player-Steuer Elements in einer Konsolenanwendung</span><span class="sxs-lookup"><span data-stu-id="22a8e-128">Using the Windows Media Player Control in a Console Application</span></span>](using-the-windows-media-player-control-in-a-console-application.md)     | <span data-ttu-id="22a8e-129">Beschreibt eine einfache Konsolenanwendung C++, die das Windows Media Player-Steuerelement instanziiert, um die Version anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22a8e-129">Describes a simple C++ console application that instantiates the Windows Media Player control to display the version.</span></span>                                                       |
| [<span data-ttu-id="22a8e-130">Hosting des Windows Media Player-Steuer Elements in einer Windows-Anwendung</span><span class="sxs-lookup"><span data-stu-id="22a8e-130">Hosting the Windows Media Player Control in a Windows Application</span></span>](hosting-the-windows-media-player-control-in-a-windows-application.md) | <span data-ttu-id="22a8e-131">Beschreibt die Verwendung des ATL-ActiveX-Host Fensters zum Einbetten des Windows Media Player-Steuer Elements in ein Windows-Programm.</span><span class="sxs-lookup"><span data-stu-id="22a8e-131">Describes how to use the ATL ActiveX host window to embed the Windows Media Player control in a Windows program.</span></span>                                                            |
| [<span data-ttu-id="22a8e-132">Remoting des Windows Media Player-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="22a8e-132">Remoting the Windows Media Player Control</span></span>](remoting-the-windows-media-player-control.md)                                                 | <span data-ttu-id="22a8e-133">Beschreibt, wie das Windows Media Player-Steuerelement in einem C++-Programm im Remote Modus eingebettet wird, sodass Ihre Benutzer das Steuerelement Eindocken können, um in den vollständigen Modus des Players zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="22a8e-133">Describes how to embed the Windows Media Player control in a C++ program in remote mode, which lets your users undock the control to switch to the full mode of the Player.</span></span> |
| [<span data-ttu-id="22a8e-134">Behandeln von Ereignissen in C++</span><span class="sxs-lookup"><span data-stu-id="22a8e-134">Handling Events in C++</span></span>](handling-events-in-c.md)                                                                                         | <span data-ttu-id="22a8e-135">Hier wird beschrieben, wie Ereignis Benachrichtigungen von Windows Media Player empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="22a8e-135">Describes how to receive event notifications from Windows Media Player.</span></span>                                                                                                     |
| [<span data-ttu-id="22a8e-136">Verwenden von Skins mit dem Windows Media Player-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="22a8e-136">Using Skins with the Windows Media Player Control</span></span>](using-skins-with-the-windows-media-player-control.md)                                 | <span data-ttu-id="22a8e-137">Beschreibt, wie eine Skin-Datei auf ein in einem C++-Programm eingebettetes Windows Media Player-Steuerelement angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="22a8e-137">Describes how to apply a skin file to a Windows Media Player control embedded in a C++ program.</span></span>                                                                             |



 

> [!Note]  
> <span data-ttu-id="22a8e-138">Sie können das Windows Media Player 10 Mobile-Steuerelement in eine Windows CE Anwendung einbetten.</span><span class="sxs-lookup"><span data-stu-id="22a8e-138">You can embed the Windows Media Player 10 Mobile control in a Windows CE application.</span></span> <span data-ttu-id="22a8e-139">Die Verfahren, die Sie hierfür verwenden, ähneln denen, die mit dem Windows-Steuerelement für Desktop-Media Player verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22a8e-139">The techniques you use to do this are similar to those used with the desktop Windows Media Player control.</span></span> <span data-ttu-id="22a8e-140">Es gibt jedoch Unterschiede zwischen ATL für Windows und ATL für Windows CE.</span><span class="sxs-lookup"><span data-stu-id="22a8e-140">However, there are differences between ATL for Windows and ATL for Windows CE.</span></span> <span data-ttu-id="22a8e-141">In dieser Dokumentation werden die Unterschiede zwischen diesen Implementierungen, soweit zutreffend, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="22a8e-141">This documentation describes the differences between these implementations, where appropriate.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="22a8e-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22a8e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22a8e-143">**Objektmodell Referenz für C++**</span><span class="sxs-lookup"><span data-stu-id="22a8e-143">**Object Model Reference for C++**</span></span>](object-model-reference-for-c.md)
</dt> <dt>

[<span data-ttu-id="22a8e-144">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="22a8e-144">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




