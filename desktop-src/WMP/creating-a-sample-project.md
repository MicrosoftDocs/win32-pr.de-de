---
title: Erstellen eines Beispielprojekts
description: Erstellen eines Beispielprojekts
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player Online Stores, Erstellen von Beispielprojekten
- Online Stores, Erstellen von Beispielprojekten
- Typ 2 Online Stores, Erstellen von Beispielprojekten
- Windows Media Player Online Stores, Beispiel Projekte
- Online Stores, Beispiel Projekte
- Typ 2 Online Stores, Beispiel Projekte
- Windows Media Player Online Stores, Projekt-Assistent
- Online Stores, Projekt-Assistent
- Typ 2 Online Stores, Projekt-Assistent
- Plug-ins, Projekt-Assistent
- Windows Media Player-Plug-ins, Projekt-Assistent
- Erstellen von Beispielprojekten
- Beispiele, Typ 2 Online Stores
- Projekt-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104101326"
---
# <a name="creating-a-sample-project"></a><span data-ttu-id="e9882-117">Erstellen eines Beispielprojekts</span><span class="sxs-lookup"><span data-stu-id="e9882-117">Creating a Sample Project</span></span>

<span data-ttu-id="e9882-118">Führen Sie die folgenden Schritte aus, um ein neues Projekt mit dem Projekt-Assistenten zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e9882-118">To create a new project using the project wizard, follow these steps:</span></span>

1.  <span data-ttu-id="e9882-119">Öffnen Sie Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e9882-119">Open Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="e9882-120">Zeigen Sie im Menü **Datei** auf **Neu**, und klicken Sie dann auf **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="e9882-120">From the **File** menu, point to **New**, and then click **Project**.</span></span>
3.  <span data-ttu-id="e9882-121">Wählen Sie im Listenfeld **Projekttypen** die Option **Visual C++ Projekte** aus.</span><span class="sxs-lookup"><span data-stu-id="e9882-121">In the **Project Types** list box, choose **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="e9882-122">Wählen Sie im Listenfeld **Vorlagen** die Option **Windows Media Player Online Stores-Assistent** aus.</span><span class="sxs-lookup"><span data-stu-id="e9882-122">In the **Templates** list box, choose **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="e9882-123">Geben Sie einen Namen und einen Speicherort für das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="e9882-123">Type a name and location for your project.</span></span>
6.  <span data-ttu-id="e9882-124">Klicken Sie auf **OK** , um den Projektassistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="e9882-124">Click **OK** to start the project wizard.</span></span>
7.  <span data-ttu-id="e9882-125">Wählen Sie **Typ 2 (grundlegende Integration)** aus, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e9882-125">Select **Type 2 (Basic integration)**, and click **Next**.</span></span>
8.  <span data-ttu-id="e9882-126">Geben Sie den anzeigen Amen und die Inhalts Verteiler-ID für den Dienst ein.</span><span class="sxs-lookup"><span data-stu-id="e9882-126">Type the friendly name and content distributor ID for your service.</span></span> <span data-ttu-id="e9882-127">Geben Sie die URL für die Webseite ein, die den Dienst vom Computer des Benutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9882-127">Type the URL for the webpage that removes the service from the user's computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="e9882-128">Der Wert, den Sie für die ID des Inhalts Verteilers angeben, darf keine Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9882-128">The value you provide for the content distributor ID must not contain spaces.</span></span> <span data-ttu-id="e9882-129">Der Assistent entfernt alle Leerzeichen aus der von Ihnen bereitgestellten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e9882-129">The wizard removes any spaces from the string you provide.</span></span>

     

9.  <span data-ttu-id="e9882-130">Klicken Sie auf **Fertig stellen**, um das Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e9882-130">Click **Finish** to create the project.</span></span>

