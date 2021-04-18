---
title: Vlistvw-Beispiel
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: Weitere Informationen zu vlistvw Sample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344217"
---
# <a name="vlistvw-sample"></a><span data-ttu-id="08e6f-103">Vlistvw-Beispiel</span><span class="sxs-lookup"><span data-stu-id="08e6f-103">VListVW Sample</span></span>

<span data-ttu-id="08e6f-104">In diesem Thema wird das Beispielcode Beispiel für vlistvw beschrieben.</span><span class="sxs-lookup"><span data-stu-id="08e6f-104">This topic describes the VListVW Sample code sample.</span></span> <span data-ttu-id="08e6f-105">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="08e6f-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="08e6f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08e6f-106">Description</span></span>](#description)
-   [<span data-ttu-id="08e6f-107">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="08e6f-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="08e6f-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="08e6f-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="08e6f-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="08e6f-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="08e6f-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08e6f-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="08e6f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08e6f-111">Description</span></span>

<span data-ttu-id="08e6f-112">Das vlistvw-Beispiel zeigt, wie ein einfaches virtuelles Listenansicht-Steuerelement in einer Anwendung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="08e6f-112">The VListVW Sample shows how to implement a simple virtual list-view control in an application.</span></span> <span data-ttu-id="08e6f-113">Ein virtuelles Listenansicht-Steuerelement ist ein Standardmäßiges Listenansicht-Steuerelement mit dem **LVS-Besitzer \_ Daten** Stil.</span><span class="sxs-lookup"><span data-stu-id="08e6f-113">A virtual list-view control is a standard list-view control with the **LVS\_OWNERDATA** style.</span></span> <span data-ttu-id="08e6f-114">In diesem Beispiel wird ein Listenansicht-Steuerelement erstellt, das "virtuell" 100.000 Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="08e6f-114">This example creates a list-view control that "virtually" holds 100,000 items.</span></span> <span data-ttu-id="08e6f-115">Die Elemente werden nie tatsächlich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="08e6f-115">The items are never actually added.</span></span> <span data-ttu-id="08e6f-116">Stattdessen wird das Steuerelement [**für die virtuelle \_**](lvm-setitemcount.md) Listenansicht "erzählt", wie viele Elemente es enthält.</span><span class="sxs-lookup"><span data-stu-id="08e6f-116">Instead, the virtual list-view control is "told" how many items it contains with the [**LVM\_SETITEMCOUNT**](lvm-setitemcount.md) message.</span></span> <span data-ttu-id="08e6f-117">Wenn ein Element gezeichnet werden muss, fragt das Listenansicht-Steuerelement das übergeordnete Fenster nach Anzeigeinformationen mit der [LVN \_ getdispinfo](lvn-getdispinfo.md) -Benachrichtigung ab.</span><span class="sxs-lookup"><span data-stu-id="08e6f-117">When an item needs to be drawn, the list-view control queries the parent window for display information with the [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="08e6f-118">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="08e6f-118">Minimum Requirements</span></span>



| <span data-ttu-id="08e6f-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="08e6f-119">Product</span></span>          | <span data-ttu-id="08e6f-120">Version</span><span class="sxs-lookup"><span data-stu-id="08e6f-120">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="08e6f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="08e6f-121">DLL</span></span>              | <span data-ttu-id="08e6f-122">comctl32.dll Version 4,70</span><span class="sxs-lookup"><span data-stu-id="08e6f-122">comctl32.dll version 4.70</span></span>             |
| <span data-ttu-id="08e6f-123">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="08e6f-123">Operating System</span></span> | <span data-ttu-id="08e6f-124">Windows 95, Microsoft Windows NT 3,51</span><span class="sxs-lookup"><span data-stu-id="08e6f-124">Windows 95, Microsoft Windows NT 3.51</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="08e6f-125">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="08e6f-125">Downloading the Sample</span></span>

<span data-ttu-id="08e6f-126">Das vlistvw-Beispiel ist auf GitHub im [klassischen Windows-beispielrepository](https://github.com/microsoft/Windows-classic-samples)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08e6f-126">The VListVW Sample is available on on github in the [Windows Classic Samples repository](https://github.com/microsoft/Windows-classic-samples).</span></span> <span data-ttu-id="08e6f-127">Die Listenansicht-Steuerelement Elemente finden Sie [hier](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw) .</span><span class="sxs-lookup"><span data-stu-id="08e6f-127">The list view control items examples can be found at [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="08e6f-128">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="08e6f-128">Building the Sample</span></span>

<span data-ttu-id="08e6f-129">So erstellen Sie das Beispiel mithilfe der Eingabeaufforderung:</span><span class="sxs-lookup"><span data-stu-id="08e6f-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="08e6f-130">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="08e6f-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="08e6f-131">Geben Sie `msbuild [project file]` ein.</span><span class="sxs-lookup"><span data-stu-id="08e6f-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="08e6f-132">So erstellen Sie das Beispiel mithilfe von Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="08e6f-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="08e6f-133">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="08e6f-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="08e6f-134">Doppelklicken Sie auf das Symbol für die VCPROJ-Datei, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="08e6f-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="08e6f-135">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus, um die Projekt Mappe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08e6f-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08e6f-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08e6f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e6f-137">Informationen zu List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="08e6f-137">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> </dl>

 

 




