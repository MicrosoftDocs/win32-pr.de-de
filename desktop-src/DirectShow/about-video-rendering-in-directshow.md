---
description: Informationen zum Video Rendering in DirectShow
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: Informationen zum Video Rendering in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e8ecf133f362e699e6b9d650d11da5bf43347
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860481"
---
# <a name="about-video-rendering-in-directshow"></a>Informationen zum Video Rendering in DirectShow

DirectShow bietet mehrere Filter zum Rendering von Videos:

-   [Videorenderer](video-renderer-filter.md) -Filter. Dieser Filter ist für alle Plattformen verfügbar, die DirectX unterstützen und über keine speziellen Systemanforderungen verfügen. Der Videorenderer verwendet nach Möglichkeit DirectDraw zum renderingvideo. Andernfalls wird GDI verwendet. Dieser Filter ist der Standardvideorenderer auf Plattformen vor Windows XP.
-   [Video Mischungs-Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 ist unter Windows XP verfügbar, wobei es sich um den Standard-Videorenderer handelt. VMR-7 verwendet immer DirectDraw 7 zum Rendern. Es bietet viele leistungsstarke Features, die im älteren Videorendererfilter nicht verfügbar sind, einschließlich eines Plug-in-Modells, in dem die Anwendung die für das Rendering verwendeten DirectDraw-Oberflächen steuert.
-   [Video Mischungs-Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9). VMR-9 ist eine neuere Version des Video Mischungs-Renderers, der Direct3D 9 zum Rendern verwendet. Es ist für alle Plattformen verfügbar, die DirectX unterstützen. Es ist jedoch nicht der Standard-Renderer, da er höhere Systemanforderungen als der Videorenderer-Filter aufweist.
-   Der [Overlay-Mixer](overlay-mixer-filter.md) Filter ist speziell für die DVD-Wiedergabe und Broadcast-Video konzipiert. Sie unterstützt auch Video Port Erweiterungen (vpes) und ermöglicht die Verwendung von Hardware-MPEG-2-Decodern oder analogen TV-Tunern, die Videos direkt an die Grafikkarte senden.
-   Der EVR-Filter ( [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) ) ist ab Windows Vista verfügbar. Es bietet eine verbesserte Video Leistung im Vergleich zu früheren videorenderatoren, insbesondere dann, wenn die Windows Vista-Desktop Komposition aktiviert ist.

Im Allgemeinen wird der EVR für Anwendungen bevorzugt, die auf Windows Vista oder höher ausgerichtet sind, und VMR-9 wird für Anwendungen bevorzugt, die unter früheren Versionen von Windows ausgeführt werden. Weitere Informationen zur Verwendung von VMR-7-und VMR-9-Filtern finden [Sie unter Verwenden des Video Mischungs-Renderers](using-the-video-mixing-renderer.md).

Fenstermodus und fensterloser Modus

Ein DirectShow-Videorenderer *kann entweder im* Fenstermodus oder im *fensterlosen* Modus ausgeführt werden.

-   Im Fenstermodus erstellt der Renderer ein eigenes Fenster, um das Video anzuzeigen. In der Regel wird dieses Fenster als untergeordnetes Element eines Anwendungsfensters verwendet. Weitere Informationen finden Sie unter [verwenden](using-windowed-mode.md)des Fenstermodus.
-   Im fensterlosen Modus zeichnet der Renderer das Video direkt in einem Anwendungsfenster. Es wird kein eigenes Fenster erstellt. Weitere Informationen zu diesem Modus finden Sie unter [Verwenden des fensterlosen Modus](using-windowless-mode.md).

Der Videorenderer-Filter unterstützt nur den Fenstermodus. Die Filter VMR-7 und VMR-9 unterstützen beide Modi. Standardmäßig wird der Fenstermodus aus Gründen der Abwärtskompatibilität angezeigt, der fensterlose Modus wird jedoch bevorzugt. Der EVR unterstützt nur den fensterlosen Modus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videorendering](video-rendering.md)
</dt> </dl>

 

 