<span data-ttu-id="e9882-131">Der Assistent generiert automatisch ein neues C++-Projekt, das ein Type 2 Online Store-Plug-in erstellt, das die **iwmpabonneptionservice** -und **IWMPSubscriptionService2** -Schnittstellen implementiert.</span><span class="sxs-lookup"><span data-stu-id="e9882-131">The wizard automatically generates a new C++ project that creates a type 2 online store plug-in that implements the **IWMPSubscriptionService** and **IWMPSubscriptionService2** interfaces.</span></span> <span data-ttu-id="e9882-132">Jedes Mal, wenn Sie den Assistenten ausführen, wird das gleiche Projekt erstellt, aber die Komponente, die beim Kompilieren des Projekts erstellt wird, verfügt über eine eindeutige Klassen-ID.</span><span class="sxs-lookup"><span data-stu-id="e9882-132">Each time you run the wizard it creates the same project, but the component that is created when you compile the project has a unique class ID.</span></span> <span data-ttu-id="e9882-133">Der Projektname, der Anzeige Name und die Inhalts Verteiler-ID können sich auch je nach den Werten unterscheiden, die Sie beim Durchlaufen des Assistenten angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="e9882-133">The project name, the friendly name, and content distributor ID may also be different depending on the values you provided when you ran the wizard.</span></span> <span data-ttu-id="e9882-134">Das Beispiel Projekt registriert die Komponente unter Verwendung eines Schlüssel namens, der mit dem Wert übereinstimmt, den Sie für den anzeigen Amen angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="e9882-134">The sample project registers the component by using a key name that matches the value you supplied for the friendly name.</span></span>

<span data-ttu-id="e9882-135">Im Beispiel wird Active Template Library (ATL)-Code verwendet, um com-Implementierungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e9882-135">The sample uses Active Template Library (ATL) code to provide COM implementations.</span></span>

<span data-ttu-id="e9882-136">Der Assistent erstellt die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="e9882-136">The wizard creates the following files for you:</span></span>

