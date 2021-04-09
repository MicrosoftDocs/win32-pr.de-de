---
title: Info leisten Beispiel
ms.assetid: f26c0819-523d-42a5-be2f-3cd75748b4a6
description: Weitere Informationen finden Sie im Beispiel zu Rebar.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72b58a66c22b0ef8cc60d97c0965a8ae29a20fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958195"
---
# <a name="rebar-sample"></a><span data-ttu-id="e3ef6-103">Info leisten Beispiel</span><span class="sxs-lookup"><span data-stu-id="e3ef6-103">Rebar Sample</span></span>

<span data-ttu-id="e3ef6-104">In diesem Thema wird das Beispielcode Beispiel für die Grund Leiste beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e3ef6-104">This topic describes the Rebar Sample code sample.</span></span> <span data-ttu-id="e3ef6-105">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="e3ef6-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="e3ef6-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3ef6-106">Description</span></span>](#description)
-   [<span data-ttu-id="e3ef6-107">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="e3ef6-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="e3ef6-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="e3ef6-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="e3ef6-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="e3ef6-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="e3ef6-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3ef6-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="e3ef6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3ef6-111">Description</span></span>

<span data-ttu-id="e3ef6-112">Das Grund leisten-Beispiel zeigt, wie Sie ein einfaches Grundsteuer Element für die Grund Leiste in einer Anwendung implementieren.</span><span class="sxs-lookup"><span data-stu-id="e3ef6-112">The Rebar Sample shows how to implement a simple rebar common control in an application.</span></span> <span data-ttu-id="e3ef6-113">In diesem Beispiel wird ein Grund leisten-Steuerelement mit zwei Bändern erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3ef6-113">This example creates a rebar control that has two bands.</span></span> <span data-ttu-id="e3ef6-114">Eine enthält ein Kombinations Feld, das andere enthält eine Schaltfläche "Push".</span><span class="sxs-lookup"><span data-stu-id="e3ef6-114">One contains a combo box and the other contains a push button.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="e3ef6-115">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="e3ef6-115">Minimum Requirements</span></span>



| <span data-ttu-id="e3ef6-116">Produkt</span><span class="sxs-lookup"><span data-stu-id="e3ef6-116">Product</span></span>          | <span data-ttu-id="e3ef6-117">Version</span><span class="sxs-lookup"><span data-stu-id="e3ef6-117">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="e3ef6-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e3ef6-118">DLL</span></span>              | <span data-ttu-id="e3ef6-119">comctl32.dll Version 4,71</span><span class="sxs-lookup"><span data-stu-id="e3ef6-119">comctl32.dll version 4.71</span></span>             |
| <span data-ttu-id="e3ef6-120">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="e3ef6-120">Operating System</span></span> | <span data-ttu-id="e3ef6-121">Windows 95 mit Internet Explorer 4,0</span><span class="sxs-lookup"><span data-stu-id="e3ef6-121">Windows 95 with Internet Explorer 4.0</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e3ef6-122">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="e3ef6-122">Downloading the Sample</span></span>

<span data-ttu-id="e3ef6-123">Das Rebar-Beispiel wird als Teil des [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) installiert und ist am folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3ef6-123">The Rebar Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="e3ef6-124">Standort</span><span class="sxs-lookup"><span data-stu-id="e3ef6-124">Location</span></span>    | <span data-ttu-id="e3ef6-125">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="e3ef6-125">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ef6-126">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e3ef6-126">Windows SDK</span></span> | <span data-ttu-id="e3ef6-127">% Program Files% \\ Microsoft sdert \\ Windows- \\ \[ Versionsnummer \] \\ Beispiele \\ WinUI-Steuer \\ Elemente \\ Allgemeine Info \\ Leiste</span><span class="sxs-lookup"><span data-stu-id="e3ef6-127">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\rebar</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="e3ef6-128">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="e3ef6-128">Building the Sample</span></span>

<span data-ttu-id="e3ef6-129">So erstellen Sie das Beispiel mithilfe der Eingabeaufforderung:</span><span class="sxs-lookup"><span data-stu-id="e3ef6-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="e3ef6-130">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e3ef6-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="e3ef6-131">Geben Sie `msbuild [project file]` ein.</span><span class="sxs-lookup"><span data-stu-id="e3ef6-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="e3ef6-132">So erstellen Sie das Beispiel mithilfe von Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="e3ef6-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="e3ef6-133">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e3ef6-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="e3ef6-134">Doppelklicken Sie auf das Symbol für die VCPROJ-Datei, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e3ef6-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="e3ef6-135">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus, um die Projekt Mappe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e3ef6-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3ef6-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3ef6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3ef6-137">Grund leisten-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="e3ef6-137">Rebar Controls</span></span>](rebar-controls.md)
</dt> </dl>

 

 




