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
# <a name="automatic-stream-routing"></a>Automatisches streamrouting

In diesem Artikel wird beschrieben, wie Sie eine WASAPI-Implementierung aktualisieren, um das automatische streamrouting zu nutzen.

Ab Windows 7 wird der Audiowiedergabe-Stream einer APP nahtlos vom vorherigen Standardaudiogerät auf das neue Standardaudiogerät übertragen, wenn sich das Standardaudiogerät ändert. Diese Übertragung erfolgt automatisch ohne zusätzlichen Anwendungscode. Vor Windows 10, Version 1607, konnten apps, die die Low-Level-API für die Audiositzung (WASAPI) verwendeten, nicht an dieser automatisierten streamweiterleitungs-Funktion teilnehmen. Apps, die WASAPI verwenden, mussten ihre eigene Form des Stream-Routings implementieren, indem Sie zusätzlichen Code hinzufügen, um das eintreffen und Entfernen von Audiogeräten zu erkennen und den Stream entsprechend zu wechseln. Anwendungen, die WASAPI verwenden, die nicht Ihren eigenen Stream-Routing Mechanismus beim Eintreffen oder Entfernen von Geräten implementiert haben, riskieren eine geringere Benutzer Funktionalität.

Ab Windows 10, Version 1607, können apps, die WASAPI verwenden, das automatische streamrouting nutzen. Wenn Ihre Anwendung WASAPI verwendet, wird dringend empfohlen, dass Sie Ihre Anwendung aktualisieren, um diese neue Funktion mithilfe der folgenden Schritte nutzen zu können:

1.  In Windows 10, Version 1607, werden zwei neue GUIDs definiert, mit denen ein audiorendering oder eine Aufzeichnungs Schnittstelle mit automatischem streamrouting, [devinterface \_ - \_ audiorendering](/windows/desktop/CoreAudio/devinterface-xxx-guids) und [devinterface \_ - \_ Audioerfassung](/windows/desktop/CoreAudio/devinterface-xxx-guids)aktiviert werden kann. Sie erhalten eine Zeichen folgen Darstellung dieser GUIDs, indem Sie [**stringfromiid**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid)aufrufen. Das folgende Beispiel zeigt diesen-Befehl für die Audio-Rendering-GUID.

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  Aktivieren Sie den audioendpunkt, indem Sie die Bezeichnerzeichenfolge an die WASAPI [**activateaudiointerfaceasync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) -Funktion übergeben. Das folgende Beispiel übergibt den audiorendering-Bezeichner, der in Schritt 1 abgerufen wurde:

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  Freigeben des zugeordneten Arbeitsspeichers zum Speichern des Endpunkt Bezeichners:

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

Nachdem Sie die APP so geändert haben, dass Sie die Audioschnittstelle in der oben beschriebenen Weise aktiviert, wird Sie an der Funktion für automatisches streamrouting beteiligt.

Um das automatische Streamen von Datenströmen zu veranschaulichen, verwenden Sie einen Laptop oder Tablet, der mit internen Referenten ausgestattet ist Sie sollten das Audiomaterial durch die internen Redner des Geräts hören. Wenn Audioinhalte wiedergegeben werden, verbinden Sie ein paar von Kopfhörern. Sie sollten jetzt Audioinhalte über die Kopfhörer hören. Entfernen Sie dann die Kopfhörer, und Audiodaten sollten automatisch an die internen Referenten zurückgeleitet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamrouting](stream-routing.md)
</dt> <dt>

[**Mediadevice. getdefaultaudiorenderid**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[**Mediadevice. getdefaultaudiocaptureid**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[**Activateaudiointerfaceasync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
