---
title: Verwenden des Plug-in-Assistenten in Visual Studio
description: Verwenden des Plug-in-Assistenten in Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Windows Media Player-Plug-ins, Visual Studio
- Plug-ins, Visual Studio
- Entwickeln von Plug-ins, Visual Studio
- Windows Media Player-Plug-in-Assistent, Visual Studio
- Visual Studio, Windows Media Player-Plug-in-Assistent
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310396"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="ff716-109">Verwenden des Plug-in-Assistenten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ff716-109">Using the Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="ff716-110">Nachdem Sie die erforderlichen Komponenten installiert haben, können Sie schnell ein Plug-in erstellen, das als Ausgangspunkt fungiert.</span><span class="sxs-lookup"><span data-stu-id="ff716-110">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="ff716-111">Die folgenden Schritte führen Sie durch.</span><span class="sxs-lookup"><span data-stu-id="ff716-111">The following steps will guide you.</span></span>

1.  <span data-ttu-id="ff716-112">Starten Sie Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ff716-112">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="ff716-113">Zeigen Sie im Menü **Datei** auf **neu** , und klicken Sie dann auf **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ff716-113">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="ff716-114">Wählen Sie unter **Projekttypen** die Option **Visual C++ Projekte** aus.</span><span class="sxs-lookup"><span data-stu-id="ff716-114">In **Project Types**, select **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="ff716-115">Wählen Sie unter **Vorlagen** die Option **Windows Media Player-Plug-in-Assistent** aus.</span><span class="sxs-lookup"><span data-stu-id="ff716-115">In **Templates**, select **Windows Media Player Plug-in Wizard**.</span></span>
5.  <span data-ttu-id="ff716-116">Geben Sie einen Namen für das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="ff716-116">Enter a name for your project.</span></span>
6.  <span data-ttu-id="ff716-117">Geben Sie einen Speicherort für das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="ff716-117">Enter a location for your project.</span></span> <span data-ttu-id="ff716-118">Dies ist der Ordner, in den die Projektdateien kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff716-118">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="ff716-119">Klicken Sie auf **OK** , um den Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="ff716-119">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="ff716-120">Wählen Sie den Typ des Plug-ins aus, das Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ff716-120">Select the type of plug-in you want to create.</span></span>
9.  <span data-ttu-id="ff716-121">Vervollständigen Sie alle verbleibenden Dialogfelder im Assistenten.</span><span class="sxs-lookup"><span data-stu-id="ff716-121">Complete any remaining dialog boxes in the wizard.</span></span>
10. <span data-ttu-id="ff716-122">Verwenden Sie die Visual Studio-Entwicklungsumgebung, um Ihr Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff716-122">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="ff716-123">In Windows Vista und höher wird das Projekt nicht erfolgreich erstellt, es sei denn, Sie führen Visual Studio mit einem vollen Administrator Zugriffs Token aus.</span><span class="sxs-lookup"><span data-stu-id="ff716-123">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="ff716-124">Klicken Sie mit der rechten Maustaste auf den Namen oder das Symbol von Visual Studio, und klicken Sie auf **als Administrator ausführen**</span><span class="sxs-lookup"><span data-stu-id="ff716-124">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="ff716-125">Bevor Sie versuchen, das Projekt zu erstellen, stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung so konfigurieren, dass Sie auf die Ordner include und lib verweist, in denen Sie die Windows SDK installiert haben.</span><span class="sxs-lookup"><span data-stu-id="ff716-125">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="ff716-126">Der Compiler und Linker benötigen Zugriff auf einige der Dateien in diesen Ordnern.</span><span class="sxs-lookup"><span data-stu-id="ff716-126">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="ff716-127">Wenn Sie das Visual Studio-Registrierungs Dienstprogramm ausgeführt haben, das in der Windows SDK enthalten ist, wurde die Entwicklungsumgebung wahrscheinlich bereits so konfiguriert, dass Sie auf die Ordner Windows SDK include und lib verweist.</span><span class="sxs-lookup"><span data-stu-id="ff716-127">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="ff716-128">Andernfalls müssen Sie Ihre Entwicklungsumgebung manuell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ff716-128">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="ff716-129">Führen Sie die folgenden Schritte aus, um Visual Studio manuell zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ff716-129">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="ff716-130">Klicken Sie im Menü **Extras** auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="ff716-130">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="ff716-131">Klicken Sie auf **Projekte und Projekt** Mappen und dann auf **VC + +-Verzeichnisse**.</span><span class="sxs-lookup"><span data-stu-id="ff716-131">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="ff716-132">Klicken Sie unter **Verzeichnisse anzeigen für** auf Dateien oder **Bibliotheksdateien** **einschließen** .</span><span class="sxs-lookup"><span data-stu-id="ff716-132">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="ff716-133">Fügen Sie die Verzeichnisse für die erforderlichen Dateien hinzu.</span><span class="sxs-lookup"><span data-stu-id="ff716-133">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff716-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff716-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff716-135">Aufbauen eines Plug-ins</span><span class="sxs-lookup"><span data-stu-id="ff716-135">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> </dl>

 

 




