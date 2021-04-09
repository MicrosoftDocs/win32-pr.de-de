---
description: In diesem Artikel wird beschrieben, wie Sie eine WASAPI-Implementierung aktualisieren, um das automatische streamrouting zu nutzen.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Automatisches streamrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958587"
---
# <a name="automatic-stream-routing"></a><span data-ttu-id="835e5-103">Automatisches streamrouting</span><span class="sxs-lookup"><span data-stu-id="835e5-103">Automatic Stream Routing</span></span>

<span data-ttu-id="835e5-104">In diesem Artikel wird beschrieben, wie Sie eine WASAPI-Implementierung aktualisieren, um das automatische streamrouting zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="835e5-104">This article describes how to update a WASAPI implementation to take advantage of automatic stream routing.</span></span>

<span data-ttu-id="835e5-105">Ab Windows 7 wird der Audiowiedergabe-Stream einer APP nahtlos vom vorherigen Standardaudiogerät auf das neue Standardaudiogerät übertragen, wenn sich das Standardaudiogerät ändert.</span><span class="sxs-lookup"><span data-stu-id="835e5-105">Starting with Windows 7, whenever the default audio device changes, an app's audio playback stream is seamlessly transferred from the previous default audio device to the new default audio device .</span></span> <span data-ttu-id="835e5-106">Diese Übertragung erfolgt automatisch ohne zusätzlichen Anwendungscode.</span><span class="sxs-lookup"><span data-stu-id="835e5-106">This transfer occurs automatically without any additional application code.</span></span> <span data-ttu-id="835e5-107">Vor Windows 10, Version 1607, konnten apps, die die Low-Level-API für die Audiositzung (WASAPI) verwendeten, nicht an dieser automatisierten streamweiterleitungs-Funktion teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="835e5-107">However, prior to Windows 10, version 1607, apps that used the low-level Windows Audio Session API (WASAPI) could not participate in this automated stream routing functionality.</span></span> <span data-ttu-id="835e5-108">Apps, die WASAPI verwenden, mussten ihre eigene Form des Stream-Routings implementieren, indem Sie zusätzlichen Code hinzufügen, um das eintreffen und Entfernen von Audiogeräten zu erkennen und den Stream entsprechend zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="835e5-108">Apps using WASAPI were required to implement their own form of stream routing by adding additional code to detect the arrival and removal of audio devices and switch the stream to those devices as appropriate.</span></span> <span data-ttu-id="835e5-109">Anwendungen, die WASAPI verwenden, die nicht Ihren eigenen Stream-Routing Mechanismus beim Eintreffen oder Entfernen von Geräten implementiert haben, riskieren eine geringere Benutzer Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="835e5-109">Applications using WASAPI that did not implement their own stream routing mechanism on device arrival or removal risked providing a less than ideal user experience.</span></span>

<span data-ttu-id="835e5-110">Ab Windows 10, Version 1607, können apps, die WASAPI verwenden, das automatische streamrouting nutzen.</span><span class="sxs-lookup"><span data-stu-id="835e5-110">Starting with the Windows 10, version 1607, apps that use WASAPI can take advantage of automatic stream routing.</span></span> <span data-ttu-id="835e5-111">Wenn Ihre Anwendung WASAPI verwendet, wird dringend empfohlen, dass Sie Ihre Anwendung aktualisieren, um diese neue Funktion mithilfe der folgenden Schritte nutzen zu können:</span><span class="sxs-lookup"><span data-stu-id="835e5-111">If your application uses WASAPI it is highly recommended that you update your application to take advantage of this new capability using the following steps:</span></span>

