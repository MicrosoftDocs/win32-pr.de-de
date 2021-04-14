---
description: Sie können den XAudio2-Client Code von Engine-Ereignissen Benachrichtigen, indem Sie eine Instanz einer Klasse registrieren, die die IXAudio2EngineCallback-Schnittstelle mit der XAudio2-Engine implementiert.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: "So wird's gemacht: Verwenden der Modulrückrufe"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adec0efd0625157740488d70be7896688d1176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393745"
---
# <a name="how-to-use-engine-callbacks"></a>So wird's gemacht: Verwenden der Modulrückrufe

Sie können den XAudio2-Client Code von Engine-Ereignissen Benachrichtigen, indem Sie eine Instanz einer Klasse registrieren, die die [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) -Schnittstelle mit der XAudio2-Engine implementiert. Dies ermöglicht es dem XAudio2-Client Code, zu verfolgen, wann die Audioverarbeitung stattfindet und wann die Engine im Fall eines schwerwiegenden Fehlers neu gestartet werden soll.

## <a name="to-use-an-engine-callback"></a>So verwenden Sie einen Engine-Rückruf

Mit den folgenden Schritten wird ein Objekt registriert, um Engine-Ereignisse zu verarbeiten.

1.  Erstellen Sie eine Klasse, die von der [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) -Schnittstelle erbt.

    Alle Methoden von [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) sind rein virtuell und müssen definiert werden. Die relevante Methode in diesem Beispiel ist [**IXAudio2EngineCallback:: oncriticalerror**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), mit der ein Flag festgelegt wird, mit dem die Hauptspiel Schleife signalisiert wird, dass ein kritischer Fehler aufgetreten ist. Die restlichen Methoden, [**IXAudio2EngineCallback:: onprocessingpassstart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) und [**IXAudio2EngineCallback:: onprocessingpassend**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), sind in diesem Beispiel Stubs.

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  Verwenden Sie [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) , um eine Instanz der XAudio2-Engine zu erstellen.

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Verwenden Sie [**IXAudio2:: registerforcallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) , um den Engine-Rückruf zu registrieren.

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  Wenn Sie den Engine-Rückruf nicht mehr benötigen, rufen Sie [**IXAudio2:: unregisterforcallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks)auf.

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückrufe](callbacks.md)
</dt> <dt>

[XAudio2-Rückrufe](xaudio2-callbacks.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[So wird's gemacht: Streamen von Sound von einem Datenträger](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
