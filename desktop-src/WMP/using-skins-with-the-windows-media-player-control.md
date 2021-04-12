---
title: Verwenden von Skins mit dem Windows Media Player-Steuerelement
description: Verwenden von Skins mit dem Windows Media Player-Steuerelement
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
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
- Windows Media Player ActiveX-Steuerelement, Skins
- Windows Media Player Mobile ActiveX-Steuerelement, Skins
- ActiveX-Steuerelement, Skins
- Skins, Einbettungs Steuerelement für ActiveX
- Windows Media Player Skins, Einbetten des ActiveX-Steuer Elements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206796"
---
# <a name="using-skins-with-the-windows-media-player-control"></a><span data-ttu-id="60ec0-124">Verwenden von Skins mit dem Windows Media Player-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="60ec0-124">Using Skins with the Windows Media Player Control</span></span>

<span data-ttu-id="60ec0-125">Wenn Sie das Windows Media Player-Steuerelement in ein C++-Programm einbinden, können Sie die Player-Benutzeroberfläche (User Interface, UI) anpassen, indem Sie eine Skin-Definitionsdatei darauf anwenden.</span><span class="sxs-lookup"><span data-stu-id="60ec0-125">When you embed the Windows Media Player control in a C++ program, you can customize the Player user interface (UI) by applying a skin definition file to it.</span></span> <span data-ttu-id="60ec0-126">Eine Skin-Definitionsdatei ist ein XML-basiertes Dokument, das das Layout der standardmäßigen und anpassbaren UI-Komponenten und aller zugehörigen Grafiken angibt.</span><span class="sxs-lookup"><span data-stu-id="60ec0-126">A skin definition file is an XML-based document specifying the layout of standard and customizable UI components and any accompanying graphics.</span></span> <span data-ttu-id="60ec0-127">Mithilfe von Microsoft JScript können Sie das Verhalten dieser Komponenten angeben und das Windows Media Player-Steuerelement ohne den Aufwand der C++-und com-Syntax bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="60ec0-127">Using Microsoft JScript, you can specify the behavior of these components and manipulate the Windows Media Player control without the overhead of C++ and COM syntax.</span></span>

<span data-ttu-id="60ec0-128">Skins bieten eine einfache Möglichkeit, den Code Ihrer Benutzeroberfläche und den Code des Hauptprogramms voneinander getrennt zu halten, damit Sie unabhängig voneinander verwaltet und entwickelt werden können.</span><span class="sxs-lookup"><span data-stu-id="60ec0-128">Skins provide an easy way to keep your user interface code and your main program code separate so that they can be maintained and developed independently.</span></span> <span data-ttu-id="60ec0-129">Sie können auch die ursprünglich für die Verwendung durch den eigenständigen Player im Skin-Modus vorgesehenen Skins wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="60ec0-129">You can also reuse skins originally designed for use by the standalone Player in skin mode.</span></span> <span data-ttu-id="60ec0-130">Skin-Code, den Sie speziell für C++-Programme entwerfen, kann über ein Skript fähiges Objekt, das von Ihrem Programm bereitgestellt werden kann, mit ihren Programmen interagieren.</span><span class="sxs-lookup"><span data-stu-id="60ec0-130">Skin code that you design specifically for C++ programs can interact with your programs through a scriptable object that your program can provide.</span></span>

<span data-ttu-id="60ec0-131">Um den Skin-Modus für das Windows Media Player-Steuerelement zu aktivieren, muss das Programm die **iwmpremotemediaservices** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="60ec0-131">To enable skin mode for the Windows Media Player control, your program must implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="60ec0-132">Obwohl Sie Skins mit dem-Steuerelement verwenden und das-Steuerelement gleichzeitig Remote verwenden können, können Sie diese Schnittstelle verwenden, um beide Funktionen zu aktivieren, ohne die andere zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="60ec0-132">Although you can use skins with the control and remote the control at the same time, you can use this interface to enable either feature without enabling the other.</span></span> <span data-ttu-id="60ec0-133">Um Remoting zu deaktivieren, übergeben Sie einfach den Wert "local" als out-Parameter der **getservicetype** -Methode, und geben Sie ein HRESULT von E \_ notimpl von der **getapplicationname** -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="60ec0-133">To disable remoting, simply pass a value of "Local" as the out parameter of the **GetServiceType** method, and return an HRESULT of E\_NOTIMPL from the **GetApplicationName** method.</span></span>

