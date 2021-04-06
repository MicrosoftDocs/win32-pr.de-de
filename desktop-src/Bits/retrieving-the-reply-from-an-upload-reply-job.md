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
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a><span data-ttu-id="8796d-103">Abrufen der Antwort von einem Upload-Reply Auftrag</span><span class="sxs-lookup"><span data-stu-id="8796d-103">Retrieving the Reply from an Upload-Reply Job</span></span>

<span data-ttu-id="8796d-104">Bei einem Bits-Upload-Reply Auftrag, zusätzlich zum Hochladen einer Datei auf einen Server, wird auch eine Antwort-URL untersucht, die als Teil der Serverantwort gesendet wird, und anschließend wird die Antwort-URL automatisch befolgt und eine Antwort davon heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="8796d-104">A BITS Upload-Reply job, in addition to uploading a file to a server, will also examine a reply URL sent as part of the server reply and then automatically follow the reply URL and download a response from it.</span></span> <span data-ttu-id="8796d-105">Weitere Informationen zum Header Wert "Bits-Reply-URL" finden Sie in der Dokumentation [zu "ACK for Fragment](/windows/desktop/Bits/ack-for-fragment) ".</span><span class="sxs-lookup"><span data-stu-id="8796d-105">See the [Ack for Fragment](/windows/desktop/Bits/ack-for-fragment) documentation for more details about the BITS-Reply-URL header value.</span></span>

<span data-ttu-id="8796d-106">Legen Sie den Auftragstyp auf "BG \_ Job \_ Type \_ Upload Reply" fest \_ , um einen Upload-Reply Type-Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8796d-106">Set the job type as BG\_JOB\_TYPE\_UPLOAD\_REPLY to create an Upload-Reply type job.</span></span> <span data-ttu-id="8796d-107">Die Antwortdaten stehen dem Client zur Verfügung, nachdem der Auftrag in den Status des Status "BG- \_ Auftrag \_ übertragen" gelangt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="8796d-107">The reply data is available to the client after the job enters the BG\_JOB\_STATE\_TRANSFERRED state.</span></span> <span data-ttu-id="8796d-108">Rufen Sie zum Abrufen der Antwort eine der folgenden Methoden auf:</span><span class="sxs-lookup"><span data-stu-id="8796d-108">To retrieve the reply, call one of the following methods:</span></span>

-   [<span data-ttu-id="8796d-109">**IBackgroundCopyJob2:: getreplydata**</span><span class="sxs-lookup"><span data-stu-id="8796d-109">**IBackgroundCopyJob2::GetReplyData**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    <span data-ttu-id="8796d-110">Stellt eine Kopie der Antwortdaten im Arbeitsspeicher bereit.</span><span class="sxs-lookup"><span data-stu-id="8796d-110">Provides an in-memory copy of the reply data.</span></span> <span data-ttu-id="8796d-111">Verwenden Sie diese Methode, um die Antwortdaten vor oder nach dem Aufruf der [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode zu lesen.</span><span class="sxs-lookup"><span data-stu-id="8796d-111">Use this method to read the reply data before or after calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="8796d-112">Wenn die Antwortdaten 1 MB überschreiten, muss die Anwendung die [**IBackgroundCopyJob2:: getreplyfilename**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) -Methode aufrufen, um den Namen der Antwortdatei abzurufen und den Inhalt direkt zu lesen.</span><span class="sxs-lookup"><span data-stu-id="8796d-112">If the reply data exceeds 1 MB, the application must call the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method to retrieve the name of the reply file and read its contents directly.</span></span>

-   [<span data-ttu-id="8796d-113">**IBackgroundCopyJob2:: getreplyfilename**</span><span class="sxs-lookup"><span data-stu-id="8796d-113">**IBackgroundCopyJob2::GetReplyFileName**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    <span data-ttu-id="8796d-114">Gibt den Namen der Datei an, die die Antwort enthält.</span><span class="sxs-lookup"><span data-stu-id="8796d-114">Provides the name of the file that contains the reply.</span></span> <span data-ttu-id="8796d-115">Vor dem Öffnen und Lesen der Antwortdatei müssen Sie die **ibackgroundcopyjob:: Complete** -Methode abrufen. die Antwortdatei steht dem Client erst zur Verfügung, wenn Sie die **Complete** -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="8796d-115">You must call the **IBackgroundCopyJob::Complete** method before opening and reading the reply file; the reply file is not available to the client until you call the **Complete** method.</span></span>

<span data-ttu-id="8796d-116">Rufen Sie diese Methoden in Ihrer [**ibackgroundcopycallback:: jobtransfer**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) -Methode nur auf, wenn die Antwort klein ist und schnell verarbeitet werden kann, damit der Rückruf Thread nicht blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="8796d-116">Call these methods in your [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) method only if the reply is small and can be processed quickly so as to not block the callback thread.</span></span> <span data-ttu-id="8796d-117">Wenn Sie anstelle des Rückrufs eine [**Befehlszeilen Benachrichtigung**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) verwenden, übergeben Sie den Auftrags Bezeichner an die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="8796d-117">If you use [**command line notification**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) instead of the callback, pass the job identifier to the executable file.</span></span> <span data-ttu-id="8796d-118">Die ausführbare Datei verwendet den Auftrags Bezeichner, um die **Complete** -Methode aufzurufen, um die Antwortdatei verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="8796d-118">The executable file uses the job identifier to call the **Complete** method to make the reply file available.</span></span>

<span data-ttu-id="8796d-119">In den folgenden Beispielen wird gezeigt, wie die einzelnen Methoden zum Abrufen der Antwortdaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8796d-119">The following examples show how to use each method to retrieve the reply data.</span></span>

-   [<span data-ttu-id="8796d-120">Verwenden von getreplydata</span><span class="sxs-lookup"><span data-stu-id="8796d-120">Using GetReplyData</span></span>](#using-getreplydata)
-   [<span data-ttu-id="8796d-121">Verwenden von getreplyfilename</span><span class="sxs-lookup"><span data-stu-id="8796d-121">Using GetReplyFileName</span></span>](#using-getreplyfilename)

## <a name="using-getreplydata"></a><span data-ttu-id="8796d-122">Verwenden von getreplydata</span><span class="sxs-lookup"><span data-stu-id="8796d-122">Using GetReplyData</span></span>

<span data-ttu-id="8796d-123">Im folgenden Beispiel wird gezeigt, wie die Antwortdaten mithilfe der [**IBackgroundCopyJob2:: getreplydata**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8796d-123">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) method.</span></span> <span data-ttu-id="8796d-124">Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist, der Typ des Auftrags "Upload-Reply" und der Status des Auftrags "BG Job State Transfer" lautet \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8796d-124">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of the job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


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



## <a name="using-getreplyfilename"></a><span data-ttu-id="8796d-125">Verwenden von getreplyfilename</span><span class="sxs-lookup"><span data-stu-id="8796d-125">Using GetReplyFileName</span></span>

<span data-ttu-id="8796d-126">Im folgenden Beispiel wird gezeigt, wie die Antwortdaten mithilfe der [**IBackgroundCopyJob2:: getreplyfilename**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8796d-126">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method.</span></span> <span data-ttu-id="8796d-127">Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist, der Typ des Auftrags "Upload-Reply" und der Status des Auftrags "BG Job State Transfer" lautet \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8796d-127">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


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



 

 




