---
description: Veranschaulicht, wie ein shellverb mithilfe der ExecuteCommand-Methode implementiert wird.
title: „Befehl ausführen“-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2deeb63fc6648d07b3d870888d6d2eabc6fb0490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218709"
---
# <a name="execute-command-verb-sample"></a><span data-ttu-id="9a0cc-103">„Befehl ausführen“-Verb (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="9a0cc-103">Execute Command Verb Sample</span></span>

<span data-ttu-id="9a0cc-104">Veranschaulicht, wie ein shellverb mithilfe der ExecuteCommand-Methode implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-104">Demonstrates how to implement a Shell verb using the ExecuteCommand method.</span></span>

<span data-ttu-id="9a0cc-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9a0cc-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9a0cc-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a0cc-106">Description</span></span>](#description)
-   [<span data-ttu-id="9a0cc-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a0cc-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9a0cc-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9a0cc-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="9a0cc-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="9a0cc-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="9a0cc-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9a0cc-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="9a0cc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a0cc-111">Description</span></span>

<span data-ttu-id="9a0cc-112">Diese Methode wird für Verb Implementierungen bevorzugt, da Sie die größtmögliche Flexibilität bietet, einfach ist und die Prozess interne Aktivierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-112">This method is preferred for verb implementations because it provides the most flexibility, is simple, and supports out-of-process activation.</span></span> <span data-ttu-id="9a0cc-113">In diesem Beispiel wird ein eigenständiges com-Objekt (Local Server Component Object Model) implementiert. es wird jedoch erwartet, dass die Verb-Implementierung in vorhandene Anwendungen integriert wird.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-113">This sample implements a standalone, local server Component Object Model (COM) object, but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="9a0cc-114">Zu diesem Zweck muss das Haupt Anwendungs Objekt eine Klassenfactory für sich selbst registrieren.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-114">To do so, your main application object must register a class factory for itself.</span></span> <span data-ttu-id="9a0cc-115">Dieses Objekt implementiert [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) für die Verben Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-115">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="9a0cc-116">Beachten Sie, dass die Anwendung von com gestartet wird, wenn Sie nicht bereits ausgeführt wird, sondern eine Verbindung mit einer laufenden Instanz der Anwendung herstellt, wenn eine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-116">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0cc-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9a0cc-117">Requirements</span></span>



| <span data-ttu-id="9a0cc-118">Produkt</span><span class="sxs-lookup"><span data-stu-id="9a0cc-118">Product</span></span>                                | <span data-ttu-id="9a0cc-119">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="9a0cc-119">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="9a0cc-120">Windows</span><span class="sxs-lookup"><span data-stu-id="9a0cc-120">Windows</span></span>                                | <span data-ttu-id="9a0cc-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9a0cc-121">Windows 7</span></span>               |
| <span data-ttu-id="9a0cc-122">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="9a0cc-122">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="9a0cc-123">7.0</span><span class="sxs-lookup"><span data-stu-id="9a0cc-123">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9a0cc-124">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9a0cc-124">Downloading the Sample</span></span>

| <span data-ttu-id="9a0cc-125">Standort</span><span class="sxs-lookup"><span data-stu-id="9a0cc-125">Location</span></span>      | <span data-ttu-id="9a0cc-126">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="9a0cc-126">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0cc-127">GitHub</span><span class="sxs-lookup"><span data-stu-id="9a0cc-127">GitHub</span></span>  | [<span data-ttu-id="9a0cc-128">Executecommandverb-Beispiel</span><span class="sxs-lookup"><span data-stu-id="9a0cc-128">ExecuteCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="9a0cc-129">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9a0cc-129">Building the Sample</span></span>

<span data-ttu-id="9a0cc-130">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="9a0cc-130">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="9a0cc-131">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **executecommandverb** .</span><span class="sxs-lookup"><span data-stu-id="9a0cc-131">Open the command prompt window and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="9a0cc-132">Geben Sie `msbuild ExecuteCommand.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-132">Enter `msbuild ExecuteCommand.sln`.</span></span>

<span data-ttu-id="9a0cc-133">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="9a0cc-133">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="9a0cc-134">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **executecommandverb** .</span><span class="sxs-lookup"><span data-stu-id="9a0cc-134">Open Windows Explorer and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="9a0cc-135">Doppelklicken Sie auf das Symbol für die Datei ExecuteCommand. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-135">Double-click the icon for the ExecuteCommand.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="9a0cc-136">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-136">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="9a0cc-137">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9a0cc-137">Running the Sample</span></span>

1.  <span data-ttu-id="9a0cc-138">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-138">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="9a0cc-139">Geben Sie in der Befehlszeile ein `ExecuteCommand.exe` .</span><span class="sxs-lookup"><span data-stu-id="9a0cc-139">At the command line, enter `ExecuteCommand.exe`.</span></span> <span data-ttu-id="9a0cc-140">Alternativ können Sie in Windows-Explorer auf das Symbol für ExecuteCommand.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-140">Alternatively, from Windows Explorer double-click the icon for ExecuteCommand.exe.</span></span>
3.  <span data-ttu-id="9a0cc-141">Befolgen Sie die Anweisungen im angezeigten Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9a0cc-141">Follow the instructions in the displayed dialog</span></span>

 

 
