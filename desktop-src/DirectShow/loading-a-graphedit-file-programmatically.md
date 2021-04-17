---
description: Programm gesteuertes Laden einer GraphEdit-Datei
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: Programm gesteuertes Laden einer GraphEdit-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a4780ead7b65d883bdd48917c6372425612435
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481747"
---
# <a name="loading-a-graphedit-file-programmatically"></a>Programm gesteuertes Laden einer GraphEdit-Datei

Eine Anwendung kann die **IPersistStream** -Schnittstelle verwenden, um eine GraphEdit-Datei (. GRF) zu laden. Verwenden Sie den folgenden Code:


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
> Der Aufrufe von **IPersistStream:: Load** im vorherigen Codebeispiel kann einen DirectShow-Fehler oder einen Erfolgs Code zurückgeben. Eine Liste möglicher Rückgabewerte finden Sie unter [Fehler-und Erfolgs Codes](error-and-success-codes.md).

 

GraphEdit-Dateien dienen nur zum Testen und Debuggen. Sie sind nicht für die Verwendung durch Endbenutzer Anwendungen vorgesehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Simulieren der Diagramm Erstellung mit GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[**Stgisstoragefile**](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[**StgOpenStorage**](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
