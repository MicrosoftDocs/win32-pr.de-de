---
title: Two-Pass Codierung
description: Two-Pass Codierung
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media-Format-SDK, Two-Pass-Codierung
- Windows Media-Format-SDK, 2-Pass-Codierung
- Codecs, Two-Pass-Codierung
- Codecs, 2-Pass-Codierung
- zwei-Pass-Codierung, Informationen
- '2: Codierung, Informationen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036722"
---
# <a name="two-pass-encoding"></a>Two-Pass Codierung

Die zwei-Pass-Codierung ist eine Codierungsmethode, die mit einigen Codecs verfügbar ist, z. b. Windows Media Video 9-Codec Wenn Sie die zwei-Pass-Codierung verwenden, verarbeitet der Codec alle Beispiele für den Stream zweimal. Beim ersten Durchlauf sammelt der Codec Informationen zum Inhalt des Streams. Beim zweiten Durchlauf verwendet der Codec die Informationen, die beim ersten Durchlauf gesammelt werden, um den Codierungsprozess für den Datenstrom zu optimieren.

Im konstanten Bitrate-Codierungs Modus sind Dateien, die in zwei Durchläufen codiert sind, im Allgemeinen effizienter als Dateien, die in einem einzelnen Durchlauf codiert sind. Bei der Qualitäts basierten VBR, bei der es sich um einen Durchlauf handelt, wird eine konsistentere Qualität erzielt als bei einem Bitrate-basierten VBR, der zwei Pass ist.

Sie können keine zwei-Pass-Codierung für Livestreams verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Codec-Features**](codec-features.md)
</dt> <dt>

[**Verwenden von Two-Pass Codierung**](using-two-pass-encoding.md)
</dt> </dl>

 

 




