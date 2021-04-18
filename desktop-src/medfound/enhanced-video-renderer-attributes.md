---
description: EVR-Attribute
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: EVR-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508b036a7880c48e65d3c07a80ba5baaa5a52306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338936"
---
# <a name="evr-attributes"></a>EVR-Attribute

Die folgenden Attribute können verwendet werden, um den erweiterten Videorenderer (EVR) zu konfigurieren.



| Attribut                                                                                                         | BESCHREIBUNG                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Evrconfig \_ allowbatching](evrconfig-allowbatching.md)                                                           | Ermöglicht dem EVR das Batches von Aufrufen an die Microsoft Direct3D **IDirect3DDevice9::P Resent** -Methode.                            |
| [Evrconfig \_ allowdropto Bob](evrconfig-allowdroptobob.md)                                                         | Ermöglicht dem EVR das Verbessern der Leistung mithilfe von Bob Deinterlacing.                                                        |
| [Evrconfig \_ allowdropabhalfinterlace](evrconfig-allowdroptohalfinterlace.md)                                     | Ermöglicht dem EVR, die Leistung zu verbessern, indem das zweite Feld jedes Zeilen Sprung Rahmens übersprungen wird.                            |
| ["Evrconfig \_ allowdropto Throttle"](evrconfig-allowdroptothrottle.md)                                               | Ermöglicht dem EVR, seine Ausgabe auf die GPU-Bandbreite zu begrenzen.                                                               |
| [Evrconfig \_ allowscaling](evrconfig-allowscaling.md)                                                             | Ermöglicht dem EVR, das Video innerhalb eines Rechtecks zu mischen, das kleiner als das Ausgabe Rechteck ist, und dann das Ergebnis zu skalieren. |
| [Evrconfig \_ forcebatching](evrconfig-forcebatching.md)                                                           | Zwingt den EVR, Aufrufe der **IDirect3D9Device::P Resent** -Methode in Batches zu übertragen.                                               |
| [Evrconfig \_ forcebob](evrconfig-forcebob.md)                                                                     | Erzwingt, dass der EVR Bob Deinterlacing verwendet.                                                                                 |
| [Evrconfig \_ forcehalfinterlace](evrconfig-forcehalfinterlace.md)                                                 | Zwingt den EVR, das zweite Feld jedes Zeilen Sprung Rahmens zu überspringen.                                                       |
| [Evrconfig- \_ forcescaleing](evrconfig-forcescaling.md)                                                             | Zwingt den EVR, das Video innerhalb eines Rechtecks zu mischen, das kleiner als das Ausgabe Rechteck ist, und skaliert dann das Ergebnis. |
| [Evrconfig- \_ forcethrottle](evrconfig-forcethrottle.md)                                                           | Zwingt den EVR, seine Ausgabe auf die GPU-Bandbreite zu begrenzen.                                                               |
| [**MF Aktivieren des \_ \_ benutzerdefinierten \_ Video \_ Mischers \_ aktivieren**](mf-activate-custom-video-mixer-activate-attribute.md)         | Gibt ein Aktivierungs Objekt an, das einen benutzerdefinierten Videomixer für den erweiterten Videorenderer (EVR) erstellt.                  |
| [**MF \_ - \_ benutzerdefinierte \_ Video-Mixer- \_ \_ CLSID aktivieren**](mf-activate-custom-video-mixer-clsid-attribute.md)               | CLSID eines benutzerdefinierten Video Mischers für den EVR.                                                                               |
| [**MF \_ Aktivieren von \_ benutzerdefinierten \_ Video- \_ \_ mischflags**](mf-activate-custom-video-mixer-flags-attribute.md)               | Gibt an, wie ein benutzerdefinierter Mixer für den EVR erstellt wird.                                                                      |
| [**MF Aktivieren von \_ \_ benutzerdefiniertem \_ Video \_ Presenter \_ aktivieren**](mf-activate-custom-video-presenter-activate-attribute.md) | Gibt ein Aktivierungs Objekt an, das eine benutzerdefinierte Videopräsentation für den EVR erstellt.                                        |
| [**MF \_ \_ benutzerdefinierte \_ Video \_ Presenter- \_ CLSID aktivieren**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID eines benutzerdefinierten Video Präsentators für den EVR.                                                                           |
| [**MF \_ \_ benutzerdefinierte \_ Video \_ Presenter- \_ Flags aktivieren**](mf-activate-custom-video-presenter-flags-attribute.md)       | Gibt an, wie ein benutzerdefinierter Presenter für den EVR erstellt wird.                                                                  |
| [**MF \_ - \_ Video \_ Fenster aktivieren**](mf-activate-video-window-attribute.md)                                         | Handle für das Video Clipping-Fenster.                                                                                     |
| [**\_ \_ Anzahl erforderlicher MF-Anforderungen \_ \_**](mf-sa-required-sample-count-attribute.md)                                  | Gibt die Anzahl der nicht komprimierten Puffer an, die von der EVR-Medien Senke für Deinterlacing benötigt werden.                         |
| [**Video \_ Zoom- \_ Rect**](video-zoom-rect-attribute.md)                                                            | Gibt das Zoom Rechteck für den EVR-Mixer an.                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 



