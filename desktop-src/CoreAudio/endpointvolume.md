---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um das vom Benutzer angegebene Volume des Geräts zu ändern.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: Endpointvolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483491"
---
# <a name="endpointvolume"></a><span data-ttu-id="7d60a-103">Endpointvolume</span><span class="sxs-lookup"><span data-stu-id="7d60a-103">EndpointVolume</span></span>

<span data-ttu-id="7d60a-104">Diese Beispielanwendung verwendet die kernweb-APIs, um das vom Benutzer angegebene Volume des Geräts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7d60a-104">This sample application uses the Core Audio APIs to change the volume of the device, as specified by the user.</span></span>

<span data-ttu-id="7d60a-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="7d60a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7d60a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d60a-106">Description</span></span>](#description)
-   [<span data-ttu-id="7d60a-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d60a-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7d60a-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d60a-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="7d60a-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="7d60a-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="7d60a-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d60a-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="7d60a-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d60a-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="7d60a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d60a-112">Description</span></span>

<span data-ttu-id="7d60a-113">In diesem Beispiel werden die folgenden Funktionen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7d60a-113">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="7d60a-114">[Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.</span><span class="sxs-lookup"><span data-stu-id="7d60a-114">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="7d60a-115">[Endpointvolume-API](endpointvolume-api.md) zum Steuern der volumeebenen des Geräte Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="7d60a-115">[EndpointVolume API](endpointvolume-api.md) to control volume levels of the device endpoint.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d60a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d60a-116">Requirements</span></span>



| <span data-ttu-id="7d60a-117">Produkt</span><span class="sxs-lookup"><span data-stu-id="7d60a-117">Product</span></span>                                                        | <span data-ttu-id="7d60a-118">Version</span><span class="sxs-lookup"><span data-stu-id="7d60a-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="7d60a-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7d60a-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="7d60a-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d60a-120">Windows 7</span></span> |
| <span data-ttu-id="7d60a-121">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7d60a-121">Visual Studio</span></span>                                                  | <span data-ttu-id="7d60a-122">2008</span><span class="sxs-lookup"><span data-stu-id="7d60a-122">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7d60a-123">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d60a-123">Downloading the Sample</span></span>

<span data-ttu-id="7d60a-124">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d60a-124">This sample is available in the following locations.</span></span>



| <span data-ttu-id="7d60a-125">Standort</span><span class="sxs-lookup"><span data-stu-id="7d60a-125">Location</span></span>    | <span data-ttu-id="7d60a-126">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="7d60a-126">Path/URL</span></span>                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d60a-127">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7d60a-127">Windows SDK</span></span> | <span data-ttu-id="7d60a-128">\\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audioendpointvolume \\ ...</span><span class="sxs-lookup"><span data-stu-id="7d60a-128">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\EndpointVolume\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="7d60a-129">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d60a-129">Building the Sample</span></span>

<span data-ttu-id="7d60a-130">Um das x-Beispiel zu erstellen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="7d60a-130">To build the x sample, use the following steps:</span></span>

<span data-ttu-id="7d60a-131">Um das endpointvolumechanger-Beispiel zu erstellen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="7d60a-131">To build the EndpointVolumeChanger sample, use the following steps:</span></span>

1.  <span data-ttu-id="7d60a-132">Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Beispiel Verzeichnis "endpointvolume".</span><span class="sxs-lookup"><span data-stu-id="7d60a-132">Open the CMD shell for the Windows SDK and change to the EndpointVolume sample directory.</span></span>
2.  <span data-ttu-id="7d60a-133">Führen Sie den Befehl `start EndpointVolumeChanger.sln` im Verzeichnis "endpointvolume" aus, um das Projekt "endpointvolumechanger" im Visual Studio-Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7d60a-133">Run the command `start EndpointVolumeChanger.sln` in the EndpointVolume directory to open the EndpointVolumeChanger project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="7d60a-134">Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="7d60a-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="7d60a-135">Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung.</span><span class="sxs-lookup"><span data-stu-id="7d60a-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="7d60a-136">In diesem Fall wird das Beispiel nur dann erstellt, wenn Sie die Umgebungsvariable "Mssdk" explizit festlegen, die in der Projektdatei "wasapiendpointvolume. vcproj" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d60a-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIEndpointVolume.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7d60a-137">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="7d60a-137">Running the Sample</span></span>

<span data-ttu-id="7d60a-138">Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (EndpointVolumeChanger.exe) generiert.</span><span class="sxs-lookup"><span data-stu-id="7d60a-138">If you build the demo application successfully, an executable file, EndpointVolumeChanger.exe, is generated.</span></span> <span data-ttu-id="7d60a-139">Um es auszuführen, geben Sie `EndpointVolumeChanger` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten.</span><span class="sxs-lookup"><span data-stu-id="7d60a-139">To run it, type `EndpointVolumeChanger` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="7d60a-140">Im folgenden Beispiel wird gezeigt, wie Sie die Einstellung stumm schalten auf dem Standard Konsolen Gerät umschalten können.</span><span class="sxs-lookup"><span data-stu-id="7d60a-140">The following example shows how to toggle the mute setting on the default console device.</span></span>

`EndpointVolumeChanger.exe -console -m`

<span data-ttu-id="7d60a-141">In der folgenden Tabelle werden die Argumente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d60a-141">The following table shows the arguments.</span></span>

| <span data-ttu-id="7d60a-142">Argument</span><span class="sxs-lookup"><span data-stu-id="7d60a-142">Argument</span></span>        | <span data-ttu-id="7d60a-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d60a-143">Description</span></span>                                                         |
|-----------------|---------------------------------------------------------------------|
| <span data-ttu-id="7d60a-144">-?</span><span class="sxs-lookup"><span data-stu-id="7d60a-144">-?</span></span>              | <span data-ttu-id="7d60a-145">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="7d60a-145">Shows help.</span></span>                                                         |
| <span data-ttu-id="7d60a-146">-h</span><span class="sxs-lookup"><span data-stu-id="7d60a-146">-h</span></span>              | <span data-ttu-id="7d60a-147">Zeigt die Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="7d60a-147">Shows help.</span></span>                                                         |
| -+              | <span data-ttu-id="7d60a-148">Inkremente der Volumeebene auf dem audioendpunktgerät um einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="7d60a-148">Increments the volume level on audio endpoint device by one step.</span></span> <span data-ttu-id="7d60a-149">.</span><span class="sxs-lookup"><span data-stu-id="7d60a-149">.</span></span> |
| <span data-ttu-id="7d60a-150">nach oben</span><span class="sxs-lookup"><span data-stu-id="7d60a-150">-up</span></span>             | <span data-ttu-id="7d60a-151">Inkremente der Volumeebene auf dem audioendpunktgerät um einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="7d60a-151">Increments the volume level on audio endpoint device by one step.</span></span>   |
| --              | <span data-ttu-id="7d60a-152">Verringert die Volumeebene auf dem audioendpunktgerät um einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="7d60a-152">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="7d60a-153">nach unten</span><span class="sxs-lookup"><span data-stu-id="7d60a-153">-down</span></span>           | <span data-ttu-id="7d60a-154">Verringert die Volumeebene auf dem audioendpunktgerät um einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="7d60a-154">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="7d60a-155">-v</span><span class="sxs-lookup"><span data-stu-id="7d60a-155">-v</span></span>              | <span data-ttu-id="7d60a-156">Legt die Master Volume-Ebene auf dem audioendpunktgerät fest.</span><span class="sxs-lookup"><span data-stu-id="7d60a-156">Sets the master volume level on the audio endpoint device.</span></span>          |
| <span data-ttu-id="7d60a-157">-Konsole</span><span class="sxs-lookup"><span data-stu-id="7d60a-157">-console</span></span>        | <span data-ttu-id="7d60a-158">Verwenden Sie das Standard Konsolen Gerät.</span><span class="sxs-lookup"><span data-stu-id="7d60a-158">Use the default console device.</span></span>                                     |
| <span data-ttu-id="7d60a-159">-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="7d60a-159">-communications</span></span> | <span data-ttu-id="7d60a-160">Verwenden Sie das Standard Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="7d60a-160">Use the default communication device.</span></span>                               |
| <span data-ttu-id="7d60a-161">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="7d60a-161">-multimedia</span></span>     | <span data-ttu-id="7d60a-162">Verwenden Sie das standardmäßige Multimedia-Gerät.</span><span class="sxs-lookup"><span data-stu-id="7d60a-162">Use the default multimedia device.</span></span>                                  |
| <span data-ttu-id="7d60a-163">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="7d60a-163">-endpoint</span></span>       | <span data-ttu-id="7d60a-164">Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7d60a-164">Use the endpoint identifier specified in the switch value.</span></span>          |



 

<span data-ttu-id="7d60a-165">Wenn die Anwendung ohne Argumente ausgeführt wird, werden die verfügbaren Geräte aufgelistet, und der Benutzer wird aufgefordert, ein Gerät auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7d60a-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device.</span></span> <span data-ttu-id="7d60a-166">Nachdem der Benutzer das Gerät angegeben hat, zeigt die Anwendung die aktuellen Volumeeinstellungen für den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="7d60a-166">After the user specifies the device, the application displays the current volume settings for the endpoint.</span></span> <span data-ttu-id="7d60a-167">Das Volume kann mithilfe der in der obigen Tabelle beschriebenen Switches gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="7d60a-167">The volume can be controlled by using the switches described in the preceding table.</span></span>

<span data-ttu-id="7d60a-168">Weitere Informationen zum Steuern der volumeebenen von audioendpunktgeräten finden Sie unter [endpointvolume-API](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="7d60a-168">For more information about controlling the volume levels of audio endpoint devices, see [EndpointVolume API](endpointvolume-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d60a-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d60a-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d60a-170">SDK-Beispiele für die Verwendung der kernaudioapis</span><span class="sxs-lookup"><span data-stu-id="7d60a-170">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



