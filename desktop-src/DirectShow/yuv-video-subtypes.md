---
description: 'YUV-Formate werden nach den folgenden Informationen kategorisiert:'
ms.assetid: 452f017c-81ce-4be4-9962-4b9c1a9ce849
title: YUV-Video Untertypen (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312a3d9d8e12953353ed0f61fff67a05bf87426b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354814"
---
# <a name="yuv-video-subtypes"></a>Untertypen von YUV-Video

YUV-Formate werden nach den folgenden Informationen kategorisiert:

**Gepackte Formate im Vergleich zu planaren Formaten.** In einem gepackten Format werden die Y-, U-und V-Komponenten in einem einzelnen Array gespeichert. Pixel sind in Gruppen von macropixels organisiert, deren Layout vom Format abhängt. In einem planaren Format werden die Y-, U-und V-Komponenten separat, also drei Ebenen, gespeichert.

**Chroma-Stichprobenentnahme.** Eine Notation mit dem Namen "a:b: C-Notation" wird verwendet, um zu beschreiben, wie oft Sie und V in Relation zu Y Stichproben Proben

-   4:4:4 bedeutet, dass die Chroma-Kanäle nicht herabgestuft werden.
-   4:2:2 bedeutet 2:1 horizontale Downsampling ohne vertikale Downsampling. Jede Scanzeile enthält vier Y-Beispiele für alle zwei U-oder V-Beispiele.
-   4:2:0 bedeutet 2:1 horizontale Downsampling mit 2:1 vertikaler Downsampling.
-   4:1:1 bedeutet 4:1 horizontale Downsampling ohne vertikale Downsampling. Jede Scanzeile enthält vier Y-Beispiele für jedes U-oder V-Beispiel. 4:1:1 die Stichprobenentnahme ist weniger häufig als andere Formate und wird in diesem Artikel nicht ausführlich erläutert.

**Bits pro Kanal.** Die häufigsten Beispiel Größen sind 8, 10 oder 16 Bits pro Stichprobe. Einige YUV-Formate sind palettisiert.

**Arbeitsspeicher Layout.** Zwei YUV-Format Typen können anderweitig identisch sein, aber unterschiedliche Order-Vorgänge für die Y-, V-und U-Beispiele im Arbeitsspeicher verwenden.

**Empfohlene YUV-Formate**



| GUID               | Format | Stichproben | Gepackt oder planare | Bits pro Kanal |
|--------------------|--------|----------|------------------|------------------|
| mediasubtype \_ ayuv | Ayuv   | 4:4:4    | Stop           | 8                |
| Mediasubtype \_ im YUY2 | Im YUY2   | 4:2:2    | Stop           | 8                |
| mediasubtype \_ UYVY | UYVY   | 4:2:2    | Stop           | 8                |
| Mediasubtype \_ IMC1 | IMC1   | 4:2:0    | Planare           | 8                |
| Mediasubtype \_ IMC3 | IMC2   | 4:2:0    | Planare           | 8                |
| Mediasubtype \_ IMC2 | IMC3   | 4:2:0    | Planare           | 8                |
| Mediasubtype \_ IMC4 | IMC4   | 4:2:0    | Planare           | 8                |
| Mediasubtype \_ YV12 | YV12   | 4:2:0    | Planare           | 8                |
| Mediasubtype \_ NV12 | NV12   | 4:2:0    | Planare           | 8                |



 

Eine Beschreibung dieser YUV-Formate für Video Rendering unter Windows finden Sie unter [Empfohlene 8-Bit-YUV-Formate für Video Rendering](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md) .

**Andere YUV-Format Typen**



| GUID               | Format                                                | Stichproben                                                | Gepackt oder planare                                  | Bits pro Kanal                             |
|--------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|----------------------------------------------|
| Mediasubtype \_ I420 | I420                                                  | 4:2:0                                                   | Planare                                            | 8                                            |
| Mediasubtype \_ IF09 | Wird nicht mehr unterstützt.<br/> Indeo YVU9<br/> | Wird nicht mehr unterstützt.<br/> Siehe Bemerkungen.<br/> | Wird nicht mehr unterstützt.<br/> Planare<br/> | Wird nicht mehr unterstützt.<br/> 8<br/> |
| mediasubtype \_ IYUV | IYUV                                                  | 4:2:0                                                   | Planare                                            | 8                                            |
| Mediasubtype \_ Y211 | Y211                                                  | Siehe Bemerkungen.                                            | Stop                                            | 8                                            |
| Mediasubtype \_ Y411 | Y411                                                  | 4:1:1                                                   | Stop                                            | 8                                            |
| Mediasubtype \_ im y41p | Im y41p                                                  | 4:1:1                                                   | Stop                                            | 8                                            |
| Mediasubtype \_ YVU9 | YVU9                                                  | Siehe Bemerkungen.                                            | Planare                                            | 8                                            |
| mediasubtype \_ yvyu | Im yvyu                                                  | 4:2:2                                                   | Stop                                            | 8                                            |



 

-   I420 besteht aus einer Y-Ebene, gefolgt von einer U-Ebene und einer V-Ebene.
-   IYUV ist mit I420 identisch.
-   Bei Y211 handelt es sich um ein gepacktes Format, bei dem Y alle 2 Pixel horizontal abgefragt wird, und Sie und V werden horizontal alle 4 Pixel abgetastet. Jedes Makro Pixel beträgt 4 Bytes und enthält 4 Pixel. Es verwendet die folgende Byte Reihenfolge:

    `Y0 U0 Y2 V0    Y4 U4 Y6 V4    Y8 U8 Y10 V8`

-   Im y41p ist ein 4:1:1-gepacktes Format. Es verwendet die folgende Byte Reihenfolge:

    `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`

-   YVU9 ist ein planare-Format, in dem Sie und V alle 4 Pixel horizontal und vertikal (manchmal auch als 16:1:1 bezeichnet) abgetastet werden. Die Ebene "V" wird vor der U-Ebene angezeigt.
-   Das Indeo YVU9 Format (mediasubtype \_ IF09) ist eine Variation von YVU9 mit zusätzlichen Delta Frame Informationen nach der U-Ebene. Der Indeo-Codec wird in Windows nicht mehr unterstützt.
-   Yvyu ähnelt UYVY in einer anderen Byte Reihenfolge: `Y0 V0 Y1 U0`

-   Der Indeo-Codec wird in Windows nicht mehr unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Empfohlene 8-Bit-YUV-Formate für Video Rendering](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Video Untertypen](video-subtypes.md)
</dt> <dt>

[Arbeiten mit Video Frames](working-with-video-frames.md)
</dt> </dl>

 

 
