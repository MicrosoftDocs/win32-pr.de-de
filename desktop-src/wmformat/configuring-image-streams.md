---
title: Konfigurieren von bildstreams
description: Konfigurieren von bildstreams
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- Streams, Konfigurieren von bildstreams
- Codecs, Konfigurieren von bildstreams
- bildstreams, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b05a21474143e227257dad240ff4d4464732ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388236"
---
# <a name="configuring-image-streams"></a>Konfigurieren von bildstreams

Bildstreams enthalten weiterhin Bilder im JPEG-Format. Obwohl bildstreams wie Videostreams aussehen, sind Sie nicht komprimierte Bilder als Eingaben. Sie erfordern eine etwas andere Konfiguration. Um einen Bildstream zu konfigurieren, müssen Sie die Werte für die Elemente der Video Konfigurations Strukturen festlegen, wie in der folgenden Tabelle dargestellt.



| Einstellung                                                           | BESCHREIBUNG                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ - \_ Medientyp. majortype**                                     | Legen Sie auf wmmediatype- \_ Image fest.                                                                                                                                                       |
| **WM \_ - \_ Medientyp. Untertyp**                                       | Legen Sie diese Einstellung auf wmmediasubtype \_ RGB24 fest.                                                                                                                                                    |
| **WM \_ - \_ Medientyp. bfixedsizesamples**                             | Legen Sie auf **false** fest.                                                                                                                                                                |
| **WM \_ - \_ Medientyp. btemporalcompression**                          | Legen Sie auf **false** fest.                                                                                                                                                                |
| **WM \_ - \_ Medientyp. lsamplesize**                                   | Auf 0 festlegen.                                                                                                                                                                        |
| **WM \_ - \_ Medientyp. formatType**                                    | Legen Sie auf wmformat \_ videoinfo fest.                                                                                                                                                      |
| **WM \_ - \_ Medientyp. Punk**                                          | Auf **null** festgelegt.                                                                                                                                                                 |
| **WM \_ - \_ Medientyp. cbformat**                                      | Legen Sie diese Option auf `sizeof(WMVIDEOINFOHEADER)` fest.                                                                                                                                              |
| **WM \_ - \_ Medientyp. pbformat**                                      | Legen Sie die Adresse einer ordnungsgemäß konfigurierten **wmvideoinfoheader** -Struktur fest.                                                                                                     |
| **Wmvideoinfoheader. rcSource** und **wmvideoinfoheader. rctarget** | Legen Sie beide Rechtecke so fest, dass die oberen linken Ecken Koordinaten (0,0) sind, und die unteren rechten Ecken sind Koordinaten (x, y), wobei x die Bildbreite und y die Bildhöhe ist. |
| **Wmvideoinfoheader. dwbitrate**                                   | Legen Sie auf die Bitrate des Streams fest.                                                                                                                                               |
| **Wmvideoinfoheader. dwerrorrate**                                 | Auf 0 festlegen.                                                                                                                                                                        |
| **Wmvideoinfoheader. dwbiterrorrate**                              | Auf 0 festlegen.                                                                                                                                                                        |
| **Wmvideoinfoheader. Avgtimeperframe**                             | Auf 0 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biwidth**                                      | Legen Sie die Breite des Bilds fest.                                                                                                                                                   |
| **BITMAPINFOHEADER. biheight**                                     | Legen Sie den Wert auf die Höhe des Bilds fest.                                                                                                                                                  |
| **BITMAPINFOHEADER. Biplane**                                     | Auf 1 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biBitCount**                                   | Legen Sie auf 24 fest.                                                                                                                                                                       |
| **BITMAPINFOHEADER. bicompression**                                | Legen Sie auf BI \_ RGB fest.                                                                                                                                                                  |
| **BITMAPINFOHEADER. bisizeimage**                                  | Legen Sie auf ((x \* y \* c)/8) fest, wobei x die Breite des Bilds, y die Höhe des Bilds und c die Farbtiefe des Bilds ist (in diesem Fall immer 24).                     |
| **BITMAPINFOHEADER. bixpelspermeter**                              | Auf 0 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biypelspermeter**                              | Auf 0 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biclrused**                                    | Auf 0 festlegen.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biclrimportant**                               | Auf 0 festlegen.                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Konfiguration für alle Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**Erzielen von guten Ergebnissen mit dem Windows Media Video 9-Bildschirm Codec**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**Bildstreams**](image-streams.md)
</dt> </dl>

 

 




