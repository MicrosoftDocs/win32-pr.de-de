---
description: Verwenden des Windows Media Audio Voice Codec
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Verwenden des Windows Media Audio Voice Codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e53c84a6915b8bc118015f1524e5126085e7ac199cc4726c88739b0a82738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972669"
---
# <a name="using-the-windows-media-audio-voice-codec"></a>Verwenden des Windows Media Audio Voice Codec

Der Windows Media Audio Voice-Codec bietet eine niedrige Bitratenkomprimierung, die für Audio mit Sprache optimiert ist. Die Fähigkeit des Codecs, so kleine Stichproben zu erzeugen, ist auf den begrenzten Frequenzbereich der Töne der menschlichen Stimme zurückzuführen. Diese Optimierung bedeutet, dass ein dedizierter Sprachencoder eine ausgabeschwache Ausgabe für Inhalte erstellt, die kompliziertere Sounds wie Musik enthalten. Der Windows Media Audio Voice-Codec kompensiert dieses potenzielle Qualitätsproblem jedoch, indem er separate Modi für Stimme, Musik und gemischten Inhalt bereitstellt. Der Codec analysiert gemischten Inhalt, um zu bestimmen, welcher Modus für jeden Teil der Datei verwendet werden soll.

Der Windows Media Audio Voice-Codec wird im Encoderobjekt implementiert, das durch den Klassenbezeichner CLSID \_ CWMSPEncMediaObject2 identifiziert wird, und im Decoderobjekt, das durch den Klassenbezeichner CLSID \_ CWMSPDecMediaObject identifiziert wird. Das Formattag von Medientypen, die diesen Codec verwenden, ist 0x00A.

## <a name="configuring-the-encoder"></a>Konfigurieren des Encoders

Der Sprachencoder unterstützt drei Modi: Sprache, Musik und Gemischt. Jeder Modus ist optimiert, um die besten Ergebnisse für diesen Inhaltstyp zu erhalten. Sie können den Modus des Sprachencoders konfigurieren, indem Sie die Methoden von **IPropertyStore** verwenden, um die [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode-Eigenschaft](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) festzulegen.

Bei Konfiguration für gemischte Inhalte erkennt der Windows Media Audio Voice-Codec automatisch Musikabschnitte im Inhalt. Wenn Sie mit den Ergebnissen nicht zufrieden sind, können Sie den Speicherort der Musik im Inhalt mithilfe einer Bearbeitungsentscheidungsliste (Editing Decision List, EDL) angeben. Weitere Informationen finden Sie unter [Using an Editing Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).

Im Gegensatz zu den anderen Audioencodern können Sie den Pufferfensterwert für Sprachinhalte mithilfe der [MFPKEY \_ WMAVOICE \_ ENC \_ BufferWindow-Eigenschaft](mfpkey-wmavoice-enc-bufferwindowproperty.md) festlegen. Die Standardwerte sollten jedoch in den meisten Fällen einwandfrei funktionieren.

> [!Note]  
>    Beim Konfigurieren des Sprachencoders ist es sehr wichtig, dass Sie den Ausgabetyp festlegen, bevor Sie den Eingabetyp festlegen. Dies ist die empfohlene Reihenfolge der Vorgänge für alle Audiocodecs, aber der Sprachencoder kann fehlerhafte Ausgabetypen melden, wenn eine Eingabe festgelegt wird, wenn Sie **IMediaObject::GetOutputType** oder **EINENTRANSFORM::GetOutputType** aufrufen.

 

## <a name="decoding"></a>Decodierung

Es gibt keine besonderen Anforderungen für die Decodierung von Sprachaudiodaten. Weitere Informationen finden Sie unter [Konfigurieren der Audiodecodierung.](configuringaudiodecoding.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Audio](workingwithaudio.md)
</dt> </dl>

 

 



