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
# <a name="embedding-a-table-of-contents-in-a-video-file"></a>Einbetten eines Inhaltsverzeichnisses in eine Video Datei

In diesem Thema wird veranschaulicht, wie ein Inhaltsverzeichnis (Inhaltsverzeichnis) erstellt und in eine Videodatei eingebettet wird. Um den Beispielcode kurz zu halten, ist das Inhaltsverzeichnis sehr einfach. Sie enthält nur einen Eintrag, und der Eintrag wird mit mindestens Informationen aufgefüllt.

Zum Erstellen eines Inhaltsverzeichnisses und Einbetten in eine Datei müssen Sie die folgenden vier Objekte durch Aufrufen von **CoCreateInstance** erstellen.

-   Inhaltseintrag
-   Inhaltsliste für Inhaltsverzeichnis
-   INHALTSVERZEICHNIS
-   Inhaltsverzeichnis

Klassen Bezeichner für die Objekte werden in [Klassen Bezeichner für den Inhaltsverzeichnis Inhalt](class-identifiers-for-toc-parser.md)angegeben.

Füllen Sie zuerst den Inhaltseintrag mit Informationen auf, die einen Teil der Videodatei beschreiben. Fügen Sie den Eintrag in der Inhaltsliste des Inhaltsverzeichnis hinzu, und fügen Sie dann die Inhaltsliste zum Inhaltsverzeichnis hinzu. Fügen Sie schließlich das Inhaltsverzeichnis zum Inhaltsverzeichnis hinzu, das die Funktionalität zum Einbetten des Inhalts Inhalts in die Videodatei bereitstellt. In der folgenden Liste sind die Schritte ausführlicher aufgeführt.

1.  Erstellen Sie ein Inhalts Objekt, und rufen Sie eine [**iycentry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) -Schnittstelle auf.
2.  Füllt eine [**TOC- \_ Eintrags \_ deskriptorstruktur**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) auf und übergibt sie an [**itocentry:: setdescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).
3.  Erstellen Sie ein Inhaltslisten Objekt, und rufen Sie eine [**iycentrylist**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) -Schnittstelle auf.
4.  Fügen Sie das in Schritt 1 erstellte TOC-Eintrags Objekt dem TOC-Eintrag List-Objekt hinzu, indem Sie [**itocentrylist:: addentrybyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex)aufrufen.
5.  Erstellen Sie ein-Objekt, und rufen Sie eine [**IYC**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) -Schnittstelle auf.
6.  Fügen Sie das in Schritt 3 erstellte TOC-Eintrag Listen Objekt zum TOC-Objekt hinzu, indem Sie [**itoc:: addentrylistbyindex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex)aufrufen.
7.  Erstellen Sie ein Inhaltsverzeichnis Objekt, und rufen Sie eine [**idecparser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) -Schnittstelle auf.
8.  Nennen Sie [**idecparser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) , um das Inhalts Objekt zu initialisieren und es einer Videodatei zuzuordnen.
9.  Fügen Sie das TOC-Objekt, das Sie in Schritt 5 erstellt haben, zum TOC-Parserobjekt hinzu, indem Sie [**itocparser:: addtoc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)aufrufen.
10. Betten Sie das Inhaltsverzeichnis in die Videodatei ein, indem Sie [**itocparser:: Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit)aufrufen.

Der folgende Code veranschaulicht die in der vorangehenden Liste aufgeführten Schritte.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen eines Inhaltsverzeichnisses aus einer Video Datei](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[Tabelle mit Inhalts parserobjekten](toc-parser-objects.md)
</dt> <dt>

[Programmier Handbuch für das Inhaltsverzeichnis des Parsers](toc-parser-programming-guide.md)
</dt> </dl>

 

 



