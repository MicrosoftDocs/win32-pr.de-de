---
description: XAudio2 wird für die Audiowiedergabe initialisiert, indem eine Instanz der XAudio2-Engine erstellt und eine Mastering-Stimme erstellt wird.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: "So wird's gemacht: Initialisieren von XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a613c1ae2b7c3a7f0c55ab5349a0a605aaeb2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862951"
---
# <a name="how-to-initialize-xaudio2"></a>So wird's gemacht: Initialisieren von XAudio2

XAudio2 wird für die Audiowiedergabe initialisiert, indem eine Instanz der XAudio2-Engine erstellt und eine Mastering-Stimme erstellt wird.

**So initialisieren Sie XAudio2**

1.  Stellen Sie sicher, dass Sie com initialisiert haben. Für eine Windows Store-App erfolgt dies im Rahmen der Initialisierung der Windows-Runtime. Andernfalls verwenden Sie [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  Verwenden Sie die [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) -Funktion, um eine Instanz der XAudio2-Engine zu erstellen.

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Verwenden Sie die Methode " [**kreatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) ", um eine Stimme zu erstellen.

    Die Mastering-Stimmen Kapseln ein Audiogerät. Es ist das ultimative Ziel für alle Audiodaten, die über ein audiodiagramm geleitet werden.

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Hinweise für Windows Store-Apps

Es wird empfohlen, einen [intelligenten Zeiger](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) zu verwenden, um die Lebensdauer von XAUDIO2-Objekten auf sichere Weise zu verwalten. Für Windows Store-Apps können Sie die Vorlage " [**comptr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) -intelligenter Zeiger" aus der Windows-Runtime C++ Template Library (WRL) verwenden.


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
> Stellen Sie sicher, dass alle untergeordneten XAUDIO2-Objekte vollständig freigegeben werden, bevor Sie das [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) -Objekt

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2](getting-started.md)
</dt> <dt>

[So wird's gemacht: Laden von Datendateien in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[So wird's gemacht: Wiedergeben von Ton mit XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
