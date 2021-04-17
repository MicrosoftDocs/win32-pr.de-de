---
description: In diesem Thema werden die Schritte beschrieben, die für die Wiedergabe zuvor geladener Audiodaten in XAudio2 erforderlich sind.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: "So wird's gemacht: Wiedergeben von Ton mit XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526882"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a>So wird's gemacht: Wiedergeben von Ton mit XAudio2

In diesem Thema werden die Schritte beschrieben, die für die Wiedergabe zuvor geladener Audiodaten in XAudio2 erforderlich sind. Nach dem Initialisieren von XAudio2 (siehe Gewusst [wie: Initialisieren von XAudio2](how-to--initialize-xaudio2.md)) und Laden der Audiodaten (siehe Gewusst wie: Gewusst [wie: Laden von audiodatendateien in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)) können Sie einen Sound wiedergeben, indem Sie eine Quell Stimme erstellen und Audiodaten an diese übergeben.

## <a name="to-play-a-sound"></a>So spielen Sie einen Sound wieder

1.  Initialisieren Sie die XAudio2-Engine, indem Sie die unter Gewusst [wie: Initialisieren von XAudio2](how-to--initialize-xaudio2.md)beschriebenen Schritte befolgen.
2.  Füllen Sie eine [**WaveFormatEx**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) -und [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aus, indem Sie die Schritte befolgen, die unter Gewusst [wie: Laden von audiodatendateien in XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md)beschrieben sind.
    > [!Note]  
    > Abhängig vom Format der Audiodaten müssen Sie möglicherweise eine größere Datenstruktur verwenden, die eine [**WaveFormatEx**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) -Struktur anstelle eines **WaveFormatEx**-Struktur enthält. Weitere Informationen finden Sie auf der Referenzseite zu **WaveFormatEx** .

     

3.  Erstellen Sie eine Quell Stimme, indem Sie die [**IXAudio2:: createsourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) -Methode für eine Instanz der XAudio2-Engine aufrufen. Das Format der Stimme wird durch die Werte angegeben, die in einer [**WaveFormatEx**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) -Struktur festgelegt sind.
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Senden Sie mithilfe der Funktion " [**submitsourcebuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer)" einen [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) an die Quell Stimme.
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > Die audiobeispieldaten, an die *Puffer* Punkte immer noch im Besitz von der APP sind und die zugewiesen und zugänglich bleiben müssen, bis der Sound angehalten wird.

     

5.  Verwenden Sie die [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) -Funktion, um die Quell Stimme zu starten. Da alle XAudio2 stimmen ihre Ausgabe standardmäßig an die Mastering-Stimme senden, wird das Audiogerät, das bei der Initialisierung ausgewählt wird, automatisch von Audiodaten aus der Quellsprache entfernt. In einem komplizierteren audiodiagramm müsste die Quell Stimme die Stimme angeben, an die die Ausgabe gesendet werden soll.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Hinweise für Windows Store-Apps

Es wird empfohlen, einen [intelligenten Zeiger](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) zu verwenden, um die Lebensdauer von XAUDIO2-Objekten auf sichere Weise zu verwalten. Für Windows Store-Apps können Sie die Vorlage " [**comptr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) -intelligenter Zeiger" aus der Windows-Runtime C++ Template Library (WRL) verwenden.


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> Stellen Sie sicher, dass alle intelligenten Zeiger auf XAUDIO2 Objekte vollständig freigegeben werden, bevor Sie das [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) -Objekt freigeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2](getting-started.md)
</dt> <dt>

[So wird's gemacht: Initialisieren von XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[So wird's gemacht: Laden von Datendateien in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
