---
description: Verwenden des Windows Media Audio Voice-Codecs
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Verwenden des Windows Media Audio Voice-Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530467"
---
# <a name="using-the-windows-media-audio-voice-codec"></a>Verwenden des Windows Media Audio Voice-Codecs

Der Windows Media Audio Voice-Codec bietet eine niedrige Bitrate-Komprimierung, die für Audioinhalte optimiert ist. Die Fähigkeit des Codecs, solche kleinen Stichproben zu liefern, ist auf den begrenzten Frequenzbereich der Klänge der menschlichen Stimme zurückzuführen. Diese Optimierung bedeutet, dass ein dedizierter sprach Encoder eine Ausgabe mit schlechter Qualität für Inhalte erstellt, die kompliziertere Sounds wie Musik enthalten. Der Windows Media Audio Voice-Codec kompensiert jedoch dieses potenzielle Qualitätsproblem, indem es separate Modi für sprach-, Musik-und gemischte Inhalte bereitstellt. Der Codec analysiert gemischte Inhalte, um zu bestimmen, welcher Modus für die einzelnen Teile der Datei verwendet werden soll.

Der Windows Media Audio Voice-Codec wird in das durch den Klassen Bezeichner CLSID CWMSPEncMediaObject2 identifizierte Codierungs Objekt implementiert \_ , und im Decoderobjekt, das durch den Klassen Bezeichner CLSID \_ cwmspdecmediaobject identifiziert wird. Das Formattag von Medientypen, die diesen Codec verwenden, ist 0x00a.

## <a name="configuring-the-encoder"></a>Konfigurieren des Encoders

Der sprach Encoder unterstützt drei Modi: Sprache, Musik und gemischt. Jeder Modus ist so optimiert, dass die besten Ergebnisse für diesen Inhaltstyp erzielt werden. Sie können den Modus des Voice-Encoders konfigurieren, indem Sie die Methoden von **IPropertyStore** verwenden, um die Eigenschaft " [mfpkey \_ wmavoice \_ ENC \_ musicvoiceclassmode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) " festzulegen.

Wenn der Windows Media Audio Voice-Codec für gemischte Inhalte konfiguriert ist, erkennt er automatisch die im Inhalt vorhandenen Musikpassagen. Wenn Sie mit den Ergebnissen nicht zufrieden sind, können Sie den Speicherort der Musik im Inhalt mithilfe einer Bearbeitungs Entscheidungs Liste ("EDL") angeben. Weitere Informationen finden Sie unter [using an Bearbeitung Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).

Im Gegensatz zu den anderen audioencodern können Sie den Wert für das Puffer Fenster für sprach Inhalt mithilfe der Eigenschaft [mfpkey \_ wmavoice \_ ENC \_ bufferwindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) festlegen. Die Standardwerte sollten jedoch in den meisten Fällen einwandfrei funktionieren.

> [!Note]  
>    Beim Konfigurieren des sprach Encoders ist es sehr wichtig, dass Sie den Ausgabetyp festlegen, bevor Sie den Eingabetyp festlegen. Dies ist die empfohlene Reihenfolge von Vorgängen für alle Audiocodecs, aber der sprach Encoder kann fehlerhafte Ausgabetypen melden, wenn eine Eingabe festgelegt wird, wenn Sie **imediaobject:: getoutputtype** oder **imftransform:: getoutputtype** aufrufen.

 

## <a name="decoding"></a>Decodierung

Es gibt keine besonderen Anforderungen für das Decodieren von sprach Audiodaten. Weitere Informationen finden Sie unter [Konfigurieren der Audiodecodierung](configuringaudiodecoding.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Audiodaten](workingwithaudio.md)
</dt> </dl>

 

 



