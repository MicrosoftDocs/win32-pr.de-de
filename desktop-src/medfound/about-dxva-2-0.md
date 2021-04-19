---
description: Übersicht über DXVA 2 und seine Beziehung zu DXVA 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: Informationen zu DXVA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f622c863f433be44bbce6460024ffb06bb1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348798"
---
# <a name="about-dxva-20"></a>Informationen zu DXVA 2,0

Bei DirectX Video Acceleration (DXVA) handelt es sich um eine API und ein entsprechendes DDI zum beschleunigen der Video Verarbeitung mithilfe der Hardwarebeschleunigung. Software Codecs und Software-Video Prozessoren können mithilfe von DXVA bestimmte CPU-intensive Vorgänge an die GPU auslagern. Beispielsweise kann ein Software Decoder die umgekehrte diskrete Kosinus Transformation (IDCT) in die GPU auslagern.

In DXVA werden einige Decodierungs Vorgänge vom Grafikhardware Treiber implementiert. Dieser Funktions Satz wird als *Accelerator* bezeichnet. Andere Decodierungs Vorgänge werden von der Benutzermodus-Anwendungssoftware implementiert, die als *Host Decoder* oder *Software Decoder* bezeichnet wird. (Die Begriffe *Host Decoder* und *Software Decoder* sind gleichwertig.) Die von der Zugriffstaste ausgeführte Verarbeitung wird als *Off-Host-Verarbeitung* bezeichnet. In der Regel verwendet die Zugriffstaste die GPU, um einige Vorgänge zu beschleunigen. Wenn die Zugriffstaste einen Decodierungs Vorgang ausführt, muss der Host Decoder die Zugriffstasten Puffer mit den zum Ausführen des Vorgangs erforderlichen Informationen übermitteln.

Die DXVA 2-API erfordert Windows Vista oder höher. Die DXVA 1-API wird in Windows Vista weiterhin aus Gründen der Abwärtskompatibilität unterstützt. Es wird eine Emulations Ebene bereitgestellt, die sowohl zwischen Version der API als auch mit der gegenüberliegenden Version des DDI konvertiert:

-   Wenn der Grafiktreiber dem Windows-Anzeigetreiber Modell (WDDM) entspricht, werden DXVA 1-API-Aufrufe in DXVA 2 DDI-Aufrufe konvertiert.
-   Wenn die Grafiktreiber das ältere Windows XP-Anzeigetreiber Modell (XPDM) verwenden, werden DXVA 2-API-Aufrufe in DXVA 1 DDI-Aufrufe konvertiert.

In der folgenden Tabelle werden die Betriebssystemanforderungen und die unterstützten Videorenderer für jede Version der DXVA-API angezeigt.



| API-Version | Anforderungen          | Unterstützung für Videorenderer                        |
|-------------|-----------------------|-----------------------------------------------|
| DXVA 1      | Windows 2000 oder höher | Overlay-Mixer, VMR-7, VMR-9 (nur DirectShow) |
| DXVA 2      | Windows Vista         | EVR (DirectShow und Media Foundation)         |



 

In DXVA 1 muss der Software Decoder über den Videorenderer auf die API zugreifen können. Es gibt keine Möglichkeit, die DXVA 1-API zu verwenden, ohne den Videorenderer aufrufen zu müssen. Diese Einschränkung wurde mit DXVA 2 entfernt. Mithilfe von DXVA 2 kann der Host Decoder (oder eine beliebige Anwendung) direkt über die [**idirectxvideodecoderservice**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) -Schnittstelle auf die API zugreifen.

Die DXVA 1-Dokumentation beschreibt die Decodierungs Strukturen, die für die folgenden Videostandards verwendet werden:

-   ITU-T Rec. H. 261
-   ITU-T Rec. H. 263
-   MPEG-1-Video
-   Video zu MPEG-2-Hauptprofil

Die folgenden Spezifikationen definieren DXVA-Erweiterungen für andere Videostandards:

-   [DXVA-Spezifikation für H. 264/AVC-Decodierung](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [DXVA-Spezifikation für H. 264/MPEG-4 AVC MultiView Video Coding (MVC), einschließlich Stereo High Profile](https://www.microsoft.com/download/details.aspx?id=25200)
-   [DXVA-Spezifikation für MPEG-1 VLD und kombinierte MPEG-1/MPEG-2 VLD Video Decodierung](https://www.microsoft.com/download/details.aspx?id=9374).
-   [DXVA-Spezifikation für Off-Host VLD-Modus für MPEG-4 Part 2-Video Decodierung](https://www.microsoft.com/download/details.aspx?id=21100)
-   [DXVA-Spezifikation für Windows Media Video® V8, v9 und VA-Decodierung (einschließlich SMPTE 421m "VC-1")](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [DirectX Video Acceleration (DXVA)-Spezifikation für H. 264/MPEG-4 Scalable Video Coding (SVC) Off-Host VLD-modusdecodierung](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [DirectX-Videobeschleunigung-Spezifikation für VP8-und VP9-Videocodierung](https://www.microsoft.com/download/details.aspx?id=49188)

DXVA 1 und DXVA 2 verwenden dieselben Datenstrukturen für das decodieren. Die Prozedur zum Konfigurieren der Decodierungs Sitzung hat sich jedoch geändert. DXVA 1 verwendet einen "Probe and Lock"-Mechanismus, bei dem der Host-Decoder verschiedene Konfigurationen testen kann, bevor die gewünschte Konfiguration auf der Zugriffstaste festgelegt wird. In DXVA 2 gibt die Zugriffstaste eine Liste der unterstützten Konfigurationen zurück, und der Host Decoder wählt eine Liste aus der Liste aus. Details finden Sie in den folgenden Abschnitten:

-   [Unterstützung von DXVA 2,0 in DirectShow](supporting-dxva-2-0-in-directshow.md)
-   [Unterstützung von DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA 1,0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
