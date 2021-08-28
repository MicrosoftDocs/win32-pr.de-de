---
title: Implementieren von IMediaObject AllocateStreamingResources
description: Implementieren von IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Windows Media Player-Plug-Ins,Echo-Beispielstreamingressourcen
- Plug-Ins, Echo-Beispielstreamingressourcen
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispielstreamingressourcen
- DSP-Plug-Ins, Echo-Beispielstreamingressourcen
- Echo DSP-Plug-In-Beispiel,Streamingressourcen
- Echo DSP-Plug-In-Beispiel, Verzögerungspuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291b1f9627d9dfb78ae2aff9d34b6fadd47cbf28a5c2f0830f5833d9e83cde21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508960"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a>Implementieren von IMediaObject::AllocateStreamingResources

Im Echo-Beispiel erstellt die **AllocateStreamingResources-Methode** den Verzögerungspuffer. Dazu wird Folgendes verwendet:

1.  Berechnen einer Größe für den Puffer, die der angegebenen Verzögerungszeit für den angegebenen Medientyp entspricht.
2.  Entweder wird neuer Arbeitsspeicher zugewiesen, oder die Puffergröße wird neu zugewiesen, wenn sie bereits vorhanden ist.
3.  Aufrufen einer Methode, die den Puffer mit Werten füllt, die Stille darstellen.

Der Wert für die Stille ist abhängig von der Bittiefe unterschiedlich. Bei 8-Bit-Audio wird Stille durch den Hexadezimalwert 80 dargestellt. Bei 16-Bit-Audio wird Stille durch 0 (null) dargestellt.

## <a name="calculating-the-delay-buffer-size"></a>Berechnen der Verzögerungspuffergröße

Um die erforderliche Größe für den Verzögerungspuffer zu berechnen, müssen Sie zunächst eine **WAVEFORMATEX-Struktur** abrufen, die Informationen zu den Audiodaten enthält. Im folgenden Beispiel wird ein Zeiger auf diese Struktur aus der Eingabe DMO **\_ MEDIA \_ TYPE-Struktur** abgerufen:


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



Nachdem Sie einen Zeiger auf die richtige **WAVEFORMATEX-Struktur** gespeichert haben, können Sie deren Member überprüfen und sie verwenden, um die erforderliche Puffergröße zu berechnen. Im folgenden Codebeispiel wird dies veranschaulicht:


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



Dieser Algorithmus berechnet die Puffergröße, indem er die Verzögerungszeit in Millisekunden mit der Anzahl der Stichproben pro Millisekunde multipliziert, das Ergebnis dann mit der Anzahl der Kanäle multipliziert und dann das Ergebnis mit der Anzahl der Bytes pro Stichprobe multipliziert. Die Anzahl der Kanäle und die Anzahl der Bytes pro Stichprobe sind nicht offensichtlich. sie werden im nBlockAlign-Member codiert. Die Division durch 1000 reduziert den nSamplesPerSec-Wert auf Stichproben pro Millisekunde. Die Millisekunde ist die gewünschte Einheit, da die Verzögerungszeit in Millisekunden ausgedrückt wird.

## <a name="allocating-the-delay-buffer-memory"></a>Zuordnen des Verzögerungspufferspeichers

Nachdem Sie die Arbeitsspeicheranforderungen berechnet haben, können Sie den Puffer zuordnen. Der Puffer muss möglicherweise gelöscht werden, wenn er vorhanden ist, z. B. wenn der Benutzer die Eigenschaftenseite aufruft, um den Verzögerungszeitwert zu ändern. Der folgende Code veranschaulicht die Zuweisung des Verzögerungspuffers:


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



Wenn der Puffer erfolgreich zugeordnet wurde, sollten Sie den verschiebbaren Zeiger auf den Kopf des Puffers verschieben, wie im folgenden Beispiel gezeigt:


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a>Auffüllen des Verzögerungspuffers mit Stille

Es ist praktisch, eine Methode zu schreiben, um den Verzögerungspuffer mit Werten zu füllen, die Stille darstellen. Die -Methode sollte den Zeiger auf die gültige WAVEFORMATEX-Struktur empfangen und dann den wBitsPerSample-Member überprüfen, um zu ermitteln, ob die Audiodatei 8-Bit oder höher ist. Im folgenden Beispiel wird der Verzögerungspuffer mit dem richtigen Wert für Stille auffüllt:


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



Denken Sie daran, die Vorwärtsdeklaration für die Funktion der Headerdatei Echo.h im privaten Abschnitt hinzuzufügen:


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



Sie sollten Code am Ende von AllocateStreamingResources hinzufügen, um diese Methode jedes Mal auf aufruft, wenn der Verzögerungspuffer erstellt oder die Größe geändert wird. Der folgende Beispielcode übergibt den WAVEFORMATEX-Zeiger mit dem Namen pWave an die neue Methode:


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a>Neuverlegung des Verzögerungspufferspeichers

Wenn der Benutzer die Verzögerungszeit über die Eigenschaftenseite ändert, muss sich auch die Größe des Verzögerungspuffers ändern. Sie haben den Code bereits zu AllocateStreamingResources hinzugefügt, um die Größe des Puffers zu ändern. Sie müssen jedoch eine Codezeile zu CEcho::p ut delay hinzufügen, um die Ressourcenzuordnungsmethode bei jeder Änderung des Eigenschaftswerts auf \_ aufruft. Hier folgt der Code:


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Streamingressourcen**](working-with-streaming-resources.md)
</dt> </dl>

 

 




