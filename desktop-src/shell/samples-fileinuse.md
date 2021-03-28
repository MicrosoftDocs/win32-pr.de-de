---
description: Veranschaulicht, wie das Dialogfeld "Datei in Verwendung" angepasst wird, um zusätzliche Informationen und Optionen für Dateien anzuzeigen, die zurzeit in der Anwendung geöffnet sind.
title: Datei wird verwendet (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223e0addf201f3526654a17346963b4639e0d215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345928"
---
# <a name="file-is-in-use-sample"></a><span data-ttu-id="9c9aa-103">Datei wird verwendet (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-103">File Is In Use Sample</span></span>

<span data-ttu-id="9c9aa-104">Veranschaulicht, wie das Dialogfeld " **Datei in Verwendung** " angepasst wird, um zusätzliche Informationen und Optionen für Dateien anzuzeigen, die zurzeit in der Anwendung geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-104">Demonstrates how to customize the **File In Use** dialog to display additional information and options for files that are currently opened in the application.</span></span>

<span data-ttu-id="9c9aa-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9c9aa-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c9aa-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9c9aa-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9c9aa-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="9c9aa-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="9c9aa-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="9c9aa-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9c9aa-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="9c9aa-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-110">Requirements</span></span>



| <span data-ttu-id="9c9aa-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="9c9aa-111">Product</span></span>                                | <span data-ttu-id="9c9aa-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="9c9aa-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="9c9aa-113">Windows</span><span class="sxs-lookup"><span data-stu-id="9c9aa-113">Windows</span></span>                                | <span data-ttu-id="9c9aa-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c9aa-114">Windows Vista</span></span>           |
| <span data-ttu-id="9c9aa-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="9c9aa-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="9c9aa-116">6.1</span><span class="sxs-lookup"><span data-stu-id="9c9aa-116">6.1</span></span>                     |



 

<span data-ttu-id="9c9aa-117">Weitere Anforderungen finden Sie in dersample.docx Datei "iatleisinuse", \_ die im Beispiel enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-117">For additional requirements, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="9c9aa-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9c9aa-118">Downloading the Sample</span></span>

| <span data-ttu-id="9c9aa-119">Standort</span><span class="sxs-lookup"><span data-stu-id="9c9aa-119">Location</span></span>      | <span data-ttu-id="9c9aa-120">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="9c9aa-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9aa-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="9c9aa-121">GitHub</span></span>  | [<span data-ttu-id="9c9aa-122">Beispiel für "fleisinuse"</span><span class="sxs-lookup"><span data-stu-id="9c9aa-122">FileIsInUse sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a><span data-ttu-id="9c9aa-123">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9c9aa-123">Building the Sample</span></span>

<span data-ttu-id="9c9aa-124">So erstellen Sie das Beispiel über das Eingabe Aufforderungs Fenster:</span><span class="sxs-lookup"><span data-stu-id="9c9aa-124">To build the sample from the Command Prompt window:</span></span>

1.  <span data-ttu-id="9c9aa-125">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis " **fleisinuse** ".</span><span class="sxs-lookup"><span data-stu-id="9c9aa-125">Open the Command Prompt window and navigate to the **FileIsInUse** project directory.</span></span>
2.  <span data-ttu-id="9c9aa-126">Geben Sie `msbuild FileIsInUse.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-126">Enter `msbuild FileIsInUse.sln`.</span></span>

<span data-ttu-id="9c9aa-127">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="9c9aa-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="9c9aa-128">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **FilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="9c9aa-128">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="9c9aa-129">Der vollständige Standard Installationspfad lautet beispielsweise `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .</span><span class="sxs-lookup"><span data-stu-id="9c9aa-129">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse`.</span></span>
2.  <span data-ttu-id="9c9aa-130">Doppelklicken Sie auf das Symbol für die Datei "Datei" "" ", um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-130">Double-click the icon for the FileIsInUseSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="9c9aa-131">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-131">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="9c9aa-132">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-132">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="9c9aa-133">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="9c9aa-134">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="9c9aa-134">Running the Sample</span></span>

1.  <span data-ttu-id="9c9aa-135">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-135">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="9c9aa-136">Geben Sie an der Eingabeaufforderung ein, `FileIsInUseSample.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für FileIsInUseSample.exe.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-136">At the command prompt, enter `FileIsInUseSample.exe`, or from Windows Explorer, double-click the icon for FileIsInUseSample.exe.</span></span>

<span data-ttu-id="9c9aa-137">Ausführliche Informationen zu diesem Codebeispiel finden Sie in der Datei "ifleisinusesample.docx", \_ die im Beispiel enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9c9aa-137">For detailed information about this code sample, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

 

 



