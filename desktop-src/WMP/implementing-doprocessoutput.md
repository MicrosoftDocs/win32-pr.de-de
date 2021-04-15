---
title: Implementieren von DoProcess Output
description: Implementieren von DoProcess Output
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, DoProcess Output
- DSP-Plug-ins, DoProcess Output
- audiodsp-Plug-ins, DoProcess Output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388418"
---
# <a name="implementing-doprocessoutput"></a>Implementieren von DoProcess Output

Um Audiodaten zu verarbeiten, müssen Sie in " **DoProcess Output**" mehrere Schritte ausführen. In den folgenden Schritten wird der Beispielcode des Plug-in-Assistenten als Beispiele verwendet. Wenn Sie ein audiodsp-Plug-in erstellen möchten, das Medieninhalte desselben Typs verarbeitet, den der Plug-in-Assistent für den Beispielcode verwendet, müssen Sie nur den eigentlichen Verarbeitungs Code ändern, auf den in Schritt 6 verwiesen wird. Im folgenden werden alle in " **DoProcess Output**" implementierten Schritte aufgeführt:

-   Wenn das Plug-in derzeit nicht aktiviert ist, kopieren Sie die Daten einfach unverändert in den Ausgabepuffer. Wenn das Plug-in die Daten in ein anderes Format konvertiert, müssen Sie die Konvertierungs Verarbeitung auch hier durchführen.

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   Rufen Sie einen Zeiger auf die Eingabe Formatstruktur ab. Sie müssen Elementdaten aus dieser Struktur abrufen, also kopieren Sie den Zeiger von *m \_ mtinput*.**pbformat** in eine lokale Zeiger Variable eines Typs, der mit dem Format Strukturtyp übereinstimmt. Im folgenden Beispiel wird ein Zeiger auf eine **WaveFormatEx** -Eingabe Formatstruktur gespeichert:

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   Berechnen Sie die Anzahl der zu verarbeitenden Stichproben. Der Beispielcode, den der Plug-in-Assistent generiert, führt diesen Schritt aus, indem die Anzahl der zu verarbeitenden Bytes durch das **nBlockAlign** -Element der Struktur des WaveFormatEx-Eingabe Formats dividiert und das Ergebnis dann mit der Anzahl der Kanäle multipliziert wird, die im **nchannels** -Member gespeichert wurden. Das folgende Beispiel zeigt den Beispielcode des Plug-in-Assistenten:

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  Legen Sie die Bittiefe der Audiodatei fest. Der Beispielcode des Plug-in-Assistenten bestimmt eine 8-Bit-oder 16-Bit-Audiodatei, indem der **wbitspersample** -Member der **WaveFormatEx** -Struktur überprüft wird. Anschließend wird dieser Wert in einer Switch-Anweisung verwendet, um separate Verarbeitungs Routinen für jede Bittiefe bereitzustellen. Möglicherweise müssen Sie eine andere Methode verwenden, wenn Sie mit anderen Format Typen und Bittiefen arbeiten.
    2.  Erstellen Sie eine-Schleife, um die Audiobeispiele im Eingabepuffer schrittweise zu durchlaufen.
    3.  Rufen Sie ein Beispiel aus dem Eingabepuffer ab. Dazu Dereferenzieren Sie den Eingabedaten Zeiger und speichern das Ergebnis in einer Variablen vom Typ "int". Für 16-Bit-Audiodaten müssen Sie den Byte Zeiger auf einen kurzen Zeiger umgestalten, um die höhere audiostichproben Genauigkeit zu verarbeiten. Sobald Sie über den Wert verfügen, können Sie den *pbinputdata* -Zeiger sofort erhöhen, sodass er auf das nächste Beispiel zeigt. Dies wird in den folgenden Beispielen veranschaulicht:

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

    

    1.  Führen Sie die Verarbeitung aus. An dieser Stelle wenden Sie die Algorithmen an, die das Beispiel irgendwie ändern. Was Sie hier tun, ist Ihnen überlassen.
    2.  Schreiben Sie die verarbeiteten Daten in den Ausgabepuffer. Erhöhen Sie den Zeiger direkt auf den Ausgabepuffer, wie im folgenden Beispiel gezeigt:

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  Wiederholen Sie die Schleife, bis alle Beispiele verarbeitet wurden.
    2.  Gibt ein entsprechendes **HRESULT** zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines audiodsp-Plug-ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




