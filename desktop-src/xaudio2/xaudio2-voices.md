---
description: 'Es gibt drei Arten von XAudio2-Stimmobjekten: Quell-, Submix- und Masteringstimmen.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: XAudio2-Stimmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b756033be5b64dbf03e3b3756902014774a53c9aebc8f41a1df1f982685cca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025938"
---
# <a name="xaudio2-voices"></a>XAudio2-Stimmen

Es gibt drei Arten von XAudio2-Stimmobjekten: *Quell-,* *Submix-* und *Masteringstimmen.* Quellstimmen verarbeiten die vom Client bereitgestellten Audiodaten. Quell- und Submixstimmen senden ihre Ausgabe an mindestens eine Submix- oder Masterstimme. Submix- und Masterstimmen mischen die Audiodaten aller Stimmen, von denen sie Daten erhalten, und verarbeiten das Ergebnis. Masterstimmen schreiben Audiodaten auf ein Audiogerät.

## <a name="actions-performed-by-all-voices"></a>Von allen Stimmen ausgeführte Aktionen

Alle Stimmen führen die folgenden Aktionen in der Reihenfolge der Audiodaten aus, die sie durchziehen.

1.  Allgemeine Volumeanpassung, die sich auf alle Audiokanäle auswirkt. Siehe [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).
2.  Eine optionale vom Client angegebene Kette von einem oder mehreren DSP-Effekten, z. B. dem integrierten Hall oder einem benutzerdefinierten Effekt, der von der [**IXAPO-Schnittstelle**](/windows/desktop/api/XAPO/nn-xapo-ixapo) definiert wird. Weitere Informationen finden Sie unter [XAudio2-Audioeffekte.](xaudio2-audio-effects.md)
3.  Anpassung des Ausgabevolumes pro Kanal. Siehe [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).
4.  Trennen Sie die Matrixmischung mit jeder der Zielstimmen oder mit dem Audioausgabegerät, um Stimmen zu mastern. Diese Mischung ändert bei Bedarf die Anzahl der Kanäle in der Audiodatei.

## <a name="source-voices"></a>Quellstimmen

Verwenden Sie Quellstimmen, um Audiodaten an die XAudio2-Verarbeitungspipeline zu übermitteln. Sie sind die Einstiegspunkte in [XAudio2 Audio Graph](xaudio2-audio-graph.md). Sie müssen Sprachdaten an eine Masterstimme senden, um gehört zu werden, entweder direkt oder über zwischengeschaltete Submixstimmen.

Zusätzlich zu den Aktionen, die von allen Stimmen ausgeführt werden, führen Quellstimmen die folgenden Aktionen aus.

-   Bei Bedarf wird zuerst ein Decoder ausgeführt, um codierte Quelldaten in Pulse Code Pulse (PCM) zu konvertieren.
-   Eine Konvertierung der Abtastrate mit variabler Rate (Variable Rate Sample Rate Conversion, SRC) konvertiert die Quellaudiodaten der Stimme ggf. in die von den Zielstimmen erwartete Abtastrate und unterstützt auch dynamische Tonhöhenänderungen.
-   Ein optionaler Zustandsvariablenfilter kann verwendet werden, um den Sound auf verschiedene Weise zu farblich zu gestalten. Siehe [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Ein optionaler Filter kann auf die Ausgaben der Stimme angewendet werden. Siehe [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="submix-voices"></a>Submix-Stimmen

Eine Submixstimme wird hauptsächlich für Leistungsverbesserungen und Effekte verwendet. Datenpuffer können nicht direkt an Submix-Stimmen übermittelt werden. Sie ist nur hörbar, wenn Sie sie an eine Masteringstimme übermitteln. Sie können eine Submix-Stimme verwenden, um sicherzustellen, dass ein bestimmter Satz von Stimmendaten in das gleiche Format konvertiert wird und eine bestimmte Effektkette für das gesamte Ergebnis verarbeitet wird.

Zusätzlich zu den Aktionen, die von allen Stimmen ausgeführt werden, führen Submix-Stimmen die folgenden Aktionen aus.

-   Ein SRC mit festem Prozentsatz wird bei Bedarf für die Ausgabe der Stimme ausgeführt, um die Audiodaten in die von den Zielstimmen erwartete Abtastrate zu konvertieren.
-   Ein optionaler Zustandsvariablenfilter kann verwendet werden, um den Sound auf verschiedene Weise zu farblich zu gestalten. Siehe [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Ein optionaler Filter kann auf die Ausgaben der Stimme angewendet werden. Siehe [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="mastering-voices"></a>Mastering Voices

Verwenden Sie eine Masteringstimme, um das Audioausgabegerät darzustellen. Sie können Datenpuffer nicht direkt an mastering-Stimmen übermitteln, aber Daten, die an andere Arten von Stimmen übermittelt werden, müssen an eine Masterstimme gesendet werden, um gehört zu werden.

Zusätzlich zu den Aktionen, die von allen Stimmen ausgeführt werden, führen mastering-Stimmen die folgenden Aktionen aus.

-   Wenn Sie die Masteringstimme mit einem expliziten *InputSampleRate-Wert* erstellen, der vom Audiogerät nicht unterstützt wird, wird ein SRC mit festem Prozentsatz verwendet, um in die nächste abtastrate zu konvertieren, die vom Gerät unterstützt wird.
-   Beschneiden Sie die endgültige Ausgabeaudiodatei, wenn sie vom Ausgabegerät benötigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stimmen](voices.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
