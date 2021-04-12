---
title: Implementieren von imediaobject-"depjeestreamingresources"
description: Implementieren von imediaobject-"depjeestreamingresources"
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Windows Media Player-Plug-ins, Echo Sample Streaming Resources
- Plug-ins, Echo Sample Streaming-Ressourcen
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Streaming-Ressourcen
- DSP-Plug-ins, Echo Sample Streaming-Ressourcen
- Echo DSP-Plug-in-Beispiel, Streamingressourcen
- Echo DSP-Plug-in-Beispiel, Verzögerungs Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388438"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a>Implementieren von imediaobject:: Zuweisung

Im Echo-Beispiel erstellt die Methode " **depingestreamingresources** " den Verzögerungs Puffer. Dies geschieht wie folgt:

1.  Berechnen einer Größe für den Puffer, der der angegebenen Verzögerungszeit für den angegebenen Medientyp entspricht.
2.  Ordnen Sie entweder neuen Speicher zu, oder ordnen Sie die Puffergröße neu zu, wenn Sie bereits vorhanden ist.
3.  Aufrufen einer Methode, die den Puffer mit Werten füllt, die die Stille darstellen.

Der Wert für "Stille" ist abhängig von der Bittiefe unterschiedlich. Für 8-Bit-Audiodaten wird Stille durch den Hexadezimalwert 80 dargestellt. für 16-Bit-Audiodaten wird die Ruhe durch 0 (null) dargestellt.

## <a name="calculating-the-delay-buffer-size"></a>Berechnen der Verzögerungs Puffergröße

Um die für den Verzögerungs Puffer erforderliche Größe zu berechnen, müssen Sie zuerst eine **WaveFormatEx** -Struktur abrufen, die Informationen über die Audiodaten enthält. Im folgenden Beispiel wird ein Zeiger auf diese-Struktur aus der Eingabe- **DMO- \_ \_ Medientyp** Struktur abgerufen:


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



Nachdem Sie einen Zeiger auf die richtige **WaveFormatEx** -Struktur gespeichert haben, können Sie seine Member überprüfen und verwenden, um die erforderliche Puffergröße zu berechnen. Dies wird im folgenden Codebeispiel veranschaulicht:


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



Mit diesem Algorithmus wird die Puffergröße berechnet, indem die Verzögerungszeit (in Millisekunden) multipliziert mit der Anzahl von Samplings pro Millisekunde multipliziert wird. Anschließend wird das Ergebnis mit der Anzahl der Kanäle multipliziert und das Ergebnis dann mit der Anzahl der Bytes pro Stichprobe multipliziert. Die Anzahl der Kanäle und die Anzahl der Bytes pro Stichprobe sind nicht offensichtlich. Sie werden im nBlockAlign-Member codiert. Division durch 1000 reduziert den nsamplespersec-Wert auf Stichproben pro Millisekunde. die Millisekunde ist die gewünschte Einheit, da die Verzögerungszeit in Millisekunden angegeben wird.

## <a name="allocating-the-delay-buffer-memory"></a>Zuordnen des Verzögerungs Pufferspeichers

Nachdem Sie die Arbeitsspeicher Anforderungen berechnet haben, können Sie den Puffer zuordnen. Der Puffer muss möglicherweise gelöscht werden, wenn er vorhanden ist, z. b. wenn der Benutzer die Eigenschaften Seite aufruft, um den Wert für die Verzögerungszeit zu ändern. Der folgende Code veranschaulicht die Zuordnung des Verzögerungs Puffers:


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



Wenn der Puffer erfolgreich zugewiesen wurde, sollten Sie den verschiebbaren Zeiger auf den Anfang des Puffers verschieben, wie im folgenden Beispiel gezeigt:


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a>Auffüllen des Verzögerungs Puffers mit Ruhe

Es ist praktisch, eine Methode zu schreiben, um den Verzögerungs Puffer mit Werten zu füllen, die die Stille darstellen. Die Methode sollte den Zeiger auf die gültige WaveFormatEx-Struktur empfangen und dann den Member von wbitspersample überprüfen, um zu bestimmen, ob das Audioelement 8-Bit oder höher ist. Im folgenden Beispiel wird der Verzögerungs Puffer mit dem korrekten Wert für "Stille" gefüllt:


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



Denken Sie daran, die vorwärts Deklaration für die Funktion der Header Datei "Echo. h" im Abschnitt "private" hinzuzufügen:


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



Sie sollten Code am Ende von "zufügerestreamingresources" hinzufügen, um diese Methode jedes Mal aufzurufen, wenn der Verzögerungs Puffer erstellt oder seine Größe geändert wird. Der folgende Beispielcode übergibt den WaveFormatEx-Zeiger mit dem Namen pwave an die neue Methode:


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a>Neuzuordnen des Verzögerungs Pufferspeichers

Wenn der Benutzer die Verzögerungszeit mithilfe der Eigenschaften Seite ändert, muss auch die Größe des Verzögerungs Puffers geändert werden. Sie haben den Code zu alloingestreamingresources bereits hinzugefügt, um die Größe des Puffers zu ändern. Sie müssen jedoch eine Codezeile zu Cecho::p UT Delay hinzufügen, \_ um die Ressourcen Zuordnungs Methode bei jeder Änderung des Eigenschafts Werts aufzurufen. Hier folgt der Code:


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Streamingressourcen**](working-with-streaming-resources.md)
</dt> </dl>

 

 




