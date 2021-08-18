---
description: Introduction (WIC Guidelines for Camera RAW Image Formats)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introduction (WIC Guidelines for Camera RAW Image Formats)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96da37d36fed6af0aef271471eb2a0e5dae44bef71dfe14a4da37eba3f658c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086863"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Introduction (WIC Guidelines for Camera RAW Image Formats)

Die Windows Imaging Component (WIC) bietet ein erweiterbares Framework für die Arbeit mit Bildern und Bildmetadaten. WIC ermöglicht Software- und Hardwareanbietern die Entwicklung von Codecs, sodass ihre eigenen Bildformate die gleiche Plattformunterstützung wie native Bildformate wie TIFF (Tagged Image File Format), Joint Photographic Experts Group (JPEG) oder HD Photo erhalten können.

WIC bietet einen einzelnen, konsistenten Satz von Schnittstellen für die gesamte Bildverarbeitung, unabhängig vom Bildformat. Daher erhält jede Anwendung, die WIC verwendet, automatische Unterstützung für neue Bildformate, sobald der Codec installiert ist. WIC bietet auch ein erweiterbares Metadatenframework, mit dem Anwendungen ihre eigenen proprietären Metadaten direkt in Bilddateien lesen und schreiben können, sodass die Metadaten niemals verloren geht oder vom Image getrennt werden.

WIC ist in Windows Presentation Foundation (WPF) enthalten und in Windows Vista und höher Windows Versionen integriert. Sie ist auch als eigenständige verteilbare Komponente für Windows XP verfügbar.

Diese Richtlinien sollen RAW-Formathersteller bei der Entwicklung von WIC-Codecs unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC Guidelines for Camera RAW Image Formats](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



