---
title: Behandeln von Fehlern (Bits)
description: Es gibt zwei Arten von Fehlern, die in Ihrer Anwendung behandelt werden müssen.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- Behandeln von Fehler Bits
- Übertragen von Auftrags Bits, Fehlern
- Fehler Bits
- Fehler Bits, Behandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039923"
---
# <a name="handling-errors-bits"></a><span data-ttu-id="3ab15-107">Behandeln von Fehlern (Bits)</span><span class="sxs-lookup"><span data-stu-id="3ab15-107">Handling Errors (BITS)</span></span>

<span data-ttu-id="3ab15-108">Es gibt zwei Arten von Fehlern, die in Ihrer Anwendung behandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3ab15-108">There are two types of errors to handle in your application.</span></span> <span data-ttu-id="3ab15-109">Der erste Fehler ist ein fehlerhafter Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3ab15-109">The first error is a failed method call.</span></span> <span data-ttu-id="3ab15-110">Jede Methode gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3ab15-110">Each method returns an **HRESULT** value.</span></span> <span data-ttu-id="3ab15-111">Die Referenzseite für jede Methode identifiziert die Rückgabewerte, die mit der höchsten Wahrscheinlichkeit generiert werden.</span><span class="sxs-lookup"><span data-stu-id="3ab15-111">The reference page for each method identifies the return values that it is most likely to generate.</span></span> <span data-ttu-id="3ab15-112">Weitere Rückgabewerte finden Sie unter [Bits-Rückgabewerte](bits-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3ab15-112">For additional return values, see [BITS Return Values](bits-return-values.md).</span></span> <span data-ttu-id="3ab15-113">Um den Nachrichtentext zu erhalten, der dem Rückgabewert zugeordnet ist, müssen Sie die [**ibackgroundcopymanager:: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3ab15-113">To get the message text associated with the return value, call the [**IBackgroundCopyManager::GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) method.</span></span>

<span data-ttu-id="3ab15-114">Der zweite zu behandelnde Fehlertyp ist ein Auftrag, dessen [Status](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) in den Status " [BG- \_ Auftrags \_ Status \_](/windows/desktop/api/Bits/ne-bits-bg_job_state) " oder " **BG- \_ Auftrags \_ Status \_ vorübergehender \_ Fehler**" übergeht.</span><span class="sxs-lookup"><span data-stu-id="3ab15-114">The second type of error to handle is a job whose [state](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) transitions to [BG\_JOB\_STATE\_ERROR](/windows/desktop/api/Bits/ne-bits-bg_job_state) or **BG\_JOB\_STATE\_TRANSIENT\_ERROR**.</span></span> <span data-ttu-id="3ab15-115">Um Informationen zu diesen Arten von Fehlern abzurufen, rufen Sie die [**ibackgroundcopyjob:: getError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) -Methode des Auftrags auf.</span><span class="sxs-lookup"><span data-stu-id="3ab15-115">To retrieve information related to these types of errors, call the job's [**IBackgroundCopyJob::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) method.</span></span> <span data-ttu-id="3ab15-116">Die-Methode gibt einen [**ibackgroundcopyerror**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) -Schnittstellen Zeiger zurück, der Informationen enthält, die Sie verwenden, um die Ursache des Fehlers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3ab15-116">The method returns an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer that contains information you use to determine the cause of the error.</span></span> <span data-ttu-id="3ab15-117">Sie können auch eine Fehler Benachrichtigung erhalten, indem Sie sich für den Empfang von Ereignis Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="3ab15-117">You can also receive error notification by registering to receive event notification.</span></span> <span data-ttu-id="3ab15-118">Weitere Informationen finden Sie unter [Registrieren eines com-Rückrufs](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="3ab15-118">For details, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="3ab15-119">Bits betrachtet jeden Auftrag als atomarisch.</span><span class="sxs-lookup"><span data-stu-id="3ab15-119">BITS considers each job to be atomic.</span></span> <span data-ttu-id="3ab15-120">Wenn eine der Dateien im Auftrag einen Fehler generiert, verbleibt der Auftrag in einem Fehlerzustand, bis der Fehler behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="3ab15-120">If one of the files in the job generates an error, the job remains in an error state until the error is resolved.</span></span> <span data-ttu-id="3ab15-121">Daher können Sie die Datei, die den Fehler verursacht, nicht aus dem Auftrag löschen.</span><span class="sxs-lookup"><span data-stu-id="3ab15-121">Thus, you cannot delete the file that is causing the error from the job.</span></span> <span data-ttu-id="3ab15-122">Wenn der Fehler jedoch dadurch verursacht wird, dass der Server nicht verfügbar oder eine ungültige Remote Datei ist, können Sie die [**IBackgroundCopyJob3:: REPLACEREMOTEPREFIX**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) -Methode oder die [**IBackgroundCopyFile2:: Setup Report**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) Name-Methode zum Identifizieren eines neuen Servers oder Datei namens abrufen.</span><span class="sxs-lookup"><span data-stu-id="3ab15-122">However, if the error is caused by the server not being available or an invalid remote file, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) or [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method to identify a new server or file name.</span></span>

<span data-ttu-id="3ab15-123">Nachdem Sie die Ursache des Fehlers bestimmt haben, führen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="3ab15-123">After determining the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="3ab15-124">Brechen Sie den Auftrag ab, indem Sie die [**ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3ab15-124">Cancel the job by calling the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>
-   <span data-ttu-id="3ab15-125">Bei einem Download Auftrag wird die [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode aufgerufen, um die Dateien zu speichern, die vor dem Auftreten des Fehlers erfolgreich übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="3ab15-125">For a download job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method to save the files that transferred successfully before the error occurred.</span></span>
-   <span data-ttu-id="3ab15-126">Beheben Sie den Fehler, und wenden Sie die [**ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) -Methode an, um den Auftrag abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3ab15-126">Fix the error and call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method to finish the job.</span></span>

<span data-ttu-id="3ab15-127">Überprüfen Sie bei einem Upload-Antwort-Auftrag den Wert des **bytesTotal** -Members der Status Struktur der [**BG- \_ Auftrags \_ Antwort \_**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) , um zu ermitteln, ob der Fehler im Upload-oder Reply-Teil des Auftrags aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3ab15-127">For an upload-reply job, check the value of the **BytesTotal** member of the [**BG\_JOB\_REPLY\_PROGRESS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) structure to determine if the error occurred on the upload or reply portion of the job.</span></span> <span data-ttu-id="3ab15-128">Der Fehler ist beim Hochladen aufgetreten, wenn der Wert BG- \_ Größe \_ unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="3ab15-128">The error occurred on the upload if the value is BG\_SIZE\_UNKNOWN.</span></span>

<span data-ttu-id="3ab15-129">Im folgenden Beispiel wird gezeigt, wie ein [**ibackgroundcopyerror**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) -Schnittstellen Zeiger abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3ab15-129">The following example shows how to retrieve an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer.</span></span> <span data-ttu-id="3ab15-130">Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist.</span><span class="sxs-lookup"><span data-stu-id="3ab15-130">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




