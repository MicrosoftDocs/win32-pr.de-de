---
description: Graph-Building Komponenten
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Graph-Building Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aabcf31f55d0d42117e39cb22fa286b383641c94fe21f386345fd8db1cc890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564640"
---
# <a name="graph-building-components"></a>Graph-Building Komponenten

DirectShow bietet mehrere Komponenten, die zum Erstellen von Filterdiagrammen verwendet werden können. Dabei handelt es sich z. B. um:

-   [Filtern Graph Manager](filter-graph-manager.md). Dieses Objekt steuert das Filterdiagramm. Sie unterstützt [**u.a. die Schnittstellen IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)und [**IMediaEventEx.**](/windows/desktop/api/Control/nn-control-imediaeventex) Alle DirectShow-Anwendungen verwenden dieses Objekt zu einem bestimmten Zeitpunkt, obwohl in einigen Fällen ein anderes Objekt den Filter Graph Manager für die Anwendung erstellt.
-   [Capture Graph Builder](capture-graph-builder.md). Dieses Objekt bietet zusätzliche Methoden zum Erstellen von Filterdiagrammen. Es wurde ursprünglich für das Erstellen von Diagrammen entwickelt, die Videoaufnahmen (daher den Namen) ausführen, aber für viele andere Arten von benutzerdefiniertem Filterdiagramm nützlich sind. Es unterstützt die [**ICaptureGraphBuilder2-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)
-   [Filter Mapper](filter-mapper.md) und [System device Enumerator](system-device-enumerator.md). Diese Objekte suchen nach Filtern, die auf dem System des Benutzers registriert sind oder Hardwaregeräte darstellen.
-   [DVD Graph Builder](dvd-graph-builder.md). Dieses Objekt erstellt Filterdiagramme für dvd-Wiedergabe und -Navigation. Es unterstützt die [**IDvdGraphBuilder-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)

### <a name="intelligent-connect"></a>Intelligente Verbinden

Der Begriff "Intelligent Verbinden" umfasst eine Reihe von Algorithmen, die der Filter Graph Manager verwendet, um einen Filtergraphen ganz oder teilweise zu erstellen. Wenn der Filter Graph-Manager zusätzliche Filter benötigt, um das Diagramm zu vervollständigen, führt er ungefähr Folgendes aus:

1.  Wenn das Diagramm derzeit einen Filter mit mindestens einem nicht verbundenen Eingabepin auflistet, versucht der Graph-Manager, diesen Filter zu verwenden.
2.  Andernfalls sucht Graph Filter-Manager in der Registrierung nach Filtern, die den richtigen Medientyp für die Verbindung akzeptieren können. Jeder Filter verfügt über einen Registrierungswert mit dem Namen " Standardwert", der ungefähr angibt, wie wahrscheinlich der Filter beim Abschließen des Diagramms sein wird. Der Filter Graph-Manager versucht Filter in der Reihenfolge des Werts. Für jeden Streamtyp (z. B. Audio, Video oderGUIDE) hat der Standardrenderer eine hohe Leistung. Decoder haben auch hohe Vorteile. Filter für spezielle Zwecke haben geringen Nutzen.

Wenn der Filter Graph-Manager hängen bleibt, wird er zurückgesetzt und versucht, eine andere Kombination von Filtern auszuprobieren. Die genauen Details finden Sie im Thema [Intelligent Verbinden](intelligent-connect.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen des Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