-   <span data-ttu-id="e9882-137">*ProjectName* dll. cpp.</span><span class="sxs-lookup"><span data-stu-id="e9882-137">*ProjectName* dll.cpp.</span></span> <span data-ttu-id="e9882-138">Implementiert die DLL-Exporte (Dynamic Link Library), wie z. b. die Haupt-DLL-Einstiegspunkt Funktion.</span><span class="sxs-lookup"><span data-stu-id="e9882-138">Implements the Dynamic Link Library (DLL) exports such as the main DLL entry point function.</span></span> <span data-ttu-id="e9882-139">Enthält auch die ATL-Objekt Zuordnung und die Modul Deklaration.</span><span class="sxs-lookup"><span data-stu-id="e9882-139">Also contains the ATL object map and module declaration.</span></span>
-   <span data-ttu-id="e9882-140">*ProjectName*. cpp.</span><span class="sxs-lookup"><span data-stu-id="e9882-140">*ProjectName*.cpp.</span></span> <span data-ttu-id="e9882-141">Enthält Standard Implementierungen für die Methoden der iwmpabonneptionservice-und IWMPSubscriptionService2-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="e9882-141">Contains default implementations for the methods of the IWMPSubscriptionService and IWMPSubscriptionService2 interfaces.</span></span> <span data-ttu-id="e9882-142">Enthält auch Code zum Definieren der Dialogfelder, die das Beispiel öffnet, wenn Methoden von Windows Media Player aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e9882-142">Also contains code to define the dialog boxes that the sample opens when methods are called by Windows Media Player.</span></span>
-   <span data-ttu-id="e9882-143">*ProjectName*. def. Deklariert die DLL-Exporte.</span><span class="sxs-lookup"><span data-stu-id="e9882-143">*ProjectName*.def. Declares the DLL exports.</span></span>
-   <span data-ttu-id="e9882-144">Stdafx. cpp.</span><span class="sxs-lookup"><span data-stu-id="e9882-144">StdAfx.cpp.</span></span> <span data-ttu-id="e9882-145">Schließt Standard Header ein.</span><span class="sxs-lookup"><span data-stu-id="e9882-145">Includes standard headers.</span></span>
-   <span data-ttu-id="e9882-146">WMP. h.</span><span class="sxs-lookup"><span data-stu-id="e9882-146">wmp.h.</span></span> <span data-ttu-id="e9882-147">Die Windows-Media Player Header Datei.</span><span class="sxs-lookup"><span data-stu-id="e9882-147">The Windows Media Player header file.</span></span>
-   <span data-ttu-id="e9882-148">wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="e9882-148">wmpplug.h.</span></span> <span data-ttu-id="e9882-149">Die Windows Media Player-Plug-in-Header Datei.</span><span class="sxs-lookup"><span data-stu-id="e9882-149">The Windows Media Player plug-in header file.</span></span>
-   <span data-ttu-id="e9882-150">Abonnement Services. h.</span><span class="sxs-lookup"><span data-stu-id="e9882-150">subscriptionservices.h.</span></span> <span data-ttu-id="e9882-151">Die Header Datei des Windows Media Player Online Stores.</span><span class="sxs-lookup"><span data-stu-id="e9882-151">The Windows Media Player online stores header file.</span></span>
-   <span data-ttu-id="e9882-152">Resource. h.</span><span class="sxs-lookup"><span data-stu-id="e9882-152">resource.h.</span></span> <span data-ttu-id="e9882-153">Enthält Ressourcen Definitionen.</span><span class="sxs-lookup"><span data-stu-id="e9882-153">Contains resource definitions.</span></span>
-   <span data-ttu-id="e9882-154">**ProjectName**. h.</span><span class="sxs-lookup"><span data-stu-id="e9882-154">**ProjectName**.h.</span></span> <span data-ttu-id="e9882-155">Enthält Klassendefinitionen für das Onlinespeicher Objekt und die Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="e9882-155">Contains class definitions for the online store object and the dialog boxes.</span></span> <span data-ttu-id="e9882-156">Definiert die Klassen-ID des Objekts und die ID-Konstante des Inhalts Verteilers.</span><span class="sxs-lookup"><span data-stu-id="e9882-156">Defines the object's class ID and the content distributor ID constant.</span></span>
-   <span data-ttu-id="e9882-157">Stdafx. h.</span><span class="sxs-lookup"><span data-stu-id="e9882-157">StdAfx.h.</span></span> <span data-ttu-id="e9882-158">Enthält Standardsystem-includes.</span><span class="sxs-lookup"><span data-stu-id="e9882-158">Contains standard system includes.</span></span>
-   <span data-ttu-id="e9882-159">*ProjectName*. rc.</span><span class="sxs-lookup"><span data-stu-id="e9882-159">*ProjectName*.rc.</span></span> <span data-ttu-id="e9882-160">Die Ressourcen Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="e9882-160">The resource script file.</span></span> <span data-ttu-id="e9882-161">Diese enthält Definitionen für die Dialogfeld Ressourcen und Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e9882-161">This contains definitions for the dialog box resources and controls.</span></span> <span data-ttu-id="e9882-162">An dieser Stelle wird auch die Zeichen folgen Tabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e9882-162">This is also where the string table is stored.</span></span> <span data-ttu-id="e9882-163">Die Zeichen folgen Tabelle enthält den Projektnamen und die Zeichen folgen Konstanten für den anzeigen Amen.</span><span class="sxs-lookup"><span data-stu-id="e9882-163">The string table contains your project name and friendly name string constants.</span></span> <span data-ttu-id="e9882-164">Normalerweise arbeiten Sie mit dieser Datei im Ressourcen-Editor von Visual Studio, nicht als Klartext.</span><span class="sxs-lookup"><span data-stu-id="e9882-164">Usually you work with this file in the Visual Studio resource editor, not as plain text.</span></span>
-   <span data-ttu-id="e9882-165">*ProjectName*. rgs.</span><span class="sxs-lookup"><span data-stu-id="e9882-165">*ProjectName*.rgs.</span></span> <span data-ttu-id="e9882-166">Die Registrierungs Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="e9882-166">The registry script file.</span></span> <span data-ttu-id="e9882-167">Diese Datei enthält die Informationen, die verwendet werden, um die Komponenten Klasse zur Registrierung hinzuzufügen, damit Windows Media Player Sie finden kann.</span><span class="sxs-lookup"><span data-stu-id="e9882-167">This file contains the information used to add your component class to the registry so Windows Media Player can locate it.</span></span> <span data-ttu-id="e9882-168">Sie können den Schlüsselnamen für Ihren Dienst in dieser Datei ändern.</span><span class="sxs-lookup"><span data-stu-id="e9882-168">You can change the key name for your service in this file.</span></span>

> [!Note]  
> <span data-ttu-id="e9882-169">Sie sollten die Basisadresse für die dll auf 0x0f100000 festlegen, um Konflikte mit Windows-Media Player zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e9882-169">You should set the base address for your DLL to 0x0F100000 to avoid conflicts with Windows Media Player.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e9882-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9882-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9882-171">**Entwickeln des Plug-Ins für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="e9882-171">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e9882-172">**Iwmpabonneptionservice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e9882-172">**IWMPSubscriptionService Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[<span data-ttu-id="e9882-173">**IWMPSubscriptionService2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e9882-173">**IWMPSubscriptionService2 Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




