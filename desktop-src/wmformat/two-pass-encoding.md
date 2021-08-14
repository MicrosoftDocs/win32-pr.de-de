---
title: Two-Pass Codierung
description: Two-Pass Codierung
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Medienformat-SDK, Codierung mit zwei Durchgangen
- Windows Medienformat-SDK, 2-Pass-Codierung
- Codecs,Zwei-Pass-Codierung
- Codecs,2-Pass-Codierung
- Codierung mit zwei Durchgangen, Informationen
- 2-Pass-Codierung,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cd769049b5fa3869c844e00d9ee14cfae596b197d06d414b04a544d831bbeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845338"
---
# <a name="two-pass-encoding"></a>Two-Pass Codierung

Die Zweipasscodierung ist eine Codierungsmethode, die mit einigen Codecs verfügbar ist, z. B. dem Windows Media Video 9-Codec. Wenn Sie die Zwei-Pass-Codierung verwenden, verarbeitet der Codec alle Beispiele für den Stream zweimal. Beim ersten Durchlauf sammelt der Codec Informationen zum Inhalt des Streams. Beim zweiten Durchlauf verwendet der Codec die beim ersten Durchlauf erfassten Informationen, um den Codierungsprozess für den Stream zu optimieren.

Im Codierungsmodus Konstante Bitrate sind Dateien, die in zwei Durchläufen codiert werden, im Allgemeinen effizienter als Dateien, die in einem einzelnen Durchgang codiert sind. Die qualitätsbasierte VBR, bei der es sich um einen Durchgang handelt, erzeugt eine konsistentere Qualität als die bitratenbasierte VBR, bei der es sich um einen Zwei-Durch-Durchgang handelt.

Sie können die Codierung mit zwei Durchläufen nicht für Livestreams verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Codecfunktionen**](codec-features.md)
</dt> <dt>

[**Verwenden der Two-Pass Codierung**](using-two-pass-encoding.md)
</dt> </dl>

 

 




