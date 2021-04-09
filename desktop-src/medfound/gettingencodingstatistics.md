---
description: Beschreibt Statistiken, die Sie aus einem Windows Media-Codec abrufen können.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Erhalten von Codierungs Statistiken (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749217"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>Erhalten von Codierungs Statistiken (Microsoft Media Foundation)

Informationen dazu, was in einer Codierungs Sitzung geschieht, sind in der Regel sofort in Form von Fehlercodes verfügbar, die beim Verarbeiten von Beispielen zurückgegeben werden. Es gibt jedoch einige Statistiken, die Sie aus dem Codec über verschiedene Codierungs Aspekte abrufen können.

## <a name="video-frame-information"></a>Video Frame Informationen

Einige Video Statistiken, die Sie abrufen können, sind mit der Anzahl der vom Encoder verarbeiteten Frames zu beschäftigen. Es gibt drei Eigenschaften von Frame Nummern, die Sie aus dem Video Encoder lesen können:

-   [Mfpkey \_ Total Frames](mfpkey-totalframesproperty.md) ist die Anzahl der Frames, die über den Eingabestream des DMO verarbeitet werden.
-   [Mfpkey \_ Codedframes](mfpkey-codedframesproperty.md) ist die Anzahl der codierten Frames. Wenn Sie diesen Wert von der Gesamtzahl der übergebenen Frames subtrahieren, können Sie bestimmen, wie viele Frames gelöscht wurden.
-   [Mfpkey \_ Zerobyteframes](mfpkey-zerobyteframesproperty.md) ist die Anzahl der Frames, die nicht codiert werden, da Sie bereits enthaltene Inhalte duplizieren. Dieser Wert wird nicht von der Anzahl der vom DMO gemeldeten codierten Frames subtrahiert.

Sie können während der Codierung jederzeit Video Frame Eigenschaften lesen. Dies kann hilfreich sein, um zu bestimmen, ob die Codierungs Einstellungen für Ihre Inhalte geeignet sind. Wenn ein großer Unterschied zwischen den Gesamtrahmen und den codierten Frames besteht, entsprechen die komprimierten Inhalte möglicherweise nicht Ihren Qualitätsanforderungen. Sie können die endgültigen Werte lesen, nachdem Sie die Codierung abgeschlossen haben.

## <a name="vbr-buffer-statistics"></a>VBR-Puffer Statistik

Abhängig vom verwendeten Codierungs Modus können einige oder alle Puffer Einstellungen während der Codierung bestimmt werden (z. b. ist die Bitrate von Quality-basiertem VBR erst bekannt, wenn der Inhalt codiert ist). Es gibt vier VBR-Puffer Eigenschaften, die Sie mithilfe der **IPropertyBag:: Read** -Methode erhalten können:

-   [Mfpkey \_ Ravg](mfpkey-ravgproperty.md) ist die durchschnittliche Bitrate des VBR-Inhalts.
-   [Mfpkey \_ Bavg](mfpkey-bavgproperty.md) ist das Puffer Fenster für die durchschnittliche Bitrate.
-   [Mfpkey \_ Rmax](mfpkey-rmaxproperty.md) ist die Spitzen Bitrate der VBR-Inhalte.
-   [Mfpkey \_ Bmax](mfpkey-bmaxproperty.md) ist das Hauptpuffer Fenster.

Nachdem Sie mit der Verarbeitung von Beispielen begonnen haben, sollten Sie die VBR-Eigenschaften erst lesen, wenn Sie mit dem Codieren des Streams fertig sind. Wenn Sie dies tun, interpretiert der Encoder Ihre Anforderung als Signal, dass die Codierung fertiggestellt ist. Das nächste Beispiel, das Sie verarbeiten, wird als neue Codierungs Sitzung behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 



