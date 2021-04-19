---
description: Verarbeiten von Format Änderungen vom Videorenderer
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: Verarbeiten von Format Änderungen vom Videorenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d731ac4b9d6985cf5ad92f642b6d8262209fa91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346597"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>Verarbeiten von Format Änderungen vom Videorenderer

In diesem Abschnitt wird beschrieben, wie ein Decoderfilter oder Transformations Filter Formatänderungen vom Videorenderer behandeln soll.

**Videorenderer-Filter**

Wenn der alte [Videorendererfilter](video-renderer-filter.md) eine Verbindung herstellt, ist ein RGB-Format erforderlich, das mit dem Anzeige Format des primären Monitors übereinstimmt. Dies ermöglicht es, GDI zum Rendern zu verwenden, wenn DirectDraw nicht verfügbar ist. Wenn die Wiedergabe gestartet wird, kann der Videorenderer zu einem DirectDraw-kompatiblen Format wechseln. Um zu vereinigen, ob der upstreamfilter das neue Format unterstützen kann, ruft der Videorenderer [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) in der Ausgabe-PIN des Upstream-Filters auf. Wenn der upstreamfilter das neue Format annimmt, gibt die **queryaccept** -Methode S \_ OK zurück. Der Videorenderer schaltet Formate durch Anfügen eines Medientyps mit dem neuen Format an das nächste Medien Beispiel, das von seiner Zuweisung zurückgegeben wird. Der upstreamfilter sollte überprüfen, ob Formatänderungen vorliegen, indem [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) für jedes Beispiel aufgerufen wird. Der Videorenderer kann während des Streamings jederzeit zwischen dem ursprünglichen Format und dem neuen Format wechseln. **Queryaccept** wird nach der ersten Formatänderung nicht aufgerufen. Nachdem der upstreamfilter das neue Format akzeptiert hat, muss es in der Lage sein, hin und her zu wechseln.

Der upstreamfilter kann die Formatänderung ablehnen, indem er \_ von **queryaccept** den Wert "false" zurückgibt. In diesem Fall verwendet der Videorenderer weiterhin GDI im ursprünglichen Format.

**Filter für Video Mischungs Renderer**

Der Filter für den videomischungs-Renderer (VMR-7 und VMR-9) stellt eine Verbindung mit einem beliebigen Format her, das von der Grafikhardware des Systems unterstützt wird. VMR-7 verwendet immer DirectDraw zum Rendern und ordnet die zugrunde liegenden DirectDraw-Oberflächen zu, wenn der upstreamfilter eine Verbindung herstellt. VMR-9 verwendet immer Direct3D zum Rendern und ordnet die zugrunde liegenden Direct3D-Oberflächen zu, wenn der upstreamfilter eine Verbindung herstellt.

Die Grafikhardware erfordert möglicherweise eine größere Angriffsfläche als die Breite des Bilds. In diesem Fall fordert VMR ein neues Format durch Aufrufen von **queryaccept** an. Er meldet den Oberflächen Schritt im **biwidth** -Member von [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) im Videoformat. Wenn der upstreamfilter nicht S \_ OK aus **queryaccept** zurückgibt, lehnt VMR das Format ab und versucht, eine Verbindung herzustellen, indem das nächste vom upstreamfilter angekündigte Format verwendet wird. Der VMR fügt den Medientyp mit dem neuen Format an das erste Medien Beispiel an. Nach dem ersten Beispiel bleibt das Format konstant. bei der Ausführung des Diagramms werden die Formate von VMR nicht gewechselt.

**Verbessertes Video Rendering (EVR)**

Der EVR verwendet immer Direct3D für das Rendering. Wenn ein größerer Oberflächen Schritt erforderlich ist, verwendet der EVR denselben **queryaccept** -Mechanismus wie VMR.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Queryaccept (Upstream)](queryaccept--upstream.md)
</dt> </dl>

 

 



