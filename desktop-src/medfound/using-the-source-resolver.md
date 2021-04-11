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
# <a name="using-the-source-resolver"></a>Verwenden des quellresolvers

Der Source Resolver nimmt einen URL oder Bytedatenstrom und erstellt die entsprechende Medienquelle für den Inhalt. Um den quellresolver zu erstellen, rufen Sie [**mfkreatesourceresolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)auf. Diese Funktion gibt einen [**IMF sourceresolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) -Schnittstellen Zeiger zurück.

Der Quell Konflikt Löser verfügt über synchrone und asynchrone Methoden. Wenn Sie den quellresolver aus dem Hauptanwendungs Thread verwenden, machen die asynchronen Methoden eine reaktionsfähigere Benutzeroberfläche. Die synchronen Methoden können für eine merkliche Zeitspanne blockieren, insbesondere dann, wenn der quellresolver eine Netzwerkressource öffnen muss.

Die synchronen Methoden lauten wie folgt:

-   [**IMF sourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [**IMF sourceresolver:: anforateobjectfromb testream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

Die asynchronen Methoden sind:

-   [**IMF sourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [**IMF sourceresolver:: beginkreateobjectfromb testream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

Für die asynchronen Methoden verfügt jede Methode über eine entsprechende **End...** -Methode, um die asynchrone Anforderung abzuschließen, und eine **Cancel...** -Methode, um eine ausstehende Anforderung abzubrechen. Weitere Informationen zu asynchronen Methoden in Media Foundation finden Sie unter [asynchrone Rückruf Methoden](asynchronous-callback-methods.md).

Im folgenden Codebeispiel wird eine Medienquelle aus einer URL erstellt. In diesem Beispiel wird die synchrone-Methode verwendet.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellresolver](source-resolver.md)
</dt> </dl>

 

 



