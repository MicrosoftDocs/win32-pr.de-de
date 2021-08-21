---
description: EVR-Attribute
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: EVR-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5af186a909dc672876eb12846e842360ccabfd3f2cc1de8f203d3e40d94ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974539"
---
# <a name="evr-attributes"></a>EVR-Attribute

Die folgenden Attribute können verwendet werden, um den Enhanced Video Renderer (EVR) zu konfigurieren.



| attribute                                                                                                         | BESCHREIBUNG                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)                                                           | Ermöglicht dem EVR das Batchen von Aufrufen der Microsoft **Direct3D IDirect3DDevice9::P resent-Methode.**                            |
| [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)                                                         | Ermöglicht der EVR, die Leistung mithilfe von Bob-Deinterlacing zu verbessern.                                                        |
| [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)                                     | Ermöglicht es dem EVR, die Leistung zu verbessern, indem das zweite Feld jedes Verschachtelungsrahmens übersprungen wird.                            |
| [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)                                               | Ermöglicht dem EVR, seine Ausgabe auf die GPU-Bandbreite zu beschränken.                                                               |
| [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)                                                             | Ermöglicht dem EVR, das Video innerhalb eines Rechtecks zu mischen, das kleiner als das Ausgaberechteck ist, und dann das Ergebnis zu skalieren. |
| [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)                                                           | Erzwingt, dass die EVR Aufrufe der **IDirect3D9Device::P resent-Methode batchet.**                                               |
| [EVRConfig \_ ForceBob](evrconfig-forcebob.md)                                                                     | Zwingt die EVR, Bob-Deinterlacing zu verwenden.                                                                                 |
| [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)                                                 | Zwingt die EVR, das zweite Feld jedes Geschachtelten Frames zu überspringen.                                                       |
| [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)                                                             | Zwingt die EVR, das Video in einem Rechteck zu mischen, das kleiner als das Ausgaberechteck ist, und dann das Ergebnis zu skalieren. |
| [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)                                                           | Zwingt den EVR, seine Ausgabe auf die GPU-Bandbreite zu beschränken.                                                               |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ ACTIVATE**](mf-activate-custom-video-mixer-activate-attribute.md)         | Gibt ein Aktivierungsobjekt an, das einen benutzerdefinierten Videomixer für den erweiterten Videorenderer (EVR) erstellt.                  |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)               | CLSID eines benutzerdefinierten Videomixers für die EVR.                                                                               |
| [**MF \_ ACTIVATE CUSTOM VIDEO MIXER FLAGS (MF: AKTIVIEREN VON \_ \_ BENUTZERDEFINIERTEN \_ \_ VIDEOMIXERFLAGS)**](mf-activate-custom-video-mixer-flags-attribute.md)               | Gibt an, wie ein benutzerdefinierter Mixer für die EVR erstellt wird.                                                                      |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ PRESENTER \_ ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Gibt ein Aktivierungsobjekt an, das einen benutzerdefinierten Video presenter für die EVR erstellt.                                        |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ PRESENTER \_ CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID eines benutzerdefinierten Video presenters für die EVR.                                                                           |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ PRESENTER \_ FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md)       | Gibt an, wie eine benutzerdefinierte Präsentation für die EVR erstellt wird.                                                                  |
| [**\_MF-FENSTER \_ "VIDEO \_ AKTIVIEREN"**](mf-activate-video-window-attribute.md)                                         | Handle für das Videoausschneidefenster.                                                                                     |
| [**MF \_ SA \_ REQUIRED \_ SAMPLE \_ COUNT**](mf-sa-required-sample-count-attribute.md)                                  | Gibt die Anzahl der unkomprimierten Puffer an, die die EVR-Mediensenke für das Deinterlacing benötigt.                         |
| [**VIDEO \_ ZOOM \_ RECT**](video-zoom-rect-attribute.md)                                                            | Gibt das Zoomrechteck für den EVR-Mixer an.                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 



