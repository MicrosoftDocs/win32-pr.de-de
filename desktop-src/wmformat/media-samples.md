---
title: Medien Beispiele (Windows Media-Format 11 SDK)
description: Medien Beispiele
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media-Format-SDK, Medien Beispiele
- Windows Media-Format-SDK, Beispiele
- Advanced Systems Format (ASF), Medien Beispiele
- ASF (Advanced Systems Format), Medien Beispiele
- Advanced Systems Format (ASF), Beispiele
- ASF (Advanced Systems Format), Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103949360"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>Medien Beispiele (Windows Media-Format 11 SDK)

Ein Medien Beispiel (oder ein Beispiel) ist ein Block digitaler Mediendaten. Ein Beispiel ist die grundlegende Einheit, die durch das Lesen und Schreiben von Objekten des Windows Media Format SDK manipuliert wird. Der Inhalt einer einzelnen Stichprobe wird durch den Medientyp vorgegeben, der mit dem Beispiel verknüpft ist. Jedes Beispiel stellt einen einzelnen Frame dar. Für Audiodaten wird die Menge der Daten in einer einzelnen Stichprobe im Profil festgelegt, das zum Erstellen der ASF-Datei verwendet wird.

Beispiele können nicht komprimierte Daten enthalten, oder Sie können komprimierte Daten enthalten. in diesem Fall werden Sie als *streambeispiele* bezeichnet. Wenn Sie eine ASF-Datei erstellen, übergeben Sie Beispiele an den Writer. Der Writer koordiniert die Komprimierung der Beispiele mit dem entsprechenden Codec und ordnet die komprimierten Daten im Data-Abschnitt der ASF-Datei an. Bei der Wiedergabe liest der Reader die komprimierten Daten, dekomprimiert ihn und stellt die rekonstruierten unkomprimierten Daten als Ausgabe Beispiele zur Verfügung.

Alle vom Windows Media-Format-SDK verwendeten Beispiele sind in einem Puffer Objekt gekapselt, dessen Speicher automatisch von den SDK-Laufzeitkomponenten zugewiesen wird. Sie können bei Bedarf auch Ihre eigenen Puffer zuordnen, indem Sie erweiterte Funktionen von Writer und Reader verwenden.

**Hinweis** Der Begriff Sample wird in diesem SDK verwendet, um auf ein Medien Beispiel zu verweisen, nicht auf ein Audiobeispiel. Bei der Audiocodierung bezieht sich ein Beispiel auf einen einzelnen codierten Audiowert. In der Regel wird die Qualität der codierten Audiodaten durch eine Anzahl von Stichproben pro Sekunde angegeben. Beispielsweise wird CD Quality Sound bei 44.100-Stichproben pro Sekunde aufgezeichnet. Dieser Wert wird in der Regel mit der Hz-Notation abgekürzt, 44.100-Stichproben pro Sekunde wären also 44.100 Hz oder 44,1 kHz.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**Inssbuffer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




