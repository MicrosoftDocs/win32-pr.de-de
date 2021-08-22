---
title: Puffern von Inhalten
description: Puffern von Inhalten
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Medienformat-SDK,Puffern von Inhalten
- Puffern von Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3005895f7a196073566c32bb455f5808bf6f11feb491000b140e1bbf88b94b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586990"
---
# <a name="buffering-content"></a>Puffern von Inhalten

Wenn das Readerobjekt eine Streamingdatei öffnet, bestimmt es die Größe des Puffers basierend auf den Einstellungen im Header der Datei. Sie können sich den Puffer als Bucket mit einer Lücke im unteren Bereich vorstellen, die mit konstanter Rate ausläuft. Solange die Rate, mit der der Bucket gefüllt wird, durchschnittlich nicht größer als die Rate ist, mit der er verloren geht, wird der Bucket nie überlaufen.

Die Rate, mit der der imaginäre Bucket verloren geht, ist die Bitrate des Streams. Die Rate, mit der der Bucket gefüllt wird, ist die tatsächliche Streamingbitrate. Die Daten in einem komprimierten Stream variieren je nach erreichter Komprimierungsmenge von Stichprobe zu Stichprobe. Obwohl die Bitrate des Streams im Profil festgelegt ist, stellt sie daher die durchschnittliche Bitrate und keine Konstante dar.

Die andere für den Pufferprozess wichtige Streameinstellung ist das Pufferfenster. Das Pufferfenster wird zeitlich gemessen und gibt an, wie viel Inhalt gepuffert werden kann. Die Kapazität des imaginären Buckets kann über das Pufferfenster ermittelt werden. Wenn Sie beispielsweise über einen Stream mit einer Bitrate von 32 KBit/s und einem Pufferfenster von 3 Sekunden verfügen, ist der Puffer so dimensioniert, dass er 3 Sekunden mit 32 KBit/s-Inhalt oder 12.000 Bytes (32.000 Bits pro Sekunde x 3 Sekunden/8 Bits pro Byte) enthält. Der Codec schränkt die Variation zwischen der tatsächlichen Streamingbitrate codierter Stichproben ein, sodass die durchschnittliche Bitrate über einen bestimmten Zeitraum, der dem Pufferfenster entspricht, nicht größer als die Bitrate des Streams ist.

Normalerweise legen Sie die Bitrate und das Pufferfenster für einen Stream in einem Profil fest, und der Writer verarbeitet den Rest. Wenn Sie komprimierte Stichproben an den Reader übergeben, müssen Sie jedoch sicherstellen, dass die richtigen Werte in die neue Datei übertragen werden, indem Sie die Bitrate und das Pufferfenster für den Stream im Zielprofil auf die Werte aus dem komprimierten Stream festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**Medienbeispiele**](media-samples.md)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




