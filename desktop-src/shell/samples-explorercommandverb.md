---
description: Veranschaulicht, wie ein shellverb mithilfe der Methoden explorercommand und explorercommandstate implementiert wird.
title: Explorer-Befehl-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868304"
---
# <a name="explorer-command-verb-sample"></a><span data-ttu-id="7d172-103">Explorer-Befehl-Verb (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="7d172-103">Explorer Command Verb Sample</span></span>

<span data-ttu-id="7d172-104">Veranschaulicht, wie ein shellverb mithilfe der Methoden explorercommand und explorercommandstate implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="7d172-104">Demonstrates how to implement a Shell verb using the ExplorerCommand and ExplorerCommandState methods.</span></span>

<span data-ttu-id="7d172-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="7d172-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7d172-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d172-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7d172-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d172-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="7d172-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="7d172-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="7d172-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d172-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="7d172-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7d172-110">Requirements</span></span>



| <span data-ttu-id="7d172-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="7d172-111">Product</span></span>                                | <span data-ttu-id="7d172-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="7d172-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="7d172-113">Windows</span><span class="sxs-lookup"><span data-stu-id="7d172-113">Windows</span></span>                                | <span data-ttu-id="7d172-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d172-114">Windows Vista</span></span>           |
| <span data-ttu-id="7d172-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="7d172-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="7d172-116">7.0</span><span class="sxs-lookup"><span data-stu-id="7d172-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7d172-117">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d172-117">Downloading the Sample</span></span>

| <span data-ttu-id="7d172-118">Standort</span><span class="sxs-lookup"><span data-stu-id="7d172-118">Location</span></span>      | <span data-ttu-id="7d172-119">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="7d172-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d172-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="7d172-120">GitHub</span></span>  | [<span data-ttu-id="7d172-121">Explorercommandverb-Beispiel</span><span class="sxs-lookup"><span data-stu-id="7d172-121">ExplorerCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="7d172-122">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d172-122">Building the Sample</span></span>

<span data-ttu-id="7d172-123">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="7d172-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="7d172-124">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **explorercommandverb** .</span><span class="sxs-lookup"><span data-stu-id="7d172-124">Open the command prompt window and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="7d172-125">Geben Sie `msbuild ExplorerCommandVerb.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="7d172-125">Enter `msbuild ExplorerCommandVerb.sln`.</span></span>

<span data-ttu-id="7d172-126">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="7d172-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="7d172-127">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **explorercommandverb** .</span><span class="sxs-lookup"><span data-stu-id="7d172-127">Open Windows Explorer and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="7d172-128">Doppelklicken Sie auf das Symbol für die Datei explorercommandverb. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7d172-128">Double-click the icon for the ExplorerCommandVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="7d172-129">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="7d172-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7d172-130">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d172-130">Running the Sample</span></span>

1.  <span data-ttu-id="7d172-131">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die ExplorerCommandVerb.dll enthält.</span><span class="sxs-lookup"><span data-stu-id="7d172-131">Navigate to the directory that contains the ExplorerCommandVerb.dll, using the command prompt or Windows Explorer.</span></span> <span data-ttu-id="7d172-132">Stellen Sie sicher, dass Sie die 64-Bit-DLL-Datei auf 64-Bit-Windows verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d172-132">Make sure you use the 64-bit DLL file on 64-bit Windows.</span></span>
2.  <span data-ttu-id="7d172-133">Geben Sie in der Befehlszeile ein `regsvr32.exe ExplorerCommandVerb.dll` .</span><span class="sxs-lookup"><span data-stu-id="7d172-133">At the command line, enter `regsvr32.exe ExplorerCommandVerb.dll`.</span></span>
3.  <span data-ttu-id="7d172-134">Wenn Sie mit der rechten Maustaste auf eine txt-Datei klicken, werden zwei neue Verben im Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d172-134">Two new verbs will be shown on the context menu when you right-click a .txt file.</span></span>

 

 



