---
description: Graph-Building Komponenten
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Graph-Building Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3ba346356109d8080d887a510cfcb85b6a6c80
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125587"
---
# <a name="graph-building-components"></a>Graph-Building Komponenten

DirectShow stellt mehrere Komponenten bereit, die zum Erstellen von Filter Diagrammen verwendet werden können. Dabei handelt es sich z. B. um:

-   [Filtern](filter-graph-manager.md)Sie den Diagramm-Manager. Dieses Objekt steuert das Filter Diagramm. Sie unterstützt unter anderem die Schnittstellen [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder), [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)und [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) . Alle DirectShow-Anwendungen verwenden dieses Objekt zu einem bestimmten Zeitpunkt, obwohl in einigen Fällen ein anderes Objekt den Filter Graph-Manager für die Anwendung erstellt.
-   [Erfassungs Diagramm](capture-graph-builder.md)-Generator. Dieses Objekt stellt zusätzliche Methoden zum Entwickeln von Filter Diagrammen bereit. Sie wurde ursprünglich für das Erstellen von Diagrammen entwickelt, die eine Video Erfassung durchführen (daher der Name), ist aber für viele andere Arten von benutzerdefinierten Filter Diagrammen nützlich. Die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle wird unterstützt.
-   [Filtermapper](filter-mapper.md) und [System Geräte Enumerator](system-device-enumerator.md). Diese Objekte suchen Filter, die im System des Benutzers registriert sind oder Hardware Geräte darstellen.
-   [DVD-Diagramm](dvd-graph-builder.md)-Generator. Dieses Objekt erstellt Filter Diagramme für die DVD-Wiedergabe und-Navigation. Die [**idvdgraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) -Schnittstelle wird unterstützt.

### <a name="intelligent-connect"></a>Intelligent Connect

Der Begriff "Intelligent Connect" umfasst eine Reihe von Algorithmen, die der Filter Graph-Manager verwendet, um den gesamten oder einen Teil eines Filter Diagramms zu erstellen. Wenn der Filter Graph-Manager zusätzliche Filter zum Vervollständigen des Diagramms erfordert, erfolgt ungefähr Folgendes:

1.  Wenn sich derzeit ein Filter im Diagramm befindet und mindestens eine nicht verbundene Eingabe-PIN vorhanden ist, versucht der Filter Graph-Manager, diesen Filter zu verwenden.
2.  Andernfalls sucht der Filter Graph-Manager in der Registrierung nach Filtern, die den richtigen Medientyp für die Verbindung akzeptieren können. Jeder Filter hat einen Registrierungs Wert mit dem Namen "Verdienst", der ungefähr angibt, wie wahrscheinlich der Filter für das vervollständigen des Diagramms nützlich ist. Der Filter Graph-Manager versucht Filter in der Reihenfolge der Verdienst Werte zu filtern. Für jeden Streamtyp (z. b. Audiodatei, Video oder MIDI) hat der Standardrenderer einen hohen Vorteil. Decoders haben außerdem eine hohe Leistung. Filter für spezielle Zwecke haben eine geringe Leistung.

Wenn der Filter Graph-Manager hängen bleibt, wird er zurückgesetzt, und es wird eine andere Kombination von Filtern ausprobiert. Die genauen Details finden Sie im Thema [Intelligent Connect](intelligent-connect.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufbauen des Filter Diagramms](building-the-filter-graph.md)
</dt> </dl>

 

 



