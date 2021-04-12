---
description: Dieses Thema enthält Informationen zum Erstellen des Standardindexer-Objekts, das von Media Foundation bereitgestellt wird.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Erstellung und Konfiguration von Indexern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217035"
---
# <a name="indexer-creation-and-configuration"></a><span data-ttu-id="1de46-103">Erstellung und Konfiguration von Indexern</span><span class="sxs-lookup"><span data-stu-id="1de46-103">Indexer Creation and Configuration</span></span>

<span data-ttu-id="1de46-104">Der ASF- *Indexer* ist eine wmcontainer-Ebenenkomponente, die verwendet wird, um Index Objekte in einer ASF-Datei (Advanced Systems Format) zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1de46-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="1de46-105">Dieses Thema enthält Informationen zum Erstellen des Standardindexer-Objekts, das von Media Foundation bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1de46-105">This topic provides information about creating the default indexer object provided by Media Foundation.</span></span>

<span data-ttu-id="1de46-106">Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1de46-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="1de46-107">**So erstellen und initialisieren Sie den ASF-Indexer**</span><span class="sxs-lookup"><span data-stu-id="1de46-107">**To create and initialize the ASF indexer**</span></span>

1.  <span data-ttu-id="1de46-108">Ruft die [**mfkreateasfindexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) -Funktion auf, um einen [**imfasfindexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) -Zeiger auf das Indexer-Objekt zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="1de46-108">Call the [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) function to receive an [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) pointer to the indexer object.</span></span>
2.  <span data-ttu-id="1de46-109">Aufrufen von [**imfasfindexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) zum Angeben des Lese-oder Schreibmodus für das Indexer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1de46-109">Call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) to specify the read or write mode for indexer object.</span></span> <span data-ttu-id="1de46-110">Standardmäßig ist der Indexer für die vorwärts Suche konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1de46-110">By default, the indexer is configured for forward seeking.</span></span>

    

    | <span data-ttu-id="1de46-111">Zweck</span><span class="sxs-lookup"><span data-stu-id="1de46-111">Use</span></span>                       | <span data-ttu-id="1de46-112">Flag</span><span class="sxs-lookup"><span data-stu-id="1de46-112">Flag</span></span>                                           |
    |---------------------------|------------------------------------------------|
    | <span data-ttu-id="1de46-113">Lesen (vorwärts Suche)</span><span class="sxs-lookup"><span data-stu-id="1de46-113">Reading (forward seeking)</span></span> | <span data-ttu-id="1de46-114">NULL (Standard)</span><span class="sxs-lookup"><span data-stu-id="1de46-114">Zero (default)</span></span>                                 |
    | <span data-ttu-id="1de46-115">Lesen (Reverse-Suche)</span><span class="sxs-lookup"><span data-stu-id="1de46-115">Reading (reverse seeking)</span></span> | <span data-ttu-id="1de46-116">**mfasf- \_ Indexer- \_ Lesevorgang \_ für \_ reverleplayback**</span><span class="sxs-lookup"><span data-stu-id="1de46-116">**MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK**</span></span> |
    | <span data-ttu-id="1de46-117">Schreiben</span><span class="sxs-lookup"><span data-stu-id="1de46-117">Writing</span></span>                   | <span data-ttu-id="1de46-118">mfasf- \_ Indexer \_ schreiben \_ neuer \_ Index</span><span class="sxs-lookup"><span data-stu-id="1de46-118">MFASF\_INDEXER\_WRITE\_NEW\_INDEX</span></span>              |

    

     

    > [!Note]  
    > <span data-ttu-id="1de46-119">Die gleiche Instanz des Indexers kann nicht sowohl für Lese-als auch für Schreibvorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1de46-119">The same instance of the indexer cannot be used for both reading and writing.</span></span> <span data-ttu-id="1de46-120">Sie müssen den Indexer für einen oder den anderen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1de46-120">You must configure the indexer for one or the other.</span></span>

     

3.  <span data-ttu-id="1de46-121">Zum Initialisieren des [**Indexers wird imfasfindexer:: Initialisieren**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) aufgerufen, indem der [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Zeiger des ContentInfo-Objekts angegeben wird, das die zu schreibenden oder zu lesende Datei beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1de46-121">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer by specifying the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer of the ContentInfo object that describes the file to be written or read.</span></span> <span data-ttu-id="1de46-122">Das ContentInfo-Objekt enthält Informationen, die das [ASF-Header Objekt](asf-file-structure.md)bilden.</span><span class="sxs-lookup"><span data-stu-id="1de46-122">The ContentInfo object contains information that constitutes the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="1de46-123">Das Indexer-Objekt benötigt ein gültiges ContentInfo-Objekt, bevor Indexeinträge einer ASF-Datei erzeugt oder gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="1de46-123">The indexer object requires a valid ContentInfo object before generating or reading index entries of an ASF file.</span></span>

<span data-ttu-id="1de46-124">Im folgenden Codebeispiel wird gezeigt, wie eine Anwendung das Indexer-Objekt erstellen und initialisieren kann, um mit einem bestimmten ASF-Inhalt zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1de46-124">The following code example shows how an application can create and initialize the indexer object to work with specific ASF content.</span></span> <span data-ttu-id="1de46-125">Das ContentInfo-Objekt stellt das ASF-Header Objekt dar. der Inhalt wird als Bytestream übermittelt.</span><span class="sxs-lookup"><span data-stu-id="1de46-125">The ContentInfo object represents the ASF Header Object; the content is passed as a byte stream.</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1de46-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1de46-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1de46-127">ASF-Indexer</span><span class="sxs-lookup"><span data-stu-id="1de46-127">ASF Indexer</span></span>](asf-index-object.md)
</dt> <dt>

[<span data-ttu-id="1de46-128">Verwenden des Indexers zum Suchen in einer ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="1de46-128">Using the Indexer to Seek Within an ASF File</span></span>](using-the-indexer-to-seek.md)
</dt> <dt>

[<span data-ttu-id="1de46-129">Verwenden des Indexers zum Schreiben eines neuen Indexes</span><span class="sxs-lookup"><span data-stu-id="1de46-129">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



