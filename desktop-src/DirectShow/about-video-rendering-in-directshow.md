---
description: Informationen zum Videorendering in DirectShow
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: Informationen zum Videorendering in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d2d39cab75f2943a052b157296673f504a1220c17369d5a1639215f074a359
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873670"
---
# <a name="about-video-rendering-in-directshow"></a>Informationen zum Videorendering in DirectShow

DirectShow bietet mehrere Filter zum Rendern von Videos:

-   [Videorendererfilter.](video-renderer-filter.md) Dieser Filter ist für alle Plattformen verfügbar, die DirectX unterstützen, und hat keine besonderen Systemanforderungen. Der Videorenderer verwendet nach Möglichkeit DirectDraw, um das Video zu rendern. Andernfalls wird GDI verwendet. Dieser Filter ist der Standardvideorenderer auf Plattformen vor Windows XP.
-   [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 ist auf Windows XP verfügbar, wobei es sich um den Standardvideorenderer handelt. VMR-7 verwendet immer DirectDraw 7 für das Rendering. Es bietet viele leistungsstarke Features, die im älteren Videorendererfilter nicht verfügbar sind, einschließlich eines Plug-In-Modells, bei dem die Anwendung die directDraw-Oberflächen steuert, die für das Rendering verwendet werden.
-   [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9). VMR-9 ist eine neuere Version des Renderers zum Mischen von Videos, der Direct3D 9 für das Rendering verwendet. Es ist für alle Plattformen verfügbar, die DirectX unterstützen. Es handelt sich jedoch nicht um den Standardrenderer, da er höhere Systemanforderungen als der Videorendererfilter hat.
-   Der [Filter overlay Mixer](overlay-mixer-filter.md) ist speziell für die Wiedergabe und Übertragung von Videos auf DVD konzipiert. Außerdem werden Videoporterweiterungen (VIDEO Port Extensions, VPEs) unterstützt, sodass sie mit MPEG-2-Hardwaredecodern oder analogen TV-Tunern verwendet werden können, die Videos direkt an die Grafikkarte senden.
-   Der [**EVR-Filter (Enhanced Video Renderer)**](enhanced-video-renderer-filter.md) ist ab Windows Vista verfügbar. Es bietet eine verbesserte Videoleistung im Vergleich zu früheren Videorenderern, insbesondere wenn Windows Vista-Desktopkomposition aktiviert ist.

Im Allgemeinen wird die EVR für Anwendungen bevorzugt, die auf Windows Vista oder höher zielen, und VMR-9 wird für Anwendungen bevorzugt, die unter früheren Versionen von Windows. Weitere Informationen zur Verwendung der Filter VMR-7 und VMR-9 finden Sie unter [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).

Fenstermodus und fensterloser Modus

Ein DirectShow-Videorenderer kann entweder im *Fenstermodus* oder im *fensterlosen Modus ausgeführt* werden.

-   Im Fenstermodus erstellt der Renderer ein eigenes Fenster zum Anzeigen des Videos. In der Regel machen Sie dieses Fenster zum untergeordneten Fenster eines Anwendungsfensters. Weitere Informationen finden Sie unter [Verwenden des Fenstermodus](using-windowed-mode.md).
-   Im fensterlosen Modus zeichnet der Renderer das Video direkt in einem Anwendungsfenster. Es wird kein eigenes Fenster erstellt. Weitere Informationen zu diesem Modus finden Sie unter [Verwenden des fensterlosen Modus.](using-windowless-mode.md)

Der Videorendererfilter unterstützt nur den Fenstermodus. Die Filter VMR-7 und VMR-9 unterstützen beide Modi. Aus Gründen der Abwärtskompatibilität wird standardmäßig der Fenstermodus verwendet, der fensterlose Modus wird jedoch bevorzugt. Die EVR unterstützt nur den fensterlosen Modus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videorendering](video-rendering.md)
</dt> </dl>

 

 



