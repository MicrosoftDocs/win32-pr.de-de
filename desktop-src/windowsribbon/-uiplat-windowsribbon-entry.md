---
title: Windows-Menü Band Framework
description: Das Windows-Menü Band Framework ist ein Funktions Reiches Befehls Präsentationssystem, das eine moderne Alternative zu den geschichteten Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen bietet.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Windows-Menüband
- Menüband
- Windows-Menü Band Dokumentation
- Menüband-Dokumentation
- Menüband-API
- Multifunktionsleisten-API
- Windows-Menüband, Framework
- Menüband, Framework
- Windows-Menüband, Info
- Multifunktionsleiste, Info
- Windows-Menüband, Komponenten
- Multifunktionsleiste, Komponenten
- Windows-Menüband, Ansichten
- Menüband, Ansichten
- Windows-Multifunktionsleiste, Architektur
- Multifunktionsleiste, Architektur
- Windows-Menüband, APIs
- Multifunktionsleiste, APIs
- Windows-Menüband, Sicherheit
- Multifunktionsleiste, Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6906401573cb244ddc4386faf8c283d7938a0ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949725"
---
# <a name="windows-ribbon-framework"></a><span data-ttu-id="f1b0d-123">Windows-Menü Band Framework</span><span class="sxs-lookup"><span data-stu-id="f1b0d-123">Windows Ribbon Framework</span></span>

<span data-ttu-id="f1b0d-124">Das Windows-Menü Band Framework ist ein Funktions Reiches Befehls Präsentationssystem, das eine moderne Alternative zu den geschichteten Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen bietet.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-124">The Windows Ribbon framework is a rich command presentation system that provides a modern alternative to the layered menus, toolbars, and task panes of traditional Windows applications.</span></span> <span data-ttu-id="f1b0d-125">Ähnlich wie bei der Funktionalität und Darstellung der Benutzeroberfläche für die Microsoft Office 2007-Benutzeroberfläche besteht das Multifunktionsleisten-Framework aus einer Multifunktionsleisten-Befehlsleiste, die die Hauptfunktionen einer Anwendung über eine Reihe von Registerkarten am oberen Rand eines Anwendungsfensters und ein Kontextmenü System verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-125">Similar in functionality and appearance to the Microsoft Office 2007 Fluent user interface, the Ribbon framework is composed of a ribbon command bar that exposes the major features of an application through a series of tabs at the top of an application window, and a context menu system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f1b0d-126">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f1b0d-126">In this section</span></span>



