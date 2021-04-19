---
description: 'Es gibt drei Arten von XAudio2 Voice-Objekten: Quelle, teilmischung und Mastering Stimmen.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: XAudio2-Stimmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364227"
---
# <a name="xaudio2-voices"></a>XAudio2-Stimmen

Es gibt drei Arten von XAudio2 Voice-Objekten: *Quelle*, *teilmischung* und *Mastering* Stimmen. Quellstimmen verarbeiten die vom Client bereitgestellten Audiodaten. Quell- und Submixstimmen senden ihre Ausgabe an mindestens eine Submix- oder Masterstimme. Submix- und Masterstimmen mischen die Audiodaten aller Stimmen, von denen sie Daten erhalten, und verarbeiten das Ergebnis. Masterstimmen schreiben Audiodaten auf ein Audiogerät.

## <a name="actions-performed-by-all-voices"></a>Von allen Stimmen ausgeführte Aktionen

Alle Stimmen führen die folgenden Aktionen für die Audiodatei aus, die Sie übertragen.

1.  Gesamte volumeanpassung, die sich auf alle Audiokanäle auswirkt. Weitere Informationen finden Sie unter [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).
2.  Eine optionale, vom Client angegebene Kette von einem oder mehreren DSP-Effekten, z. b. der integrierte oder der von der [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -Schnittstelle definierte Benutzer Effekt. Siehe [XAudio2-Audioeffekte](xaudio2-audio-effects.md).
3.  Anpassung des pro-Kanal-Ausgabe Volumens. Weitere Informationen finden Sie unter [**IXAudio2Voice:: setchannelvolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).
4.  Trennen Sie die Matrix Mischung mit den einzelnen Ziel Stimmen oder dem Audioausgabegerät für das beherrschen von Stimmen. Diese Mischung ändert die Anzahl der Kanäle im Audioformat, falls erforderlich.

## <a name="source-voices"></a>Quellen Stimmen

Verwenden Sie Quell Stimmen, um Audiodaten an die XAudio2-Verarbeitungs Pipeline zu senden. Sie sind die Einstiegspunkte in das [XAudio2-audiodiagramm](xaudio2-audio-graph.md). Sie müssen Sprach Daten an eine Mastering-Stimme senden, damit Sie entweder direkt oder über zwischenteilmix-Stimmen gehört.

Zusätzlich zu den Aktionen, die von allen Stimmen durchgeführt werden, führen Quell Stimmen die folgenden Aktionen aus.

-   Bei Bedarf wird ein Decoder zuerst ausgeführt, um codierte Quelldaten in Pulse Code Modulation (PCM) zu konvertieren.
-   Eine Stichprobenrate Konvertierung (src) für Variablen Raten konvertiert die Quell Audiodaten der Stimme in die von den Ziel Stimmen erwartete Samplingrate, falls erforderlich, und unterstützt auch dynamische Änderungen.
-   Ein optionaler Zustandsvariablen Filter kann verwendet werden, um den Sound auf verschiedene Weise zu färben. Weitere Informationen finden Sie unter [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Ein optionaler Filter kann auf die Ausgaben der Stimme angewendet werden. Weitere Informationen finden Sie unter [**IXAudio2Voice:: setoutputfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="submix-voices"></a>Teilmengen von Stimmen

Eine teilmix-Stimme wird hauptsächlich für Leistungsverbesserungen und Auswirkungen der Verarbeitung verwendet. Sie können keine Datenpuffer direkt an submischungs Stimmen senden. Es ist nicht hörbar, es sei denn, Sie senden es an eine Mastering Voice. Sie können eine unter Mischungs Stimme verwenden, um sicherzustellen, dass ein bestimmter Satz von Sprach Daten in das gleiche Format konvertiert wird und eine bestimmte Wirkungskette für das Ergebnis des gemeinsamen Ergebnisses verarbeitet wird.

Zusätzlich zu den Aktionen, die von allen Stimmen ausgeführt werden, führen teilmischungs Stimmen die folgenden Aktionen aus.

-   Ein src mit fester Rate wird bei Bedarf in der Ausgabe der Stimme ausgeführt, um die Audiodaten in die von den Ziel Stimmen erwartete Stichprobenrate zu konvertieren.
-   Ein optionaler Zustandsvariablen Filter kann verwendet werden, um den Sound auf verschiedene Weise zu färben. Weitere Informationen finden Sie unter [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   Ein optionaler Filter kann auf die Ausgaben der Stimme angewendet werden. Weitere Informationen finden Sie unter [**IXAudio2Voice:: setoutputfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="mastering-voices"></a>Meistern von Stimmen

Verwenden Sie eine Mastering Voice, um das Audioausgabegerät darzustellen. Datenpuffer können nicht direkt an die Mastering-Stimmen übermittelt werden, aber Daten, die an andere Arten von Stimmen übermittelt werden, müssen zu einer zu hörenden Stimme gelangen.

Zusätzlich zu den Aktionen, die von allen Stimmen ausgeführt werden, führen Mastering-Stimmen die folgenden Aktionen aus.

-   Wenn Sie die Mastering Voice mit einem expliziten *inputsamplerate* -Wert erstellen, der vom Audiogerät nicht unterstützt wird, wird ein src mit fester Rate verwendet, um die nächstgelegene, vom Gerät unterstützte Stichprobenrate zu konvertieren.
-   Schneiden Sie die endgültige Ausgabe Audiodatei ab, wenn Sie vom Ausgabegerät benötigt wird.

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

 

 
