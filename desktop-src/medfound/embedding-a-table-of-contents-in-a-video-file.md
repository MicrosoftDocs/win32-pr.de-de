---
description: Einbetten eines Inhaltsverzeichnisses in eine Video Datei
ms.assetid: 1546388a-7868-4411-be20-34d28becbe76
title: Einbetten eines Inhaltsverzeichnisses in eine Video Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8303082e454dde181de336ee0f64ff9d583312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127896"
---
# <a name="embedding-a-table-of-contents-in-a-video-file"></a><span data-ttu-id="2ed64-103">Einbetten eines Inhaltsverzeichnisses in eine Video Datei</span><span class="sxs-lookup"><span data-stu-id="2ed64-103">Embedding a Table of Contents in a Video File</span></span>

<span data-ttu-id="2ed64-104">In diesem Thema wird veranschaulicht, wie ein Inhaltsverzeichnis (Inhaltsverzeichnis) erstellt und in eine Videodatei eingebettet wird.</span><span class="sxs-lookup"><span data-stu-id="2ed64-104">This topic demonstrates how to create a table of contents (TOC) and embed it in a video file.</span></span> <span data-ttu-id="2ed64-105">Um den Beispielcode kurz zu halten, ist das Inhaltsverzeichnis sehr einfach. Sie enthält nur einen Eintrag, und der Eintrag wird mit mindestens Informationen aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="2ed64-105">To keep the example code short, the table of contents is very simple; it contains only one entry, and the entry is populated with a minimum of information.</span></span>

<span data-ttu-id="2ed64-106">Zum Erstellen eines Inhaltsverzeichnisses und Einbetten in eine Datei müssen Sie die folgenden vier Objekte durch Aufrufen von **CoCreateInstance** erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ed64-106">To create a table of contents and embed it in a file, you must create the following four objects by calling **CoCreateInstance**.</span></span>

-   <span data-ttu-id="2ed64-107">Inhaltseintrag</span><span class="sxs-lookup"><span data-stu-id="2ed64-107">TOC Entry</span></span>
-   <span data-ttu-id="2ed64-108">Inhaltsliste für Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="2ed64-108">TOC Entry List</span></span>
-   <span data-ttu-id="2ed64-109">INHALTSVERZEICHNIS</span><span class="sxs-lookup"><span data-stu-id="2ed64-109">TOC</span></span>
-   <span data-ttu-id="2ed64-110">Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="2ed64-110">TOC Parser</span></span>

