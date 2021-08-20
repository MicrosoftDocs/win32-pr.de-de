---
title: Dateinamenerweiterungen
description: Dateinamenerweiterungen
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Windows Medienmetadateien, Erweiterungen
- Windows Medienmetadateien, Dateinamenerweiterungen
- Metadateien, Erweiterungen
- Metadateien, Dateinamenerweiterungen
- Windows Medien, Metadateien
- Dateinamenerweiterungen für Windows Media-Metadateien
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c69c36a5865b3496cf63e8cc08d73b9187f5107b14bf0bbb0d52b462e90c88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054988"
---
# <a name="file-name-extensions"></a>Dateinamenerweiterungen

Es gibt spezifische Richtlinien für die Verwendung von Dateinamenerweiterungen für Windows Media-Metadateien. Windows Medienmetadateinamenerweiterungen werden verwendet, um die verschiedenen Typen von Windows Mediendateien zu identifizieren. Eine Dateinamenerweiterung stellt einem unabhängigen Softwarehersteller (Independent Software Vendor, ISV) Informationen zu den Renderinganforderungen einer Anwendung bereit, die eine bestimmte Erweiterung verwendet, und ermöglicht Es Inhaltsautoren, allgemeine Typen von Medienplayern als Ziel zu verwenden.

Die Richtlinien für die Dateinamenerweiterung sind in der folgenden Tabelle aufgeführt. Es wird empfohlen, den MIME-Typ einer Datei, der sich im Dateiheader befindet, für die Dateitypidentifikation zu verwenden.



| Dateinamenerweiterung | MIME-Typ (MIME type)      | Dateiinhalte                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .wma                | audio/x-ms-wma | Windows Mediendatei nur mit Audioinhalten. Wird in der Regel zum Herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet.                                                                             |
| .wmv                | video/x-ms-wmv | Windows Mediendatei mit Audio- und/oder Videoinhalten. Wird in der Regel zum Herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet.                                                                     |
| .asf                | video/x-ms-asf | Legacyinhalt. Wird in der Regel zum Herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet. Kann Audio- und/oder Videoinhalte enthalten. Wird in der Regel zum Herunterladen und Wiedergeben von Dateien oder zum Streamen von Inhalten verwendet. |
| WM                 | video/x-ms-wm  | Reserviert                                                                                                                                                                                |
| .dll                | audio/x-ms-org | Metadateien, die auf Windows Mediendateien mit den Dateinamenerweiterungen .asf, .wma oder .extensions verweisen.                                                                                             |
| WVX                | video/x-ms-wvx | Metadateien, die auf Windows Mediendateien mit WMA-, WMV-, WVX- oder DATEIERWEITERUNGEN verweisen.                                                                                       |
| .asx                | video/x-ms-asf | Metadateien, die auf Windows Mediendateien mit dateinamenserweiterungen .wma, .extension, .wmv, .wvx, .asf oder .asx verweisen.                                                                           |
| WMX                | video/x-ms-wvx | Reserviert.                                                                                                                                                                               |



 

## <a name="remarks"></a>Hinweise

Skripterstellung und Verwaltung digitaler Rechte (DRM) müssen von jeder Anwendung unterstützt werden, die Windows Mediendateien rendert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media Metafile Guide**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




