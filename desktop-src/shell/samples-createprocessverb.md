---
description: Veranschaulicht die Implementierung eines shellverbs mithilfe der Methode "Methode".
title: CreateProcess-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980329"
---
# <a name="createprocess-verb-sample"></a><span data-ttu-id="12c78-103">CreateProcess-Verb (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="12c78-103">CreateProcess Verb Sample</span></span>

<span data-ttu-id="12c78-104">Veranschaulicht die Implementierung eines shellverbs mithilfe der Methode "Methode".</span><span class="sxs-lookup"><span data-stu-id="12c78-104">Demonstrates how to implement a Shell verb using the CreateProcess method.</span></span>

<span data-ttu-id="12c78-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="12c78-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="12c78-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12c78-106">Description</span></span>](#description)
-   [<span data-ttu-id="12c78-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12c78-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="12c78-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="12c78-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="12c78-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="12c78-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="12c78-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="12c78-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="12c78-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12c78-111">Description</span></span>

<span data-ttu-id="12c78-112">Auf dem Prozess basierende Verben sind von der Ausführung einer ausführbaren Datei und der Übergabe eines Befehlszeilen Arguments abhängig.</span><span class="sxs-lookup"><span data-stu-id="12c78-112">CreateProcess-based verbs depend on running a executable and passing it a command-line argument.</span></span> <span data-ttu-id="12c78-113">Diese Methode ist nicht so leistungsfähig wie die Methoden "DropTarget" und "ExecuteCommand", aber Sie erreicht das wünschenswert Verhalten außerhalb des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="12c78-113">This method is not as powerful as the DropTarget and ExecuteCommand methods but it does achieve the desirable out-of-process behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="12c78-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="12c78-114">Requirements</span></span>



| <span data-ttu-id="12c78-115">Produkt</span><span class="sxs-lookup"><span data-stu-id="12c78-115">Product</span></span>                                | <span data-ttu-id="12c78-116">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="12c78-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="12c78-117">Windows</span><span class="sxs-lookup"><span data-stu-id="12c78-117">Windows</span></span>                                | <span data-ttu-id="12c78-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12c78-118">Windows Vista</span></span>           |
| <span data-ttu-id="12c78-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="12c78-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="12c78-120">7.0</span><span class="sxs-lookup"><span data-stu-id="12c78-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="12c78-121">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="12c78-121">Downloading the Sample</span></span>

| <span data-ttu-id="12c78-122">Standort</span><span class="sxs-lookup"><span data-stu-id="12c78-122">Location</span></span>      | <span data-ttu-id="12c78-123">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="12c78-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12c78-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="12c78-124">GitHub</span></span>  | [<span data-ttu-id="12c78-125">Beispiel für "kreateprocessverb"</span><span class="sxs-lookup"><span data-stu-id="12c78-125">CreateProcessVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="12c78-126">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="12c78-126">Building the Sample</span></span>

<span data-ttu-id="12c78-127">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="12c78-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="12c78-128">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie **zum Projektverzeichnis** für das Projekt "Projekt".</span><span class="sxs-lookup"><span data-stu-id="12c78-128">Open the command prompt window and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="12c78-129">Geben Sie `msbuild CreateProcessVerb.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="12c78-129">Enter `msbuild CreateProcessVerb.sln`.</span></span>

<span data-ttu-id="12c78-130">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="12c78-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="12c78-131">Öffnen Sie Windows-Explorer, und navigieren Sie **zum Projektverzeichnis** für das Projekt "Projekt".</span><span class="sxs-lookup"><span data-stu-id="12c78-131">Open Windows Explorer and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="12c78-132">Doppelklicken Sie auf das Symbol für die Datei "Datei" in Visual Studio, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="12c78-132">Double-click the icon for the CreateProcessVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="12c78-133">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="12c78-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="12c78-134">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="12c78-134">Running the Sample</span></span>

1.  <span data-ttu-id="12c78-135">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="12c78-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="12c78-136">Geben Sie in der Befehlszeile ein `CreateProcessVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="12c78-136">At the command line, enter `CreateProcessVerb.exe`.</span></span> <span data-ttu-id="12c78-137">Alternativ können Sie in Windows-Explorer auf das Symbol für CreateProcessVerb.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="12c78-137">Alternatively, from Windows Explorer double-click the icon for CreateProcessVerb.exe.</span></span>
3.  <span data-ttu-id="12c78-138">Befolgen Sie die Anweisungen im angezeigten Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="12c78-138">Follow the instructions in the displayed dialog</span></span>

 

 



