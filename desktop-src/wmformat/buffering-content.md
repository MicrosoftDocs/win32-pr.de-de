---
title: Pufferung von Inhalten
description: Pufferung von Inhalten
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media-Format-SDK, Pufferung von Inhalten
- Pufferung von Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341421"
---
# <a name="buffering-content"></a>Pufferung von Inhalten

Wenn das Reader-Objekt eine Streamingdatei öffnet, bestimmt es die Größe des Puffers basierend auf den Einstellungen im Header der Datei. Sie können sich den Puffer als Bucket mit einem Loch im unteren Bereich vorstellen, das bei konstanter Geschwindigkeit eine Dichte gibt. Solange die Rate, mit der der Bucket aufgefüllt wird, nicht im Durchschnitt größer ist als die Rate, mit der er nicht mehr erreicht wird, führt der Bucket nie zu einem Überlauf.

Die Rate, mit der die imaginären Bucket-Lecks die Bitrate des Streams ist. Die Rate, mit der der Bucket ausgefüllt wird, ist die tatsächliche streamingbitrate. Die Daten in einem komprimierten Datenstrom variieren abhängig von der erreichten Komprimierung von Sample zu Sample. Obwohl die Bitrate des Streams im Profil festgelegt ist, stellt Sie somit die durchschnittliche Bitrate dar, nicht eine Konstante.

Die andere streamingeinstellung, die für den Puffer Prozess wichtig ist, ist das Puffer Fenster. Das Puffer Fenster wird zeitlich gemessen und gibt an, wie viel Inhalt gepuffert werden kann. Die Kapazität des imaginären Bucket kann mithilfe des Puffer Fensters gefunden werden. Wenn Sie z. b. einen Datenstrom mit einer Bitrate von 32 Kbit/s und einem Puffer Fenster von 3 Sekunden haben, wird der Puffer so skaliert, dass er 3 Sekunden mit 32 Kbit/s-Inhalt und 12.000 Bytes (32.000 Bits pro Sekunde x 3 Sekunden/8 Bits pro Byte) enthält. Der Codec schränkt die Variation zwischen der tatsächlichen streamingbitrate codierter Stichproben ein, sodass die durchschnittliche Bitrate über einen Zeitraum, der gleich dem Puffer Fenster ist, nicht größer als die Bitrate des Streams ist.

Normalerweise legen Sie die Bitrate und das Puffer Fenster für einen Stream in einem Profil fest, und der Writer übernimmt den Rest. Wenn Sie komprimierte Beispiele an den Reader übergeben, müssen Sie jedoch sicherstellen, dass die richtigen Werte in die neue Datei übertragen werden, indem Sie die Bitrate und das Puffer Fenster für den Stream im Ziel Profil auf die Werte aus dem komprimierten Stream festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**Medien Beispiele**](media-samples.md)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




