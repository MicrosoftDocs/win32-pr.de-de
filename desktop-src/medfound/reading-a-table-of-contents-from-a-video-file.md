---
description: Lesen eines Inhaltsverzeichnis aus einer Videodatei
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: Lesen eines Inhaltsverzeichnis aus einer Videodatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bee379b0c50263463b0aa56e7ebb86bba447e70ef94ff82a6ba89e025d450bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034938"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a>Lesen eines Inhaltsverzeichnis aus einer Videodatei

In diesem Thema wird veranschaulicht, wie Sie ein Inhaltsverzeichnis lesen, das bereits in eine Videodatei eingebettet wurde.

Rufen Sie zunächst [**CoCreateInstance auf,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein TOC-Parserobjekt zu erstellen und eine [**ITocParser-Schnittstelle zu**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) erhalten. Rufen Sie dann die folgenden Schnittstellen ab, indem Sie Methoden aufrufen.

-   [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

Verwenden Sie die Methoden von [**ITocEntry,**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) um einen einzelnen Eintrag im Inhaltsverzeichnis zu überprüfen. Beispielsweise können Sie den Titel, die Startzeit und die Endzeit des Eintrags überprüfen.

In der folgenden Liste sind die Schritte ausführlicher aufgeführt.

1.  Rufen [**Sie CoCreateInstance auf,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein TOC-Parserobjekt zu erstellen und eine [**ITocParser-Schnittstelle**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) zu erhalten.
2.  Rufen [**Sie ITocParser::Init auf,**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) um den TOC-Parser zu initialisieren und einer Videodatei zu zuordnen.
3.  Rufen Sie eine [**IToc-Schnittstelle**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) ab, indem [**Sie ITocParser::GetTocByIndex aufrufen.**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
4.  Rufen Sie eine [**ITocEntryList-Schnittstelle**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) ab, indem [**Sie IToc::GetEntryListByIndex aufrufen.**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex)
5.  Rufen Sie [**eine ITocEntry-Schnittstelle**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) ab, indem [**Sie ITocEntryList::GetEntryByIndex aufrufen.**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex)
6.  Ordnen Sie eine [**TOC \_ ENTRY \_ DESCRIPTOR-Struktur**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) zu.
7.  Füllen Sie die [**TOC \_ ENTRY \_ DESCRIPTOR-Struktur**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) auf, indem [**Sie ITocEntry::GetDescriptor aufrufen.**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor)

Der folgende Code veranschaulicht die Schritte in der vorherigen Liste.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einbetten eines Inhaltsverzeichnis in eine Videodatei](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[Inhaltsverzeichnisparserobjekte](toc-parser-objects.md)
</dt> <dt>

[Table of Contents Parser Programming Guide](toc-parser-programming-guide.md)
</dt> </dl>

 

 
