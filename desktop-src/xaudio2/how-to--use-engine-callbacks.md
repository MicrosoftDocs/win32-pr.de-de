---
description: Sie können den XAudio2-Clientcode über Engine-Ereignisse benachrichtigen, indem Sie eine Instanz einer Klasse registrieren, die die IXAudio2EngineCallback-Schnittstelle mit der XAudio2-Engine implementiert.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: "So wird's gemacht: Verwenden der Modulrückrufe"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc51e673be6972c1c5ba012c12f616e1bfe78a345081fee683aba83b6944c17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054370"
---
# <a name="how-to-use-engine-callbacks"></a>So wird's gemacht: Verwenden der Modulrückrufe

Sie können den XAudio2-Clientcode über Engine-Ereignisse benachrichtigen, indem Sie eine Instanz einer Klasse registrieren, die die [**IXAudio2EngineCallback-Schnittstelle**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) mit der XAudio2-Engine implementiert. Dadurch kann der XAudio2-Clientcode nachverfolgen, wann die Audioverarbeitung erfolgt und wann die Engine bei einem kritischen Fehler neu gestartet werden muss.

## <a name="to-use-an-engine-callback"></a>So verwenden Sie einen Engine-Rückruf

Mit den folgenden Schritten wird ein -Objekt registriert, um Engine-Ereignisse zu behandeln.

1.  Erstellen Sie eine Klasse, die von der [**IXAudio2EngineCallback-Schnittstelle**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) erbt.

    Alle Methoden von [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) sind rein virtuell und müssen definiert werden. Die für dieses Beispiel wichtige Methode ist [**IXAudio2EngineCallback::OnCriticalError,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror)die ein Flag zum Signalisieren der Hauptspielschleife anordnt, dass ein kritischer Fehler aufgetreten ist. Die verbleibenden Methoden [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) und [**IXAudio2EngineCallback::OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend)sind Stubs in diesem Beispiel.

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  Verwenden [**Sie XAudio2Create,**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) um eine Instanz der XAudio2-Engine zu erstellen.

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Verwenden [**Sie IXAudio2::RegisterForCallbacks,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) um den Engine-Rückruf zu registrieren.

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  Wenn Sie den Engine-Rückruf nicht mehr benötigen, rufen Sie [**IXAudio2::UnregisterForCallbacks auf.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks)

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

 

 
