---
description: Veranschaulicht, wie ein Verb erstellt wird, das für shellelemente und Container funktioniert, die Elemente wieder gibt oder Elemente zu einer Warteschlange hinzufügen.
title: Player-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216420"
---
# <a name="player-verb-sample"></a><span data-ttu-id="332a2-103">Player-Verb (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="332a2-103">Player Verb Sample</span></span>

<span data-ttu-id="332a2-104">Veranschaulicht, wie ein Verb erstellt wird, das für shellelemente und Container funktioniert, die Elemente wieder gibt oder Elemente zu einer Warteschlange hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="332a2-104">Demonstrates how to create a verb that operates on Shell items and containers which plays items or adds items to a queue.</span></span> <span data-ttu-id="332a2-105">Dieses Beispiel ist besonders nützlich für Medienanwendungen.</span><span class="sxs-lookup"><span data-stu-id="332a2-105">This sample is particularly useful for media applications.</span></span>

<span data-ttu-id="332a2-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="332a2-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="332a2-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="332a2-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="332a2-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="332a2-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="332a2-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="332a2-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="332a2-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="332a2-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="332a2-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="332a2-111">Requirements</span></span>



| <span data-ttu-id="332a2-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="332a2-112">Product</span></span>                                | <span data-ttu-id="332a2-113">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="332a2-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="332a2-114">Windows</span><span class="sxs-lookup"><span data-stu-id="332a2-114">Windows</span></span>                                | <span data-ttu-id="332a2-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="332a2-115">Windows Vista</span></span>           |
| <span data-ttu-id="332a2-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="332a2-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="332a2-117">7.0</span><span class="sxs-lookup"><span data-stu-id="332a2-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="332a2-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="332a2-118">Downloading the Sample</span></span>

| <span data-ttu-id="332a2-119">Standort</span><span class="sxs-lookup"><span data-stu-id="332a2-119">Location</span></span>      | <span data-ttu-id="332a2-120">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="332a2-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332a2-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="332a2-121">GitHub</span></span>  | [<span data-ttu-id="332a2-122">Playerverb-Beispiel</span><span class="sxs-lookup"><span data-stu-id="332a2-122">PlayerVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a><span data-ttu-id="332a2-123">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="332a2-123">Building the Sample</span></span>

<span data-ttu-id="332a2-124">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="332a2-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="332a2-125">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **playerverbsample** .</span><span class="sxs-lookup"><span data-stu-id="332a2-125">Open the command prompt window and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="332a2-126">Geben Sie `msbuild PlayerVerbSample.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="332a2-126">Enter `msbuild PlayerVerbSample.sln`.</span></span>

<span data-ttu-id="332a2-127">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="332a2-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="332a2-128">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **playerverbsample** .</span><span class="sxs-lookup"><span data-stu-id="332a2-128">Open Windows Explorer and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="332a2-129">Doppelklicken Sie auf das Symbol für die Datei playerverbsample. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="332a2-129">Double-click the icon for the PlayerVerbSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="332a2-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="332a2-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="332a2-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="332a2-131">Running the Sample</span></span>

1.  <span data-ttu-id="332a2-132">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="332a2-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="332a2-133">Geben Sie in der Befehlszeile ein `PlayerVerbSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="332a2-133">At the command line, enter `PlayerVerbSample.exe`.</span></span> <span data-ttu-id="332a2-134">Alternativ können Sie in Windows-Explorer auf das Symbol für PlayerVerbSample.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="332a2-134">Alternatively, from Windows Explorer double-click the icon for PlayerVerbSample.exe.</span></span>
3.  <span data-ttu-id="332a2-135">Wählen Sie `Register Verbs` im Dialogfeld **Player Verb Sample** aus.</span><span class="sxs-lookup"><span data-stu-id="332a2-135">Select `Register Verbs` in the **Player Verb Sample** dialog.</span></span>
4.  <span data-ttu-id="332a2-136">Klicken Sie mit der rechten Maustaste auf Bildelemente (Datei, Ordner oder Stapel) in Windows-Explorer, um Sie einer Warteschlange hinzuzufügen, oder geben Sie Sie in der Beispielanwendung wieder.</span><span class="sxs-lookup"><span data-stu-id="332a2-136">Right-click picture items (file, folder, or stack) in Windows Explorer to add them to a queue or play them in the sample application.</span></span> <span data-ttu-id="332a2-137">Verwenden Sie Musik Elemente, wenn Sie das Beispiel ändern, um mit Musik zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="332a2-137">Use music items when you change the sample to work with music.</span></span>

 

 



