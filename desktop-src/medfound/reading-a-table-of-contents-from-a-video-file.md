---
description: Lesen eines Inhaltsverzeichnisses aus einer Video Datei
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: Lesen eines Inhaltsverzeichnisses aus einer Video Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d75d1101b2ad0a2ecd57dcf53acbe6a6e7d435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354570"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a><span data-ttu-id="5bf84-103">Lesen eines Inhaltsverzeichnisses aus einer Video Datei</span><span class="sxs-lookup"><span data-stu-id="5bf84-103">Reading a Table of Contents from a Video File</span></span>

<span data-ttu-id="5bf84-104">In diesem Thema wird veranschaulicht, wie Sie ein Inhaltsverzeichnis lesen, das bereits in eine Videodatei eingebettet wurde.</span><span class="sxs-lookup"><span data-stu-id="5bf84-104">This topic demonstrates how to read a table of contents that has already been embedded in a video file.</span></span>

<span data-ttu-id="5bf84-105">Beginnen Sie, indem Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um ein TOC-Parser-Objekt zu erstellen und eine [**itocparser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5bf84-105">Start by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface.</span></span> <span data-ttu-id="5bf84-106">Rufen Sie dann die folgenden Schnittstellen durch Aufrufen von-Methoden ab.</span><span class="sxs-lookup"><span data-stu-id="5bf84-106">Then obtain the following interfaces by calling methods.</span></span>

-   [<span data-ttu-id="5bf84-107">**Iinhalts Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="5bf84-107">**IToc**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [<span data-ttu-id="5bf84-108">**Iycentrylist**</span><span class="sxs-lookup"><span data-stu-id="5bf84-108">**ITocEntryList**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [<span data-ttu-id="5bf84-109">**IIn Centry**</span><span class="sxs-lookup"><span data-stu-id="5bf84-109">**ITocEntry**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

<span data-ttu-id="5bf84-110">Verwenden Sie die Methoden von [**iycentry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) , um einen einzelnen Eintrag im Inhaltsverzeichnis zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5bf84-110">Use the methods of [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) to inspect an individual entry in the table of contents.</span></span> <span data-ttu-id="5bf84-111">Beispielsweise können Sie den Titel, die Startzeit und die Endzeit des Eintrags überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5bf84-111">For example, you can inspect the title, the start time, and the end time of the entry.</span></span>

<span data-ttu-id="5bf84-112">In der folgenden Liste sind die Schritte ausführlicher aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bf84-112">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="5bf84-113">Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um ein Inhalts Objekt Objekt zu erstellen und eine [**idecparser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5bf84-113">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
2.  <span data-ttu-id="5bf84-114">Nennen Sie [**idecparser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) , um den Inhaltsverzeichnis-Parser zu initialisieren und einer Videodatei zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5bf84-114">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC parser and associate it with a video file.</span></span>
3.  <span data-ttu-id="5bf84-115">Rufen Sie eine [**itoc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) -Schnittstelle ab, indem Sie [**itocparser:: gettocbyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5bf84-115">Obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface by calling [**ITocParser::GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).</span></span>
4.  <span data-ttu-id="5bf84-116">Rufen Sie eine [**itocentrylist**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) -Schnittstelle ab, indem Sie [**itoc:: getentrylistbyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5bf84-116">Obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface by calling [**IToc::GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).</span></span>
5.  <span data-ttu-id="5bf84-117">Rufen Sie eine [**itocentry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) -Schnittstelle ab, indem Sie [**itocentrylist:: getentrybyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5bf84-117">Obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface by calling [**ITocEntryList::GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).</span></span>
6.  <span data-ttu-id="5bf84-118">Zuordnen einer [**TOC- \_ Eintrags \_ deskriptorstruktur**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="5bf84-118">Allocate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure.</span></span>
7.  <span data-ttu-id="5bf84-119">Füllen Sie die [**TOC- \_ Eintrags \_ deskriptorstruktur**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) durch Aufrufen von [**itocentry:: getDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor)auf.</span><span class="sxs-lookup"><span data-stu-id="5bf84-119">Populate the [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure by calling [**ITocEntry::GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).</span></span>

<span data-ttu-id="5bf84-120">Der folgende Code veranschaulicht die Schritte in der vorangehenden Liste.</span><span class="sxs-lookup"><span data-stu-id="5bf84-120">The following code demonstrates the steps in the preceding list.</span></span>


```C++
#include <stdio.h>
#include <wmcodecdsp.h>

HRESULT ShowEntryInfo(ITocEntry* pEntry);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocParser* pTocParser = NULL;

      hr = CoCreateInstance(CLSID_CTocParser, NULL, CLSCTX_INPROC_SERVER, 
         IID_ITocParser, (VOID**)&pTocParser);  
      
      if(SUCCEEDED(hr))
      {  
         hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

         if(SUCCEEDED(hr))
         {
            IToc* pToc = NULL;
            hr = pTocParser->GetTocByIndex(TOC_POS_TOPLEVELOBJECT, 0, &pToc);

            if(SUCCEEDED(hr))
            {
               ITocEntryList* pEntryList = NULL;
               hr = pToc->GetEntryListByIndex(0, &pEntryList);

               if(SUCCEEDED(hr))
               {
                  ITocEntry* pEntry = NULL;
                  hr = pEntryList->GetEntryByIndex(0, &pEntry);

                  if(SUCCEEDED(hr))
                  {
                     hr = ShowEntryInfo(pEntry);
                     pEntry->Release();
                     pEntry = NULL;
                  }

                  pEntryList->Release();
                  pEntryList = NULL;
               }

               pToc->Release();
               pToc = NULL;
            }
         }

         pTocParser->Release();
         pTocParser = NULL;  
      }
                   
      CoUninitialize();
   }
}

HRESULT ShowEntryInfo(ITocEntry* pEntry)
{
   HRESULT hr = E_FAIL;

   TOC_ENTRY_DESCRIPTOR entryDesc = {0};
   hr = pEntry->GetDescriptor(&entryDesc);

   if(SUCCEEDED(hr))
   {
      printf_s("qwStartTime: %x\n", entryDesc.qwStartTime);
      printf_s("qwEndTime: %x\n", entryDesc.qwEndTime);
      printf_s("qwStartStartPacketOffset: %x\n", entryDesc.qwStartPacketOffset);
      printf_s("qwEndPacketOffset: %x\n", entryDesc.qwEndPacketOffset);
      printf_s("qwRepresentativeFrameTime: %x\n", entryDesc.qwRepresentativeFrameTime);
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5bf84-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5bf84-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bf84-122">Einbetten eines Inhaltsverzeichnisses in eine Video Datei</span><span class="sxs-lookup"><span data-stu-id="5bf84-122">Embedding a Table of Contents in a Video File</span></span>](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="5bf84-123">Tabelle mit Inhalts parserobjekten</span><span class="sxs-lookup"><span data-stu-id="5bf84-123">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="5bf84-124">Programmier Handbuch für das Inhaltsverzeichnis des Parsers</span><span class="sxs-lookup"><span data-stu-id="5bf84-124">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
