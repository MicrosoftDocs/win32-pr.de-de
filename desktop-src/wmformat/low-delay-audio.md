---
title: Low-Delay Audiodaten
description: Low-Delay Audiodaten
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media-Format-SDK, Low-Delay-Audiodaten
- Windows Media-Format-SDK, Audiounterstützung
- Codecs, Low-Delay-Audiodaten
- Codecs, Audiounterstützung
- Low-Delay-Audiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337814"
---
# <a name="low-delay-audio"></a>Low-Delay Audiodaten

Das Low-Delay-Audioformat ist ein Codierungs Modus, der komprimierte Audiodaten mit einer kleineren Puffer Fenster Einstellung als andere Modi erzeugt. Dies ist nützlich für Datenströme, die während der Wiedergabe schnell gewechselt werden müssen. Das typische Szenario für dieses Feature ist eine Streamingpräsentation, die die Möglichkeit bietet, Inhalte willkürlich zu wechseln, wie z. b. das Ändern des Kanals eines Fernsehsenders.

Bei Verwendung eines Audioformats mit niedriger Verzögerung wird die Latenz beim Wechseln von Inhalten im Vergleich zu anderen Audioformaten drastisch reduziert. Die Latenzzeit wird auch bei Live Übertragungen reduziert, wenn Sie Low-Delay-Formate verwenden.

Diese Funktion wird von den Windows Media Audio 9,1-und Windows Media Audio 9,1 Professional-Codecs unterstützt. Low-Delay-Formate sind nur für die Konstante Bitrate-Codierung (sowohl ein-als auch zwei-Pass-) verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Codec-Features**](codec-features.md)
</dt> </dl>

 

 




