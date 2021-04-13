---
title: Verwenden des Windows Media Player-Steuer Elements mit Visual Basic
description: Verwenden des Windows Media Player-Steuer Elements mit Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player Visual Basic
- Windows Media Player-Objektmodell, Visual Basic
- Objektmodell, Visual Basic
- Windows Media Player Mobile, Visual Basic
- Windows Media Player ActiveX-Steuerelement, Visual Basic
- Windows Media Player Mobile ActiveX-Steuerelement, Visual Basic
- ActiveX-Steuerelement, Visual Basic
- Visual Basic basierte Programm Einbettung
- einbetten, Visual Basic basierte Programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310459"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a><span data-ttu-id="8971d-119">Verwenden des Windows Media Player-Steuer Elements mit Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8971d-119">Using the Windows Media Player Control with Visual Basic</span></span>

<span data-ttu-id="8971d-120">In diesem Abschnitt wird beschrieben, wie Sie das ActiveX-Steuerelement Windows Media Player 9 oder höher in Anwendungen verwenden, die mit Microsoft Visual Basic 6,0 erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="8971d-120">This section describes how to use the Windows Media Player 9 Series or later ActiveX control in applications created with Microsoft Visual Basic 6.0.</span></span>

## <a name="getting-started"></a><span data-ttu-id="8971d-121">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="8971d-121">Getting Started</span></span>

<span data-ttu-id="8971d-122">Wenn Sie der Toolbox das Windows Media Player-Steuerelement hinzufügen möchten, wählen Sie zunächst **Komponenten** aus dem Menü **Projekt** aus.</span><span class="sxs-lookup"><span data-stu-id="8971d-122">To add the Windows Media Player control to the toolbox, first select **Components** from the **Project** menu.</span></span> <span data-ttu-id="8971d-123">Aktivieren Sie im Dialogfeld Komponenten das Kontrollkästchen neben "Windows Media Player".</span><span class="sxs-lookup"><span data-stu-id="8971d-123">In the Components dialog box, select the check box next to "Windows Media Player".</span></span> <span data-ttu-id="8971d-124">Vergewissern Sie sich am unteren Rand des Dialog Felds, dass die ausgewählte Datei wmp.dll ist.</span><span class="sxs-lookup"><span data-stu-id="8971d-124">At the bottom of the dialog box, confirm that the selected file is wmp.dll.</span></span> <span data-ttu-id="8971d-125">Nachdem Sie das Dialogfeld geschlossen haben, können Sie eine Instanz des Windows Media Player-Steuer Elements auf die übliche Weise auf dem Formular platzieren.</span><span class="sxs-lookup"><span data-stu-id="8971d-125">After closing the dialog box, you can place an instance of the Windows Media Player control on your form in the usual ways.</span></span>

<span data-ttu-id="8971d-126">Sie können viele Steuerelement Eigenschaften mithilfe des Eigenschaftenfenster festlegen.</span><span class="sxs-lookup"><span data-stu-id="8971d-126">You can set many control properties using the Properties window.</span></span> <span data-ttu-id="8971d-127">Um einige Eigenschaften festzulegen, müssen Sie das Dialogfeld Eigenschaften von Windows Media Player verwenden, das Sie mit dem Element "(Custom)" in der Eigenschaftenfenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="8971d-127">To set some properties you must use the Windows Media Player Properties dialog box, which you open using the "(Custom)" item in the Properties window.</span></span>

## <a name="object-references"></a><span data-ttu-id="8971d-128">Objektverweise</span><span class="sxs-lookup"><span data-stu-id="8971d-128">Object References</span></span>

<span data-ttu-id="8971d-129">Sie können bestimmte Player-Steuerelement Eigenschaften verwenden, um Verweise auf bestimmte Objekte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8971d-129">You use certain Player control properties to get references to particular objects.</span></span> <span data-ttu-id="8971d-130">Beispielsweise gibt die **cdromcollection** -Eigenschaft einen Verweis auf ein **cdromcollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8971d-130">For example, the **cdromCollection** property returns a reference to a **CdromCollection** object.</span></span> <span data-ttu-id="8971d-131">Sie müssen einen solchen Verweis auf eine Variable zuweisen, die Sie als entsprechende Schnittstelle deklariert haben.</span><span class="sxs-lookup"><span data-stu-id="8971d-131">You must assign such a reference to a variable that you declared as the corresponding interface.</span></span> <span data-ttu-id="8971d-132">Im Fall der **cdromcollection** -Eigenschaft weisen Sie z. b. den Rückgabewert einer Variablen vom Typ " **iwmpcdromcollection**" zu.</span><span class="sxs-lookup"><span data-stu-id="8971d-132">In the case of the **cdromCollection** property, for example, you assign its return value to a variable of type **IWMPCdromCollection**.</span></span>

