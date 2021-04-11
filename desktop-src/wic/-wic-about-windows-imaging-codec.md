---
description: Die Windows Imaging Component (WIC) stellt ein erweiterbares Framework zum Arbeiten mit Bildern und Bild Metadaten bereit.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Übersicht über die Windows Imaging-Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216396"
---
# <a name="windows-imaging-component-overview"></a>Übersicht über die Windows Imaging-Komponente

Die Windows Imaging Component (WIC) stellt ein erweiterbares Framework zum Arbeiten mit Bildern und Bild Metadaten bereit. Mit WIC können unabhängige Softwarehersteller (ISVs) und unabhängige Hardwarehersteller (IHVs) ihre eigenen Bild Codecs entwickeln und die gleiche Platt Form Unterstützung wie Standard Image Formate (z. b. TIFF, JPEG, PNG, GIF, BMP und HDPhoto) erhalten. Ein einzelner, konsistentes Satz von Schnittstellen wird unabhängig vom Bildformat für die gesamte Bildverarbeitung verwendet, sodass jede Anwendung, die WIC verwendet, automatisch Unterstützung für neue Bildformate erhält, sobald der Codec installiert ist. Das erweiterbare metadatenframework ermöglicht es Anwendungen, eigene proprietäre Metadaten direkt in Bilddateien zu lesen und zu schreiben, sodass die Metadaten niemals verloren gehen oder von dem Image getrennt werden.

Das Thema enthält folgende Abschnitte:

-   [Windows Imaging-Komponenten Features](#windows-imaging-component-features)
-   [Native Codecs](#native-codecs)
-   [Zugehörige Themen](#related-topics)

## <a name="windows-imaging-component-features"></a>Windows Imaging-Komponenten Features

Die wichtigsten Features von WIC sind:

-   Ermöglicht es Anwendungsentwicklern, Bild Verarbeitungsvorgänge in beliebigen Bildformaten durch einen einzelnen, konsistenten Satz von allgemeinen Schnittstellen auszuführen, ohne dass vorherige Kenntnisse über bestimmte Bildformate erforderlich sind.
-   Bietet eine erweiterbare "Plug & Play"-Architektur für Bild Codecs, Pixel Formate und Metadaten mit automatischer Lauf Zeit Ermittlung neuer Formate.
-   Unterstützt das Lesen und schreiben beliebiger Metadaten in Bilddateien mit der Möglichkeit, unbekannte Metadaten während der Bearbeitung beizubehalten.
-   Speichert High-Bit-dateibilddaten (bis zu 32 Bits pro Kanal) in der gesamten Bild Verarbeitungs Pipeline.
-   Bietet integrierte Unterstützung für die beliebtesten Bildformate, Pixel Formate und Metadatenschemas.

## <a name="native-codecs"></a>Native Codecs

WIC umfasst mehrere integrierte Codecs. Die folgenden Standard-Codecs werden mit der-Plattform bereitgestellt. 

| Codec                                                                                             | MIME-Typen                       | Decoder | Encoder |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| BMP (Windows-Bitmap-Format), BMP-Spezifikation V5.                                                | image/bmp                        | Ja      | Ja      |
| GIF (Graphics Interchange Format 89A), GIF-Spezifikation 89A/89m                                  | image/gif                        | Ja      | Ja      |
| ICO (Symbol Format)                                                                                 | Image/ICO                        | Ja      | Nein       |
| JPEG (Joint Photographic Experts Group), JFIF-Spezifikation 1,02                                  | Image/JPEG, Image/jpe, Image/JPG | Ja      | Ja      |
| PNG (Portable Network Graphics), PNG-Spezifikation 1,2                                            | image/png                        | Ja      | Ja      |
| TIFF (Tagged Image File Format), TIFF-Spezifikation 6,0                                           | Bild/TIFF, Bild/TIF            | Ja      | Ja      |
| Windows Media Photo, [HD Photo Specification 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | Image/vnd. ms-Phot                | Ja      | Ja      |
| DDS (DirectDraw-Oberfläche)                                                                          | Image/vnd. ms-DDS                 | Ja      | Ja      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[AITCodec-Beispielcodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))
</dt> </dl>

 

 
