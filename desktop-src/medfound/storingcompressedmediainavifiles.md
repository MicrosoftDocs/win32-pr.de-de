---
description: Hier wird beschrieben, wie Windows Media-Daten in einer AVI-Datei gespeichert werden.
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: Speichern von komprimierten Medien in AVI-Dateien (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080524a47b4295517d50705f6aeb125d085a8346
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351498"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>Speichern von komprimierten Medien in AVI-Dateien (Microsoft Media Foundation)

Jeder Inhalt, den Sie mit dem Windows Media Audio und den Video Codecs komprimieren, muss in einem Containerformat abgelegt werden. Eines der beliebtesten Formate ist Audiovideointerleave oder AVI. Sie können mit Microsoft Video for Windows (Vfw) oder Microsoft DirectShow AVI-Dateien erstellen. Weitere Informationen zur Verwendung von Video für Windows oder DirectShow finden Sie in der Produktdokumentation auf MSDN.

Die Windows Media Audio-und Video Codecs wurden entwickelt, um die Eigenschaften des Advanced Systems Format (ASF) zu verwenden, bei dem es sich um den von Windows Media verwendeten Container handelt. Da AVI und ASF Inhalte anders speichern, treten beim Speichern von Inhalten, die mit den Windows Media Audio-und Video Codecs in einer AVI-Datei komprimiert werden, einige Schwierigkeiten auf.

Die Windows Media Audio Codecs komprimieren Audioinhalte so, dass Sie ohne Zeitstempel für die einzelnen Beispiele nicht ordnungsgemäß deaktiviert werden können. Dies ermöglicht einige Optimierungen in den komprimierten Medien. Da der ASF-Container Zeitstempel mit allen Beispielen speichert, hat dieses Merkmal der audioalgorithmen immer gut funktioniert.

Von AVI-Dateien werden Zeitstempel jedoch nicht mit Beispielen aufbewahrt. Dies bedeutet, dass Windows Media Audio Inhalt nicht ordnungsgemäß dekomprimiert werden kann, wenn er in einer AVI-Datei gespeichert wird. Windows Media Video Inhalt weist diese Einschränkung nicht auf und kann in AVI-Dateien eingeschlossen werden. Zum Codieren Windows Media Video Inhalts in eine AVI-Datei mit synchronisiertem Sound müssen Sie einen anderen Audiocodec verwenden.

Das andere Problem bei der Verwendung einer AVI-Datei als Container für Windows Media betrifft ein Video mit niedriger Bitrate. Eine der Methoden, mit denen die Windows Media Video Codecs Video Inhalte für niedrige Bitraten erzeugt, besteht darin, doppelte Frames zu löschen. Wenn Sie Windows Media Video Inhalt in eine ASF-Datei einfügen möchten, müssen Sie den Encoder so festlegen, dass dummyframes für doppelte Frames bereitgestellt werden (legen Sie [mfpkey \_ producedummyframes](mfpkey-producedummyframesproperty.md) auf Variant \_ true fest), damit jeder Frame in der Datei dargestellt wird. Die vom Codec erzeugten Pseudo Rahmen sind 8 Bytes groß. Der in die Datei von AVI Multiplexer geschriebene Frame kann jedoch mehrere hundert Byte groß sein und mit zufälligen Daten gefüllt werden. Eine auf diese Weise erstellte AVI-Datei ist zwar weiterhin Wiedergabe fähig, aber Sie ist viel größer als erwartet. Sie können dieses Problem vermeiden, indem Sie beim Codieren von Videos für die Speicherung in AVI-Dateien höhere Bitraten verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 



