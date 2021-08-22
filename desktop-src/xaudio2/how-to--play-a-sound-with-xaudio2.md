---
description: In diesem Thema werden die Mindestschritte beschrieben, die für die Wiedergabe zuvor geladener Audiodaten in XAudio2 erforderlich sind.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: "So wird's gemacht: Wiedergeben von Ton mit XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfa5cb2a7a47b7fb54e6a7e9f098a545b0c630c6c27889d7aa6eff1242121d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082909"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a>So wird's gemacht: Wiedergeben von Ton mit XAudio2

In diesem Thema werden die Mindestschritte beschrieben, die für die Wiedergabe zuvor geladener Audiodaten in XAudio2 erforderlich sind. Nachdem Sie XAudio2 initialisiert (siehe How [to: Initialize XAudio2](how-to--initialize-xaudio2.md)) und die Audiodaten geladen haben (siehe How to: [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), können Sie einen Sound wieder geben, indem Sie eine Quellstimme erstellen und Audiodaten an sie übergeben.

## <a name="to-play-a-sound"></a>So spielen Sie einen Sound wieder

1.  Initialisieren Sie die XAudio2-Engine, indem Sie die unter [How to: Initialize XAudio2 beschriebenen Schritte ausführen.](how-to--initialize-xaudio2.md)
2.  Füllen Sie [**eine WAVEFORMATEX-**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) und [**XAUDIO2 \_ BUFFER-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) auf, indem Sie die unter [How to: Load Audio Data Files in XAudio2 beschriebenen Schritte ausführen.](how-to--load-audio-data-files-in-xaudio2.md)
    > [!Note]  
    > Je nach Format der Audiodaten müssen Sie möglicherweise eine größere Datenstruktur verwenden, die eine [**WAVEFORMATEX-Struktur**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) statt **einer WAVEFORMATEX enthält.** Weitere Informationen finden Sie auf der Referenzseite zu **WAVEFORMATEX.**

     

3.  Erstellen Sie eine Quellstimme, indem Sie die [**IXAudio2::CreateSourceVoice-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) auf einer Instanz der XAudio2-Engine aufrufen. Das Format der Stimme wird durch die Werte angegeben, die in einer [**WAVEFORMATEX-Struktur festgelegt**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) sind.
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Übermitteln Sie mithilfe der Funktion [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer)einen [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) an die Quellstimme.
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > Die Audiobeispieldaten,  für die Pufferpunkte noch "im Besitz der App" sind, müssen zugeordnet und zugänglich bleiben, bis die Wiedergabe des Sounds beendet wird.

     

5.  Verwenden [](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) Sie die Start-Funktion, um die Quellstimme zu starten. Da alle XAudio2-Stimmen ihre Ausgabe standardmäßig an die Masterstimme senden, geht audio von der Quellstimme automatisch zu dem Audiogerät, das bei der Initialisierung ausgewählt wurde. In einem komplizierteren Audiographen müsste die Quellstimme die Stimme angeben, an die die Ausgabe gesendet werden soll.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Hinweise für Windows Store-Apps

Es wird empfohlen, einen [](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) intelligenten Zeiger zu verwenden, um die Lebensdauer von XAUDIO2-Objekten auf ausnahmesichere Weise zu verwalten. Für Windows Store-Apps können Sie die [**intelligente ComPtr-Zeigervorlage**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) aus der Windows Runtime C++-Vorlagenbibliothek (WRL) verwenden.


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
> Stellen Sie sicher, dass alle intelligenten Zeiger auf XAUDIO2-Objekte vollständig freigegeben werden, bevor Sie das [**IXAudio2-Objekt**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) veröffentlichen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2-Erste Schritte](getting-started.md)
</dt> <dt>

[So wird's gemacht: Initialisieren von XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[So wird's gemacht: Laden von Datendateien in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
