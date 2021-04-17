---
description: In diesem Thema wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben. Weitere Informationen zum Verwenden von Media Foundation für bestimmte Programmieraufgaben finden Sie unter Media Foundation Programming Guide.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Übersicht über die Media Foundation-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104562529"
---
# <a name="overview-of-the-media-foundation-architecture"></a>Übersicht über die Media Foundation-Architektur

In diesem Thema wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben. Weitere Informationen zum Verwenden von Media Foundation für bestimmte Programmieraufgaben finden Sie unter [Media Foundation Programming Guide](media-foundation-programming-guide.md).

Das folgende Diagramm zeigt eine allgemeine Übersicht über die Media Foundation Architektur.

![das Diagramm zeigt eine allgemeine Übersicht über die Media Foundation-Architektur.](images/mfarch01.png)

Media Foundation bietet zwei unterschiedliche Programmier Modelle. Das erste Modell, das auf der linken Seite des Diagramms angezeigt wird, verwendet eine End-to-End-Pipeline für Mediendaten. Die Anwendung initialisiert die Pipeline – beispielsweise durch Bereitstellen der URL einer wieder zugebende Datei – und ruft dann Methoden zum Steuern des Streamings auf. Im zweiten Modell, das auf der rechten Seite des Diagramms angezeigt wird, ruft die Anwendung Daten entweder aus einer Quelle ab oder schiebt sie an ein Ziel (oder beides). Dieses Modell ist besonders nützlich, wenn Sie die Daten verarbeiten müssen, da die Anwendung direkten Zugriff auf den Datenstrom hat.

### <a name="primitives-and-platform"></a>Primitive und Plattform

Beginnend am unteren Rand des Diagramms sind die *primitiven* Hilfsobjekte, die in der Media Foundation-API verwendet werden:

-   [Attribute](attributes-and-properties.md) sind eine generische Methode zum Speichern von Informationen in einem Objekt als Liste von Schlüssel-Wert-Paaren.
-   [Medientypen](media-types.md) beschreiben das Format eines Mediendaten Stroms.
-   [Medien Puffer](media-buffers.md) enthalten Blöcke von Mediendaten, z. b. Video Frames und Audiobeispiele, und werden zum Transportieren von Daten zwischen Objekten verwendet.
-   [Medien Beispiele](media-samples.md) sind Container für Medien Puffer. Sie enthalten außerdem Metadaten zu den Puffern, z. b. Zeitstempel.

Die [Media Foundation Plattform-APIs](media-foundation-platform-apis.md) stellen einige Kernfunktionen bereit, die von der Media Foundation Pipeline verwendet werden, wie z. b. asynchrone Rückrufe und Arbeits Warteschlangen. Bestimmte Anwendungen müssen diese APIs möglicherweise direkt aufzurufen. Sie benötigen Sie auch, wenn Sie eine benutzerdefinierte Quelle, eine Transformation oder eine Senke für Media Foundation implementieren.

### <a name="media-pipeline"></a>Medien Pipeline

Die Medien Pipeline enthält drei Typen von Objekten, die Mediendaten generieren oder verarbeiten:

-   [Medienquellen](media-sources.md) stellen Daten in die Pipeline ein. Eine Medienquelle erhält möglicherweise Daten aus einer lokalen Datei, z. b. einer Videodatei. aus einem Netzwerkstream oder von einem Hardware Erfassungsgerät aus.
-   [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) verarbeiten von Daten aus einem Stream. Encoder und Decoder werden als MFTs implementiert.
-   [Medien senken](media-sinks.md) nutzen die Daten. beispielsweise durch das Anzeigen von Videos in der Anzeige, das Abspielen von Audiodaten oder das Schreiben der Daten in eine Mediendatei.

Drittanbieter können Ihre eigenen benutzerdefinierten Quellen, senken und MFTs implementieren. beispielsweise, um neue Mediendatei Formate zu unterstützen.

Die [Medien Sitzung](media-session.md) steuert den Datenfluss über die Pipeline und behandelt Aufgaben wie die Qualitätskontrolle, die Audio-/Videosynchronisierung und die Reaktion auf Formatänderungen.

### <a name="source-reader-and-sink-writer"></a>Quell Lese-und Senke-Writer

Der [Quell Reader](source-reader.md) und der [senkenwriter](sink-writer.md) bieten eine alternative Möglichkeit, die grundlegenden Media Foundation Komponenten (Medienquellen, Transformationen und Medien senken) zu verwenden. Der Quell Leser hostet eine Medienquelle und NULL oder mehr Decoders, während der Senke Writer eine Medien Senke und NULL oder mehr Encoder hostet. Sie können den Quell Reader verwenden, um komprimierte oder unkomprimierte Daten aus einer Medienquelle zu erhalten, und den sendenden Writer verwenden, um Daten zu codieren und die Daten an eine Medien Senke zu senden.

> [!Note]  
> Der Quell Reader und der Senke Writer sind in Windows 7 verfügbar.

 

Dieses Programmiermodell ermöglicht der Anwendung eine bessere Kontrolle über den Datenfluss. Außerdem erhält die Anwendung direkten Zugriff auf die Daten aus der Quelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation: Grundlegende Konzepte](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> </dl>

 

 



