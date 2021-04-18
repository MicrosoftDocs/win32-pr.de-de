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
# <a name="reading-a-table-of-contents-from-a-video-file"></a>Lesen eines Inhaltsverzeichnisses aus einer Video Datei

In diesem Thema wird veranschaulicht, wie Sie ein Inhaltsverzeichnis lesen, das bereits in eine Videodatei eingebettet wurde.

Beginnen Sie, indem Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um ein TOC-Parser-Objekt zu erstellen und eine [**itocparser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) -Schnittstelle abzurufen. Rufen Sie dann die folgenden Schnittstellen durch Aufrufen von-Methoden ab.

-   [**Iinhalts Verzeichnis**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [**Iycentrylist**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [**IIn Centry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

Verwenden Sie die Methoden von [**iycentry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) , um einen einzelnen Eintrag im Inhaltsverzeichnis zu überprüfen. Beispielsweise können Sie den Titel, die Startzeit und die Endzeit des Eintrags überprüfen.

In der folgenden Liste sind die Schritte ausführlicher aufgeführt.

1.  Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um ein Inhalts Objekt Objekt zu erstellen und eine [**idecparser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) -Schnittstelle zu erhalten.
2.  Nennen Sie [**idecparser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) , um den Inhaltsverzeichnis-Parser zu initialisieren und einer Videodatei zuzuordnen.
3.  Rufen Sie eine [**itoc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) -Schnittstelle ab, indem Sie [**itocparser:: gettocbyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)aufrufen.
4.  Rufen Sie eine [**itocentrylist**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) -Schnittstelle ab, indem Sie [**itoc:: getentrylistbyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex)aufrufen.
5.  Rufen Sie eine [**itocentry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) -Schnittstelle ab, indem Sie [**itocentrylist:: getentrybyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex)aufrufen.
6.  Zuordnen einer [**TOC- \_ Eintrags \_ deskriptorstruktur**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) .
7.  Füllen Sie die [**TOC- \_ Eintrags \_ deskriptorstruktur**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) durch Aufrufen von [**itocentry:: getDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor)auf.

Der folgende Code veranschaulicht die Schritte in der vorangehenden Liste.


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

[Einbetten eines Inhaltsverzeichnisses in eine Video Datei](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[Tabelle mit Inhalts parserobjekten](toc-parser-objects.md)
</dt> <dt>

[Programmier Handbuch für das Inhaltsverzeichnis des Parsers](toc-parser-programming-guide.md)
</dt> </dl>

 

 
