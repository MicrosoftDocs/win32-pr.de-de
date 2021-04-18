---
title: Kompilieren des Beispielprojekts
description: Kompilieren des Beispielprojekts
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player Online Stores, Kompilieren von Beispielprojekten
- Online Stores, Kompilieren von Beispielprojekten
- Typ 2 Online Stores, Kompilieren von Beispielprojekten
- Windows Media Player Online Stores, Beispiel Projekte
- Online Stores, Beispiel Projekte
- Typ 2 Online Stores, Beispiel Projekte
- Windows Media Player Online Stores, Projekt-Assistent
- Online Stores, Projekt-Assistent
- Typ 2 Online Stores, Projekt-Assistent
- Plug-ins, Projekt-Assistent
- Windows Media Player-Plug-ins, Projekt-Assistent
- Kompilieren von Beispielprojekten
- Beispiele, Typ 2 Online Stores
- Projekt-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340220"
---
# <a name="compiling-the-sample-project"></a><span data-ttu-id="b540c-117">Kompilieren des Beispielprojekts</span><span class="sxs-lookup"><span data-stu-id="b540c-117">Compiling the Sample Project</span></span>

<span data-ttu-id="b540c-118">Der Assistent generiert alle Dateien, die Sie benötigen, um das Beispiel Projekt zu kompilieren, sodass Sie die standardmäßigen Projekteinstellungen nicht ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="b540c-118">The wizard generates all the files you need to compile the sample project, so you shouldn't need to change the default project settings.</span></span> <span data-ttu-id="b540c-119">Klicken Sie in Visual Studio im Menü **Erstellen** auf Projekt Mappe **Erstellen** , um die COM-Komponente zu erstellen und zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b540c-119">In Visual Studio, from the **Build** menu, click **Build Solution** to build and register the COM component.</span></span> <span data-ttu-id="b540c-120">Standardmäßig ist die Debug-Konfiguration aktiv.</span><span class="sxs-lookup"><span data-stu-id="b540c-120">By default, the Debug configuration is active.</span></span>

> [!Note]  
> <span data-ttu-id="b540c-121">In Windows Vista und höher wird das Projekt nicht erfolgreich erstellt, es sei denn, Sie führen Visual Studio mit einem vollen Administrator Zugriffs Token aus.</span><span class="sxs-lookup"><span data-stu-id="b540c-121">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="b540c-122">Klicken Sie mit der rechten Maustaste auf den Namen oder das Symbol von Visual Studio, und klicken Sie auf **als Administrator ausführen**</span><span class="sxs-lookup"><span data-stu-id="b540c-122">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

 

<span data-ttu-id="b540c-123">Bevor Sie versuchen, das Projekt zu erstellen, stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung so konfigurieren, dass Sie auf die Ordner include und lib verweist, in denen Sie die Windows SDK installiert haben.</span><span class="sxs-lookup"><span data-stu-id="b540c-123">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="b540c-124">Der Compiler und Linker benötigen Zugriff auf einige der Dateien in diesen Ordnern.</span><span class="sxs-lookup"><span data-stu-id="b540c-124">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="b540c-125">Wenn Sie das Visual Studio-Registrierungsprogramm ausgeführt haben, das im Windows Vista SDK enthalten ist, wurde Ihre Entwicklungsumgebung wahrscheinlich bereits so konfiguriert, dass Sie auf die Windows SDK include-und lib-Ordner verweist.</span><span class="sxs-lookup"><span data-stu-id="b540c-125">If you ran the Visual Studio Registration utility that comes with the Windows Vista SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="b540c-126">Andernfalls müssen Sie Ihre Entwicklungsumgebung manuell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b540c-126">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="b540c-127">Führen Sie die folgenden Schritte aus, um Visual Studio manuell zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b540c-127">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="b540c-128">Klicken Sie im Menü **Extras** auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="b540c-128">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="b540c-129">Klicken Sie auf **Projekte und Projekt** Mappen und dann auf **VC + +-Verzeichnisse**.</span><span class="sxs-lookup"><span data-stu-id="b540c-129">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="b540c-130">Klicken Sie unter **Verzeichnisse anzeigen für** auf Dateien oder **Bibliotheksdateien** **einschließen** .</span><span class="sxs-lookup"><span data-stu-id="b540c-130">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="b540c-131">Fügen Sie die Verzeichnisse für die erforderlichen Dateien hinzu.</span><span class="sxs-lookup"><span data-stu-id="b540c-131">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b540c-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b540c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b540c-133">Entwickeln des Plug-Ins für einen Typ 2-Online Store</span><span class="sxs-lookup"><span data-stu-id="b540c-133">Building the Plug-in for a Type 2 Online Store</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




