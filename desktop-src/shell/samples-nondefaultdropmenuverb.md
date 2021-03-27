---
description: Veranschaulicht, wie das Kontextmenü für Drag & amp; Drop (manchmal auch als Kontextmenü bezeichnet) erweitert wird.
title: NonDefaultDropMenuVerb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347929"
---
# <a name="nondefaultdropmenuverb-sample"></a><span data-ttu-id="c3613-103">NonDefaultDropMenuVerb (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="c3613-103">NonDefaultDropMenuVerb Sample</span></span>

<span data-ttu-id="c3613-104">Veranschaulicht, wie das Kontextmenü für Drag & amp; Drop (manchmal auch als Kontextmenü bezeichnet) erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="c3613-104">Demonstrates how to extend the drag-and-drop shortcut menu (sometimes referred to as a context menu).</span></span>

<span data-ttu-id="c3613-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c3613-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c3613-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3613-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c3613-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c3613-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c3613-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="c3613-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c3613-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c3613-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="c3613-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c3613-110">Requirements</span></span>



| <span data-ttu-id="c3613-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="c3613-111">Product</span></span>                                | <span data-ttu-id="c3613-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="c3613-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="c3613-113">Windows</span><span class="sxs-lookup"><span data-stu-id="c3613-113">Windows</span></span>                                | <span data-ttu-id="c3613-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3613-114">Windows Vista</span></span>           |
| <span data-ttu-id="c3613-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="c3613-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="c3613-116">7.0</span><span class="sxs-lookup"><span data-stu-id="c3613-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c3613-117">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c3613-117">Downloading the Sample</span></span>

| <span data-ttu-id="c3613-118">Standort</span><span class="sxs-lookup"><span data-stu-id="c3613-118">Location</span></span>      | <span data-ttu-id="c3613-119">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="c3613-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3613-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="c3613-120">GitHub</span></span>  | [<span data-ttu-id="c3613-121">Nondefaultdropmenuverb-Beispiel</span><span class="sxs-lookup"><span data-stu-id="c3613-121">NonDefaultDropMenuVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="c3613-122">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c3613-122">Building the Sample</span></span>

<span data-ttu-id="c3613-123">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="c3613-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="c3613-124">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **nondefaultdropmenuverb** .</span><span class="sxs-lookup"><span data-stu-id="c3613-124">Open the command prompt window and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="c3613-125">Geben Sie `msbuild NonDefaultDropMenuVerb.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="c3613-125">Enter `msbuild NonDefaultDropMenuVerb.sln`.</span></span>

<span data-ttu-id="c3613-126">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="c3613-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="c3613-127">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **nondefaultdropmenuverb** .</span><span class="sxs-lookup"><span data-stu-id="c3613-127">Open Windows Explorer and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="c3613-128">Doppelklicken Sie auf das Symbol für die Datei nondefaultdropmenuverb. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3613-128">Double-click the icon for the NonDefaultDropMenuVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="c3613-129">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c3613-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c3613-130">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c3613-130">Running the Sample</span></span>

1.  <span data-ttu-id="c3613-131">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue dll-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="c3613-131">Navigate to the directory that contains the new DLL file, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="c3613-132">Kopieren Sie NonDefaultDropMenuVerb.dll in das System Verzeichnis (z. b. C: \\ Windows \\ system32).</span><span class="sxs-lookup"><span data-stu-id="c3613-132">Copy NonDefaultDropMenuVerb.dll to the System directory (for example, C:\\Windows\\System32).</span></span>
3.  <span data-ttu-id="c3613-133">Geben Sie an einer Eingabeaufforderung ein `regedit NonDefaultDropMenuVerb.reg` .</span><span class="sxs-lookup"><span data-stu-id="c3613-133">At a command prompt, enter `regedit NonDefaultDropMenuVerb.reg`.</span></span>
4.  <span data-ttu-id="c3613-134">Ziehen Sie mit der rechten Maustaste eine Datei aus einem Ordner in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="c3613-134">Use the right mouse button to drag a file from one folder to another.</span></span> <span data-ttu-id="c3613-135">Weitere Menü Elemente für den Drop-Vorgang werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3613-135">You will see additional menu items for the drop operation.</span></span>

 

 



