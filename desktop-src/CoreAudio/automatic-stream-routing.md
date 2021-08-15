---
description: In diesem Artikel wird beschrieben, wie Sie eine WASAPI-Implementierung aktualisieren, um das automatische Streamrouting zu nutzen.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Automatisches Streamrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd152db35c580d93cf76ccfaffd66b37225f2be7fae11f217a6895b289a58e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957389"
---
# <a name="automatic-stream-routing"></a>Automatisches Streamrouting

In diesem Artikel wird beschrieben, wie Sie eine WASAPI-Implementierung aktualisieren, um das automatische Streamrouting zu nutzen.

Ab Windows 7 wird bei jeder Änderung des Standardaudiogeräts der Audiowiedergabedatenstrom einer App nahtlos vom vorherigen Standardaudiogerät auf das neue Standardaudiogerät übertragen. Diese Übertragung erfolgt automatisch ohne zusätzlichen Anwendungscode. Vor Windows 10 Version 1607 konnten Apps, die die low-level Windows Audio Session API (WASAPI) verwendet haben, jedoch nicht an dieser automatisierten Streamroutingfunktion teilnehmen. Apps, die WASAPI verwenden, mussten ihre eigene Form des Streamroutings implementieren, indem sie zusätzlichen Code hinzufügen, um das Ein- und Entfernen von Audiogeräten zu erkennen und den Stream nach Bedarf auf diese Geräte umzustellen. Anwendungen, die WASAPI verwendeten, die keinen eigenen Streamroutingmechanismus beim Ein- oder Entfernen von Geräten implementierten, riskierten eine weniger als ideale Benutzererfahrung.

Ab der Windows 10 Version 1607 können Apps, die WASAPI verwenden, das automatische Streamrouting nutzen. Wenn Ihre Anwendung WASAPI verwendet, wird dringend empfohlen, die Anwendung mit den folgenden Schritten zu aktualisieren, um diese neue Funktion zu nutzen:

1.  Windows 10, Version 1607, definiert zwei neue GUIDs, mit denen eine Audiorendering- oder Erfassungsschnittstelle mit automatischem Streamrouting aktiviert werden kann: [DEVINTERFACE \_ AUDIO \_ RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) und [DEVINTERFACE \_ AUDIO \_ CAPTURE.](/windows/desktop/CoreAudio/devinterface-xxx-guids) Rufen Sie [**stringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid)auf, um eine Zeichenfolgendarstellung dieser GUIDs abzurufen. Das folgende Beispiel zeigt diesen Aufruf für die Audiorender-GUID.

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  Aktivieren Sie den Audioendpunkt, indem Sie die Bezeichnerzeichenfolge an die FUNKTION WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) übergeben. Im folgenden Beispiel wird der in Schritt 1 abgerufene Audiorenderbezeichner übergeben:

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  Freigeben des arbeitsspeichergebundenen Speichers für die Speicherung des Endpunktbezeichners:

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

Nachdem Sie Ihre App so geändert haben, dass die Audioschnittstelle auf die oben beschriebene Weise aktiviert wird, wird sie an der Funktion für automatisches Streamrouting beteiligt.

Um das automatische Streamrouting zu veranschaulichen, verwenden Sie einen Laptop oder ein Tablet, das mit internen Lautsprechern ausgestattet ist, um Audio wiederzuspielen. Sie sollten die Audiowiedergabe über die internen Lautsprecher des Geräts hören. Verbinden Sie während der Wiedergabe von Audiodaten ein Paar Mitwirkender. Sie sollten nun Audio hören, das durch die 160er-Jahre wiedergegeben wird. Trennen Sie dann die Stecknaps, und die Audiodaten sollten automatisch zurück an die internen Lautsprecher weitergeleitet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamrouting](stream-routing.md)
</dt> <dt>

[**MediaDevice.GetDefaultAudioRenderId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[**MediaDevice.GetDefaultAudioCaptureId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
