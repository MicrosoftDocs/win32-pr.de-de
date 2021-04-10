---
description: Warum lehnt der Video Encoder ein Ausgabeformat ab, das ich festgelegt habe, wenn ich das Format aus demselben Objekt abgerufen habe?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Warum lehnt der Video Encoder ein Ausgabeformat ab, das ich festgelegt habe, wenn ich das Format aus demselben Objekt abgerufen habe?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042037"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a>Warum lehnt der Video Encoder ein Ausgabeformat ab, das ich festgelegt habe, wenn ich das Format aus demselben Objekt abgerufen habe?

Im Unterschied zu audioencoderausgabetypen werden die von den Video Encodern aufgelisteten unterstützten Ausgaben nicht als zugestellt vervollständigt. Sie müssen die Bitrate des Streams im **dwbitrate** -Member der **videoinfoheader** -Struktur auf den Wert festlegen, der für die Eigenschaft " [mfpkey \_ Ravg](mfpkey-ravgproperty.md) " festgelegt wurde.

Nachdem alle Optionen auf die gewünschte Weise festgelegt wurden, müssen Sie die privaten Codec-Daten abrufen und Sie an die **videoinfoheader** -Struktur anfügen. Weitere Informationen finden Sie unter [Verwenden von privaten Videocodec-Daten](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 