<span data-ttu-id="60ec0-134">Um das Windows Media Player-Steuerelement in den Skin-Modus zu wechseln, wenden Sie die Methode **iwmpplayer::p UT \_ uiMode** an, und übergeben Sie dabei den Wert "Custom".</span><span class="sxs-lookup"><span data-stu-id="60ec0-134">To switch the Windows Media Player control to skin mode, call the **IWMPPlayer::put\_uiMode** method, passing in a value of "custom".</span></span> <span data-ttu-id="60ec0-135">Geben Sie den Pfad und den Dateinamen der zu verwendenden Skin-Definitionsdatei an, indem Sie Sie von der **iwmpremotemediaservices:: getcustomuimode** -Methode zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="60ec0-135">Specify the path and file name of the skin definition file to use by returning it from the **IWMPRemoteMediaServices::GetCustomUIMode** method.</span></span>

<span data-ttu-id="60ec0-136">Wenn Sie ein Skript fähiges Objekt für die Kommunikation zwischen Ihrer Skin und Ihrem Programm bereitstellen möchten, übergeben Sie einen Namen und einen Zeiger an einen **IDispatch** -Zeiger als zwei out-Parameter der **iwmpremotemediaservices:: getscriptableobject** -Methode.</span><span class="sxs-lookup"><span data-stu-id="60ec0-136">If you want to provide a scriptable object for communication between your skin and your program, pass a name and a pointer to an **IDispatch** pointer as the two out parameters of the **IWMPRemoteMediaServices::GetScriptableObject** method.</span></span> <span data-ttu-id="60ec0-137">Die Skin kann dann Aufrufe an das Skript fähige Objekt durchführen, indem der angegebene Name verwendet wird, als ob es sich um ein globales Attribut handelt, das dem globalen Attribut des **Players** ähnelt.</span><span class="sxs-lookup"><span data-stu-id="60ec0-137">Your skin can then make calls to the scriptable object by using the name specified as though it were a global attribute similar to the **player** global attribute.</span></span>

<span data-ttu-id="60ec0-138">Ein Skin, das auf ein Remotes Windows-Media Player Steuerelement angewendet wird, kann mit einem anderen globalen Attribut namens **playerapplication** auf das **playerapplication** -Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="60ec0-138">A skin applied to a remoted Windows Media Player control can access the **PlayerApplication** object using another global attribute called **playerApplication**.</span></span> <span data-ttu-id="60ec0-139">Da Skins nicht auf die **Player. playerapplication** -Eigenschaft zugreifen kann, müssen Sie dieses globale Attribut verwenden, wenn Sie möchten, dass der Skin-Code Andocken und Andocken verwaltet.</span><span class="sxs-lookup"><span data-stu-id="60ec0-139">Because the **Player.playerApplication** property cannot be accessed by skins, you must use this global attribute when you want your skin code to manage docking and undocking.</span></span>

## <a name="samples"></a><span data-ttu-id="60ec0-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60ec0-140">Samples</span></span>

<span data-ttu-id="60ec0-141">Das Windows Media Player SDK-Setup Paket installiert ein Beispiel, das das Anwenden einer Skin auf das Windows Media Player-Steuerelement veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="60ec0-141">The Windows Media Player SDK setup package installs a sample that demonstrates applying a skin to the Windows Media Player control.</span></span> <span data-ttu-id="60ec0-142">Weitere Informationen finden Sie im remoteskin-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="60ec0-142">See the RemoteSkin sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60ec0-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60ec0-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60ec0-144">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="60ec0-144">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="60ec0-145">**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**</span><span class="sxs-lookup"><span data-stu-id="60ec0-145">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




