---
title: Einführung in das Windows Media Player SDK
description: Einführung in das Windows Media Player SDK
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, Plug-ins
- Windows Media Player Mobile, Benutzerschnittstellen-Plug-ins
- Mobile Windows Media Player-Plug-ins
- Plug-ins, Benutzeroberfläche
- Plug-ins, Windows Media Player Mobile
- Plug-Ins für Benutzeroberflächen, Windows Media Player Mobile
- UI-Plug-ins, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739304"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a><span data-ttu-id="1a33c-110">Einführung in das Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="1a33c-110">Getting Started with the Windows Media Player SDK</span></span>

<span data-ttu-id="1a33c-111">Zum Erstellen des Plug-Ins müssen Sie zuerst Microsoft Embedded Visual C++ 4,0 und Visual Studio 2003 installieren.</span><span class="sxs-lookup"><span data-stu-id="1a33c-111">To create your plug-in, you first need to install Microsoft eMbedded Visual C++ 4.0 and Visual Studio 2003.</span></span> <span data-ttu-id="1a33c-112">Sie müssen auch das Pocket PC 2003 SDK oder das Smartphone 2003 SDK installieren, bei dem es sich um separate Downloads handelt.</span><span class="sxs-lookup"><span data-stu-id="1a33c-112">You must also install the Pocket PC 2003 SDK or the Smartphone 2003 SDK, which are separate downloads.</span></span> <span data-ttu-id="1a33c-113">Zum Kompilieren und Ausführen des Projekts muss ein Pocket PC-oder Smartphone-Gerät mit dem Betriebssystem Windows Mobile 2003 Second Edition mit dem Entwicklungs Computer synchronisiert werden, indem Microsoft ActiveSync® 3.7.1 oder höher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1a33c-113">To compile and run the project, a Pocket PC or Smartphone device running the Windows Mobile 2003 Second Edition operating system must be synchronized with the development computer by using Microsoft ActiveSync® 3.7.1 or later.</span></span>

<span data-ttu-id="1a33c-114">Da Benutzeroberflächen-Plug-Ins auf Windows Mobile-Geräten das gleiche Plug-in-Modell wie die Desktop Versionen verwenden, können Sie den Windows Media Player-Plug-in-Assistenten als Ausgangspunkt verwenden, um ein Plug-in für die Benutzeroberfläche zu erstellen, das mit Windows Media Player 10 Mobile verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a33c-114">Because UI plug-ins on Windows Mobile devices use the same plug-in model as the desktop versions, you can use the Windows Media Player Plug-in Wizard as a starting point when creating a background UI plug-in that will work with Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="1a33c-115">Gehen Sie folgendermaßen vor, um den UI-Plug-in-Code zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="1a33c-115">To create UI plug-in code, do the following:</span></span>

1.  <span data-ttu-id="1a33c-116">Öffnen Sie Visual Studio 2003, und starten Sie ein neues Projekt in Visual C++.</span><span class="sxs-lookup"><span data-stu-id="1a33c-116">Open Visual Studio 2003, and start a new project in Visual C++.</span></span>
2.  <span data-ttu-id="1a33c-117">Wählen Sie im Bereich **Vorlagen** die Option **Windows Media Player-Plug-in-Assistent** aus.</span><span class="sxs-lookup"><span data-stu-id="1a33c-117">Select **Windows Media Player Plug-in Wizard** from the **Templates** pane.</span></span>
3.  <span data-ttu-id="1a33c-118">Benennen Sie Ihr Projekt mit networkplugin, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a33c-118">Name your project NetworkPlugin and click **OK**.</span></span>
4.  <span data-ttu-id="1a33c-119">Wählen Sie **UI-Plug-in** , und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1a33c-119">Select **UI Plug-in** and click **Next**.</span></span>
5.  <span data-ttu-id="1a33c-120">Wählen Sie **Hintergrund** , und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1a33c-120">Select **Background** and click **Next**.</span></span>
6.  <span data-ttu-id="1a33c-121">Klicken Sie auf **Weiter**, um den Assistenten zu beenden.</span><span class="sxs-lookup"><span data-stu-id="1a33c-121">Click **Next** to finish the wizard.</span></span> <span data-ttu-id="1a33c-122">Wenn Sie Ereignisse mit dem Plug-in überwachen möchten, müssen Sie vor dem Abschließen des Assistenten Ereignisse **lauschen** aktivieren. lesen Sie die Dokumentation für die **iwmpevents** -Schnittstelle, um herauszufinden, welche Ereignisse unter Windows Media Player 10 Mobile unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1a33c-122">If you are going to monitor events with your plug-in, you must check **Listen to events** before finishing the wizard, and you should read the documentation for the **IWMPEvents** interface to find out which events are supported on Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="1a33c-123">Nachdem Sie den UI-Plug-in-Code erstellt haben, müssen Sie in Embedded Visual C++ 4,0 ein leeres Windows CE DLL-Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a33c-123">Now that you have created your UI plug-in code, you need to create an empty Windows CE DLL project in eMbedded Visual C++ 4.0.</span></span> <span data-ttu-id="1a33c-124">Kopieren Sie dann die vom Assistenten generierten Quelldateien in dieses neue Projekt, damit Sie mit dem ARM4-Compiler kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="1a33c-124">Then copy your wizard-generated source files to that new project so that they will compile with the ARM4 compiler.</span></span>

<span data-ttu-id="1a33c-125">So erstellen Sie ein leeres Projekt</span><span class="sxs-lookup"><span data-stu-id="1a33c-125">To create an empty project</span></span>

1.  <span data-ttu-id="1a33c-126">Starten Sie ein neues Projekt in eingebettetem Visual C++, und wählen Sie dann im **Projekt** Bereich **WCE-Dynamic-Link Bibliothek** aus.</span><span class="sxs-lookup"><span data-stu-id="1a33c-126">Start a new project in eMbedded Visual C++, and then select **WCE Dynamic-Link Library** from the **Projects** pane.</span></span>
2.  <span data-ttu-id="1a33c-127">Benennen Sie Ihr Projekt, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a33c-127">Name your project and click **OK**.</span></span>
3.  <span data-ttu-id="1a33c-128">Stellen Sie sicher, dass **ein leeres Windows CE DLL-Projekt** ausgewählt ist, und klicken Sie dann auf **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="1a33c-128">Make sure **An empty Windows CE DLL project** is selected, and then click **Finish**.</span></span>
4.  <span data-ttu-id="1a33c-129">Klicken Sie auf das Menü Element **Projekt** .</span><span class="sxs-lookup"><span data-stu-id="1a33c-129">Click the **Project** menu item.</span></span>
5.  <span data-ttu-id="1a33c-130">Wählen Sie **zu Projekt hinzufügen** aus, und klicken Sie dann auf **Dateien**.</span><span class="sxs-lookup"><span data-stu-id="1a33c-130">Select **Add to Project**, and then click **Files**.</span></span>
6.  <span data-ttu-id="1a33c-131">Wählen Sie die mit dem Plug-in-Assistenten erstellten C++-Dateien aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a33c-131">Select the C++ files you created with the plug-in wizard, and then click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a33c-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a33c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a33c-133">**Erstellen eines Benutzeroberflächen-Plug-Ins für Windows Media Player 10 Mobile**</span><span class="sxs-lookup"><span data-stu-id="1a33c-133">**Creating a User Interface Plug-in for Windows Media Player 10 Mobile**</span></span>](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[<span data-ttu-id="1a33c-134">**Iwmpevents-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1a33c-134">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




