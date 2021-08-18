---
title: Implementieren von DoProcessOutput
description: Implementieren von DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Windows Media Player-Plug-Ins, Audio-DSP
- Plug-Ins, Audio-DSP
- Digitale Signalverarbeitungs-Plug-Ins, DoProcessOutput
- DSP-Plug-Ins, DoProcessOutput
- Audio-DSP-Plug-Ins, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2f5aa1a952f16de196bed72ed7ac93dfac95d8333496824e3f0740f506a6fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135583"
---
# <a name="implementing-doprocessoutput"></a>Implementieren von DoProcessOutput

Zum Verarbeiten von Audiodaten müssen Sie mehrere Schritte in **DoProcessOutput** ausführen. In den folgenden Schritten wird der Beispielcode des Plug-In-Assistenten als Beispiele verwendet. Wenn Sie ein Audio-DSP-Plug-In erstellen möchten, das Medieninhalte desselben Typs verarbeitet wie der Beispielcode des Plug-In-Assistenten, müssen Sie nur den tatsächlichen Verarbeitungscode ändern, auf den in Schritt 6 verwiesen wird. Im Folgenden sind alle Schritte beschrieben, die in **DoProcessOutput** implementiert sind:

-   Wenn das Plug-In derzeit nicht aktiviert ist, kopieren Sie einfach die Daten unverändert in den Ausgabepuffer. Wenn Ihr Plug-In die Daten in ein anderes Format konvertiert, müssen Sie hier auch die Konvertierungsverarbeitung durchführen.

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   Ruft einen Zeiger auf die Eingabeformatstruktur ab. Sie müssen Memberdaten aus dieser Struktur abrufen. Kopieren Sie daher den Zeiger von *m \_ mtInput*.**pbformat** auf eine lokale Zeigervariable eines Typs, der dem Formatstrukturtyp entspricht. Im folgenden Beispiel wird ein Zeiger auf eine **WAVEFORMATEX-Eingabeformatstruktur** gespeichert:

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   Berechnen Sie die Anzahl der zu verarbeitende Stichproben. Der Beispielcode, den der Plug-In-Assistent generiert, führt diesen Schritt aus, indem er die Anzahl der zu verarbeitenden Bytes durch den **nBlockAlign-Member** der WAVEFORMATEX-Eingabeformatstruktur dividiert und dann das Ergebnis mit der Anzahl der Kanäle multipliziert, die im **nChannels-Member** gespeichert wurden. Das folgende Beispiel stammt aus dem Beispielcode des Plug-In-Assistenten:

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  Bestimmen Sie die Bittiefe des Audios. Der Beispielcode des Plug-In-Assistenten bestimmt 8-Bit- oder 16-Bit-Audio, indem der **wBitsPerSample-Member** der **WAVEFORMATEX-Struktur** überprüft wird. Anschließend wird dieser Wert in einer switch-Anweisung verwendet, um separate Verarbeitungsroutinen für jede Bittiefe bereitzustellen. Möglicherweise müssen Sie eine andere Technik verwenden, wenn Sie mit anderen Formattypen und Bittiefe umgehen.
    2.  Erstellen Sie eine Schleife, um die Audiobeispiele im Eingabepuffer schrittweise zu durchlaufen.
    3.  Rufen Sie ein Beispiel aus dem Eingabepuffer ab. Hierzu dereferenzieren Sie den Eingabedatenzeiger und speichern das Ergebnis in einer Variablen vom Typ int. Für 16-Bit-Audio müssen Sie den BYTE-Zeiger in einen kurzen Zeiger umstellen, um die höhere Genauigkeit des Audiobeispiels zu verarbeiten. Sobald Sie über den Wert verfügen, können Sie den *pbInputData-Zeiger* sofort erhöhen, sodass er auf das nächste Beispiel zeigt. Dies wird in den folgenden Beispielen veranschaulicht:

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    Oder

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  Führen Sie die Verarbeitung aus. Hier wenden Sie die Algorithmen an, die das Beispiel ändern. Dies liegt an Ihnen.
    2.  Schreiben Sie die verarbeiteten Daten in den Ausgabepuffer. Erhöhen Sie den Zeiger sofort auf den Ausgabepuffer, wie im folgenden Beispiel:

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  Wiederholen Sie die Schleife, bis alle Stichproben verarbeitet wurden.
    2.  Gibt ein entsprechendes **HRESULT** zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Audio-DSP-Plug-Ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




