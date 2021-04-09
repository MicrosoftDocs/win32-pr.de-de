---
description: SDK-Beispiele für die Verwendung der kernaudioapis
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: SDK-Beispiele für die Verwendung der kernaudioapis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958426"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>SDK-Beispiele für die Verwendung der kernaudioapis

Die Windows SDK enthält die folgenden Codebeispiele, die die Verwendung der kernaudioapis veranschaulichen. Die folgenden Beispiele befinden sich im Verzeichnis% MSSDK% \\ Samples \\ Multimedia \\ Audiodatei, wobei% MSSDK% das Stammverzeichnis der Windows SDK-Installation auf Ihrem Computer ist.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Beispiel</th>
<th>Wird entschlüsselt.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="aecmicarray.md">Aecmicarray</a></td>
<td>In diesem Beispiel werden die APIs mmdevice, WASAPI, devicetopology und endpointvolume verwendet, um einen hochwertigen sprach Datenstrom zu erfassen. Das Beispiel unterstützt die Verarbeitung von Akustik Echo Abbruch (AEC) und die Verarbeitung von mikrofonarrays mithilfe des AEC-DMO, der auch als sprach Erfassungs-DSP von Microsoft bereitgestellt wird.</td>
</tr>
<tr class="even">
<td><a href="capturesharedeventdriven.md">Capturesharedebug</a></td>
<td>Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem Eingabegerät, das vom Benutzer angegeben wird, aufzuzeichnen und in einen eindeutigen Namen zu schreiben. WAV-Datei im aktuellen Verzeichnis. In diesem Beispiel wird die ereignisgesteuerte Pufferung veranschaulicht.</td>
</tr>
<tr class="odd">
<td><a href="capturesharedtimerdriven.md">Capturesharedtimer-gesteuert</a></td>
<td>Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem Eingabegerät, das vom Benutzer angegeben wird, aufzuzeichnen und in einen eindeutigen Namen zu schreiben. WAV-Datei im aktuellen Verzeichnis. In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung veranschaulicht.</td>
</tr>
<tr class="even">
<td><a href="duckingcapturesample.md">Duckingcapturesample</a></td>
<td>Diese Beispielanwendung veranschaulicht das Öffnen und Schließen von Kommunikationsstreams und bewirkt, dass Ducking-Ereignisse auftreten, die eine Anwendung zum Implementieren der Datenstrom Dämpfung erhalten kann. Diese Anwendung implementiert einen Chat Client, der kernaudioapis verwendet, um Audiodaten von einem Kommunikationsgerät zu lesen und auf dem Ausgabegerät wiederzugeben.</td>
</tr>
<tr class="odd">
<td><a href="endpointvolume.md">Endpointvolume</a></td>
<td>Diese Beispielanwendung verwendet die kernweb-APIs, um das vom Benutzer angegebene Volume des Geräts zu ändern.</td>
</tr>
<tr class="even">
<td><a href="osd.md">OSD</a></td>
<td>Dieses Beispiel verwendet die mmdevice-und endpointvolume-APIs, um eine Bildschirm Anzeige zu implementieren, die volumeänderungen an dem Ausgabestream anzeigt, die über das standardmäßige audiorenderingendpunkt-Gerät abgespielt werden. Die Anzeige auf dem Bildschirm wird angezeigt, wenn der Benutzer die Volumeebene im Windows-Programm zur volumesteuerung (Sndvol.exe) anpasst, und er verschwindet, wenn die Volumeebene für einen kurzen Zeitraum unverändert bleibt.</td>
</tr>
<tr class="odd">
<td><a href="renderexclusiveeventdriven.md">Renderexclusiveeventdriver</a></td>
<td>Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering. In diesem Beispiel wird die ereignisgesteuerte Pufferung für einen renderingclient im exklusiven Modus veranschaulicht. Für einen Stream im exklusiven Modus gibt der Client den Endpunkt Puffer mit dem Audiogerät frei.</td>
</tr>
<tr class="even">
<td><a href="renderexclusivetimerdriven.md">Renderexclusivetimer-gesteuert</a></td>
<td>Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering. In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung für einen renderingclient im exklusiven Modus veranschaulicht. Für einen Stream im exklusiven Modus gibt der Client den Endpunkt Puffer mit dem Audiogerät frei.</td>
</tr>
<tr class="odd">
<td><a href="rendersharedeventdriven.md">Rendersharedebug-gesteuert</a></td>
<td>Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering. Dieses Beispiel veranschaulicht die ereignisgesteuerte Pufferung für einen renderingclient im freigegebenen Modus. Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine.</td>
</tr>
<tr class="even">
<td><a href="rendersharedtimerdriven.md">Rendersharedtimer-gesteuert</a></td>
<td>Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering. Dieses Beispiel veranschaulicht die Zeit Geber gesteuerte Pufferung für einen renderingclient im freigegebenen Modus. Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine.</td>
</tr>
<tr class="odd">
<td>Winaudiodatei</td>
<td>In diesem Beispiel werden die mmdevice-API und die WASAPI verwendet, um Audiostreams wiederzugeben und zu erfassen. Die Benutzeroberfläche dieser Beispielanwendung ermöglicht Benutzern das Auswählen von audioendpunktgeräten, das Ändern der Volumeebene der lokalen Audiositzung und das Wiedergeben von WAV-Dateien und Mikrofon Eingaben.
<blockquote>
[!Note]<br />
Dieses Beispiel wurde in Windows 7 als veraltet eingestuft.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Sie können die Windows SDK von der [Microsoft Windows SDK Download Center](https://developer.microsoft.com/windows/downloads/sdk-archive/) -Website herunterladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu den Windows Core-audioapis](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




