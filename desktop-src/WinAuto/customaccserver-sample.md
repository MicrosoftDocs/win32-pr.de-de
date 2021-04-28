---
title: CustomAccServer-Beispiel
description: CustomAccServer-Beispiel
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f8ee7d82361177af07aa7ad53a6137c39bc38
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088008"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="7e74f-103">CustomAccServer-Beispiel</span><span class="sxs-lookup"><span data-stu-id="7e74f-103">CustomAccServer Sample</span></span>

<span data-ttu-id="7e74f-104">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="7e74f-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7e74f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e74f-105">Description</span></span>](#description)
-   [<span data-ttu-id="7e74f-106">Herunterladen von Informationen</span><span class="sxs-lookup"><span data-stu-id="7e74f-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="7e74f-107">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="7e74f-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="7e74f-108">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7e74f-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="7e74f-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7e74f-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="7e74f-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7e74f-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="7e74f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e74f-111">Description</span></span>

<span data-ttu-id="7e74f-112">In diesem Beispiel wird gezeigt, wie Sie einen Microsoft Active Accessibility für ein einfaches benutzerdefiniertes Steuerelement implementieren.</span><span class="sxs-lookup"><span data-stu-id="7e74f-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="7e74f-113">Das barrierefreie Objekt für das Steuerelement besteht aus dem Stammelement (ein Listenfeld) und seinen unteren Elementen (den Listenelementen).</span><span class="sxs-lookup"><span data-stu-id="7e74f-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="7e74f-114">Herunterladen von Informationen</span><span class="sxs-lookup"><span data-stu-id="7e74f-114">Download Information</span></span>

<span data-ttu-id="7e74f-115">Das CustomAccServer-Beispiel wird als Teil des [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) installiert und ist an folgendem Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7e74f-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="7e74f-116">Standort</span><span class="sxs-lookup"><span data-stu-id="7e74f-116">Location</span></span>    | <span data-ttu-id="7e74f-117">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="7e74f-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e74f-118">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7e74f-118">Windows SDK</span></span> | <span data-ttu-id="7e74f-119">%Programme% \\ Microsoft SDKs \\ \\ \[ Windows-Versionsnummer \] \\ Beispiele \\ winui \\ msaa</span><span class="sxs-lookup"><span data-stu-id="7e74f-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="7e74f-120">Mindestanforderungen</span><span class="sxs-lookup"><span data-stu-id="7e74f-120">Minimum Requirements</span></span>



| <span data-ttu-id="7e74f-121">Produkt</span><span class="sxs-lookup"><span data-stu-id="7e74f-121">Product</span></span>          | <span data-ttu-id="7e74f-122">Version</span><span class="sxs-lookup"><span data-stu-id="7e74f-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="7e74f-123">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="7e74f-123">Operating System</span></span> | <span data-ttu-id="7e74f-124">Windows XP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e74f-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="7e74f-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7e74f-125">Windows SDK</span></span>      | <span data-ttu-id="7e74f-126">7.0</span><span class="sxs-lookup"><span data-stu-id="7e74f-126">7.0</span></span>                             |
| <span data-ttu-id="7e74f-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7e74f-127">Visual Studio</span></span>    | <span data-ttu-id="7e74f-128">2008</span><span class="sxs-lookup"><span data-stu-id="7e74f-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="7e74f-129">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7e74f-129">Building the Sample</span></span>

<span data-ttu-id="7e74f-130">So erstellen Sie das Beispiel mit Visual Studio 2008:</span><span class="sxs-lookup"><span data-stu-id="7e74f-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="7e74f-131">Führen Sie das mit dem SDK bereitgestellte Microsoft Windows Software Development Kit -Konfigurationstool (SDK) aus, um SDK-Includeverzeichnisse zum Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7e74f-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="7e74f-132">Öffnen Windows-Explorer, und navigieren Sie zum Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7e74f-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="7e74f-133">Doppelklicken Sie auf das Symbol für die SLN-Datei (Projektmappe), um das Projekt in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7e74f-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="7e74f-134">Wählen Sie **im Menü Erstellen** die Option **Projektmappe erstellen aus,** um die Projektmappe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7e74f-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="7e74f-135">Die Anwendung wird im Standardverzeichnis \\ Debuggen oder \\ Release erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e74f-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="7e74f-136">Informationen zum Erstellen des Beispiels über die Befehlszeile finden Sie unter Building Samples in the Windows SDK release notes at the following location: %Program Files% \\ Microsoft SDKs \\ Windows \\ v7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="7e74f-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7e74f-137">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7e74f-137">Running the Sample</span></span>

<span data-ttu-id="7e74f-138">So führen Sie das Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="7e74f-138">To run the sample:</span></span>

1.  <span data-ttu-id="7e74f-139">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="7e74f-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="7e74f-140">Geben Sie in der Befehlszeile AccServer.exe ein, oder doppelklicken Sie auf das Symbol für AccServer.exe, um es über Windows-Explorer zu starten.</span><span class="sxs-lookup"><span data-stu-id="7e74f-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="7e74f-141">Drücken Sie F5, oder klicken Sie im Menü **Debuggen** auf **Debuggen starten,** um Visual Studio auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7e74f-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e74f-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7e74f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e74f-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e74f-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




