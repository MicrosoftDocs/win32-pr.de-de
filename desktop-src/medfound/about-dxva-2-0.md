---
description: Übersicht über DXVA 2 und seine Beziehung zu DXVA 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: Informationen zu DXVA 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d6ab595be1f167f777e50001c8d31658dc697866c8d11db3865e66e87508ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606820"
---
# <a name="about-dxva-20"></a>Informationen zu DXVA 2.0

DirectX Video Acceleration (DXVA) ist eine API und eine entsprechende DDI für die Verwendung der Hardwarebeschleunigung, um die Videoverarbeitung zu beschleunigen. Softwarecodecs und Softwarevideoprozessoren können DXVA verwenden, um bestimmte CPU-intensive Vorgänge an die GPU auszulagern. Beispielsweise kann ein Softwaredecoder die inverse diskrete Kosinustransformation (iDCT) an die GPU auslagern.

In DXVA werden einige Decodierungsvorgänge vom Grafikhardwaretreiber implementiert. Dieser Satz von Funktionen wird als *Zugriffstaste* bezeichnet. Andere Decodierungsvorgänge werden von der Anwendungssoftware im Benutzermodus implementiert, die als *Hostdecoder* oder *Softwaredecoder* bezeichnet wird. (Die Begriffe *Hostdecoder* und *Softwaredecoder* sind gleichwertig.) Die vom Accelerator ausgeführte Verarbeitung wird als *Offhostverarbeitung* bezeichnet. In der Regel verwendet der Accelerator die GPU, um einige Vorgänge zu beschleunigen. Immer wenn die Zugriffstaste einen Decodierungsvorgang ausführt, muss der Hostdecoder den Zugriffstastenpuffern übermitteln, die die zum Ausführen des Vorgangs erforderlichen Informationen enthalten.

Die DXVA 2-API erfordert Windows Vista oder höher. Die DXVA 1-API wird in Windows Vista aus Gründen der Abwärtskompatibilität weiterhin unterstützt. Es wird eine Emulationsebene bereitgestellt, die zwischen beiden Versionen der API und der entgegengesetzten Version der DDI konvertiert:

-   Wenn der Grafiktreiber dem Windows Display Driver Model (WDDM) entspricht, werden DXVA 1-API-Aufrufe in DXVA 2 DDI-Aufrufe konvertiert.
-   Wenn die Grafiktreiber das ältere Windows XP Display Driver Model (XPDM) verwenden, werden DXVA 2-API-Aufrufe in DXVA 1 DDI-Aufrufe konvertiert.

Die folgende Tabelle zeigt die Betriebssystemanforderungen und die unterstützten Videorenderer für jede Version der DXVA-API.



| API-Version | Anforderungen          | Videorenderer-Unterstützung                        |
|-------------|-----------------------|-----------------------------------------------|
| DXVA 1      | Windows 2000 oder höher | Overlay Mixer, VMR-7, VMR-9 (nur DirectShow) |
| DXVA 2      | Windows Vista         | EVR (DirectShow und Media Foundation)         |



 

In DXVA 1 muss der Softwaredecoder über den Videorenderer auf die API zugreifen. Es gibt keine Möglichkeit, die DXVA 1-API zu verwenden, ohne den Videorenderer aufzurufen. Diese Einschränkung wurde mit DXVA 2 aufgehoben. Mit DXVA 2 kann der Hostdecoder (oder eine beliebige Anwendung) direkt über die [**IDirectXVideoDecoderService-Schnittstelle**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) auf die API zugreifen.

In der DXVA 1-Dokumentation werden die Decodierungsstrukturen beschrieben, die für die folgenden Videostandards verwendet werden:

-   ITU-T Rec. H.261
-   ITU-T Rec. H.263
-   MPEG-1-Video
-   MPEG-2-Hauptprofilvideo

Die folgenden Spezifikationen definieren DXVA-Erweiterungen für andere Videostandards:

-   [DXVA-Spezifikation für H.264/AVC-Decodierung](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [DXVA-Spezifikation für H.264/MPEG-4 AVC Multiview Video Coding (MVC), einschließlich Stereo High Profile](https://www.microsoft.com/download/details.aspx?id=25200)
-   [DXVA-Spezifikation für MPEG-1-VLD und kombinierte MPEG-1/MPEG-2-VLD-Videodecodierung.](https://www.microsoft.com/download/details.aspx?id=9374)
-   [DXVA-Spezifikation für Off-Host VLD-Modus für MPEG-4 Part 2 Video Decoding](https://www.microsoft.com/download/details.aspx?id=21100)
-   [DXVA-Spezifikation für Windows Media Video® v8-, v9- und vA-Decodierung (einschließlich SMPTE 421M "VC-1")](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [DXVA-Spezifikation (DirectX Video Acceleration) für die decodierung im VLD-Modus (Scalable Video Coding, SVC Off-Host) für H.264/MPEG-4](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [DirectX-Videobeschleunigungsspezifikation für VP8- und VP9-Videocodierung](https://www.microsoft.com/download/details.aspx?id=49188)

DXVA 1 und DXVA 2 verwenden die gleichen Datenstrukturen für die Decodierung. Das Verfahren zum Konfigurieren der Decodierungssitzung wurde jedoch geändert. DXVA 1 verwendet einen "Test- und Sperrmechanismus", bei dem der Hostdecoder verschiedene Konfigurationen testen kann, bevor die gewünschte Konfiguration auf der Zugriffstaste festgelegt wird. In DXVA 2 gibt der Accelerator eine Liste der unterstützten Konfigurationen zurück, und der Hostdecoder wählt eine konfiguration aus der Liste aus. Details finden Sie in den folgenden Abschnitten:

-   [Unterstützen von DXVA 2.0 in DirectShow](supporting-dxva-2-0-in-directshow.md)
-   [Unterstützung von DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA 1.0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