<span data-ttu-id="2ed64-111">Klassen Bezeichner für die Objekte werden in [Klassen Bezeichner für den Inhaltsverzeichnis Inhalt](class-identifiers-for-toc-parser.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="2ed64-111">Class identifiers for the objects are given in [Class Identifiers for Table of Contents Parser](class-identifiers-for-toc-parser.md).</span></span>

<span data-ttu-id="2ed64-112">Füllen Sie zuerst den Inhaltseintrag mit Informationen auf, die einen Teil der Videodatei beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2ed64-112">First populate the TOC entry with information that describes one portion of the video file.</span></span> <span data-ttu-id="2ed64-113">Fügen Sie den Eintrag in der Inhaltsliste des Inhaltsverzeichnis hinzu, und fügen Sie dann die Inhaltsliste zum Inhaltsverzeichnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ed64-113">Add the TOC entry to the TOC entry list, and then add the TOC entry list to the TOC.</span></span> <span data-ttu-id="2ed64-114">Fügen Sie schließlich das Inhaltsverzeichnis zum Inhaltsverzeichnis hinzu, das die Funktionalität zum Einbetten des Inhalts Inhalts in die Videodatei bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2ed64-114">Finally, add the TOC to the TOC parser, which provides the functionality for embedding the TOC in the video file.</span></span> <span data-ttu-id="2ed64-115">In der folgenden Liste sind die Schritte ausführlicher aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ed64-115">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="2ed64-116">Erstellen Sie ein Inhalts Objekt, und rufen Sie eine [**iycentry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="2ed64-116">Create a TOC Entry object and obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface on it.</span></span>
2.  <span data-ttu-id="2ed64-117">Füllt eine [**TOC- \_ Eintrags \_ deskriptorstruktur**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) auf und übergibt sie an [**itocentry:: setdescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span><span class="sxs-lookup"><span data-stu-id="2ed64-117">Populate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure and pass it to [**ITocEntry::SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span></span>
3.  <span data-ttu-id="2ed64-118">Erstellen Sie ein Inhaltslisten Objekt, und rufen Sie eine [**iycentrylist**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="2ed64-118">Create a TOC Entry List object and obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface on it.</span></span>
4.  <span data-ttu-id="2ed64-119">Fügen Sie das in Schritt 1 erstellte TOC-Eintrags Objekt dem TOC-Eintrag List-Objekt hinzu, indem Sie [**itocentrylist:: addentrybyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2ed64-119">Add the TOC Entry object you created in step 1 to the TOC Entry List object by calling [**ITocEntryList::AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span></span>
5.  <span data-ttu-id="2ed64-120">Erstellen Sie ein-Objekt, und rufen Sie eine [**IYC**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="2ed64-120">Create a TOC object and obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface on it.</span></span>
6.  <span data-ttu-id="2ed64-121">Fügen Sie das in Schritt 3 erstellte TOC-Eintrag Listen Objekt zum TOC-Objekt hinzu, indem Sie [**itoc:: addentrylistbyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2ed64-121">Add the TOC Entry List object you created in step 3 to the TOC object by calling [**IToc::AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span></span>
7.  <span data-ttu-id="2ed64-122">Erstellen Sie ein Inhaltsverzeichnis Objekt, und rufen Sie eine [**idecparser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="2ed64-122">Create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
8.  <span data-ttu-id="2ed64-123">Nennen Sie [**idecparser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) , um das Inhalts Objekt zu initialisieren und es einer Videodatei zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2ed64-123">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC Parser object and associate it with a video file.</span></span>
9.  <span data-ttu-id="2ed64-124">Fügen Sie das TOC-Objekt, das Sie in Schritt 5 erstellt haben, zum TOC-Parserobjekt hinzu, indem Sie [**itocparser:: addtoc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2ed64-124">Add the TOC object you created in step 5 to the TOC Parser object by calling [**ITocParser::AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span></span>
10. <span data-ttu-id="2ed64-125">Betten Sie das Inhaltsverzeichnis in die Videodatei ein, indem Sie [**itocparser:: Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2ed64-125">Embed the table of contents in the video file by calling [**ITocParser::Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span></span>

<span data-ttu-id="2ed64-126">Der folgende Code veranschaulicht die in der vorangehenden Liste aufgeführten Schritte.</span><span class="sxs-lookup"><span data-stu-id="2ed64-126">The following code demonstrates the steps given in the preceding list.</span></span>


```C++
#include <wmcodecdsp.h>
HRESULT InitTocParserAndCommit(IToc* pToc);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocEntry* pEntry = NULL;
      hr = CoCreateInstance(CLSID_CTocEntry, NULL, 
         CLSCTX_INPROC_SERVER, IID_ITocEntry, (VOID**)&pEntry); 

      if(SUCCEEDED(hr))
      {
         TOC_ENTRY_DESCRIPTOR tocDesc = {0};
         tocDesc.qwStartTime = 4; 
         tocDesc.qwEndTime = 8;
         pEntry->SetDescriptor(&tocDesc); // HRESULT ignored for simplicity.    
    
         ITocEntryList* pEntryList = NULL;
         hr = CoCreateInstance(CLSID_CTocEntryList, NULL, 
            CLSCTX_INPROC_SERVER, IID_ITocEntryList, (VOID**)&pEntryList);

         if(SUCCEEDED(hr))
         {
            pEntryList->AddEntryByIndex(0, pEntry); // HRESULT ignored.
      
            IToc* pToc = NULL;
            hr = CoCreateInstance(CLSID_CToc, NULL, 
               CLSCTX_INPROC_SERVER, IID_IToc, (VOID**)&pToc);

            if(SUCCEEDED(hr))
            {
               pToc->AddEntryListByIndex(0, pEntryList); // HRESULT ignored.
               hr = InitTocParserAndCommit(pToc);
            }
         }
      }
     
      CoUninitialize();
   }
}

HRESULT InitTocParserAndCommit(IToc* pToc)
{
   ITocParser* pTocParser = NULL;
   HRESULT hr = CoCreateInstance(CLSID_CTocParser, NULL, 
      CLSCTX_INPROC_SERVER, IID_ITocParser, (VOID**)&pTocParser);

   if(SUCCEEDED(hr))
   {
      hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

      if(SUCCEEDED(hr))
      {
         DWORD tocIndex = 0;
         hr = pTocParser->AddToc(TOC_POS_TOPLEVELOBJECT, pToc, &tocIndex);

         if(SUCCEEDED(hr))
         {
            hr = pTocParser->Commit();
         }
      }

      pTocParser->Release();
      pTocParser = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2ed64-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ed64-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed64-128">Lesen eines Inhaltsverzeichnisses aus einer Video Datei</span><span class="sxs-lookup"><span data-stu-id="2ed64-128">Reading a Table of Contents From a Video File</span></span>](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="2ed64-129">Tabelle mit Inhalts parserobjekten</span><span class="sxs-lookup"><span data-stu-id="2ed64-129">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="2ed64-130">Programmier Handbuch für das Inhaltsverzeichnis des Parsers</span><span class="sxs-lookup"><span data-stu-id="2ed64-130">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



