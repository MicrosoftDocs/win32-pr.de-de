---
description: Beschreibt Statistiken, die Sie aus einem Windows Mediencodec abrufen können.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Abrufen von Codierungsstatistiken (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa718a27894ea3e91faa953cb7b23e6c92b57c93d4b0fc0cf2c15b6995f28b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449160"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>Abrufen von Codierungsstatistiken (Microsoft Media Foundation)

Informationen dazu, was in einer Codierungssitzung geschieht, sind in der Regel sofort in Form von Fehlercodes verfügbar, die bei der Verarbeitung von Beispielen zurückgegeben werden. Es gibt jedoch einige Statistiken, die Sie aus dem Codec zu verschiedenen Codierungsaspekten abrufen können.

## <a name="video-frame-information"></a>Videoframeinformationen

Einige Videostatistiken, die Sie abrufen können, verarbeiten die Anzahl der vom Encoder verarbeiteten Frames. Es gibt drei Framenummerneigenschaften, die Sie aus dem Videoencoder lesen können:

-   [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) ist die Anzahl der Frames, die über den Eingabestream des DMO verarbeitet werden.
-   [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) ist die Anzahl der codierten Frames. Indem Sie diesen Wert von der Gesamtzahl der übergebenen Frames subtrahieren, können Sie bestimmen, wie viele Frames gelöscht wurden.
-   [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) ist die Anzahl der Frames, die nicht codiert sind, da sie bereits enthaltenen Inhalt dupliziert haben. Dieser Wert wird nicht von der Anzahl der codierten Frames subtrahiert, die vom DMO gemeldet werden.

Sie können videoframe-Eigenschaften jederzeit während der Codierung lesen. Dies kann nützlich sein, um zu bestimmen, ob die Codierungseinstellungen für Ihren Inhalt geeignet sind. Wenn es einen großen Unterschied zwischen Gesamtframes und codierten Frames gibt, erfüllt der komprimierte Inhalt möglicherweise nicht Ihre Qualitätsanforderungen. Sie können die endgültigen Werte lesen, nachdem Sie die Codierung abgeschlossen haben.

## <a name="vbr-buffer-statistics"></a>VBR-Pufferstatistik

Abhängig vom verwendeten Codierungsmodus können einige oder alle Puffereinstellungen während der Codierung bestimmt werden (z. B. ist die bitrate der qualitätsbasierten VBR erst bekannt, wenn der Inhalt codiert wurde). Es gibt vier VBR-Puffereigenschaften, die Sie mit der **IPropertyBag::Read-Methode** abrufen können:

-   [MFPKEY \_ DIE durchschnittliche](mfpkey-ravgproperty.md) Bitrate des VBR-Inhalts.
-   [MFPKEY \_ BAVG](mfpkey-bavgproperty.md) ist das Pufferfenster für die durchschnittliche Bitrate.
-   [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) ist die Spitzenbitrate des VBR-Inhalts.
-   [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) ist das Spitzenpufferfenster.

Nachdem Sie mit der Verarbeitung von Beispielen begonnen haben, sollten Sie keine der VBR-Eigenschaften lesen, bis Sie die Codierung des Streams abgeschlossen haben. Wenn Sie dies tun, interpretiert der Encoder Ihre Anforderung als Signal, dass die Codierung abgeschlossen ist. Das nächste Beispiel, das Sie verarbeiten, wird als neue Codierungssitzung behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 



