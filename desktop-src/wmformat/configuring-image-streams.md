---
title: Konfigurieren von Streams
description: Konfigurieren von Streams
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- Streams,Konfigurieren von Imagestreams
- Codecs,Konfigurieren von Imagestreams
- Imagestreams,Konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ce58fe3da709772b08d0956f3f5540713f7960742338f73c9d9807ad1a1e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848965"
---
# <a name="configuring-image-streams"></a>Konfigurieren von Streams

Bildstreams enthalten noch Bilder im JPEG-Format. Obwohl Bildstreams wie Videostreams sind, da sie nicht komprimierte Bilder als Eingaben verwenden, erfordern sie eine etwas andere Konfiguration. Zum Konfigurieren eines Bilddatenstroms müssen Sie die Werte für die Member der Videokonfigurationsstrukturen festlegen, wie in der folgenden Tabelle gezeigt.



| Einstellung                                                           | Beschreibung                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ MEDIA \_ TYPE.majortype**                                     | Legen Sie auf WMMEDIATYPE \_ Image fest.                                                                                                                                                       |
| **WM \_ MEDIA \_ TYPE.subtype**                                       | Legen Sie auf WMMEDIASUBTYPE \_ RGB24 fest.                                                                                                                                                    |
| **WM \_ MEDIA \_ TYPE.bFixedSizeSamples**                             | Legen Sie auf **FALSE fest.**                                                                                                                                                                |
| **WM \_ MEDIA \_ TYPE.bTemporalCompression**                          | Legen Sie auf **FALSE fest.**                                                                                                                                                                |
| **WM \_ MEDIA \_ TYPE.lSampleSize**                                   | Auf 0 festlegen.                                                                                                                                                                        |
| **WM \_ MEDIA \_ TYPE.formattype**                                    | Legen Sie auf WMFORMAT \_ VideoInfo fest.                                                                                                                                                      |
| **WM \_ MEDIA \_ TYPE.pUnk**                                          | Legen Sie auf **NULL fest.**                                                                                                                                                                 |
| **WM \_ MEDIA \_ TYPE.cbFormat**                                      | Legen Sie diese Option auf `sizeof(WMVIDEOINFOHEADER)` fest.                                                                                                                                              |
| **WM \_ MEDIA \_ TYPE.pbFormat**                                      | Legen Sie auf die Adresse einer ordnungsgemäß konfigurierten **WMVIDEOINFOHEADER-Struktur** fest.                                                                                                     |
| **WMVIDEOINFOHEADER.rcSource** und **WMVIDEOINFOHEADER.rcTarget** | Legen Sie beide Rechtecke so fest, dass die oberen linken Ecken Koordinaten (0, 0) und die unteren rechten Ecken Koordinaten (x, y) sind, wobei x die Bildbreite und y die Bildhöhe ist. |
| **WMVIDEOINFOHEADER.dwBitRate**                                   | Wird auf die Bitrate des Streams festgelegt.                                                                                                                                               |
| **WMVIDEOINFOHEADER.dwErrorRate**                                 | Auf 0 festlegen.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.dwBitErrorRate**                              | Auf 0 festlegen.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER. AvgTimePerFrame**                             | Auf 0 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biWidth**                                      | Legen Sie auf die Breite des Bilds fest.                                                                                                                                                   |
| **BITMAPINFOHEADER.biHeight**                                     | Legen Sie auf die Höhe des Bilds fest.                                                                                                                                                  |
| **BITMAPINFOHEADER.biPlanes**                                     | Auf 1 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biBitCount**                                   | Legen Sie auf 24 fest.                                                                                                                                                                       |
| **BITMAPINFOHEADER.biCompression**                                | Legen Sie auf BI \_ RGB fest.                                                                                                                                                                  |
| **BITMAPINFOHEADER.biSizeImage**                                  | Legen Sie auf ((x y c) / 8) fest, wobei x die Breite des Bilds, y die Höhe des Bilds und c die Farbtiefe des Bilds (in diesem Fall \* \* immer 24) ist.                     |
| **BITMAPINFOHEADER.biXPelsPerMeter**                              | Auf 0 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biYPelsPerMeter**                              | Auf 0 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrUsed**                                    | Auf 0 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrImportant**                               | Auf 0 festlegen.                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Configuration Common to All Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren Streams**](configuring-streams.md)
</dt> <dt>

[**Getting Good Results with the Windows Media Video 9 Screen Codec**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**Image Streams**](image-streams.md)
</dt> </dl>

 

 




