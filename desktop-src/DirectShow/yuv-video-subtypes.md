---
description: 'YUV-Formate werden nach den folgenden Informationen kategorisiert:'
ms.assetid: 452f017c-81ce-4be4-9962-4b9c1a9ce849
title: YUV-Videountertypen (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d31afa11c855b865c7e524d393d1f86ae836e00119a3171b35a3c0c2549d184b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632690"
---
# <a name="yuv-video-subtypes"></a>YUV-Videountertypen

YUV-Formate werden nach den folgenden Informationen kategorisiert:

**Gepackte Formate im Vergleich zu planaren Formaten.** In einem gepackten Format werden die Komponenten Y, U und V in einem einzelnen Array gespeichert. Pixel sind in Gruppen von Makropixeln organisiert, deren Layout vom Format abhängt. In einem planaren Format werden die Komponenten Y, U und V separat als drei Ebenen gespeichert.

**Sampling von Mustern.** Eine Notation namens A:B:C-Notation wird verwendet, um zu beschreiben, wie oft für Sie und V im Verhältnis zu Y Stichproben entnommen werden:

-   4:4:4 bedeutet kein Downsampling der Senderkanäle.
-   4:2:2 bedeutet 2:1 horizontales Downsampling ohne vertikales Downsampling. Jede Scanzeile enthält vier Y-Stichproben für alle zwei U- oder V-Beispiele.
-   4:2:0 bedeutet 2:1 horizontales Downsampling, mit 2:1 vertikalem Downsampling.
-   4:1:1 bedeutet 4:1 horizontales Downsampling ohne vertikales Downsampling. Jede Scanzeile enthält vier Y-Stichproben für jedes U- oder V-Beispiel. 4:1:1 Sampling ist weniger üblich als andere Formate und wird in diesem Artikel nicht ausführlich erläutert.

**Bits pro Kanal.** Die gängigsten Stichprobengrößen sind 8, 10 oder 16 Bits pro Stichprobe. Einige YUV-Formate sind palettiert.

**Speicherlayout.** Zwei YUV-Formattypen können andernfalls identisch sein, verwenden jedoch unterschiedliche Reihenfolgen für die Y-, V- und U-Beispiele im Arbeitsspeicher.

**Empfohlene YUV-Formate**



| GUID               | Format | Stichproben | Gepackt oder planar | Bits pro Kanal |
|--------------------|--------|----------|------------------|------------------|
| MEDIASUBTYPE \_ AYUV | AYUV   | 4:4:4    | Verpackt           | 8                |
| MEDIASUBTYPE \_ YUY2 | YUY2   | 4:2:2    | Verpackt           | 8                |
| MEDIASUBTYPE \_ UY WIE | UYAFFINITÄT   | 4:2:2    | Verpackt           | 8                |
| MEDIASUBTYPE \_ IMC1 | IMC1   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ IMC3 | IMC2   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ IMC2 | IMC3   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ IMC4 | IMC4   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ YV12 | YV12   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ NV12 | NV12   | 4:2:0    | Planar           | 8                |



 

Eine Beschreibung dieser YUV-Formate für video rendering on Windows finden Sie unter [Recommended 8-Bit YUV Formats for Video Rendering (Empfohlene 8-Bit-YUV-Formate für video rendering).](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)

**Andere YUV-Formattypen**



| GUID               | Format                                                | Stichproben                                                | Gepackt oder planar                                  | Bits pro Kanal                             |
|--------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|----------------------------------------------|
| MEDIASUBTYPE \_ I420 | I420                                                  | 4:2:0                                                   | Planar                                            | 8                                            |
| MEDIASUBTYPE \_ IF09 | Wird nicht mehr unterstützt.<br/> Indeo YHOR9<br/> | Wird nicht mehr unterstützt.<br/> Siehe Bemerkungen.<br/> | Wird nicht mehr unterstützt.<br/> Planar<br/> | Wird nicht mehr unterstützt.<br/> 8<br/> |
| MEDIASUBTYPE \_ IYUV | IYUV                                                  | 4:2:0                                                   | Planar                                            | 8                                            |
| MEDIASUBTYPE \_ Y211 | Y211                                                  | Siehe Bemerkungen.                                            | Verpackt                                            | 8                                            |
| MEDIASUBTYPE \_ Y411 | Y411                                                  | 4:1:1                                                   | Verpackt                                            | 8                                            |
| MEDIASUBTYPE \_ Y41P | Y41P                                                  | 4:1:1                                                   | Verpackt                                            | 8                                            |
| MEDIASUBTYPE \_ Y CHRONO9 | YVU9                                                  | Siehe Bemerkungen.                                            | Planar                                            | 8                                            |
| MEDIASUBTYPE \_ YVINNEN | YVKY                                                  | 4:2:2                                                   | Verpackt                                            | 8                                            |



 

-   I420 besteht aus einer Y-Ebene, gefolgt von einer U-Ebene, gefolgt von einer V-Ebene.
-   IYUV ist identisch mit I420.
-   Y211 ist ein gepacktes Format, in dem Y alle 2 Pixel horizontal abtastiert wird und sie und V alle 4 Pixel horizontal entnommen werden. Jedes Makropixel ist 4 Bytes und enthält 4 Pixel. Dabei wird die folgende Byte reihenfolge verwendet:

    `Y0 U0 Y2 V0    Y4 U4 Y6 V4    Y8 U8 Y10 V8`

-   Y41P ist ein gepacktes 4:1:1-Format. Dabei wird die folgende Byte reihenfolge verwendet:

    `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`

-   YJAR9 ist ein planares Format, bei dem Sie und V alle 4 Pixel horizontal und vertikal abtast (manchmal auch als 16:1:1 bezeichnet). Die V-Ebene wird vor der U-Ebene angezeigt.
-   Das Indeo YIVA9-Format (MEDIASUBTYPE IF09) ist eine Variation von YIVA9 mit zusätzlichen \_ Deltaframeinformationen nach der U-Ebene. Der Indeo-Codec wird in der Anwendung nicht mehr Windows.
-   YVAFFIN ähnelt UYAFFIN mit einer anderen Byte reihenfolge: `Y0 V0 Y1 U0`

-   Der Indeo-Codec wird in der Anwendung nicht mehr Windows.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Empfohlene 8-Bit-YUV-Formate für video rendering](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Videountertypen](video-subtypes.md)
</dt> <dt>

[Arbeiten mit Videoframes](working-with-video-frames.md)
</dt> </dl>

 

 
