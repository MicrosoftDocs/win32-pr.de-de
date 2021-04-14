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
# <a name="how-to-use-engine-callbacks"></a><span data-ttu-id="baa45-103">So wird's gemacht: Verwenden der Modulrückrufe</span><span class="sxs-lookup"><span data-stu-id="baa45-103">How to: Use Engine Callbacks</span></span>

<span data-ttu-id="baa45-104">Sie können den XAudio2-Client Code von Engine-Ereignissen Benachrichtigen, indem Sie eine Instanz einer Klasse registrieren, die die [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) -Schnittstelle mit der XAudio2-Engine implementiert.</span><span class="sxs-lookup"><span data-stu-id="baa45-104">You can notify the XAudio2 client code of engine events by registering an instance of a class implementing the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface with the XAudio2 engine.</span></span> <span data-ttu-id="baa45-105">Dies ermöglicht es dem XAudio2-Client Code, zu verfolgen, wann die Audioverarbeitung stattfindet und wann die Engine im Fall eines schwerwiegenden Fehlers neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="baa45-105">This allows the XAudio2 client code to keep track of when audio processing is occurring, and when to restart the engine in the event of a critical error.</span></span>

## <a name="to-use-an-engine-callback"></a><span data-ttu-id="baa45-106">So verwenden Sie einen Engine-Rückruf</span><span class="sxs-lookup"><span data-stu-id="baa45-106">To use an engine callback</span></span>

<span data-ttu-id="baa45-107">Mit den folgenden Schritten wird ein Objekt registriert, um Engine-Ereignisse zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="baa45-107">The following steps register an object to handle engine events.</span></span>

1.  <span data-ttu-id="baa45-108">Erstellen Sie eine Klasse, die von der [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="baa45-108">Create a class that inherits from the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface.</span></span>

    <span data-ttu-id="baa45-109">Alle Methoden von [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) sind rein virtuell und müssen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="baa45-109">All methods of [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) are purely virtual and must be defined.</span></span> <span data-ttu-id="baa45-110">Die relevante Methode in diesem Beispiel ist [**IXAudio2EngineCallback:: oncriticalerror**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), mit der ein Flag festgelegt wird, mit dem die Hauptspiel Schleife signalisiert wird, dass ein kritischer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="baa45-110">The method of interest in this example is [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), which sets a flag to signal the main game loop that a critical error has occurred.</span></span> <span data-ttu-id="baa45-111">Die restlichen Methoden, [**IXAudio2EngineCallback:: onprocessingpassstart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) und [**IXAudio2EngineCallback:: onprocessingpassend**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), sind in diesem Beispiel Stubs.</span><span class="sxs-lookup"><span data-stu-id="baa45-111">The remaining methods, [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) and [**IXAudio2EngineCallback::OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), are stubs in this example.</span></span>

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  <span data-ttu-id="baa45-112">Verwenden Sie [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) , um eine Instanz der XAudio2-Engine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="baa45-112">Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) to create an instance of the XAudio2 engine.</span></span>

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="baa45-113">Verwenden Sie [**IXAudio2:: registerforcallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) , um den Engine-Rückruf zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="baa45-113">Use [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) to register the engine callback.</span></span>

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  <span data-ttu-id="baa45-114">Wenn Sie den Engine-Rückruf nicht mehr benötigen, rufen Sie [**IXAudio2:: unregisterforcallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks)auf.</span><span class="sxs-lookup"><span data-stu-id="baa45-114">If you don't need the engine callback any more, call [**IXAudio2::UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span></span>

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="baa45-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="baa45-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baa45-116">Rückrufe</span><span class="sxs-lookup"><span data-stu-id="baa45-116">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="baa45-117">XAudio2-Rückrufe</span><span class="sxs-lookup"><span data-stu-id="baa45-117">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="baa45-118">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="baa45-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="baa45-119">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="baa45-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="baa45-120">So wird's gemacht: Streamen von Sound von einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="baa45-120">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
