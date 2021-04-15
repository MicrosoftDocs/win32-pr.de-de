---
title: WIC-Programmier Handbuch
description: Beschreibt die Verwendung der WIC-APIs.
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393678"
---
# <a name="wic-programming-guide"></a>WIC-Programmier Handbuch

Dieser Abschnitt enthält konzeptionelle Themen, in denen die Verwendung der WIC-APIs (Windows Imaging Component) beschrieben wird.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                 | BESCHREIBUNG                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)<br/> | Der WIC bietet ein erweiterbares Framework zum Arbeiten mit Bildern und Bild Metadaten.<br/>                                                                                                                       |
| [WIC-API-Übersicht](-wic-api.md)<br/>                                           | Der WIC stellt eine Component Object Model (com)-basierte API für die Verwendung in C und C++ bereit.<br/>                                                                                                                            |
| [Decodieren digitaler Images](-wic-decoder-portal.md)<br/>                         | Dieser Abschnitt enthält konzeptionelle und Vorgehensweisen, in denen WIC-BitmapDecoder beschrieben werden, die beim Decodieren digitaler Images verwendet werden.<br/>                                                                            |
| [Verwenden von Bilddaten](-wic-bitmapsources-portal.md)<br/>                          | Dieser Abschnitt enthält konzeptionelle und Vorgehensweisen zum Beschreiben von WIC-bitmapquellen und deren Bearbeitung.<br/>                                                                                            |
| [Codieren von Bilddaten](encoding-bitmaps-to-digital-images.md)<br/>              | Dieser Abschnitt enthält konzeptionelle und Vorgehensweisen, in denen WIC-Bitmap-Encoder beschrieben werden, die zum Codieren digitaler Images verwendet werden.<br/>                                                                              |
| [Native WIC-Codecs](native-wic-codecs.md)<br/>                                 | Dieser Abschnitt enthält Informationen zu den systemeigenen, in WIC verfügbaren Codecs für die Bildverarbeitung.<br/>                                                                                                                        |
| [Verarbeiten von Bild Metadaten](-wic-metadata-portal.md)<br/>                      | Dieser Abschnitt enthält konzeptionelle Themen, in denen das WIC-Metadatensystem beschrieben wird.<br/>                                                                                                                             |
| [JPEG YCbCr-Unterstützung](jpeg-ycbcr-support.md)<br/>                               | Ab Windows 8.1 unterstützt der JPEG-Codec der [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) das Lesen und Schreiben von Bilddaten in der nativen Yc<sub>b</sub>c<sub>r</sub> -Form. <br/> |
| [Farbverwaltung](-wic-colormanagement.md)<br/>                               | WIC vereinfacht die Farbverwaltung durch die Bereitstellung der [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Schnittstelle und der [**iwiccolortransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) -Schnittstelle.<br/>          |
| [Komponentenentwicklung](-wic-component-development.md)<br/>                    | Die WIC ist eine erweiterbare Plattform, die eine Low-Level-API für digitale Images bereitstellt.<br/>                                                                                                                          |



 

## <a name="see-also"></a>Weitere Informationen

[WIC-Referenz](-wic-codec-reference.md)


[WIC-Beispiele](-wic-samples.md)


 

 




