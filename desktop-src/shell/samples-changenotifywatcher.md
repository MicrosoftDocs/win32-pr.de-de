---
description: Veranschaulicht das Lauschen auf shelländerungbenachrichtigungen für einen Ordner oder ein Element im Windows Explorer-Namespace.
title: Benachrichtigungsüberwachung ändern (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217208"
---
# <a name="change-notify-watcher-sample"></a><span data-ttu-id="129fd-103">Benachrichtigungsüberwachung ändern (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="129fd-103">Change Notify Watcher Sample</span></span>

<span data-ttu-id="129fd-104">Veranschaulicht das Lauschen auf shelländerungbenachrichtigungen für einen Ordner oder ein Element im Windows Explorer-Namespace.</span><span class="sxs-lookup"><span data-stu-id="129fd-104">Demonstrates how to listen to Shell change notifications on a folder or item in the Windows Explorer namespace.</span></span>

<span data-ttu-id="129fd-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="129fd-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="129fd-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="129fd-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="129fd-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="129fd-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="129fd-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="129fd-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="129fd-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="129fd-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="129fd-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="129fd-110">Requirements</span></span>



| <span data-ttu-id="129fd-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="129fd-111">Product</span></span>                                | <span data-ttu-id="129fd-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="129fd-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="129fd-113">Windows</span><span class="sxs-lookup"><span data-stu-id="129fd-113">Windows</span></span>                                | <span data-ttu-id="129fd-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="129fd-114">Windows Vista</span></span>           |
| <span data-ttu-id="129fd-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="129fd-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="129fd-116">7.0</span><span class="sxs-lookup"><span data-stu-id="129fd-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="129fd-117">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="129fd-117">Downloading the Sample</span></span>

| <span data-ttu-id="129fd-118">Standort</span><span class="sxs-lookup"><span data-stu-id="129fd-118">Location</span></span>      | <span data-ttu-id="129fd-119">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="129fd-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="129fd-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="129fd-120">GitHub</span></span>  | [<span data-ttu-id="129fd-121">Changenotifywatcher-Beispiel</span><span class="sxs-lookup"><span data-stu-id="129fd-121">ChangeNotifyWatcher sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a><span data-ttu-id="129fd-122">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="129fd-122">Building the Sample</span></span>

<span data-ttu-id="129fd-123">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="129fd-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="129fd-124">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis " **changenotifywatcher** ".</span><span class="sxs-lookup"><span data-stu-id="129fd-124">Open the command prompt window and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="129fd-125">Geben Sie `msbuild ChangeNotifyWatcher.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="129fd-125">Enter `msbuild ChangeNotifyWatcher.sln`.</span></span>

<span data-ttu-id="129fd-126">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="129fd-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="129fd-127">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis " **changenotifywatcher** ".</span><span class="sxs-lookup"><span data-stu-id="129fd-127">Open Windows Explorer and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="129fd-128">Doppelklicken Sie auf das Symbol für die Datei "changenotifywatcher. sln", um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="129fd-128">Double-click the icon for the ChangeNotifyWatcher.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="129fd-129">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="129fd-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="129fd-130">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="129fd-130">Running the Sample</span></span>

1.  <span data-ttu-id="129fd-131">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="129fd-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="129fd-132">Geben Sie an der Eingabeaufforderung `ChangeNotifyWatcher.exe` ein.</span><span class="sxs-lookup"><span data-stu-id="129fd-132">At the command prompt, enter `ChangeNotifyWatcher.exe`.</span></span> <span data-ttu-id="129fd-133">Alternativ können Sie in Windows-Explorer auf das Symbol für ChangeNotifyWatcher.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="129fd-133">Alternatively, from Windows Explorer double-click the icon for ChangeNotifyWatcher.exe.</span></span>
3.  <span data-ttu-id="129fd-134">Um die Auswirkung zu veranschaulichen, wählen App-Benutzer Modell-IDs (appusermudelids) einen zu überwachenden Ordner aus, indem Sie entweder auf **"Pick..."** klicken oder Drag & amp; Drop für einen Ordner aus einem Windows-Explorer-Fenster in die Listenansicht des Beispiels anwenden.</span><span class="sxs-lookup"><span data-stu-id="129fd-134">To demonstrate the effect, Application User Model IDs (AppUserModelIDs) select a folder to watch by either clicking **"Pick..."** or by using drag-and-drop on a folder from a Windows Explorer window into the sample's list view.</span></span>

 

 



