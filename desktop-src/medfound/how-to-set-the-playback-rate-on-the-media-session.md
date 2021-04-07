---
description: Festlegen der Wiedergabe Rate für die Medien Sitzung
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Festlegen der Wiedergabe Rate für die Medien Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761370"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a><span data-ttu-id="3de4c-103">Festlegen der Wiedergabe Rate für die Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="3de4c-103">How to Set the Playback Rate on the Media Session</span></span>

<span data-ttu-id="3de4c-104">Zum Implementieren von Wiedergabe Funktionen wie "schnelles vorwärts" und "Zurückspulen" müssen Anwendungen möglicherweise die Wiedergabe Rate für einen Mediendaten Strom ändern.</span><span class="sxs-lookup"><span data-stu-id="3de4c-104">To implement playback functionality such as fast forward and rewind, applications may need to change the playback rate for a media stream.</span></span> <span data-ttu-id="3de4c-105">Media Foundation stellt den Raten Steuerungs Dienst bereit, den die Anwendungen verwenden müssen, um die Wiedergabe Rate dynamisch festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3de4c-105">Media Foundation provides the rate control service that the applications must use to set the playback rate dynamically.</span></span>

<span data-ttu-id="3de4c-106">Vor dem Festlegen der Wiedergabe Rate sollte eine Anwendung überprüfen, ob die Rate von der Medienquelle unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3de4c-106">Before setting the playback rate, an application should check whether the rate is supported by the media source.</span></span> <span data-ttu-id="3de4c-107">Weitere Informationen zum Abfragen unterstützter Tarife finden Sie unter [bestimmen der unterstützten Tarife](how-to-determine-supported-rates.md).</span><span class="sxs-lookup"><span data-stu-id="3de4c-107">For information about querying for supported rates, see [How to Determine Supported Rates](how-to-determine-supported-rates.md).</span></span>

<span data-ttu-id="3de4c-108">Informationen zu den Wiedergabe Raten finden Sie unter Informationen [zur Raten Kontrolle](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="3de4c-108">For information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-set-the-playback-rate"></a><span data-ttu-id="3de4c-109">So legen Sie die Wiedergabe Rate fest</span><span class="sxs-lookup"><span data-stu-id="3de4c-109">To set the playback rate</span></span>

1.  <span data-ttu-id="3de4c-110">Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) zum Abrufen des Raten Steuerungs Objekts aus der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="3de4c-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the rate control object from the Media Session.</span></span>

    <span data-ttu-id="3de4c-111">Anwendungen, die " [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) " aufrufen, müssen Folgendes sicherstellen:</span><span class="sxs-lookup"><span data-stu-id="3de4c-111">Applications calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) must ensure the following:</span></span>

    -   <span data-ttu-id="3de4c-112">Der *punkObject* -Parameter enthält einen initialisierten [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3de4c-112">The *punkObject* parameter contains an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer.</span></span>
    -   <span data-ttu-id="3de4c-113">Das in den Parameter *ppvobject* empfangene Raten Steuerungsobjekt wird freigegeben, um Speicher Verluste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3de4c-113">The rate control object received in the *ppvObject* parameter is released to avoid memory leaks.</span></span>

2.  <span data-ttu-id="3de4c-114">Ruft die [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) -Methode auf, um die Wiedergabe Rate festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3de4c-114">Call the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method to set the playback rate.</span></span> <span data-ttu-id="3de4c-115">Nachdem **setRate** asynchron abgeschlossen wurde, empfängt die Anwendung das Ereignis [mesessionratechanged](mesessionratechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="3de4c-115">After **SetRate** completes asynchronously, the application receives the [MESessionRateChanged](mesessionratechanged.md) event.</span></span>

## <a name="example"></a><span data-ttu-id="3de4c-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3de4c-116">Example</span></span>

<span data-ttu-id="3de4c-117">Der folgende Code zeigt, wie die Wiedergabe Rate durch Aufrufen der [**setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) -Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3de4c-117">The following code shows how to set the playback rate by calling the [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



<span data-ttu-id="3de4c-118">Die Anwendung muss beendet oder angehalten werden, bevor Sie einen Übergang von einer negativen oder NULL-Rate zu einem positiven Satz durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="3de4c-118">The application must be stopped or paused before it can make a transition from a negative or zero rate to a positive rate.</span></span> <span data-ttu-id="3de4c-119">Weitere Informationen zu diesen Zuständen finden [Sie unter How to Control Presentation States](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="3de4c-119">For information about these states, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3de4c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3de4c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3de4c-121">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="3de4c-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="3de4c-122">Raten Steuerung</span><span class="sxs-lookup"><span data-stu-id="3de4c-122">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="3de4c-123">Suchen, schnelles vorwärts und umgekehrtes spielen</span><span class="sxs-lookup"><span data-stu-id="3de4c-123">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



