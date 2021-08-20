---
description: Beschreibt, wie Mediendaten Windows in einer AVI-Datei gespeichert werden.
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: Speichern von komprimierten Medien in AVI-Dateien (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d52c33f6ea01cd1a10572294eaf3ee57ab4423567e3b2cc1f0feb86e199707e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057725"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>Speichern von komprimierten Medien in AVI-Dateien (Microsoft Media Foundation)

Alle Inhalte, die Sie mithilfe der Windows Medienaudio- und Videocodecs komprimieren, müssen in einem Containerformat vorliegen. Eines der beliebtesten Formate ist Audio Video Interleave oder AVI. Sie können Microsoft Video for Windows (VfW) oder Microsoft DirectShow verwenden, um AVI-Dateien zu erstellen. Weitere Informationen zur Verwendung von Video for Windows oder DirectShow finden Sie in der Produktdokumentation auf MSDN.

Die Windows Medienaudio- und Videocodecs wurden entwickelt, um die Eigenschaften des Advanced Systems Format (ASF) zu verwenden, bei dem es sich um den Container handelt, der von Windows wird. Da AVI und ASF Inhalte unterschiedlich speichern, treten einige Schwierigkeiten beim Speichern von Inhalten auf, die mit den Windows Media Audio- und Videocodecs in einer AVI-Datei komprimiert sind.

Die Windows Media Audio-Codecs komprimieren Audioinhalte so, dass sie ohne Zeitstempel für die einzelnen Beispiele nicht ordnungsgemäß dekomprimiert werden können. Dies ermöglicht eine gewisse Optimierung der komprimierten Medien. Da der ASF-Container Zeitstempel mit allen Stichproben speichert, hat dieses Merkmal der Audioalgorithmen immer gut funktioniert.

AVI-Dateien behalten jedoch keine Zeitstempel mit Beispielen bei. Dies bedeutet, Windows Medienaudioinhalt nicht ordnungsgemäß dekomprimiert werden kann, wenn er in einer AVI-Datei gespeichert wird. Windows Medienvideoinhalte haben diese Einschränkung nicht und können in AVI-Dateien aufgenommen werden. Zum Codieren Windows Media Video-Inhalte in eine AVI-Datei mit synchronisierten Sound müssen Sie einen anderen Audiocodec verwenden.

Das andere Problem bei der Verwendung einer AVI-Datei als Container für Windows Medien betrifft Videos mit niedriger Bitrate. Eine der Möglichkeiten, wie die Windows Media Video-Codecs Videoinhalte für niedrige Bitraten erzeugen, ist das Löschen doppelter Frames. Wenn Sie Windows Media Video-Inhalte in einer ASF-Datei speichern möchten, müssen Sie den Encoder so festlegen, dass er Dummyframes für doppelte Frames liefert [(legen Sie MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) auf VARIANT TRUE fest), damit jeder Frame in der Datei dargestellt \_ wird. Die vom Codec erzeugten Dummyframes haben eine Größe von 8 Bytes. Der frame, der vom AVI-Multiplexer in die Datei geschrieben wird, kann jedoch Hunderte von Bytes größer sein und mit zufälligen Daten gefüllt werden. Eine auf diese Weise hergestellte AVI-Datei kann weiterhin abspielbar sein, ist aber viel größer als erwartet. Sie können dieses Problem vermeiden, indem Sie höhere Bitraten beim Codieren von Videos für die Speicherung in AVI-Dateien verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 



