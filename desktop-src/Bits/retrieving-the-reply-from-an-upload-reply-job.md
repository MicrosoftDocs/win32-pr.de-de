---
title: Abrufen der Antwort von einem Upload-Reply Auftrag
description: Wenn Sie Daten in eine Serveranwendung hochladen und Daten an den Client zurückgeben lassen möchten, geben Sie den Auftrag als BG- \_ \_ Auftragstyp \_ Upload- \_ Antwort Auftrag an.
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 582a37a31c13c5cc3e0b44c51a767cfbe465c64c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947457"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>Abrufen der Antwort von einem Upload-Reply Auftrag

Bei einem Bits-Upload-Reply Auftrag, zusätzlich zum Hochladen einer Datei auf einen Server, wird auch eine Antwort-URL untersucht, die als Teil der Serverantwort gesendet wird, und anschließend wird die Antwort-URL automatisch befolgt und eine Antwort davon heruntergeladen. Weitere Informationen zum Header Wert "Bits-Reply-URL" finden Sie in der Dokumentation [zu "ACK for Fragment](/windows/desktop/Bits/ack-for-fragment) ".

Legen Sie den Auftragstyp auf "BG \_ Job \_ Type \_ Upload Reply" fest \_ , um einen Upload-Reply Type-Auftrag zu erstellen. Die Antwortdaten stehen dem Client zur Verfügung, nachdem der Auftrag in den Status des Status "BG- \_ Auftrag \_ übertragen" gelangt ist \_ . Rufen Sie zum Abrufen der Antwort eine der folgenden Methoden auf:

-   [**IBackgroundCopyJob2:: getreplydata**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    Stellt eine Kopie der Antwortdaten im Arbeitsspeicher bereit. Verwenden Sie diese Methode, um die Antwortdaten vor oder nach dem Aufruf der [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode zu lesen. Wenn die Antwortdaten 1 MB überschreiten, muss die Anwendung die [**IBackgroundCopyJob2:: getreplyfilename**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) -Methode aufrufen, um den Namen der Antwortdatei abzurufen und den Inhalt direkt zu lesen.

-   [**IBackgroundCopyJob2:: getreplyfilename**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    Gibt den Namen der Datei an, die die Antwort enthält. Vor dem Öffnen und Lesen der Antwortdatei müssen Sie die **ibackgroundcopyjob:: Complete** -Methode abrufen. die Antwortdatei steht dem Client erst zur Verfügung, wenn Sie die **Complete** -Methode aufgerufen haben.

Rufen Sie diese Methoden in Ihrer [**ibackgroundcopycallback:: jobtransfer**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) -Methode nur auf, wenn die Antwort klein ist und schnell verarbeitet werden kann, damit der Rückruf Thread nicht blockiert wird. Wenn Sie anstelle des Rückrufs eine [**Befehlszeilen Benachrichtigung**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) verwenden, übergeben Sie den Auftrags Bezeichner an die ausführbare Datei. Die ausführbare Datei verwendet den Auftrags Bezeichner, um die **Complete** -Methode aufzurufen, um die Antwortdatei verfügbar zu machen.

In den folgenden Beispielen wird gezeigt, wie die einzelnen Methoden zum Abrufen der Antwortdaten verwendet werden.

-   [Verwenden von getreplydata](#using-getreplydata)
-   [Verwenden von getreplyfilename](#using-getreplyfilename)

## <a name="using-getreplydata"></a>Verwenden von getreplydata

Im folgenden Beispiel wird gezeigt, wie die Antwortdaten mithilfe der [**IBackgroundCopyJob2:: getreplydata**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) -Methode abgerufen werden. Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist, der Typ des Auftrags "Upload-Reply" und der Status des Auftrags "BG Job State Transfer" lautet \_ \_ \_ .


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
BYTE* pReply = NULL;
UINT64 ReplySize;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyData method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyData(&pReply, &ReplySize);
    if (S_OK == hr))
    {
        if (pReply)
        {
            //Do something with the data.
            CoTaskMemFree(pReply);
        }
        else
        {
            //The server application did not return a reply.
        }
    }
    else if (BG_E_TOO_LARGE == hr)
    {
        //The reply exceeds 1 MB. To retrieve the reply, get the reply file name,
        //complete the job, open the reply file, and read the reply.
    }
    else
    {
        //Handle the error
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



## <a name="using-getreplyfilename"></a>Verwenden von getreplyfilename

Im folgenden Beispiel wird gezeigt, wie die Antwortdaten mithilfe der [**IBackgroundCopyJob2:: getreplyfilename**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) -Methode abgerufen werden. Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist, der Typ des Auftrags "Upload-Reply" und der Status des Auftrags "BG Job State Transfer" lautet \_ \_ \_ .


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR* pszFileName = NULL;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyFileName method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyFileName(&pszFileName);
    if (SUCCEEDED(hr))
    {
        //Calling the Complete method removes the job from the queue, 
        //so make sure you maintain an interface pointer to this job 
        //or retrieve any job related information that you require 
        //when processing the reply.
        hr = pJob->Complete();

        //Open, read the file, and do something with the data.
        CoTaskMemFree(pszFileName);
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



 

 




