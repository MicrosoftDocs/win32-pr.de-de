---
description: Veranschaulicht, wie ein shellverb mithilfe der DropTarget-Methode implementiert wird.
title: DropTarget-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979936"
---
# <a name="droptarget-verb-sample"></a><span data-ttu-id="b50f9-103">DropTarget-Verb (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="b50f9-103">DropTarget Verb Sample</span></span>

<span data-ttu-id="b50f9-104">Veranschaulicht, wie ein shellverb mithilfe der DropTarget-Methode implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b50f9-104">Demonstrates how to implement a Shell verb using the DropTarget method.</span></span>

<span data-ttu-id="b50f9-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="b50f9-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b50f9-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b50f9-106">Description</span></span>](#description)
-   [<span data-ttu-id="b50f9-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b50f9-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b50f9-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b50f9-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b50f9-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="b50f9-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b50f9-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b50f9-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="b50f9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b50f9-111">Description</span></span>

<span data-ttu-id="b50f9-112">In diesem Beispiel wird gezeigt, wie ein shellverb mithilfe der DropTarget-Methode implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b50f9-112">This sample shows how to implement a Shell verb using the DropTarget method.</span></span> <span data-ttu-id="b50f9-113">Diese Methode wird für Verb Implementierungen bevorzugt, die unter Windows XP funktionieren müssen.</span><span class="sxs-lookup"><span data-stu-id="b50f9-113">This method is preferred for verb implementations that must work on Windows XP.</span></span> <span data-ttu-id="b50f9-114">In diesem Beispiel wird ein eigenständiges com-Objekt (Local Server Component Object Model) implementiert. es wird jedoch erwartet, dass die Verb-Implementierung in vorhandene Anwendungen integriert wird.</span><span class="sxs-lookup"><span data-stu-id="b50f9-114">This sample implements a standalone local server Component Object Model (COM) object but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="b50f9-115">Zu diesem Zweck registriert Ihr Haupt Anwendungs Objekt eine Klassenfactory für sich selbst.</span><span class="sxs-lookup"><span data-stu-id="b50f9-115">To do so, your main application object registers a class factory for itself.</span></span> <span data-ttu-id="b50f9-116">Dieses Objekt implementiert [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) für die Verben Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b50f9-116">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="b50f9-117">Beachten Sie, dass die Anwendung von com gestartet wird, wenn Sie nicht bereits ausgeführt wird, sondern eine Verbindung mit einer laufenden Instanz der Anwendung herstellt, wenn eine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b50f9-117">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="b50f9-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b50f9-118">Requirements</span></span>



| <span data-ttu-id="b50f9-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="b50f9-119">Product</span></span>                                | <span data-ttu-id="b50f9-120">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="b50f9-120">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="b50f9-121">Windows</span><span class="sxs-lookup"><span data-stu-id="b50f9-121">Windows</span></span>                                | <span data-ttu-id="b50f9-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b50f9-122">Windows Vista</span></span>           |
| <span data-ttu-id="b50f9-123">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="b50f9-123">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="b50f9-124">7.0</span><span class="sxs-lookup"><span data-stu-id="b50f9-124">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b50f9-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b50f9-125">Downloading the Sample</span></span>

| <span data-ttu-id="b50f9-126">Standort</span><span class="sxs-lookup"><span data-stu-id="b50f9-126">Location</span></span>      | <span data-ttu-id="b50f9-127">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="b50f9-127">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b50f9-128">GitHub</span><span class="sxs-lookup"><span data-stu-id="b50f9-128">GitHub</span></span>  | [<span data-ttu-id="b50f9-129">Droptargetverb-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b50f9-129">DropTargetVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="b50f9-130">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b50f9-130">Building the Sample</span></span>

<span data-ttu-id="b50f9-131">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="b50f9-131">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="b50f9-132">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **droptargetverb** .</span><span class="sxs-lookup"><span data-stu-id="b50f9-132">Open the command prompt window and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="b50f9-133">Geben Sie `msbuild DropTargetVerb.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="b50f9-133">Enter `msbuild DropTargetVerb.sln`.</span></span>

<span data-ttu-id="b50f9-134">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="b50f9-134">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="b50f9-135">Öffnen Sie Windows-Explorer, und navigieren Sie zum **droptargetverb** -Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b50f9-135">Open Windows Explorer and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="b50f9-136">Doppelklicken Sie auf das Symbol für die Datei droptargetverb. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b50f9-136">Double-click the icon for the DropTargetVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="b50f9-137">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b50f9-137">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b50f9-138">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="b50f9-138">Running the Sample</span></span>

1.  <span data-ttu-id="b50f9-139">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="b50f9-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="b50f9-140">Geben Sie in der Befehlszeile ein `DropTargetVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="b50f9-140">At the command line, enter `DropTargetVerb.exe`.</span></span> <span data-ttu-id="b50f9-141">Alternativ können Sie in Windows-Explorer auf das Symbol für DropTargetVerb.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="b50f9-141">Alternatively, from Windows Explorer double-click the icon for DropTargetVerb.exe.</span></span>
3.  <span data-ttu-id="b50f9-142">Befolgen Sie die Anweisungen im angezeigten Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="b50f9-142">Follow the instructions in the displayed dialog</span></span>

 

 
