---
title: Eigenschafts Beispiel
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 'Weitere Informationen: Eigenschafts Beispiel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c11fda9b133ca6fa3b2f9942d8d48bec3a9e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125977"
---
# <a name="property-sample"></a><span data-ttu-id="f22dd-103">Eigenschafts Beispiel</span><span class="sxs-lookup"><span data-stu-id="f22dd-103">Property Sample</span></span>

<span data-ttu-id="f22dd-104">In diesem Thema wird das Beispielcode Beispiel für die-Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f22dd-104">This topic describes the Property Sample code sample.</span></span> <span data-ttu-id="f22dd-105">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="f22dd-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="f22dd-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f22dd-106">Description</span></span>](#description)
-   [<span data-ttu-id="f22dd-107">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="f22dd-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="f22dd-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f22dd-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f22dd-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="f22dd-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f22dd-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f22dd-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="f22dd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f22dd-111">Description</span></span>

<span data-ttu-id="f22dd-112">Das Eigenschafts Beispiel zeigt, wie drei verschiedene Stile von Eigenschaften Blättern implementiert werden: Modal, MODELESS und Assistent.</span><span class="sxs-lookup"><span data-stu-id="f22dd-112">The Property Sample shows how to implement three different styles of property sheets: modal, modeless, and wizard.</span></span> <span data-ttu-id="f22dd-113">Außerdem wird gezeigt, wie die [*propsheetproc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) -Funktion verwendet wird, um das Eigenschaften Blatt Dialogfeld vor oder nach der Erstellung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f22dd-113">It also shows how to use the [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) function to modify the property sheet dialog before or after it is created.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="f22dd-114">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="f22dd-114">Minimum Requirements</span></span>



| <span data-ttu-id="f22dd-115">Produkt</span><span class="sxs-lookup"><span data-stu-id="f22dd-115">Product</span></span>          | <span data-ttu-id="f22dd-116">Version</span><span class="sxs-lookup"><span data-stu-id="f22dd-116">Version</span></span>                              |
|------------------|--------------------------------------|
| <span data-ttu-id="f22dd-117">DLL</span><span class="sxs-lookup"><span data-stu-id="f22dd-117">DLL</span></span>              | <span data-ttu-id="f22dd-118">comctl32.dll Version 4,0</span><span class="sxs-lookup"><span data-stu-id="f22dd-118">comctl32.dll version 4.0</span></span>             |
| <span data-ttu-id="f22dd-119">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="f22dd-119">Operating System</span></span> | <span data-ttu-id="f22dd-120">Windows 95, Microsoft Windows NT 3,1</span><span class="sxs-lookup"><span data-stu-id="f22dd-120">Windows 95, Microsoft Windows NT 3.1</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f22dd-121">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f22dd-121">Downloading the Sample</span></span>

<span data-ttu-id="f22dd-122">Das Eigenschafts Beispiel wird als Teil des [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) installiert und ist am folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f22dd-122">The Property Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="f22dd-123">Standort</span><span class="sxs-lookup"><span data-stu-id="f22dd-123">Location</span></span>    | <span data-ttu-id="f22dd-124">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="f22dd-124">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f22dd-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f22dd-125">Windows SDK</span></span> | <span data-ttu-id="f22dd-126">% Program Files% \\ Microsoft sdert \\ Windows- \\ \[ Versionsnummer \] \\ Beispiele \\ WinUI-Steuer \\ Elemente \\ allgemeine \\ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f22dd-126">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\property</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="f22dd-127">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f22dd-127">Building the Sample</span></span>

<span data-ttu-id="f22dd-128">So erstellen Sie das Beispiel mithilfe der Eingabeaufforderung:</span><span class="sxs-lookup"><span data-stu-id="f22dd-128">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="f22dd-129">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="f22dd-129">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="f22dd-130">Geben Sie `msbuild [project file]` ein.</span><span class="sxs-lookup"><span data-stu-id="f22dd-130">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="f22dd-131">So erstellen Sie das Beispiel mithilfe von Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="f22dd-131">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="f22dd-132">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="f22dd-132">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="f22dd-133">Doppelklicken Sie auf das Symbol für die VCPROJ-Datei, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f22dd-133">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="f22dd-134">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus, um die Projekt Mappe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f22dd-134">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f22dd-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f22dd-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f22dd-136">Informationen zu Eigenschaften Blättern</span><span class="sxs-lookup"><span data-stu-id="f22dd-136">About Property Sheets</span></span>](property-sheets.md)
</dt> </dl>

 

 




