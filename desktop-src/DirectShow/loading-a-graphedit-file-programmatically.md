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
# <a name="loading-a-graphedit-file-programmatically"></a><span data-ttu-id="debef-103">Programm gesteuertes Laden einer GraphEdit-Datei</span><span class="sxs-lookup"><span data-stu-id="debef-103">Loading a GraphEdit File Programmatically</span></span>

<span data-ttu-id="debef-104">Eine Anwendung kann die **IPersistStream** -Schnittstelle verwenden, um eine GraphEdit-Datei (. GRF) zu laden.</span><span class="sxs-lookup"><span data-stu-id="debef-104">An application can use the **IPersistStream** interface to load a GraphEdit (.grf) file.</span></span> <span data-ttu-id="debef-105">Verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="debef-105">Use the following code:</span></span>


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
> <span data-ttu-id="debef-106">Der Aufrufe von **IPersistStream:: Load** im vorherigen Codebeispiel kann einen DirectShow-Fehler oder einen Erfolgs Code zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="debef-106">The call to **IPersistStream::Load** in the previous code example can return a DirectShow error or success code.</span></span> <span data-ttu-id="debef-107">Eine Liste möglicher Rückgabewerte finden Sie unter [Fehler-und Erfolgs Codes](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="debef-107">For a list of possible return values, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 

<span data-ttu-id="debef-108">GraphEdit-Dateien dienen nur zum Testen und Debuggen.</span><span class="sxs-lookup"><span data-stu-id="debef-108">GraphEdit files are intended only for testing and debugging.</span></span> <span data-ttu-id="debef-109">Sie sind nicht für die Verwendung durch Endbenutzer Anwendungen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="debef-109">They are not meant for use by end-user applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="debef-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="debef-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="debef-111">Simulieren der Diagramm Erstellung mit GraphEdit</span><span class="sxs-lookup"><span data-stu-id="debef-111">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[<span data-ttu-id="debef-112">**Stgisstoragefile**</span><span class="sxs-lookup"><span data-stu-id="debef-112">**StgIsStorageFile**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[<span data-ttu-id="debef-113">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="debef-113">**StgOpenStorage**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
