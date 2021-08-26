---
title: Erstellen des Echoeffekts
description: Erstellen des Echoeffekts
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Windows Media Player-Plug-Ins,Echo-Beispiel-DoProcessOutput-Methode
- Plug-Ins,Echo-Beispielmethode "DoProcessOutput"
- Plug-Ins für die digitale Signalverarbeitung,Echo-Beispielmethode "DoProcessOutput"
- DSP-Plug-Ins,Echo-Beispielmethode "DoProcessOutput"
- Echo DSP-Plug-In-Beispiel, DoProcessOutput-Methode
- Echo DSP-Plug-In-Beispiel, Erstellen eines Echoeffekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcb79b5be53f391854f38ce9aeba1c1bbff61ed2c0a982395c7063ff53146760
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902290"
---
# <a name="creating-the-echo-effect"></a>Erstellen des Echoeffekts

Sie müssen zuerst den Code aus dem Assistentenbeispiel entfernen, das die Audiodatei skaliert. Entfernen Sie aus dem 8-Bit-Abschnitt den folgenden Code:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



(Denken Sie daran, dass m \_ fScaleFactor durch m \_ dwDelayTime ersetzt wurde.)

Entfernen Sie aus dem 16-Bit-Abschnitt den folgenden Code:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



Die Implementierung von **DoProcessOutput,** die vom Beispielcode des Plug-In-Assistenten bereitgestellt wird, erstellt eine while-Schleife, die einmal für jedes Beispiel im Eingabepuffer iteriert, der von Windows Media Player. Diese Schleife funktioniert sowohl für 8-Bit- als auch für 16-Bit-Audio auf die gleiche Weise, obwohl jeweils eine separate Schleife erforderlich ist. In jedem Fall wird die Schleife mit dem folgenden Test initiiert:


```C++
while (dwSamplesToProcess--)

```



Sobald sie sich innerhalb der Schleife befinden, sind die Verarbeitungsroutinen für 8-Bit- und 16-Bit-Audio sehr ähnlich. Der Hauptunterschied besteht in dem Code im 8-Bit-Abschnitt, der den Bereich der Datenwerte in -128 bis 127 ändert und dann den Bereich wieder zurück konvertiert, bevor die Daten in den Ausgabepuffer geschrieben werden. Dies ist wichtig, um die Symmetrie der Audio-Wellenform während der Verarbeitung zu erhalten.

Nun können Sie damit beginnen, Code in der Verarbeitungsschleife hinzuzufügen und zu ersetzen.

## <a name="retrieve-a-sample-from-the-input-buffer"></a>Abrufen eines Beispiels aus dem Eingabepuffer

Bei jeder Iteration der Schleife wird ein einzelnes Beispiel aus dem Eingabepuffer abgerufen. Bei 8-Bit-Audiodaten wird das Beispiel in den neuen Bereich verschoben, und dann wird der Zeiger auf den Eingabepuffer auf das nächste Beispiel erweitert. Der folgende Code wurde aus dem Plug-In-Assistenten erstellt:


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



Bei 16-Bit-Audiodaten ist der Prozess mit Ausnahme der Normalisierung identisch:


```C++
// Get the input sample.
int i = *pwInputData++;

```



Denken Sie daran, dass die Zeiger im 16-Bit-Code in den Typ short konvertiert **wurden.**

## <a name="retrieve-a-sample-from-the-delay-buffer"></a>Abrufen eines Beispiels aus dem Verzögerungspuffer

Rufen Sie als Nächstes eine einzelne Stichprobe aus dem Verzögerungspuffer ab. Für 8-Bit-Code werden die Verzögerungsbeispiele im nativen Bereich von 0 bis 255 gespeichert. Der folgende Code, den Sie hinzufügen müssen, ruft ein 8-Bit-Verzögerungsbeispiel ab:


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



Bei 16-Bit-Audiodaten sieht der Prozess ähnlich aus:


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a>Schreiben des Eingabebeispiels in den Verzögerungspuffer

Nun müssen Sie das Eingabebeispiel im Verzögerungspuffer an der gleichen Position speichern, von der Sie das Verzögerungsbeispiel abgerufen haben. Der folgende Code muss für 8-Bit-Audio hinzugefügt werden:


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



Dies ist der Code, der für den 16-Bit-Abschnitt hinzugefügt werden soll:


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a>Verschieben des Verzögerungspufferzeigers

Nachdem die Arbeit im Verzögerungspuffer für diese Iteration abgeschlossen ist, können Sie den verschiebbaren Zeiger auf den Verzögerungspuffer bewegen. Wenn der Zeiger das Ende des zirkulären Puffers erreicht, müssen Sie seinen Wert ändern, um auf den Kopf des Puffers zu zeigen. Verwenden Sie den folgenden Code, um dies für 8-Bit-Audio zu tun:


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



Hier ist der Code für den 16-Bit-Abschnitt:


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



Da der Zeiger im 16-Bit-Abschnitt tatsächlich eine Kopie der Membervariablen ist, müssen Sie daran denken, den Wert in der Membervariablen mit der neuen Adresse zu aktualisieren. Wenn Sie dies nicht tun, wird der Verzögerungspufferzeiger wiederholt auf den Kopf des Puffers zeigen, und Ihr Echoeffekt funktioniert nicht wie erwartet. Fügen Sie dem 16-Bit-Abschnitt den folgenden Code hinzu:


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a>Kombinieren des Eingabebeispiels mit dem Verzögerungsbeispiel

Hier verwenden Sie die Vermischungswerte und die Dry Mix-Werte, um das endgültige Ausgabebeispiel zu erstellen. Sie multiplizieren einfach jede Stichprobe mit dem Gleitkommawert, der den Prozentsatz des letzten Signals für die Stichprobe darstellt. Multiplizieren Sie das Eingabebeispiel mit dem in m fDryMix gespeicherten Wert. Multiplizieren Sie die Verzögerungsstichprobe mit dem \_ in m \_ fWetMix gespeicherten Wert. Fügen Sie dann die beiden Werte hinzu. Der Code, den Sie hinzufügen müssen, ist für die 8-Bit- und 16-Bit-Abschnitte identisch:


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a>Schreiben der Daten in den Ausgabepuffer

Kopieren Sie abschließend das gemischte Beispiel in den Ausgabepuffer, und geben Sie dann den Ausgabepufferzeiger ein. Für 8-Bit-Audiodaten verwendet der Plug-In-Assistent den folgenden Code, um das Beispiel in den ursprünglichen Bereich zurück zu geben:


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



Für 16-Bit-Audio verwendet der Assistent den folgenden Code als letzten Schritt in der Verarbeitungsschleife:


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




