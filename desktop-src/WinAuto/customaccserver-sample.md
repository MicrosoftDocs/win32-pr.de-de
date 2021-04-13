---
title: Customaccserver-Beispiel
description: .
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c047bde41bdf4a486e14ce6f293113a41ae9e285
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389970"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="39f4d-103">Customaccserver-Beispiel</span><span class="sxs-lookup"><span data-stu-id="39f4d-103">CustomAccServer Sample</span></span>

<span data-ttu-id="39f4d-104">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="39f4d-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="39f4d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39f4d-105">Description</span></span>](#description)
-   [<span data-ttu-id="39f4d-106">Download Informationen</span><span class="sxs-lookup"><span data-stu-id="39f4d-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="39f4d-107">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="39f4d-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="39f4d-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="39f4d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="39f4d-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="39f4d-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="39f4d-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39f4d-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="39f4d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39f4d-111">Description</span></span>

<span data-ttu-id="39f4d-112">In diesem Beispiel wird gezeigt, wie ein Microsoft Active Accessibility Server für ein einfaches benutzerdefiniertes Steuerelement implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="39f4d-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="39f4d-113">Das barrierefreie Objekt für das-Steuerelement besteht aus dem Stamm Element (einem Listenfeld) und seinen untergeordneten Elementen (Listenelemente).</span><span class="sxs-lookup"><span data-stu-id="39f4d-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="39f4d-114">Download Informationen</span><span class="sxs-lookup"><span data-stu-id="39f4d-114">Download Information</span></span>

<span data-ttu-id="39f4d-115">Das customaccserver-Beispiel wird als Teil des [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) installiert und ist am folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39f4d-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="39f4d-116">Standort</span><span class="sxs-lookup"><span data-stu-id="39f4d-116">Location</span></span>    | <span data-ttu-id="39f4d-117">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="39f4d-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39f4d-118">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="39f4d-118">Windows SDK</span></span> | <span data-ttu-id="39f4d-119">% Program Files% \\ Microsoft sdert \\ Windows- \\ \[ Versionsnummer \] \\ Beispiele \\ WinUI \\ MSAA</span><span class="sxs-lookup"><span data-stu-id="39f4d-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="39f4d-120">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="39f4d-120">Minimum Requirements</span></span>



| <span data-ttu-id="39f4d-121">Produkt</span><span class="sxs-lookup"><span data-stu-id="39f4d-121">Product</span></span>          | <span data-ttu-id="39f4d-122">Version</span><span class="sxs-lookup"><span data-stu-id="39f4d-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="39f4d-123">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="39f4d-123">Operating System</span></span> | <span data-ttu-id="39f4d-124">Windows XP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39f4d-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="39f4d-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="39f4d-125">Windows SDK</span></span>      | <span data-ttu-id="39f4d-126">7.0</span><span class="sxs-lookup"><span data-stu-id="39f4d-126">7.0</span></span>                             |
| <span data-ttu-id="39f4d-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="39f4d-127">Visual Studio</span></span>    | <span data-ttu-id="39f4d-128">2008</span><span class="sxs-lookup"><span data-stu-id="39f4d-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="39f4d-129">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="39f4d-129">Building the Sample</span></span>

<span data-ttu-id="39f4d-130">So erstellen Sie das Beispiel mit Visual Studio 2008:</span><span class="sxs-lookup"><span data-stu-id="39f4d-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="39f4d-131">Führen Sie das Microsoft Windows Software Development Kit (SDK)-Konfigurations Tool aus, das mit dem SDK bereitgestellt wird, um Visual Studio SDK include-Verzeichnisse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="39f4d-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="39f4d-132">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="39f4d-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="39f4d-133">Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappendatei), um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="39f4d-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="39f4d-134">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus, um die Projekt Mappe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39f4d-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="39f4d-135">Die Anwendung wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="39f4d-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="39f4d-136">Wenn Sie das Beispiel über die Befehlszeile erstellen möchten, finden Sie weitere Informationen unter Erstellen von Beispielen in den Anmerkungen zur Windows SDK-Version unter folgendem Speicherort:% Program Files% \\ Microsoft sdert \\ Windows \\ v 7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="39f4d-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="39f4d-137">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="39f4d-137">Running the Sample</span></span>

<span data-ttu-id="39f4d-138">So führen Sie das Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="39f4d-138">To run the sample:</span></span>

1.  <span data-ttu-id="39f4d-139">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="39f4d-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="39f4d-140">Geben Sie AccServer.exe in der Befehlszeile ein, oder Doppelklicken Sie auf das Symbol für AccServer.exe, um es im Windows-Explorer zu starten.</span><span class="sxs-lookup"><span data-stu-id="39f4d-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="39f4d-141">Um in Visual Studio auszuführen, drücken Sie F5, oder klicken Sie im Menü **Debuggen** auf **Debuggen starten** .</span><span class="sxs-lookup"><span data-stu-id="39f4d-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39f4d-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39f4d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39f4d-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39f4d-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