| <span data-ttu-id="f1b0d-127">Thema</span><span class="sxs-lookup"><span data-stu-id="f1b0d-127">Topic</span></span>                                                                           | <span data-ttu-id="f1b0d-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1b0d-128">Description</span></span>                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1b0d-129">Menüband-frameworkübersichten</span><span class="sxs-lookup"><span data-stu-id="f1b0d-129">Ribbon Framework Overviews</span></span>](windowsribbon-overviews-entry.md)<br/>      | <span data-ttu-id="f1b0d-130">Die Themen in diesem Abschnitt untersuchen die Grundlagen des Multifunktionsleisten-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-130">The topics contained in this section explore the fundamentals of the Ribbon framework.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="f1b0d-131">Entwickler Handbücher für Menüband Framework</span><span class="sxs-lookup"><span data-stu-id="f1b0d-131">Ribbon Framework Developer Guides</span></span>](windowsribbon-guides-entry.md)<br/>  | <span data-ttu-id="f1b0d-132">Die in diesem Abschnitt enthaltenen Themen beschreiben bestimmte Aspekte des Windows-Menüband-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-132">The topics contained in this section describe specific aspects of the Windows Ribbon framework.</span></span> <br/>                                                                                                          |
| [<span data-ttu-id="f1b0d-133">Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f1b0d-133">Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)<br/> | <span data-ttu-id="f1b0d-134">Die in diesem Abschnitt enthaltenen Themen beschreiben den Satz von Steuerelementen, die im Menüband-Framework enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-134">The topics contained in this section describe the set of controls that are included with the Ribbon framework.</span></span> <span data-ttu-id="f1b0d-135">Die hier aufgeführten Steuerelemente sind die UI-Objekte in einem Menüband, die Befehls Funktionalität verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-135">The controls listed here are the UI objects in a ribbon that expose Command functionality.</span></span><br/> |
| [<span data-ttu-id="f1b0d-136">Menü Band Framework-Referenz</span><span class="sxs-lookup"><span data-stu-id="f1b0d-136">Ribbon Framework Reference</span></span>](windowsribbon-reference-entry.md)<br/>      | <span data-ttu-id="f1b0d-137">Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für das Menüband-Framework.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-137">The topics contained in this section provide the Reference specifications for the Ribbon framework.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="f1b0d-138">Menü Band Framework-Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1b0d-138">Ribbon Framework Samples</span></span>](windowsribbon-samples-entry.md)<br/>          | <span data-ttu-id="f1b0d-139">Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Windows-Menü Band Framework-Dokumentation unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-139">The topics contained in this section provide details about the code samples that support the Windows Ribbon framework documentation.</span></span> <br/>                                                                     |
| [<span data-ttu-id="f1b0d-140">Menü Band Framework-Glossar</span><span class="sxs-lookup"><span data-stu-id="f1b0d-140">Ribbon Framework Glossary</span></span>](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a><span data-ttu-id="f1b0d-141">Entwicklerzielgruppe</span><span class="sxs-lookup"><span data-stu-id="f1b0d-141">Developer Audience</span></span>

<span data-ttu-id="f1b0d-142">Das Windows-Menü Band Framework ist für die Verwendung durch C/C++-Entwickler und Benutzeroberflächen-Designer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-142">The Windows Ribbon framework is designed for use by C/C++ developers and UI designers.</span></span>

<span data-ttu-id="f1b0d-143">Empfohlene Kenntnisse:</span><span class="sxs-lookup"><span data-stu-id="f1b0d-143">Recommended proficiencies:</span></span>

-   <span data-ttu-id="f1b0d-144">COM-Programmierung</span><span class="sxs-lookup"><span data-stu-id="f1b0d-144">COM programming</span></span>
-   <span data-ttu-id="f1b0d-145">Windows-API-Programmierung</span><span class="sxs-lookup"><span data-stu-id="f1b0d-145">Windows API programming</span></span>
-   <span data-ttu-id="f1b0d-146">XML/XAML-Programmierung</span><span class="sxs-lookup"><span data-stu-id="f1b0d-146">XML/XAML programming</span></span>

<span data-ttu-id="f1b0d-147">Empfohlene grundlegende Kenntnisse:</span><span class="sxs-lookup"><span data-stu-id="f1b0d-147">Recommended foundational knowledge:</span></span>

-   <span data-ttu-id="f1b0d-148">Konzepte der Benutzeroberflächen Programmierung</span><span class="sxs-lookup"><span data-stu-id="f1b0d-148">UI programming concepts</span></span>
-   <span data-ttu-id="f1b0d-149">Allgemeine Benutzeroberflächen Konzepte</span><span class="sxs-lookup"><span data-stu-id="f1b0d-149">General UI concepts</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="f1b0d-150">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="f1b0d-150">Minimum Requirements</span></span>



| <span data-ttu-id="f1b0d-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1b0d-151">Requirement</span></span> | <span data-ttu-id="f1b0d-152">Wert</span><span class="sxs-lookup"><span data-stu-id="f1b0d-152">Value</span></span> |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b0d-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1b0d-153">Minimum supported client</span></span>               | <span data-ttu-id="f1b0d-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f1b0d-154">Windows 7</span></span><br/> <span data-ttu-id="f1b0d-155">Windows Vista mit Service Pack 2 (SP2) und [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1b0d-155">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="f1b0d-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1b0d-156">Minimum supported server</span></span>               | <span data-ttu-id="f1b0d-157">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1b0d-157">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="f1b0d-158">Windows Server 2008 mit SP2 und [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1b0d-158">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="f1b0d-159">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="f1b0d-159">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="f1b0d-160">7.0</span><span class="sxs-lookup"><span data-stu-id="f1b0d-160">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="f1b0d-161">Header-und IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="f1b0d-161">Header and IDL files</span></span>                   | <span data-ttu-id="f1b0d-162">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="f1b0d-162">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="f1b0d-163">Das [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und das [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menü Band Anwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-163">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="f1b0d-164">Die Platt Form Updates werden für alle Windows Vista-und Windows Server 2008-Kunden über Windows Update verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-164">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="f1b0d-165">Anwendungen von Drittanbietern, die ein [Platt Form Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein [Platt Form Update für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen, ob das erforderliche aktualisierte installiert ist. Wenn dies nicht der Fall ist, wird Windows Update im Hintergrund heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="f1b0d-165">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f1b0d-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f1b0d-166">See Also</span></span>

[<span data-ttu-id="f1b0d-167">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="f1b0d-167">Component Object Model (COM)</span></span>](../com/component-object-model--com--portal.md)


<span data-ttu-id="f1b0d-168">[Windows-API](/previous-versions//cc433218(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1b0d-168">[Windows API](/previous-versions//cc433218(v=vs.85))</span></span>


[<span data-ttu-id="f1b0d-169">XAML</span><span class="sxs-lookup"><span data-stu-id="f1b0d-169">XAML</span></span>](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

