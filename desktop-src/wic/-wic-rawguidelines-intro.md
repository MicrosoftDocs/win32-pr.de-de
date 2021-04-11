---
description: Einführung (WIC-Richtlinien für Kamera Rohbild Formate)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Einführung (WIC-Richtlinien für Kamera Rohbild Formate)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217372"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Einführung (WIC-Richtlinien für Kamera Rohbild Formate)

Die Windows Imaging Component (WIC) stellt ein erweiterbares Framework zum Arbeiten mit Bildern und Bild Metadaten bereit. Mit WIC können Software-und Hardwarehersteller Codecs entwickeln, sodass Ihre eigenen Bildformate die gleiche Platt Form Unterstützung wie Native Image Formate wie z. b. TIFF (Tagged Image File Format), Joint Photographic Experts Group (JPEG) oder HD-Foto erhalten.

WIC stellt unabhängig vom Bildformat einen einzelnen, konsistenten Satz von Schnittstellen für die gesamte Bildverarbeitung bereit. Daher erhält jede Anwendung, die WIC verwendet, automatische Unterstützung für neue Bildformate, sobald der Codec installiert ist. WIC bietet auch ein erweiterbares metadatenframework, das es Anwendungen ermöglicht, eigene proprietäre Metadaten direkt in Bilddateien zu lesen und zu schreiben, sodass die Metadaten niemals verloren gehen oder von dem Image getrennt werden.

WIC ist in Windows Presentation Foundation (WPF) enthalten und ist in Windows Vista und spätere Windows-Versionen integriert. Es ist auch als eigenständige verteilbare Komponente für Windows XP verfügbar.

Diese Richtlinien sind so konzipiert, dass Sie Rohformat Herstellern bei der Entwicklung von WIC-Codecs unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-Richtlinien für Kamera Rohbild Formate](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



