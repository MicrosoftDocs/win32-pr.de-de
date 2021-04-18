---
title: Dateinamenerweiterungen
description: Dateinamenerweiterungen
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Windows Media-Metadateien, Erweiterungen
- Windows Media-Metadateien, Dateinamen Erweiterungen
- Metadatendateien, Erweiterungen
- Metadateien, Dateinamen Erweiterungen
- Windows Media, Metafiles
- Dateinamen Erweiterungen für Windows Media-Metadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340853"
---
# <a name="file-name-extensions"></a>Dateinamenerweiterungen

Es gibt spezielle Richtlinien für die Verwendung von Dateinamen Erweiterungen für Windows Media-Metadateien. Windows Media Metadatei-Erweiterungen werden verwendet, um die verschiedenen Typen von Windows Media-Dateien zu identifizieren. Eine Dateinamenerweiterung bietet einen unabhängigen Software Hersteller (Independent Software Vendor, ISV) mit Informationen zu den Renderinganforderungen einer Anwendung, die eine bestimmte Erweiterung verwendet, und ermöglicht Inhalts Entwicklern das Ausrichten allgemeiner Arten von Medien Playern.

Die Richtlinien für die Dateinamenerweiterung sind in der folgenden Tabelle aufgeführt. Es wird empfohlen, dass der MIME-Typ einer Datei, der sich im Dateiheader befindet, für die Dateityp Identifizierung verwendet wird.



| Dateinamenerweiterung | MIME-Typ (MIME type)      | Dateiinhalte                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .wma                | Audiodatei/x-ms-WMA | Windows Media-Datei mit nur Audioinhalt. Wird normalerweise zum herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet.                                                                             |
| .wmv                | Video/x-ms-WMV | Windows Media-Datei mit Audioinhalt und/oder Videoinhalt. Wird normalerweise zum herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet.                                                                     |
| .asf                | Video/x-ms-ASF | Legacy Inhalt. Wird normalerweise zum herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet. Kann Audioinhalte und/oder Videoinhalte enthalten. Wird normalerweise zum herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet. |
| WM                 | Video/x-ms-WM  | Reserviert                                                                                                                                                                                |
| . Wachs                | Audiodatei/x-ms-Wax | Metadateien, die auf Windows Media-Dateien mit den Dateinamen Erweiterungen. ASF,. WMA oder. Wax verweisen.                                                                                             |
| . wvx                | Video/x-ms-wvx | Metadateien, die auf Windows Media-Dateien mit den Dateinamen Erweiterungen. WMA,. WMV,. wvx oder. Wax verweisen.                                                                                       |
| .asx                | Video/x-ms-ASF | Metadateien, die auf Windows Media-Dateien mit den Dateinamen Erweiterungen. WMA,. Wax,. WMV,. wvx,. ASF oder. ASX verweisen.                                                                           |
| . wmx                | Video/x-ms-wvx | Reserviert.                                                                                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Skripterstellung und Digital Rights Management (DRM) müssen von jeder Anwendung unterstützt werden, die Windows Media-Dateien rendert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




