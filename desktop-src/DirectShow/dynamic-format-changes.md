---
description: Dynamische Format Änderungen
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Dynamische Format Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339656"
---
# <a name="dynamic-format-changes"></a>Dynamische Format Änderungen

Wenn zwei Filter eine Verbindung herstellen, stimmen Sie einem Medientyp zu, der das Format der Daten beschreibt, die der Upstream-Filter bereitstellt. In den meisten Fällen ist der Medientyp für die Dauer der Verbindung korrigiert. DirectShow bietet jedoch eingeschränkte Unterstützung für Filter zum Ändern des Medientyps. Wenn ein Filter die Medientypen wechselt, wird er als *dynamische Formatänderung* bezeichnet. Wenn Sie einen DirectShow-Filter schreiben, sollten Sie sich mit den Mechanismen für dynamische Formatänderungen vertraut sein. Auch wenn der Filter solche Änderungen nicht unterstützt, sollte er ordnungsgemäß reagieren, wenn ein anderer Filter ein neues Format anfordert.

DirectShow definiert mehrere verschiedene Mechanismen für dynamische Formatänderungen, abhängig vom Status des Filter Diagramms und dem erforderlichen Änderungstyp.

-   Wenn das Diagramm angehalten wurde, können die Pins erneut eine Verbindung herstellen und den Medientyp erneut aushandeln. Weitere Informationen finden Sie unter Verbinden von [Pins](reconnecting-pins.md).
-   Einige Filter können Pins erneut verbinden, auch wenn das Diagramm aktiv ist (wird ausgeführt oder angehalten). Weitere Informationen zu diesem Mechanismus finden Sie unter [Dynamic Reconnection](dynamic-reconnection.md).

Wenn das Diagramm aktiv ist, die fraglichen Filter jedoch keine dynamischen Pin-Neuverbindungen unterstützen, gibt es drei mögliche Mechanismen, um das Format zu ändern:

-   [Queryaccept (Downstream)](queryaccept--downstream.md) wird verwendet, wenn eine Ausgabepin eine Formatänderung an den downstreampeer vorschlägt, aber nur, wenn das neue Format keinen größeren Puffer erfordert.
-   [Queryaccept (Upstream)](queryaccept--upstream.md) wird verwendet, wenn eine Eingabe-PIN eine Formatänderung an Ihren upstreampeer vorschlägt. Das neue Format kann dieselbe Größe aufweisen oder größer sein.
-   [Receiveconnection](receiveconnection.md) wird verwendet, wenn eine Ausgabepin eine Formatänderung an den downstreampeer vorschlägt und das neue Format einen größeren Puffer erfordert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verarbeiten von Format Änderungen vom Videorenderer](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



