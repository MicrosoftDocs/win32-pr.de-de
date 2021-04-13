---
description: Dieses Thema bietet einen Überblick über die Datei Codierungs-APIs, die in Microsoft Media Foundation bereitgestellt werden.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Übersicht über die Codierung in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104559991"
---
# <a name="overview-of-encoding-in-media-foundation"></a>Übersicht über die Codierung in Media Foundation

Dieses Thema bietet einen Überblick über die Datei Codierungs-APIs, die in Microsoft Media Foundation bereitgestellt werden.

## <a name="terminology"></a>Begriff

Die *Codierung* ist ein allgemeiner Begriff, der mehrere verschiedene Prozesse abdeckt:

1.  Codieren eines Audiodaten-oder Videodaten Stroms in komprimierte Formate Beispiel: Codieren eines Videodaten Stroms in H. 264-Video.
2.  Multiplexing ("muxing") eines oder mehrerer Streams in einen einzelbytestream. In der Regel werden die eingehenden Datenströme zuerst codiert. Dieser Schritt kann die packetisierung der codierten Streams einschließen.
3.  Schreiben eines Multiplex-Bytestreams in eine Datei, z. b. eine MP4-Datei oder eine ASF-Datei (Advanced Systems Format). Alternativ kann der Multiplex-Stream über das Netzwerk gesendet werden.

Das folgende Diagramm zeigt diese drei Prozesse:

![Diagramm mit den Codierungs-und Multiplexing-Prozessen](images/encoding03.png)

Zu den Variationen dieses Prozesses zählen Transcodierung und remuxing:

-   *Transcoding* bedeutet, dass eine vorhandene Datei decodiert, die Streams neu codiert und die codierten Streams erneut Multiplexing werden. Die Transcodierung kann durchgeführt werden, um eine Datei von einem Codierungstyp in einen anderen zu konvertieren. So konvertieren Sie z. b. das H. 264-Video in Windows Media Video (WMV). Außerdem kann die codierte Bitrate geändert werden. die Video Frame Größe; die Framerate. oder andere Format Parameter.
-   *Remultiplexing* oder *remuxing* bedeutet, dass eine Datei Demultiplexing und die Streams erneut Multiplexing werden, ohne den Schritt "decodieren/codieren" zu verwenden. Dies kann durchgeführt werden, um zu ändern, wie die Audiodateien bzw. Video Pakete mit einem multiplext versehen werden, um einen Stream zu entfernen oder um Streams aus zwei verschiedenen Quelldateien zu kombinieren
-   *Transrating* ist ein Sonderfall von Transcoding, bei dem die Bitrate geändert wird, ohne den Komprimierungstyp zu ändern. Beispielsweise können Sie eine Datei mit hoher Bitrate in eine niedrigere Bitrate konvertieren. Ein typisches Szenario, in dem die transbewertung verwendet werden kann, ist die Synchronisierung von Medieninhalten von einem PC mit einem tragbaren Gerät. Wenn das portable Gerät keine hohe Bitrate unterstützt, wird die Datei möglicherweise vor dem Kopieren auf das portable Gerät abgehandelt.

Das folgende Blockdiagramm zeigt den transcodierungsprozess.

![Diagramm mit dem Transcodierungs Prozess](images/encoding05.png)

Das folgende Blockdiagramm zeigt den remuxing-Prozess.

![Diagramm, das den remuxing-Prozess anzeigt](images/encoding06.png)

In dieser Dokumentation wird manchmal der Begriff *Codierung* verwendet, um sowohl Transcodierung als auch remuxing einzubeziehen. Wenn es wichtig ist, zwischen diesen zu unterscheiden, wird der Unterschied in der Dokumentation festzustellen.

Siehe auch: [Media Foundation: grundlegende Konzepte](media-foundation-programming--essential-concepts.md).

## <a name="media-foundation-encoding-architecture"></a>Media Foundation Codierungs Architektur

Auf der untersten Ebene der Media Foundation-Architektur werden die folgenden Typen von Komponenten für die Codierung verwendet:

-   Für die Transcodierung werden [Medienquellen](media-sources.md) verwendet, um die Quelldatei zu dekodieren.
-   Beim Codierungsprozess werden [Media Foundation Transformationen](media-foundation-transforms.md) zum Decodieren und Codieren von Streams verwendet.
-   Für den Multiplexing-Prozess werden [Medien senken](media-sinks.md) verwendet, um die Streams zu Multiplexen und den Multiplexen Stream in eine Datei oder ein Netzwerk zu schreiben.

Das folgende Diagramm zeigt den Datenfluss zwischen diesen Komponenten in einem Transcodierungs Szenario:

![Diagramm mit den Komponenten, die bei der Transcodierung verwendet werden](images/encoding04.png)

Diese Komponenten werden von den meisten Anwendungen nicht direkt verwendet. Stattdessen werden von einer Anwendung APIs auf höherer Ebene verwendet, die diese untergeordneten Komponenten verwalten. Media Foundation bietet zwei APIs auf höherer Ebene für die Codierung:

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Medien Sitzung](media-session.md)
</dt> <dd>

Die Medien Sitzung bietet eine End-to-End-Pipeline, mit der Daten aus der Medienquelle, über die Codecs und schließlich in die Medien Senke verschoben werden. Die Anwendung steuert die Medien Sitzung und empfängt Statusereignisse von der Medien Sitzung.

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Quell Leser](source-reader.md) Plus [Senke Writer](sink-writer.md)
</dt> <dd>

Der Quell Leser umschließt die Medienquelle und optional die Decoders. Die Anwendung übermittelt entweder codierte oder decodierte Stichproben. Der Senke-Writer umschließt die Medien Senke und optional die Encoder. Die Anwendung übergibt Beispiele an den Senke-Writer.

</dd> </dl>

Das folgende Diagramm zeigt die Medien Sitzung:

![Diagramm, das zeigt, wie die Medien Sitzung die Transcodierung durchführt](images/encoding01.png)

Die [transcode-API](transcode-api.md) (das blaue schattierte Feld) ist ein Satz von APIs, die in Windows 7 eingeführt wurden, um die Konfiguration der Medien Sitzung für die Codierung zu vereinfachen.

Das nächste Diagramm zeigt den Quell Reader und den Senke-Writer:

![Diagramm, das die Transcodierung mit dem Quell-und senderwriter zeigt](images/encoding02.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codierung und Dateierstellung](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation Programmierung: grundlegende Konzepte](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



