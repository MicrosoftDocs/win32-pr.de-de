---
description: Msyuv ist ein YUV-zu-RGB-Farb Raum Konverter-Codec.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Msyuv Color Space Converter-Codec
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371316"
---
# <a name="msyuv-color-space-converter-codec"></a>Msyuv Color Space Converter-Codec

Msyuv ist ein YUV-zu-RGB-Farb Raum Konverter-Codec. Sie ermöglicht die Wiedergabe von Video Quelldaten in YUV-Formaten auf Clients, deren Videoanzeige Adapter nicht für YUV-zu-RGB-Konvertierungen in der Hardware verwendet werden kann. Der Codec ist an Filter Diagrammen über den [AVI](avi-decompressor-filter.md) -Debug-Wrapper Filter beteiligt.

Digitale Konferenz Kameras mit 1394-oder USB-Schnittstellen können Bilddaten in verschiedenen YUV-Formaten liefern. Wenn die Anzeige Hardware die Konvertierung von YUV zu RGB nicht unterstützt, oder wenn die Hardware Konvertierungs Funktion aus einem anderen Grund nicht verwendet werden kann, müssen die YUV-Bilddaten in das RGB-Format konvertiert werden, bevor Sie an den Videorenderer gesendet werden.

Aufgrund der Anforderung eines [Video-Renderers](video-renderer-filter.md)für einen RGB-Eingabetyp zur Verbindungszeit kann dieser Filter während des automatischen Diagramms in ein Diagramm vom Videorenderer eingefügt werden. Insbesondere wenn der Graph-Generator ein YUV-Format im Medientyp der Ausgabepin des Upstream-Filters erkennt, fügt der Graph-Generator den AVI-Dekompressor ein, der dann den msyuv-Codec lädt und ihn anfänglich für die Konvertierung in RGB konfiguriert. Nachdem das Diagramm zum ersten Mal in den Zustand "wird ausgeführt" oder "angehalten" übergeht, kann der Videorendererfilter erkennen, ob der Videoanzeige Adapter die Konvertierung in die Hardware durchführen kann. Wenn dies der Fall ist, wird der AVI-Dekompressor benachrichtigt und der msyuv-Dienst für den Betrieb im "Pass-Through-Modus" neu konfiguriert. Dies bewirkt, dass der Codec die Konvertierung überspringt und die YUV-Bilddaten direkt auf eine DirectDraw-Overlay-Oberfläche im Videospeicher kopiert.

Da die Video Mischungs Renderer (VMR-7 und VMR-9) niemals GDI verwenden, benötigen Sie zum Zeitpunkt der Verbindungs Herstellung keinen RGB-Typ, und der msyuv Color Space Converter wird nie vor dem VMR in einem Diagramm eingefügt.

Msyuv konvertiert gepackte YUV-Formate in RGB, wie in der folgenden Liste gezeigt:

-   Eingabeformate: UYVY, im YUY2, yvyu
-   Ausgabeformate: RGB 8, RGB 16, RGB 24, RGB 32

Der msyuv Color Space Converter Codec ist ein Video Komprimierungs-Manager-Codec (VCM). Sie wird in DirectShow über den [AVI](avi-decompressor-filter.md) -Debug-Filter verwendet. Verwenden Sie für einen allgemeineren Farb Konverter den [**Farb Konverter DSP**](../medfound/colorconverter.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 
