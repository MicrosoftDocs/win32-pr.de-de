---
title: Abrufen der Antwort aus einem Upload-Reply Auftrag
description: Wenn Sie Daten in eine Serveranwendung hochladen und an den Client zurückgeben möchten, geben Sie den Auftrag als AUFTRAGSTYP \_ \_ UPLOAD \_ \_ REPLY-Auftrag an.
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 79ca145a3ed243209fc0059b20823e32da3cf3974850a6bc3e872f43dbd40aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004880"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>Abrufen der Antwort aus einem Upload-Reply Auftrag

Ein BITS Upload-Reply-Auftrag überprüft zusätzlich zum Hochladen einer Datei auf einen Server auch eine Antwort-URL, die als Teil der Serverantwort gesendet wird, und folgt dann automatisch der Antwort-URL und lädt eine Antwort von ihr herunter. Weitere Informationen zum Bits-Reply-URL-Headerwert finden Sie in der Dokumentation zu [Ack for Fragment.](/windows/desktop/Bits/ack-for-fragment)

Legen Sie den Auftragstyp auf BG \_ JOB TYPE UPLOAD REPLY \_ \_ \_ fest, um einen Upload-Reply zu erstellen. Die Antwortdaten sind für den Client verfügbar, nachdem der Auftrag in den Status BG \_ JOB \_ STATE \_ TRANSFERD (BG-AUFTRAGSSTATUS ÜBERTRAGEN) versetzt wurde. Rufen Sie zum Abrufen der Antwort eine der folgenden Methoden auf:

-   [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    Stellt eine Speicherkopie der Antwortdaten zur Verfügung. Verwenden Sie diese Methode, um die Antwortdaten vor oder nach dem Aufruf der [**IBackgroundCopyJob::Complete-Methode zu**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) lesen. Wenn die Antwortdaten 1 MB überschreiten, muss die Anwendung die [**IBackgroundCopyJob2::GetReplyFileName-Methode**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) aufrufen, um den Namen der Antwortdatei abzurufen und ihren Inhalt direkt zu lesen.

-   [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    Gibt den Namen der Datei an, die die Antwort enthält. Sie müssen die **IBackgroundCopyJob::Complete-Methode aufrufen,** bevor Sie die Antwortdatei öffnen und lesen. Die Antwortdatei ist für den Client erst verfügbar, wenn Sie die **Complete-Methode** aufrufen.

Rufen Sie diese Methoden nur dann in Ihrer [**IBackgroundCopyCallback::JobTransferred-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) auf, wenn die Antwort klein ist und schnell verarbeitet werden kann, um den Rückrufthread nicht zu blockieren. Wenn Sie anstelle [**des Rückrufs die**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) Befehlszeilenbenachrichtigung verwenden, übergeben Sie die Auftrags-ID an die ausführbare Datei. Die ausführbare Datei verwendet den Auftragsbezeichner zum Aufrufen der **Complete-Methode,** um die Antwortdatei verfügbar zu machen.

In den folgenden Beispielen wird gezeigt, wie sie jede Methode verwenden, um die Antwortdaten abzurufen.

-   [Verwenden von GetReplyData](#using-getreplydata)
-   [Verwenden von GetReplyFileName](#using-getreplyfilename)

## <a name="using-getreplydata"></a>Verwenden von GetReplyData

Das folgende Beispiel zeigt, wie die Antwortdaten mithilfe der [**IBackgroundCopyJob2::GetReplyData-Methode abgerufen**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) werden. Im Beispiel wird davon ausgegangen, dass der [**IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) gültig ist, der Typ des Auftrags upload-reply und der Status des Auftrags BG \_ JOB STATE \_ \_ TRANSFERD ist.


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



## <a name="using-getreplyfilename"></a>Verwenden von GetReplyFileName

Das folgende Beispiel zeigt, wie die Antwortdaten mithilfe der [**IBackgroundCopyJob2::GetReplyFileName-Methode abgerufen**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) werden. Im Beispiel wird davon ausgegangen, dass der [**IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) gültig ist, der Typ des Auftrags upload-reply und der Status des Auftrags BG \_ JOB STATE \_ \_ TRANSFERD ist.


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



 

 




