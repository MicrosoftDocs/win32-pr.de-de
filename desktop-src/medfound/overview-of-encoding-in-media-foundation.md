---
description: Dieses Thema enthält eine Übersicht über die dateicodierungs-APIs, die in Microsoft Media Foundation bereitgestellt werden.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Übersicht über die Codierung in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a663260d92aad4eb23902ec35721c252f15fbba64c3404ff97bfb60f0622c674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239766"
---
# <a name="overview-of-encoding-in-media-foundation"></a>Übersicht über die Codierung in Media Foundation

Dieses Thema enthält eine Übersicht über die dateicodierungs-APIs, die in Microsoft Media Foundation bereitgestellt werden.

## <a name="terminology"></a>Begriff

*Die Codierung* ist ein allgemeiner Begriff, der mehrere verschiedene Prozesse abdeckt:

1.  Codieren eines Audio- oder Videodatenstroms in komprimierte Formate. Beispiel: Codieren eines Videostreams in H.264-Video.
2.  Multiplexing ("Muxing") eines oder mehrerer Streams in einen einzelnen Bytestream. In der Regel werden die eingehenden Datenströme zuerst codiert. Dieser Schritt kann das Packen der codierten Datenströme umfassen.
3.  Schreiben eines Multiplex-Bytestreams in eine Datei, z. B. eine MP4- oder ASF-Datei (Advanced Systems Format). Alternativ kann der Multiplexstream über das Netzwerk gesendet werden.

Das folgende Diagramm zeigt diese drei Prozesse:

![Diagramm mit den Codierungs- und Multiplexprozessen](images/encoding03.png)

Zu den Varianten dieses Prozesses gehören Transcodierung und Neubenutzererfahrung:

-   *Transcodierung* bedeutet, dass eine vorhandene Datei decodiert, die Streams erneut codiert und die codierten Streams erneut multiplexiert werden. Die Transcodierung kann durchgeführt werden, um eine Datei von einem Codierungstyp in einen anderen zu konvertieren. zum Beispiel, um H.264-Videos in Windows Media Video (WMV) zu konvertieren. Sie können auch die codierte Bitrate ändern. die Videoframegröße; die Bildfrequenz; oder andere Formatparameter.
-   *Remultiplexing* oder *Remuxing* bedeutet, eine Datei zu demultiplexing und die Streams ohne Decodierungs-/Codierungsschritt erneut zu multiplen. Dies kann geschehen, um zu ändern, wie die Audio-/Videopakete multiplexiert werden, um einen Stream zu entfernen oder Streams aus zwei verschiedenen Quelldateien zu kombinieren.
-   *Transrating* ist ein Sonderfall der Transcodierung, bei dem die Bitrate geändert wird, ohne den Komprimierungstyp zu ändern. Beispielsweise können Sie eine Datei mit hoher Bitrate in eine niedrigere Bitrate konvertieren. Ein typisches Szenario, in dem die Transratierung verwendet werden kann, ist die Synchronisierung von Medieninhalten von einem PC mit einem portablen Gerät. Wenn das portable Gerät keine hohe Bitrate unterstützt, wird die Datei möglicherweise transratiert, bevor sie auf das portable Gerät kopiert wird.

Das folgende Blockdiagramm zeigt den Transcodierungsprozess.

![Diagramm des Transcodierungsprozesses](images/encoding05.png)

Das folgende Blockdiagramm zeigt den Neubenutzererfahrungsprozess.

![Diagramm des Neubenutzererfahrungsprozesses](images/encoding06.png)

In dieser Dokumentation wird manchmal der Begriff *Codierung* verwendet, um sowohl transcoding als auch remuxing einzubeziehen. Wenn es wichtig ist, zwischen ihnen zu unterscheiden, wird der Unterschied in der Dokumentation beachtet.

Siehe auch: [Media Foundation: Grundlegende Konzepte.](media-foundation-programming--essential-concepts.md)

## <a name="media-foundation-encoding-architecture"></a>Media Foundation-Codierungsarchitektur

Auf der untersten Ebene der Media Foundation-Architektur werden die folgenden Komponententypen für die Codierung verwendet:

-   Für die Transcodierung werden [Medienquellen](media-sources.md) verwendet, um die Quelldatei zu demultiplexen.
-   Für den Codierungsprozess werden [Media Foundation Transformationen](media-foundation-transforms.md) verwendet, um Streams zu decodieren und zu codieren.
-   Für den Multiplexprozess werden [Mediensenken](media-sinks.md) verwendet, um die Datenströme zu multiplexieren und den Multiplexstream in eine Datei oder ein Netzwerk zu schreiben.

Das folgende Diagramm zeigt den Datenfluss zwischen diesen Komponenten in einem Transcodierungsszenario:

![Diagramm der bei der Transcodierung verwendeten Komponenten](images/encoding04.png)

Die meisten Anwendungen verwenden diese Komponenten nicht direkt. Stattdessen verwendet eine Anwendung APIs auf höherer Ebene, die diese Komponenten auf niedrigerer Ebene verwalten. Media Foundation bietet zwei übergeordnete APIs für die Codierung:

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Mediensitzung](media-session.md)
</dt> <dd>

Die Mediensitzung stellt eine End-to-End-Pipeline bereit, die Daten aus der Medienquelle, über die Codecs und schließlich in die Mediensenke verschiebt. Die Anwendung steuert die Mediensitzung und empfängt Statusereignisse von der Mediensitzung.

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Quellleser](source-reader.md) plus [Sink Writer](sink-writer.md)
</dt> <dd>

Der Quellleser umschließt die Medienquelle und optional die Decoder. Sie stellt entweder codierte oder decodierte Stichproben für die Anwendung bereit. Der Sink Writer umschließt die Mediensenke und optional die Encoder. Die Anwendung übergibt Beispiele an den Sink Writer.

</dd> </dl>

Das folgende Diagramm zeigt die Mediensitzung:

![Diagramm, das zeigt, wie die Mediensitzung die Transcodierung ausführt](images/encoding01.png)

Die [Transcodierungs-API](transcode-api.md) (das blau schattierte Feld) ist eine Reihe von APIs, die in Windows 7 eingeführt wurden und die Konfiguration der Mediensitzung für die Codierung vereinfachen.

Das nächste Diagramm zeigt den Quellleser und den Senkenwriter:

![Diagramm, das die Transcodierung mit dem Quellleser und dem Senkenwriter zeigt](images/encoding02.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codierung und Dateierstellung](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation-Programmierung: Grundlegende Konzepte](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



