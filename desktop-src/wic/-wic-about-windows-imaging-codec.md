---
description: Die Windows Imaging Component (WIC) bietet ein erweiterbares Framework für die Arbeit mit Bildern und Bildmetadaten.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Windows Übersicht über Bildverarbeitungskomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f4276a70b94fd190b7254d8d3d2666581c0c9dbb991dee3ac6e0568b6ee649
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772510"
---
# <a name="windows-imaging-component-overview"></a>Windows Übersicht über Bildverarbeitungskomponenten

Die Windows Imaging Component (WIC) bietet ein erweiterbares Framework für die Arbeit mit Bildern und Bildmetadaten. WIC ermöglicht unabhängigen Softwareherstellern (INDEPENDENT Software Vendors, ISVs) und unabhängigen Hardwareanbietern (Independent Hardware Vendors, IHVs), eigene Bildcodecs zu entwickeln und die gleiche Plattformunterstützung wie Standardbildformate (z. B. TIFF, JPEG, PNG, GIF, BMP und HDPhoto) zu erhalten. Ein einzelner, konsistenter Satz von Schnittstellen wird unabhängig vom Bildformat für die gesamte Bildverarbeitung verwendet, sodass jede Anwendung, die die WIC verwendet, automatische Unterstützung für neue Bildformate erhält, sobald der Codec installiert ist. Das erweiterbare Metadatenframework ermöglicht es Anwendungen, ihre eigenen proprietären Metadaten direkt in Bilddateien zu lesen und zu schreiben, sodass die Metadaten nie verloren oder vom Image getrennt werden.

Das Thema enthält folgende Abschnitte:

-   [Windows Features von Bildverarbeitungskomponenten](#windows-imaging-component-features)
-   [Native Codecs](#native-codecs)
-   [Zugehörige Themen](#related-topics)

## <a name="windows-imaging-component-features"></a>Windows Features von Bildverarbeitungskomponenten

Die wichtigsten Features von WIC sind:

-   Ermöglicht Es Anwendungsentwicklern, Bildverarbeitungsvorgänge für jedes Bildformat über einen einzelnen, konsistenten Satz allgemeiner Schnittstellen auszuführen, ohne dass sie sich mit bestimmten Bildformaten aus dem Vorherigen aussetzen müssen.
-   Bietet eine erweiterbare Plug & Play-Architektur für Bildcodecs, Pixelformate und Metadaten mit automatischer Laufzeitermittlung neuer Formate.
-   Unterstützt das Lesen und Schreiben beliebiger Metadaten in Bilddateien mit der Möglichkeit, nicht erkannte Metadaten während der Bearbeitung beizubehalten.
-   Behält Bilddaten mit hoher Bittiefe (bis zu 32 Bit pro Kanal) in der gesamten Bildverarbeitungspipeline bei.
-   Bietet integrierte Unterstützung für die beliebtesten Bildformate, Pixelformate und Metadatenschemas.

## <a name="native-codecs"></a>Native Codecs

WIC enthält mehrere integrierte Codecs. Die folgenden Standardcodecs werden mit der Plattform bereitgestellt. 

| Codec                                                                                             | Mime-Typen                       | Decoder | Encoder |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| BMP (Windows Bitmapformat), BMP-Spezifikation v5.                                                | image/bmp                        | Ja      | Ja      |
| GIF (Graphics Interchange Format 89a), GIF-Spezifikation 89a/89m                                  | image/gif                        | Ja      | Ja      |
| ICO (Symbolformat)                                                                                 | image/ico                        | Ja      | Nein       |
| JPEG (Joint Photographic Experts Group), JFIF-Spezifikation 1.02                                  | image/jpeg, image/jpe, image/jpg | Ja      | Ja      |
| PNG (Portable Network Graphics), PNG-Spezifikation 1.2                                            | image/png                        | Ja      | Ja      |
| TIFF (Tagged Image File Format), TIFF-Spezifikation 6.0                                           | image/tiff, image/tif            | Ja      | Ja      |
| Windows Medienfoto, [HD-Fotospezifikation 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | image/vnd.ms-orgt                | Ja      | Ja      |
| DDS (DirectDraw Surface)                                                                          | image/vnd.ms-dds                 | Ja      | Ja      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[AITCodec-Beispielcodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))
</dt> </dl>

 

 