<span data-ttu-id="8971d-133">Lesen Sie das Thema " [Schnittstellen](interfaces.md) " in der [Objektmodell Referenz für C++](object-model-reference-for-c.md) , um zu ermitteln, welche Objekte mehrere Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="8971d-133">Read the [Interfaces](interfaces.md) topic in the [Object Model Reference for C++](object-model-reference-for-c.md) to identify which objects implement multiple interfaces.</span></span> <span data-ttu-id="8971d-134">In diesen Fällen müssen Sie eine Objekt Variable als höchste nummerierte Schnittstelle deklarieren, die in diesem SDK dokumentiert ist, um Zugriff auf alle Eigenschaften und Methoden dieses Objekts zu haben.</span><span class="sxs-lookup"><span data-stu-id="8971d-134">In those cases, you must declare an object variable as the highest-numbered interface documented in this SDK to have access to all of the properties and methods of that object.</span></span> <span data-ttu-id="8971d-135">Sie sollten z. b. den Wert der Windows Media Player-Steuerelement Eigenschaft **currentMedia** einer Variablen zuweisen, die als **IWMPMedia3** deklariert ist, um sicherzustellen, dass Sie Zugriff auf die Methoden **getattributecountrytbytype** und **getItemInfoByType** haben.</span><span class="sxs-lookup"><span data-stu-id="8971d-135">For example, you should assign the value of the Windows Media Player control **currentMedia** property to a variable declared as **IWMPMedia3** to assure that you have access to the **getAttributeCountByType** and **getItemInfoByType** methods.</span></span>

> [!Note]  
> <span data-ttu-id="8971d-136">Das **windowsmediaplayer** -Objekt implementiert alle Eigenschaften und Methoden der Schnittstellen **iwmpcore**, **IWMPCore2**, **IWMPCore3**, **iwmpplayer**, **IWMPPlayer2**, **IWMPPlayer3** und **IWMPPlayer4** .</span><span class="sxs-lookup"><span data-stu-id="8971d-136">The **WindowsMediaPlayer** object implements all of the properties and methods of the **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3**, and **IWMPPlayer4** interfaces.</span></span> <span data-ttu-id="8971d-137">Sie müssen keine separaten Variablen für eine dieser Schnittstellen deklarieren.</span><span class="sxs-lookup"><span data-stu-id="8971d-137">You do not need to declare separate variables for any of these interfaces.</span></span> <span data-ttu-id="8971d-138">Mit dem Namen, den Sie Ihrer **windowsmediaplayer** -Instanz zugewiesen haben, können Sie auf alle ihre Member zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8971d-138">You can access all of their members using the name you assigned to your **WindowsMediaPlayer** instance.</span></span>

 

<span data-ttu-id="8971d-139">Im Visual Basic Objektkatalog werden viele Schnittstellen angezeigt, die für die private Verwendung durch das Windows Media Player-Steuerelement vorgesehen sind, einschließlich einiger, die Skin-Entwickler unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8971d-139">In the Visual Basic Object Browser you will see many interfaces that are intended for private use by the Windows Media Player control, including some that support skin developers.</span></span> <span data-ttu-id="8971d-140">Sie sollten nur die Objekte, Eigenschaften, Methoden und Ereignisse verwenden, die in diesem SDK dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="8971d-140">You should use only the objects, properties, methods, and events that are documented in this SDK.</span></span>

## <a name="additional-tips"></a><span data-ttu-id="8971d-141">Weitere Tipps</span><span class="sxs-lookup"><span data-stu-id="8971d-141">Additional Tips</span></span>

-   <span data-ttu-id="8971d-142">Die Referenz Dokumentation zeigt die JScript-Syntax.</span><span class="sxs-lookup"><span data-stu-id="8971d-142">The reference documentation shows JScript syntax.</span></span> <span data-ttu-id="8971d-143">In JScript werden Argumente, die an Methoden übergeben werden, immer in Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8971d-143">In JScript, arguments passed to methods are always enclosed in parentheses.</span></span> <span data-ttu-id="8971d-144">In Visual Basic 6,0 müssen Argumente, die an Methoden übergeben werden, die keinen Wert zurückgeben, nicht in Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8971d-144">In Visual Basic 6.0, arguments passed to methods that do not return a value must not be enclosed in parentheses.</span></span>
-   <span data-ttu-id="8971d-145">Einige Eigenschaften oder Methoden werden möglicherweise nicht im Code Vervollständigungs Feature der automatischen Liste im Visual Basic Code-Editor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8971d-145">Some properties or methods may not appear in the Auto List code-completion feature in the Visual Basic code editor.</span></span> <span data-ttu-id="8971d-146">Sie können diese Member weiterhin verwenden, indem Sie Ihre Namen genau so eingeben, wie Sie in dieser Dokumentation angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8971d-146">You can still use those members by typing their names exactly as they appear in this documentation.</span></span>
-   <span data-ttu-id="8971d-147">Verwalten der visuellen Darstellung des Steuer Elements mithilfe der **uiMode** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8971d-147">Manage the visual appearance of the control using the **uimode** property.</span></span> <span data-ttu-id="8971d-148">Dies kann auf zwei Arten erfolgen.</span><span class="sxs-lookup"><span data-stu-id="8971d-148">You can do so in two ways.</span></span> <span data-ttu-id="8971d-149">Im Dialogfeld Eigenschaften von Windows-Media Player können Sie die Dropdown Liste **Modus auswählen** verwenden, oder Sie können den richtigen Wert in die Eigenschaftenfenster eingeben.</span><span class="sxs-lookup"><span data-stu-id="8971d-149">You can use the **Select a mode** drop-down list in the Windows Media Player Properties dialog box, or you can type the correct value in the Properties window.</span></span>

    <span data-ttu-id="8971d-150">Verwenden Sie insbesondere die **Visible** -Eigenschaft nicht, um das Steuerelement auszublenden. Weisen Sie stattdessen den Wert "unsichtbar" der **uiMode** -Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="8971d-150">In particular, do not use the **visible** property to hide the control; instead, assign the value "invisible" to the **uimode** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8971d-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8971d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8971d-152">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="8971d-152">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




