---
description: Programmgesteuertes Laden einer GraphEdit-Datei
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: Programmgesteuertes Laden einer GraphEdit-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf2bdff86a47e740e6cb177a70a7b1e12ffc7c865d8ad231f6ada9122f286d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153178"
---
# <a name="loading-a-graphedit-file-programmatically"></a>Programmgesteuertes Laden einer GraphEdit-Datei

Eine Anwendung kann die **IPersistStream-Schnittstelle** verwenden, um eine GraphEdit-Datei (.grf) zu laden. Verwenden Sie den folgenden Code:


```C++
HRESULT LoadGraphFile(IGraphBuilder *pGraph, const WCHAR* wszName)
{
    IStorage *pStorage = 0;
    if (S_OK != StgIsStorageFile(wszName))
    {
        return E_FAIL;
    }
    HRESULT hr = StgOpenStorage(wszName, 0, 
        STGM_TRANSACTED | STGM_READ | STGM_SHARE_DENY_WRITE, 
        0, 0, &pStorage);
    if (FAILED(hr))
    {
        return hr;
    }
    IPersistStream *pPersistStream = 0;
    hr = pGraph->QueryInterface(IID_IPersistStream,
             reinterpret_cast<void**>(&pPersistStream));
    if (SUCCEEDED(hr))
    {
        IStream *pStream = 0;
        hr = pStorage->OpenStream(L"ActiveMovieGraph", 0, 
            STGM_READ | STGM_SHARE_EXCLUSIVE, 0, &pStream);
        if(SUCCEEDED(hr))
        {
            hr = pPersistStream->Load(pStream);
            pStream->Release();
        }
        pPersistStream->Release();
    }
    pStorage->Release();
    return hr;
}

```



> [!Note]  
> Der Aufruf von **IPersistStream::Load** im vorherigen Codebeispiel kann einen DirectShow-Fehler- oder Erfolgscode zurückgeben. Eine Liste der möglichen Rückgabewerte finden Sie unter [Fehler- und Erfolgscodes.](error-and-success-codes.md)

 

GraphEdit-Dateien sind nur zum Testen und Debuggen vorgesehen. Sie sind nicht für die Verwendung durch Endbenutzeranwendungen vorgesehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Simulieren Graph Erstellen mit GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[**StgIsStorageFile**](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[**StgOpenStorage**](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
