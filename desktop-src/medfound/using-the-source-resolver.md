---
description: Verwenden des quellresolvers
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Verwenden des quellresolvers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215407"
---
# <a name="using-the-source-resolver"></a><span data-ttu-id="f6eed-103">Verwenden des quellresolvers</span><span class="sxs-lookup"><span data-stu-id="f6eed-103">Using the Source Resolver</span></span>

<span data-ttu-id="f6eed-104">Der Source Resolver nimmt einen URL oder Bytedatenstrom und erstellt die entsprechende Medienquelle für den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f6eed-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="f6eed-105">Um den quellresolver zu erstellen, rufen Sie [**mfkreatesourceresolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)auf.</span><span class="sxs-lookup"><span data-stu-id="f6eed-105">To create the source resolver, call [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span></span> <span data-ttu-id="f6eed-106">Diese Funktion gibt einen [**IMF sourceresolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="f6eed-106">This function returns an [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface pointer.</span></span>

<span data-ttu-id="f6eed-107">Der Quell Konflikt Löser verfügt über synchrone und asynchrone Methoden.</span><span class="sxs-lookup"><span data-stu-id="f6eed-107">The source resolver has both synchronous and asynchronous methods.</span></span> <span data-ttu-id="f6eed-108">Wenn Sie den quellresolver aus dem Hauptanwendungs Thread verwenden, machen die asynchronen Methoden eine reaktionsfähigere Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f6eed-108">If you are using the source resolver from your main application thread, the asynchronous methods will make your user interface more responsive.</span></span> <span data-ttu-id="f6eed-109">Die synchronen Methoden können für eine merkliche Zeitspanne blockieren, insbesondere dann, wenn der quellresolver eine Netzwerkressource öffnen muss.</span><span class="sxs-lookup"><span data-stu-id="f6eed-109">The synchronous methods can block for a noticeable amount of time, particularly if the source resolver must open a network resource.</span></span>

<span data-ttu-id="f6eed-110">Die synchronen Methoden lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f6eed-110">The synchronous methods are:</span></span>

-   [<span data-ttu-id="f6eed-111">**IMF sourceresolver:: forateobjectfromurl**</span><span class="sxs-lookup"><span data-stu-id="f6eed-111">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [<span data-ttu-id="f6eed-112">**IMF sourceresolver:: anforateobjectfromb testream**</span><span class="sxs-lookup"><span data-stu-id="f6eed-112">**IMFSourceResolver::CreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

<span data-ttu-id="f6eed-113">Die asynchronen Methoden sind:</span><span class="sxs-lookup"><span data-stu-id="f6eed-113">The asynchronous methods are:</span></span>

-   [<span data-ttu-id="f6eed-114">**IMF sourceresolver:: beginkreateobjectfromurl**</span><span class="sxs-lookup"><span data-stu-id="f6eed-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [<span data-ttu-id="f6eed-115">**IMF sourceresolver:: beginkreateobjectfromb testream**</span><span class="sxs-lookup"><span data-stu-id="f6eed-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

<span data-ttu-id="f6eed-116">Für die asynchronen Methoden verfügt jede Methode über eine entsprechende **End...** -Methode, um die asynchrone Anforderung abzuschließen, und eine **Cancel...** -Methode, um eine ausstehende Anforderung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="f6eed-116">For the asynchronous methods, each method has a corresponding **End...** method to complete the asynchronous request, and a **Cancel...** method to cancel a pending request.</span></span> <span data-ttu-id="f6eed-117">Weitere Informationen zu asynchronen Methoden in Media Foundation finden Sie unter [asynchrone Rückruf Methoden](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f6eed-117">For more information about asynchronous methods in Media Foundation, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="f6eed-118">Im folgenden Codebeispiel wird eine Medienquelle aus einer URL erstellt.</span><span class="sxs-lookup"><span data-stu-id="f6eed-118">The following code example creates a media source from a URL.</span></span> <span data-ttu-id="f6eed-119">In diesem Beispiel wird die synchrone-Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6eed-119">This example uses the synchronous method.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f6eed-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6eed-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6eed-121">Quellresolver</span><span class="sxs-lookup"><span data-stu-id="f6eed-121">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



