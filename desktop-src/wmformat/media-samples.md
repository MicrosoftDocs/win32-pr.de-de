---
title: Medienbeispiele (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über Medienbeispiele im Windows Media Format 11 SDK. Ein Medienbeispiel ist ein Objekt, das eine sortierte Liste von null oder mehr Puffern enthält.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK, Medienbeispiele
- Windows Media Format SDK, Beispiele
- Advanced Systems Format (ASF), Medienbeispiele
- ASF (Advanced Systems Format), Medienbeispiele
- Advanced Systems Format (ASF), Beispiele
- ASF (Advanced Systems Format), Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8d264aa23e80f1e692f28789c2f2e631ef3ed8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989073"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>Medienbeispiele (Windows Media Format 11 SDK)

Ein Medienbeispiel oder Beispiel ist ein Block digitaler Mediendaten. Ein Beispiel ist die grundlegende Einheit, die durch das Lesen und Schreiben von Objekten des Windows Media Format SDK bearbeitet wird. Der Inhalt eines einzelnen Beispiels wird durch den Medientyp vorgegeben, der dem Beispiel zugeordnet ist. Für Videos stellt jedes Beispiel einen einzelnen Frame dar. Für Audiodaten wird die Datenmenge in einem einzelnen Beispiel in dem Profil festgelegt, das zum Erstellen der ASF-Datei verwendet wird.

Beispiele können unkomprimierte Daten enthalten, oder sie können komprimierte Daten enthalten. In diesem Fall werden sie *als Streambeispiele* bezeichnet. Beim Erstellen einer ASF-Datei übergeben Sie Beispiele an den Writer. Der Writer koordiniert die Komprimierung der Stichproben mit dem entsprechenden Codec und ordnet die komprimierten Daten im Datenabschnitt der ASF-Datei an. Bei der Wiedergabe liest der Reader die komprimierten Daten, dekomprimiert sie und stellt die rekonstruierten unkomprimierten Daten als Ausgabebeispiele bereit.

Alle vom Windows Media Format SDK verwendeten Beispiele werden im Pufferobjekt gekapselt, dessen Arbeitsspeicher automatisch von den SDK-Laufzeitkomponenten zugeordnet wird. Sie können bei Bedarf auch eigene Puffer zuordnen, indem Sie erweiterte Features des Writers und Readers verwenden.

**Hinweis** Der Begriff Sample wird in diesem SDK verwendet, um auf ein Medienbeispiel und nicht auf ein Audiobeispiel zu verweisen. Bei der Audiocodierung bezieht sich ein Beispiel auf einen einzelnen codierten Audiowert. In der Regel wird die Qualität codierter Audiodaten durch eine Reihe von Stichproben pro Sekunde angegeben. Beispielsweise wird cd quality sound mit 44.100 Stichproben pro Sekunde aufgezeichnet. Dieser Wert wird häufig mit der Hz-Notation abgekürzt, sodass 44.100 Stichproben pro Sekunde 44.100 Hz oder 44,1 kHz betragen würden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**INSSBuffer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




