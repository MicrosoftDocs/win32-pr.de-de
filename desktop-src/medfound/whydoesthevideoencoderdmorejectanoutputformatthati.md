---
description: Warum lehnt der Videoencoder ein Ausgabeformat ab, das ich festlegen möchte, wenn ich das Format aus demselben Objekt abgerufen habe?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Warum lehnt der Videoencoder ein Ausgabeformat ab, das ich festlegen möchte, wenn ich das Format aus demselben Objekt abgerufen habe?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2e744285140df13a9aa251983ab801033c481d1452029c955ee3a39235fcea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112890"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a>Warum lehnt der Videoencoder ein Ausgabeformat ab, das ich festlegen möchte, wenn ich das Format aus demselben Objekt abgerufen habe?

Im Gegensatz zu Audioencoder-Ausgabetypen sind die unterstützten Ausgaben, die von den Videoencodern aufzählt werden, nicht vollständig wie übermittelt. Sie müssen die Bitrate des Streams im **dwBitrate-Member** der **VIDEOINFOHEADER-Struktur** so festlegen, dass sie mit dem wert übereinstimmt, der für die [MFPKEY-EIGENSCHAFT \_ VOMG](mfpkey-ravgproperty.md) festgelegt wurde.

Nachdem alle Optionen wie gewünscht festgelegt wurden, müssen Sie die privaten Codecdaten abrufen und an die **VIDEOINFOHEADER-Struktur** anfügen. Weitere Informationen finden Sie unter [Verwenden privater Videocodec-Daten.](usingvideocodecprivatedata.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Häufig gestellte Fragen](frequentlyaskedquestions.md)
</dt> </dl>

 

 



