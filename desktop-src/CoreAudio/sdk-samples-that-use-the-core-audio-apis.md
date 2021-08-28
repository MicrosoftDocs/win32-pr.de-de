---
description: SDK-Beispiele, die die Kernaudio-APIs verwenden
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: SDK-Beispiele, die die Kernaudio-APIs verwenden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f875095579b40c6646d89e31328c148c5724c309
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479696"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>SDK-Beispiele, die die Kernaudio-APIs verwenden

Das Windows SDK enthält die folgenden Codebeispiele, die die Verwendung der Core Audio-APIs veranschaulichen. Die folgenden Beispiele befinden sich im Verzeichnis %MSSdk% samples multimedia audio, wobei \\ \\ %MSSdk% das Stammverzeichnis der Windows SDK-Installation auf Ihrem Computer \\ ist.




| Beispiel | Deaskription | 
|--------|--------------|
| <a href="aecmicarray.md">AECMicArray</a> | In diesem Beispiel werden die APIs MMDevice, WASAPI, DeviceTopology und EndpointVolume verwendet, um einen hochwertigen Sprachstream zu erfassen. Das Beispiel unterstützt die Verarbeitung von AEC (Acoustic Echo Cancellation) und Mikrofonarrays mithilfe des AEC-DMO auch als Spracherfassungs-DSP von Microsoft bezeichnet. | 
| <a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a> | Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten von einem Eingabegerät zu erfassen, das vom Benutzer angegeben wird, und schreibt sie in einen eindeutigen Namen. WAV-Datei im aktuellen Verzeichnis. In diesem Beispiel wird die ereignisgesteuerte Pufferung veranschaulicht. | 
| <a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a> | Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten von einem Eingabegerät zu erfassen, das vom Benutzer angegeben wird, und schreibt sie in einen eindeutigen Namen. WAV-Datei im aktuellen Verzeichnis. In diesem Beispiel wird die zeitgesteuerte Pufferung veranschaulicht. | 
| <a href="duckingcapturesample.md">IngCaptureSample</a> | Diese Beispielanwendung veranschaulicht das Öffnen und Schließen von Kommunikationsstreams und führt zu Verhendungsereignissen, die eine Anwendung erhalten kann, um die Streamdämpfung zu implementieren. Diese Anwendung implementiert einen Chatclient, der Core Audio-APIs verwendet, um Audiodaten von einem Kommunikationsgerät zu lesen und auf dem Ausgabegerät wieder zu spielen. | 
| <a href="endpointvolume.md">EndpointVolume</a> | Diese Beispielanwendung verwendet die Core Audio-APIs, um das Vom Benutzer angegebene Volumen des Geräts zu ändern. | 
| <a href="osd.md">OSD</a> | In diesem Beispiel werden die APIs MMDevice und EndpointVolume verwendet, um eine Anzeige auf dem Bildschirm zu implementieren, die Volumeänderungen am Ausgabestream zeigt, der über das Standardgerät des Audiorenderingendpunkts abspielt. Die Anzeige auf dem Bildschirm wird angezeigt, wenn der Benutzer die Volumeebene im Windows-Volumesteuerprogramm Sndvol.exe an passt und nicht mehr angezeigt wird, nachdem die Volumeebene für einen kurzen Zeitraum unverändert bleibt. | 
| <a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a> | Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern. In diesem Beispiel wird die ereignisgesteuerte Pufferung für einen Renderingclient im exklusiven Modus veranschaulicht. Bei einem Stream im exklusiven Modus teilt der Client den Endpunktpuffer mit dem Audiogerät. | 
| <a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a> | Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern. In diesem Beispiel wird die zeitgesteuerte Pufferung für einen Renderingclient im exklusiven Modus veranschaulicht. Bei einem Stream im exklusiven Modus teilt der Client den Endpunktpuffer mit dem Audiogerät. | 
| <a href="rendersharedeventdriven.md">RenderSharedEventDriven</a> | Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern. In diesem Beispiel wird die ereignisgesteuerte Pufferung für einen Renderingclient im freigegebenen Modus veranschaulicht. Bei einem Stream im freigegebenen Modus teilt der Client den Endpunktpuffer mit der Audio-Engine. | 
| <a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a> | Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern. In diesem Beispiel wird die zeitgesteuerte Pufferung für einen Renderingclient im freigegebenen Modus veranschaulicht. Bei einem Stream im freigegebenen Modus teilt der Client den Endpunktpuffer mit der Audio-Engine. | 
| WinAudio | In diesem Beispiel werden die MMDevice-API und WASAPI verwendet, um Audiostreams wieder- und zu erfassen. Über die Benutzeroberfläche dieser Beispielanwendung können Benutzer Audioendpunktgeräte auswählen, die Lautstärke der lokalen Audiositzung ändern und WAV-Dateien und Mikrofoneingaben wieder geben.<blockquote>[!Note]<br />Dieses Beispiel ist in 7 Windows veraltet.</blockquote><br /> | 




 

Sie können das Windows SDK von der [Microsoft Windows SDK Download Center-Website](https://developer.microsoft.com/windows/downloads/sdk-archive/) herunterladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows Core-Audio-APIs](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




