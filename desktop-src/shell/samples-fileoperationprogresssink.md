---
description: Zeigt, wie die IFileOperationProgressSink-Schnittstellen Methoden zum Überwachen der Details von IFileOperation-Schnittstellen Aktionen verwendet werden.
title: Dateivorgangsfortschritt-Senke
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042425"
---
# <a name="file-operation-progress-sink"></a><span data-ttu-id="c73f6-103">Dateivorgangsfortschritt-Senke</span><span class="sxs-lookup"><span data-stu-id="c73f6-103">File Operation Progress Sink</span></span>

<span data-ttu-id="c73f6-104">Zeigt, wie die [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) -Schnittstellen Methoden zum Überwachen der Details von [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) -Schnittstellen Aktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c73f6-104">Demonstrates how to use the [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) interface methods for monitoring the details of [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) interface actions.</span></span>

<span data-ttu-id="c73f6-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c73f6-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c73f6-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c73f6-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c73f6-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c73f6-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c73f6-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="c73f6-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c73f6-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c73f6-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="c73f6-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c73f6-110">Requirements</span></span>



| <span data-ttu-id="c73f6-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="c73f6-111">Product</span></span>                                | <span data-ttu-id="c73f6-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="c73f6-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="c73f6-113">Windows</span><span class="sxs-lookup"><span data-stu-id="c73f6-113">Windows</span></span>                                | <span data-ttu-id="c73f6-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c73f6-114">Windows Vista</span></span>           |
| <span data-ttu-id="c73f6-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="c73f6-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="c73f6-116">6.1</span><span class="sxs-lookup"><span data-stu-id="c73f6-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c73f6-117">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c73f6-117">Downloading the Sample</span></span>

| <span data-ttu-id="c73f6-118">Standort</span><span class="sxs-lookup"><span data-stu-id="c73f6-118">Location</span></span>      | <span data-ttu-id="c73f6-119">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="c73f6-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c73f6-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="c73f6-120">GitHub</span></span>  | [<span data-ttu-id="c73f6-121">FileOperationProgressSink-Beispiel</span><span class="sxs-lookup"><span data-stu-id="c73f6-121">FileOperationProgressSink sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a><span data-ttu-id="c73f6-122">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c73f6-122">Building the Sample</span></span>

<span data-ttu-id="c73f6-123">So erstellen Sie das Beispiel über das Eingabe Aufforderungs Fenster:</span><span class="sxs-lookup"><span data-stu-id="c73f6-123">To build the sample from the command prompt window:</span></span>

1.  <span data-ttu-id="c73f6-124">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **FileOperationProgressSink** .</span><span class="sxs-lookup"><span data-stu-id="c73f6-124">Open the command prompt window and navigate to the **FileOperationProgressSink** project directory.</span></span>
2.  <span data-ttu-id="c73f6-125">Geben Sie `msbuild FileOperationProgressSinkSample.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="c73f6-125">Enter `msbuild FileOperationProgressSinkSample.sln`.</span></span>

<span data-ttu-id="c73f6-126">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="c73f6-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="c73f6-127">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **FilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="c73f6-127">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="c73f6-128">Der vollständige Standard Installationspfad lautet beispielsweise `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .</span><span class="sxs-lookup"><span data-stu-id="c73f6-128">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample`.</span></span>
2.  <span data-ttu-id="c73f6-129">Doppelklicken Sie auf das Symbol für die Datei "FileOperationProgressSink Sample. sln", um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c73f6-129">Double-click the icon for the FileOperationProgressSinkSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="c73f6-130">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c73f6-130">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="c73f6-131">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c73f6-131">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="c73f6-132">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c73f6-132">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c73f6-133">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c73f6-133">Running the Sample</span></span>

1.  <span data-ttu-id="c73f6-134">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="c73f6-134">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="c73f6-135">Geben Sie an der Eingabeaufforderung ein, `FileOperationProgressSinkSample.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für FileOperationProgressSinkSample.exe.</span><span class="sxs-lookup"><span data-stu-id="c73f6-135">At the command prompt, enter `FileOperationProgressSinkSample.exe`, or from Windows Explorer, double-click the icon for FileOperationProgressSinkSample.exe.</span></span>

 

 



