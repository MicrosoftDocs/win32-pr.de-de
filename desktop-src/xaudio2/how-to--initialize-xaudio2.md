---
description: XAudio2 wird für die Audiowiedergabe initialisiert, indem eine Instanz der XAudio2-Engine und eine Masterstimme erstellt werden.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: "So wird's gemacht: Initialisieren von XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb55425c92e6d28a2689fb388869bbf42339d14bec3550e3f9e17798c1af68f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962729"
---
# <a name="how-to-initialize-xaudio2"></a>So wird's gemacht: Initialisieren von XAudio2

XAudio2 wird für die Audiowiedergabe initialisiert, indem eine Instanz der XAudio2-Engine und eine Masterstimme erstellt werden.

**So initialisieren Sie XAudio2**

1.  Stellen Sie sicher, dass Sie COM initialisiert haben. Für eine Windows Store-App erfolgt dies im Rahmen der Initialisierung der Windows Runtime. Verwenden Sie andernfalls [**CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  Verwenden Sie [**die XAudio2Create-Funktion,**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) um eine Instanz der XAudio2-Engine zu erstellen.

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Verwenden Sie [**die CreateMasteringVoice-Methode,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) um eine Masterstimme zu erstellen.

    Die Masterstimmen kapseln ein Audiogerät. Es ist das endgültige Ziel für alle Audiodaten, die einen Audiographen durchläuft.

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Hinweise für Windows Store-Apps

Es wird empfohlen, einen [](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) intelligenten Zeiger zu verwenden, um die Lebensdauer von XAUDIO2-Objekten auf ausnahmesichere Weise zu verwalten. Für Windows Store-Apps können Sie die [**Intelligente ComPtr-Zeigervorlage**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) aus der C++-Vorlagenbibliothek (WRL Windows Runtime) verwenden.


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> Stellen Sie sicher, dass alle untergeordneten XAUDIO2-Objekte vollständig freigegeben werden, bevor Sie das [**IXAudio2-Objekt**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) veröffentlichen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2-Erste Schritte](getting-started.md)
</dt> <dt>

[So wird's gemacht: Laden von Datendateien in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[So wird's gemacht: Wiedergeben von Ton mit XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
