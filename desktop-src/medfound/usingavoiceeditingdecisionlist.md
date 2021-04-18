---
description: Verwenden einer Bearbeitungs Entscheidungs Liste zum Codieren von Stimme
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Verwenden einer Bearbeitungs Entscheidungs Liste zum Codieren von Stimme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343421"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a>Verwenden einer Bearbeitungs Entscheidungs Liste zum Codieren von Stimme

Bei einer Bearbeitungs Entscheidungs Liste (EDL) handelt es sich um Daten, die einem Codec übergeben werden und Informationen darüber bereitstellen, wie bestimmte Inhalts Teile codiert werden sollen. Der Windows Media Audio 9 Voice Codec unterstützt eine einfache EDL, in der Sie die Teile von Inhalten angeben können, die Musik enthalten. Standardmäßig erkennt der Codec bei der Konfiguration zum Codieren von gemischtem Inhalt selbst Durchgänge von Musik selbst. Sie sollten eine EDL nur dann verwenden, wenn der Codec die Inhaltstypen nicht ordnungsgemäß erkennt.

Um eine EDL zu verwenden, muss der sprach Encoder so festgelegt werden, dass gemischter Inhalt codiert wird. Konfigurieren Sie den Modus des voicecodec als "gemischt", indem Sie die Eigenschaft " [mfpkey \_ wmavoice \_ ENC \_ musicvoiceclassmode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) " auf "2" festlegen. Legen Sie die EDL mithilfe der Eigenschaft [mfpkey \_ wmavoice \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) fest. Der Wert dieser Eigenschaft ist eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste der Zeit Bereiche im Inhalt enthält, die als Musik codiert werden sollen. Das erste Element in der Liste ist die Version von EDL, die immer 1 ist. Das zweite Element ist die Anzahl der in der Liste beschriebenen Musik Abschnitte. Auf das zweite Element folgt eine Reihe von Werten, die dem zweiten Element entsprechen. Jedes Wertepaar beschreibt den Anfang und den Endpunkt einer Musik Passage im Inhalt in Millisekunden.

Beispielsweise gibt die EDL-Zeichenfolge "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" vier musikalische Passagen an, von denen jede eine Sekunde lang ist. Wenn die Informationen in der EDL-Zeichenfolge ungültig sind, wird Sie ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Windows Media Audio 9-Sprach Codecs](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Arbeiten mit Audiodaten](workingwithaudio.md)
</dt> </dl>

 

 



