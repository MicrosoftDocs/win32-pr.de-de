---
description: MSYUV ist ein YUV-zu-RGB-Farbraumkonvertercodec.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: MSYUV-Farbraumkonvertercodec
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189ff787ee5b28311dd0357c245c7a6ca251d207f2448fc08a88fb856d7c2fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075740"
---
# <a name="msyuv-color-space-converter-codec"></a>MSYUV-Farbraumkonvertercodec

MSYUV ist ein YUV-zu-RGB-Farbraumkonvertercodec. Sie ermöglicht die Wiedergabe von Videoquelldaten in YUV-Formaten auf Clients, deren Videoanzeigeadapter nicht für YUV-zu-RGB-Konvertierungen in Hardware verwendet werden kann. Der Codec nimmt über den [WRAPPERfilter AVI Decompressor](avi-decompressor-filter.md) an Filterdiagrammen teil.

Digitale Konferenzkameras mit 1394- oder USB-Schnittstellen können Bilddaten in verschiedenen YUV-Formaten erzeugen. Wenn die Anzeigehardware die YuV-zu-RGB-Konvertierung im Board nicht unterstützt oder die Hardwarekonvertierungsfunktion aus einem anderen Grund nicht verwendet werden kann, müssen die YUV-Bilddaten in das RGB-Format konvertiert werden, bevor sie an den Videorenderer gesendet werden.

Aufgrund der Anforderung des [Videorenderers](video-renderer-filter.md)an einen RGB-Eingabetyp zum Zeitpunkt der Verbindung kann dieser Filter während der automatischen Grapherstellung vom Videorenderer in ein Diagramm vorgeschaltet werden. Insbesondere wenn der Graph Builder ein YUV-Format im Medientyp des Ausgabepins des Upstreamfilters erkennt, fügt der Graph Builder den AVI-Dekomprimierer ein, der dann den MSYUV-Codec lädt und ihn anfänglich für die Konvertierung in RGB konfiguriert. Nachdem das Diagramm zum ersten Mal in einen Ausführungs- oder Angehalten-Zustand übergeht, kann der Videorenderer-Filter erkennen, ob der Videoanzeigeadapter die Konvertierung in Hardware durchführen kann. Wenn dies möglich ist, wird der AVI-Dekomprimierer benachrichtigt und konfiguriert MSYUV neu für den Betrieb im "Pass-Through-Modus", wodurch der Codec die Konvertierung überspringt und die YUV-Bilddaten direkt auf eine DirectDraw-Überlagerungsoberfläche im Videospeicher kopiert.

Da die VideoMischungsrenderer (VMR-7 und VMR-9) nie GDI verwenden, benötigen sie zur Verbindungszeit keinen RGB-Typ, und der MSYUV Color Space Converter wird nie vor der VMR in einem Diagramm eingefügt.

MSYUV konvertiert gepackte YUV-Formate in RGB, wie in der folgenden Liste dargestellt:

-   Eingabeformate: UYVY, YUY2, YVDURCHLÄSSIG
-   Ausgabeformate: RGB 8, RGB 16, RGB 24, RGB 32

Der MSYUV Color Space Converter-Codec ist ein VCM-Codec (Video Compression Manager). Sie wird in DirectShow über den [AVI-Dekomprimiererfilter](avi-decompressor-filter.md) verwendet. Für einen allgemeineren Farbkonverter verwenden Sie den [**Farbkonverter-DSP.**](../medfound/colorconverter.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 