1.  <span data-ttu-id="835e5-112">In Windows 10, Version 1607, werden zwei neue GUIDs definiert, mit denen ein audiorendering oder eine Aufzeichnungs Schnittstelle mit automatischem streamrouting, [devinterface \_ - \_ audiorendering](/windows/desktop/CoreAudio/devinterface-xxx-guids) und [devinterface \_ - \_ Audioerfassung](/windows/desktop/CoreAudio/devinterface-xxx-guids)aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="835e5-112">Windows 10, version 1607, defines two new GUIDs that can be used to activate an audio render or capture interface with automatic stream routing, [DEVINTERFACE\_AUDIO\_RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) and [DEVINTERFACE\_AUDIO\_CAPTURE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span></span> <span data-ttu-id="835e5-113">Sie erhalten eine Zeichen folgen Darstellung dieser GUIDs, indem Sie [**stringfromiid**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="835e5-113">Get a string representation of these GUIDs by calling [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span></span> <span data-ttu-id="835e5-114">Das folgende Beispiel zeigt diesen-Befehl für die Audio-Rendering-GUID.</span><span class="sxs-lookup"><span data-stu-id="835e5-114">The following example shows this call for the audio render GUID.</span></span>

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  <span data-ttu-id="835e5-115">Aktivieren Sie den audioendpunkt, indem Sie die Bezeichnerzeichenfolge an die WASAPI [**activateaudiointerfaceasync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="835e5-115">Activate the audio endpoint by passing the identifier string to the WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) function.</span></span> <span data-ttu-id="835e5-116">Das folgende Beispiel übergibt den audiorendering-Bezeichner, der in Schritt 1 abgerufen wurde:</span><span class="sxs-lookup"><span data-stu-id="835e5-116">The following example passes in the audio render identifier obtained in step 1:</span></span>

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  <span data-ttu-id="835e5-117">Freigeben des zugeordneten Arbeitsspeichers zum Speichern des Endpunkt Bezeichners:</span><span class="sxs-lookup"><span data-stu-id="835e5-117">Free the memory allocated for holding the endpoint identifier:</span></span>

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

<span data-ttu-id="835e5-118">Nachdem Sie die APP so geändert haben, dass Sie die Audioschnittstelle in der oben beschriebenen Weise aktiviert, wird Sie an der Funktion für automatisches streamrouting beteiligt.</span><span class="sxs-lookup"><span data-stu-id="835e5-118">After you have modified your app to activate the audio interface in the manner described above, it will participate in the automatic stream routing feature.</span></span>

<span data-ttu-id="835e5-119">Um das automatische Streamen von Datenströmen zu veranschaulichen, verwenden Sie einen Laptop oder Tablet, der mit internen Referenten ausgestattet ist</span><span class="sxs-lookup"><span data-stu-id="835e5-119">To demonstrate automatic stream routing, use a laptop or tablet equipped with internal speakers to play back audio.</span></span> <span data-ttu-id="835e5-120">Sie sollten das Audiomaterial durch die internen Redner des Geräts hören.</span><span class="sxs-lookup"><span data-stu-id="835e5-120">You should hear the audio playing through the device's internal speakers.</span></span> <span data-ttu-id="835e5-121">Wenn Audioinhalte wiedergegeben werden, verbinden Sie ein paar von Kopfhörern.</span><span class="sxs-lookup"><span data-stu-id="835e5-121">While audio is playing, connect a pair of headphones.</span></span> <span data-ttu-id="835e5-122">Sie sollten jetzt Audioinhalte über die Kopfhörer hören.</span><span class="sxs-lookup"><span data-stu-id="835e5-122">You should now hear audio playing through the headphones.</span></span> <span data-ttu-id="835e5-123">Entfernen Sie dann die Kopfhörer, und Audiodaten sollten automatisch an die internen Referenten zurückgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="835e5-123">Then, unplug the headphones and audio should automatically route back to the internal speakers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="835e5-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="835e5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="835e5-125">Streamrouting</span><span class="sxs-lookup"><span data-stu-id="835e5-125">Stream Routing</span></span>](stream-routing.md)
</dt> <dt>

[<span data-ttu-id="835e5-126">**Mediadevice. getdefaultaudiorenderid**</span><span class="sxs-lookup"><span data-stu-id="835e5-126">**MediaDevice.GetDefaultAudioRenderId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[<span data-ttu-id="835e5-127">**Mediadevice. getdefaultaudiocaptureid**</span><span class="sxs-lookup"><span data-stu-id="835e5-127">**MediaDevice.GetDefaultAudioCaptureId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[<span data-ttu-id="835e5-128">**Activateaudiointerfaceasync**</span><span class="sxs-lookup"><span data-stu-id="835e5-128">**ActivateAudioInterfaceAsync**</span></span>](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
