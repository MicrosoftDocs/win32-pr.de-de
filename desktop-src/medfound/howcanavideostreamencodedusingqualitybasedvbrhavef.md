---
description: Wie kann ein Videostream, der mit einem Qualitäts basierten VBR codiert ist, weniger Frames aufweisen als der ursprüngliche Stream?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: Wie kann ein Videostream, der mit einem Qualitäts basierten VBR codiert ist, weniger Frames aufweisen als der ursprüngliche Stream?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215573"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a>Wie kann ein Videostream, der mit einem Qualitäts basierten VBR codiert ist, weniger Frames aufweisen als der ursprüngliche Stream?

Die Frame-Anzahl eines codierten Streams kann aus zwei Gründen niedriger sein als die Frame Anzahl der ursprünglichen: doppelte Frames und gelöschte Frames.

Der Encoder erzeugt normalerweise keine Frames, die exakte Duplikate des vorherigen Frames sind. Wenn Sie ein Beispiel für jeden Frame benötigen (Dies ist z. b. für einige Container erforderlich), können Sie den Encoder so konfigurieren, dass "Dummy"-Frames erzeugt werden, indem Sie die Eigenschaft " [mfpkey \_ producedummyframes](mfpkey-producedummyframesproperty.md) " auf "Variant true" festlegen \_ .

Der Encoder löscht Frames, wenn er nicht alle Frames codieren kann, ohne den Puffer zu überlaufen. Verworfene Frames beeinflussen die Qualität des Streams, doppelte Frames nicht.

Sie können eine Frame-Statistik aus dem Encoder erhalten, um zu bestimmen, ob Frames gelöscht wurden. Weitere Informationen finden Sie unter [erhalten von Codierungs Statistiken](gettingencodingstatistics.md).

In der Regel verfügen Qualitäts basierte VBR-Streams nur über weniger Frames als das ursprüngliche, wenn es doppelte Frames gibt (da die Bitrate nicht eingeschränkt ist).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 



