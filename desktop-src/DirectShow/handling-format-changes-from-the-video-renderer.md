---
description: Behandeln von Formatänderungen über den Videorenderer
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: Behandeln von Formatänderungen über den Videorenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1dd0ec2f87a8604d3b03aa6c2f334161d218f4d7fb45c76aad1015f071d947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905300"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>Behandeln von Formatänderungen über den Videorenderer

In diesem Abschnitt wird beschrieben, wie ein Decoderfilter oder Transformationsfilter Formatänderungen vom Videorenderer verarbeiten soll.

**Videorendererfilter**

Wenn der alte [Videorendererfilter](video-renderer-filter.md) eine Verbindung herstellt, ist ein RGB-Format erforderlich, das dem Anzeigeformat des primären Monitors entspricht. Dadurch kann GDI für das Rendering verwendet werden, wenn DirectDraw nicht verfügbar ist. Wenn die Wiedergabe gestartet wird, kann der Videorenderer in ein DirectDraw-kompatibles Format wechseln. Um zu überprüfen, ob der Upstreamfilter das neue Format unterstützen kann, ruft der Videorenderer [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Ausgabepin des Upstreamfilters auf. Wenn der Upstreamfilter das neue Format akzeptiert, gibt die **QueryAccept-Methode** S \_ OK zurück. Der Videorenderer schaltet Formate um, indem er einen Medientyp mit dem neuen Format an das nächste Medienbeispiel anfügen, das von seiner Zuweisung zurückgegeben wird. Der Upstreamfilter sollte auf Formatänderungen überprüfen, indem [**er IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) für jedes Beispiel aufruft. Der Videorenderer kann während des Streamings jederzeit zwischen dem ursprünglichen und dem neuen Format wechseln. QueryAccept wird **nach der ersten** Formatänderung nicht mehr aufruft. Sobald der Upstreamfilter das neue Format akzeptiert hat, muss er in der Lage sein, hin und her zu wechseln.

Der Upstreamfilter kann die Formatänderung ablehnen, indem er S \_ FALSE von **QueryAccept zurücksendet.** In diesem Fall verwendet der Videorenderer weiterhin GDI mit dem ursprünglichen Format.

**Filter für Videomischungsrenderer**

Der Filter "Video Mixing Renderer" (VMR-7 und VMR-9) stellt eine Verbindung mit jedem Format sicher, das von der Grafikhardware auf dem System unterstützt wird. VMR-7 verwendet immer DirectDraw für das Rendering und ordnet die zugrunde liegenden DirectDraw-Oberflächen zu, wenn der Upstreamfilter eine Verbindung herstellt. VMR-9 verwendet immer Direct3D für das Rendering und ordnet die zugrunde liegenden Direct3D-Oberflächen zu, wenn der Upstreamfilter eine Verbindung herstellt.

Die Grafikhardware erfordert möglicherweise einen größeren Oberflächenschritt als die Bildbreite. In diesem Fall fordert die VMR durch Aufrufen von **QueryAccept** ein neues Format an. Er meldet den Oberflächenschritt im **biWidth-Member** von [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) im Videoformat. Wenn der Upstreamfilter von QueryAccept nicht S OK zurück gibt, lehnt der VMR das Format ab und versucht, eine Verbindung mit dem nächsten Format herzustellen, das vom \_ Upstreamfilter angekündigt wird. Der VMR hängt den Medientyp mit dem neuen Format an das erste Medienbeispiel an. Nach dem ersten Beispiel bleibt das Format konstant. Der VMR wechselt die Formate nicht, während der Graph ausgeführt wird.

**Erweitertes Videorendering (EVR)**

Der EVR verwendet immer Direct3D für das Rendering. Wenn ein größerer Oberflächenschritt erforderlich ist, verwendet der EVR den gleichen **QueryAccept-Mechanismus** wie der VMR.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[QueryAccept (Upstream)](queryaccept--upstream.md)
</dt> </dl>

 

 



