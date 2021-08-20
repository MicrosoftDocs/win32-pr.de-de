---
description: Wie kann ein Videostream, der mit qualitätsbasiertem VBR codiert ist, weniger Frames als der ursprüngliche Stream aufweisen?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: Wie kann ein Videostream, der mit qualitätsbasiertem VBR codiert ist, weniger Frames als der ursprüngliche Stream aufweisen?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33ebdc4e8538bfd5cf0d8b74670d593c20cfbc4adbf237a7e3c59f9951379b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063337"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a>Wie kann ein Videostream, der mit qualitätsbasiertem VBR codiert ist, weniger Frames als der ursprüngliche Stream aufweisen?

Die Frameanzahl eines codierten Streams kann aus zwei Gründen niedriger als die Frameanzahl des Originals sein: doppelte Frames und gelöschte Frames.

Der Encoder erzeugt normalerweise keine Frames, die exakte Duplikate des vorherigen Frames sind. Wenn Sie ein Beispiel für jeden Frame benötigen (dies ist z. B. für einige Container erforderlich), können Sie den Encoder so konfigurieren, dass er "Dummyframes" erzeugt, indem Sie die [MFPKEY \_ PRODUCEDUMMYFRAMES-Eigenschaft](mfpkey-producedummyframesproperty.md) auf VARIANT \_ TRUE festlegen.

Der Encoder löscht Frames, wenn er nicht alle Frames codieren kann, ohne den Puffer zu überlaufen. Gelöschte Frames wirken sich auf die Qualität des Streams aus, doppelte Frames nicht.

Sie können Framestatistiken vom Encoder abrufen, um zu bestimmen, ob Frames gelöscht wurden. Weitere Informationen finden Sie unter [Abrufen von Codierungsstatistiken.](gettingencodingstatistics.md)

In der Regel verfügen qualitätsbasierte VBR-Streams nur über weniger Frames als die ursprünglichen, wenn doppelte Frames vorhanden sind (da die Bitrate nicht eingeschränkt ist).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 



