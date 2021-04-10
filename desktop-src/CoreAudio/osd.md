---
description: In diesem Beispiel werden die Kern-audioapis verwendet, um eine Bildschirm Anzeige zu implementieren, die volumeänderungen an dem Ausgabedatenstrom anzeigt, die über das standardmäßige audiorenderingendpunkt-Gerät abgespielt werden.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: OSD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041460"
---
# <a name="osd"></a><span data-ttu-id="f074f-103">OSD</span><span class="sxs-lookup"><span data-stu-id="f074f-103">OSD</span></span>

<span data-ttu-id="f074f-104">In diesem Beispiel werden die Kern-audioapis verwendet, um eine Bildschirm Anzeige zu implementieren, die volumeänderungen an dem Ausgabedatenstrom anzeigt, die über das standardmäßige audiorenderingendpunkt-Gerät abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="f074f-104">This sample uses the Core Audio APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="f074f-105">Die Anzeige auf dem Bildschirm wird angezeigt, wenn der Benutzer die Volumeebene im Windows-Programm zur volumesteuerung (Sndvol.exe) anpasst, und er verschwindet, wenn die Volumeebene für einen kurzen Zeitraum unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="f074f-105">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span>

<span data-ttu-id="f074f-106">In diesem Thema werden die folgenden Abschnitte behandelt.</span><span class="sxs-lookup"><span data-stu-id="f074f-106">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="f074f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f074f-107">Description</span></span>](#description)
-   [<span data-ttu-id="f074f-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f074f-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f074f-109">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f074f-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f074f-110">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="f074f-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f074f-111">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f074f-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="f074f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f074f-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="f074f-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f074f-113">Description</span></span>

<span data-ttu-id="f074f-114">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f074f-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="f074f-115">[Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="f074f-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="f074f-116">[Audioendpointvolume-API](endpointvolume-api.md)</span><span class="sxs-lookup"><span data-stu-id="f074f-116">Audio [EndpointVolume API](endpointvolume-api.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="f074f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f074f-117">Requirements</span></span>



| <span data-ttu-id="f074f-118">Produkt</span><span class="sxs-lookup"><span data-stu-id="f074f-118">Product</span></span>                                                        | <span data-ttu-id="f074f-119">Version</span><span class="sxs-lookup"><span data-stu-id="f074f-119">Version</span></span>                |
|----------------------------------------------------------------|------------------------|
| [<span data-ttu-id="f074f-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f074f-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="f074f-121">Windows Vista oder höher</span><span class="sxs-lookup"><span data-stu-id="f074f-121">Windows Vista or later</span></span> |
| <span data-ttu-id="f074f-122">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f074f-122">Visual Studio</span></span>                                                  | <span data-ttu-id="f074f-123">2005 oder höher</span><span class="sxs-lookup"><span data-stu-id="f074f-123">2005 or later</span></span>          |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f074f-124">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f074f-124">Downloading the Sample</span></span>

<span data-ttu-id="f074f-125">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f074f-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="f074f-126">Standort</span><span class="sxs-lookup"><span data-stu-id="f074f-126">Location</span></span>    | <span data-ttu-id="f074f-127">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="f074f-127">Path/URL</span></span>                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f074f-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f074f-128">Windows SDK</span></span> | <span data-ttu-id="f074f-129">\\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audioosd \\ ...</span><span class="sxs-lookup"><span data-stu-id="f074f-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\OSD\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="f074f-130">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f074f-130">Building the Sample</span></span>

1.  <span data-ttu-id="f074f-131">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum OSD-Beispiel Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="f074f-131">Open the CMD shell for the Windows SDK and change to the OSD sample directory.</span></span>
2.  <span data-ttu-id="f074f-132">Führen Sie den Befehl "Start OSD. sln" im OSD-Verzeichnis aus, um das OSD-Projekt im Visual Studio-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f074f-132">Run the command "start OSD.sln" in the OSD directory to open the OSD project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="f074f-133">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="f074f-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="f074f-134">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="f074f-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="f074f-135">In diesem Fall wird das Beispiel nur dann erstellt, wenn Sie die Umgebungsvariable "Mssdk" explizit festlegen, die in der Projektdatei "OSD. vcproj" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f074f-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, OSD.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f074f-136">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f074f-136">Running the Sample</span></span>

1.  <span data-ttu-id="f074f-137">Führen Sie die ausführbare OSD-Datei OSD.exe in Windows Vista oder höher aus.</span><span class="sxs-lookup"><span data-stu-id="f074f-137">Run the OSD executable file, OSD.exe, in Windows Vista or later.</span></span> <span data-ttu-id="f074f-138">Beachten Sie, dass kein Task leisten Symbol oder ein Fenster für die Anwendung angezeigt wird, aber Sie können den Prozess anzeigen, der mit TaskMgr.exe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f074f-138">Note that you will not see a system tray icon or a window for the application, but you can see the process running using TaskMgr.exe.</span></span>
2.  <span data-ttu-id="f074f-139">Führen Sie sndvol.exe aus, um das Volume zu ändern oder das Volume mithilfe von Tastatur Steuerelementen oder einem HID-Steuerelement zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f074f-139">Run sndvol.exe to change the volume or mute, or change the volume using keyboard controls or an HID control.</span></span> <span data-ttu-id="f074f-140">Die Benutzeroberfläche von OSD wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f074f-140">The OSD user interface is displayed.</span></span>
3.  <span data-ttu-id="f074f-141">Führen Sie TaskMgr.exe aus, markieren Sie den OSD.exe Prozess, und klicken Sie auf **Prozess beenden**, um die Anwendung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f074f-141">To exit the application, run TaskMgr.exe, highlight the OSD.exe process and click **End Process**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f074f-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f074f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f074f-143">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="f074f-143">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



