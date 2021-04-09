---
title: Erstellen des Echo Effekts
description: Erstellen des Echo Effekts
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Windows Media Player-Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample DoProcess Output-Methode
- DSP-Plug-ins, Echo Sample DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, DoProcess Output-Methode
- Plug-in-Beispiel für ECHO DSP, Erstellen eines ECHO Effekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036400"
---
# <a name="creating-the-echo-effect"></a>Erstellen des Echo Effekts

Sie müssen zunächst den Code aus dem Assistenten Beispiel entfernen, der die Audiodatei skaliert. Entfernen Sie den folgenden Code aus dem 8-Bit-Abschnitt:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



(Denken Sie daran, dass m "m" \_ durch m \_ dwdelta-Time ersetzt wurde.)

Entfernen Sie den folgenden Code aus dem 16-Bit-Abschnitt:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



Die im Beispielcode des Plug-in-Assistenten bereitgestellte Implementierung von " **DoProcess Output** " erstellt eine while-Schleife, die ein Mal für jedes Beispiel im von Windows Media Player bereitgestellten Eingabepuffer iteriert. Diese Schleife funktioniert auf die gleiche Weise für 8-Bit-und 16-Bit-Audiodaten, obwohl jeweils eine separate Schleife erforderlich ist. In jedem Fall wird die Schleife mit folgendem Test initiiert:


```C++
while (dwSamplesToProcess--)

```



In der Schleife sind die Verarbeitungs Routinen für 8-Bit-und 16-Bit-Audiodaten sehr ähnlich. Der Hauptunterschied besteht darin, dass der Code im 8-Bit-Abschnitt den Bereich der Datenwerte in-128 bis 127 ändert und dann den Bereich wieder zurück konvertiert, bevor die Daten in den Ausgabepuffer geschrieben werden. Dies ist wichtig, um die Symmetrie des Audiowellen Formulars während der Verarbeitung beizubehalten.

Nun können Sie beginnen, Code in der Verarbeitungs Schleife hinzuzufügen und zu ersetzen.

## <a name="retrieve-a-sample-from-the-input-buffer"></a>Abrufen eines Beispiels aus dem Eingabepuffer

Während jeder Iterationen der Schleife wird eine einzelne Stichprobe aus dem Eingabepuffer abgerufen. Für 8-Bit-Audiodaten wird das Beispiel in den neuen Bereich verschoben, und der Zeiger auf den Eingabepuffer wird auf das nächste Beispiel erweitert. Der folgende Code wird vom Plug-in-Assistenten angezeigt:


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



Bei einem 16-Bit-audiovorgang ist der Prozess mit Ausnahme der Normalisierung identisch:


```C++
// Get the input sample.
int i = *pwInputData++;

```



Beachten Sie, dass die Zeiger im 16-Bit-Code in den Typ **Short** konvertiert wurden.

## <a name="retrieve-a-sample-from-the-delay-buffer"></a>Abrufen eines Beispiels aus dem Verzögerungs Puffer

Rufen Sie als nächstes eine einzelne Stichprobe aus dem verzögerten Puffer ab. Für 8-Bit-Code werden die Verzögerungs Proben in ihrem nativen Bereich von 0 bis 255 gespeichert. Der folgende Code, den Sie hinzufügen müssen, Ruft ein 8-Bit-Verzögerungs Beispiel ab:


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



Bei einem 16-Bit-audiovorgang ist der Prozess ähnlich:


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a>Eingabe Beispiel in den Verzögerungs Puffer schreiben

Nun müssen Sie das Eingabe Beispiel im Verzögerungs Puffer an dem Speicherort speichern, von dem aus Sie das Verzögerungs Beispiel abgerufen haben. Im folgenden finden Sie den Code, den Sie für 8-Bit-Audiodaten hinzufügen müssen:


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



Dies ist der Code, der für den 16-Bit-Abschnitt hinzugefügt werden soll:


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a>Verschieben des Verzögerungs Puffer Zeigers

Nachdem die Arbeit im Verzögerungs Puffer für diese Iterationen abgeschlossen ist, können Sie den verschiebbaren Zeiger auf den Verzögerungs Puffer verschieben. Wenn der Zeiger das Ende des Kreis Puffers erreicht, müssen Sie seinen Wert ändern, um auf den Anfang des Puffers zu zeigen. Um dies für 8-Bit-Audiodaten zu erreichen, verwenden Sie den folgenden Code:


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



Dies ist der Code für den 16-Bit-Abschnitt:


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



Da der Zeiger im 16-Bit-Abschnitt wirklich eine Kopie der Element Variablen ist, müssen Sie daran denken, den Wert in der Element Variablen mit der neuen Adresse zu aktualisieren. Wenn Sie dies nicht tun, zeigt der Verzögerungs Puffer Zeiger wiederholt auf den Anfang des Puffers, und Ihr Echo Effekt funktioniert nicht erwartungsgemäß. Fügen Sie dem 16-Bit-Abschnitt den folgenden Code hinzu:


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a>Mischen der Eingabe Stichprobe mit dem Delay-Beispiel

Hier verwenden Sie die Werte für "nass Mischung" und "Dry Mix", um das abschließende Ausgabe Beispiel zu erstellen. Sie multiplizieren einfach jede Stichprobe mit dem Gleit Komma Wert, der den Prozentsatz des endgültigen Signals für das Beispiel darstellt. Multiplizieren Sie die Eingabe Stichprobe mit dem Wert, der in m-Datei- \_ Mischungs Mischung gespeichert ist, Multiplizieren Sie das Verzögerungs Beispiel mit dem in m "m" \_ . Fügen Sie dann die beiden Werte hinzu. Der Code, den Sie hinzufügen müssen, ist für die 8-Bit-und 16-Bit-Abschnitte identisch:


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a>Schreiben der Daten in den Ausgabepuffer

Kopieren Sie schließlich das gemischte Beispiel in den Ausgabepuffer, und fahren Sie dann mit dem Ausgabepuffer Zeiger fort. Für 8-Bit-Audiodaten verwendet der Plug-in-Assistent den folgenden Code, um das Beispiel in seinen ursprünglichen Bereich zurückzusetzen:


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



Für 16-Bit-Audiodaten verwendet der Assistent den folgenden Code als letzten Schritt in der Verarbeitungs Schleife:


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Cecho::D oprocess Output**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




