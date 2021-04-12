---
title: Abrufen des Auftrags Status
description: Standardmäßig muss eine Anwendung Änderungen im Status eines Auftrags Abfragen.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- Übertragen von Auftrags Bits, Abrufen
- Abrufen von Auftragsstatus Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df7fcde49d7359ff8cfa38326eba1e1e0bfeac5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855531"
---
# <a name="polling-for-the-status-of-the-job"></a><span data-ttu-id="e6cd2-105">Abrufen des Auftrags Status</span><span class="sxs-lookup"><span data-stu-id="e6cd2-105">Polling for the Status of the Job</span></span>

<span data-ttu-id="e6cd2-106">Standardmäßig muss eine Anwendung Änderungen im Status eines Auftrags Abfragen.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-106">By default, an application must poll for changes in the status of a job.</span></span> <span data-ttu-id="e6cd2-107">Um Änderungen im Status des Auftrags aufzuzeichnen, müssen Sie die [**ibackgroundcopyjob:: GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-107">To capture changes in the job's state, call the [**IBackgroundCopyJob::GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) method.</span></span> <span data-ttu-id="e6cd2-108">Um Änderungen in der Anzahl der übertragenen Bytes und Dateien aufzuzeichnen, müssen Sie die [**ibackgroundcopyjob:: GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-108">To capture changes in the number of bytes and files transferred, call the [**IBackgroundCopyJob::GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) method.</span></span> <span data-ttu-id="e6cd2-109">Rufen Sie die [**IBackgroundCopyJob2:: getreplyprogress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) -Methode auf, um Statusinformationen über den Antwort Teil eines Upload-Antwort-Auftrags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-109">To retrieve progress information on the reply portion of an upload-reply job, call the [**IBackgroundCopyJob2::GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) method.</span></span> <span data-ttu-id="e6cd2-110">Ein Beispiel, in dem die Fortschrittsinformationen verwendet werden, finden Sie unter [bestimmen des Fortschritts eines Auftrags](determining-the-progress-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="e6cd2-110">For an example that uses the progress information, see [Determining the Progress of a Job](determining-the-progress-of-a-job.md).</span></span>

<span data-ttu-id="e6cd2-111">Die [**BG- \_ Auftrags \_ Status**](/windows/desktop/api/Bits/ne-bits-bg_job_state) -Enumeration definiert die Zustände eines Auftrags, und die Status Struktur der [**BG- \_ Aufträge \_**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) enthält Informationen zur Anzahl von Bytes und übertragenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-111">The [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration defines the states of a job, and the [**BG\_JOB\_PROGRESS**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) structure contains information on the number of bytes and files transferred.</span></span>

<span data-ttu-id="e6cd2-112">Zum Verwenden von Abruf müssen Sie einen Mechanismus zum Initiieren des Abruf Vorgangs erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-112">To use polling, you need to create a mechanism to initiate polling.</span></span> <span data-ttu-id="e6cd2-113">Erstellen Sie z. b. einen Timer, oder verwenden Sie die Schaltfläche "Aktualisieren" auf der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-113">For example, create a timer or use an "Update" button on the user interface.</span></span> <span data-ttu-id="e6cd2-114">Allerdings ist es möglicherweise einfacher, sich für Ereignis Benachrichtigungen zu registrieren und Ereignisse zu empfangen, wenn sich der Status oder der Fortschritt ändert.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-114">However, it might be easier to register for event notification and receive events when the state or progress changes.</span></span> <span data-ttu-id="e6cd2-115">Weitere Informationen zur Ereignis Benachrichtigung finden Sie unter [Registrieren eines com-Rückrufs](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="e6cd2-115">For information on event notification, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="e6cd2-116">Im folgenden Beispiel wird ein Timer verwendet, um den Status eines Auftrags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-116">The following example uses a timer to poll for the state of a job.</span></span> <span data-ttu-id="e6cd2-117">Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e6cd2-117">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_JOB_STATE State;
HANDLE hTimer = NULL;
LARGE_INTEGER liDueTime;
//IBackgroundCopyError* pError = NULL;
//BG_JOB_PROGRESS Progress;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

liDueTime.QuadPart = -10000000;  //Poll every 1 second
hTimer = CreateWaitableTimer(NULL, FALSE, L"MyTimer");
SetWaitableTimer(hTimer, &liDueTime, 1000, NULL, NULL, 0);

do
{
  WaitForSingleObject(hTimer, INFINITE);

  //Use JobStates[State] to set the window text in a user interface.
  hr = pJob->GetState(&State);
  if (FAILED(hr))
  {
    //Handle error
  }

  if (BG_JOB_STATE_TRANSFERRED == State)
    //Call pJob->Complete(); to acknowledge that the transfer is complete
    //and make the file available to the client.
  else if (BG_JOB_STATE_ERROR == State || BG_JOB_STATE_TRANSIENT_ERROR == State)
    //Call pJob->GetError(&pError); to retrieve an IBackgroundCopyError interface 
    //pointer which you use to determine the cause of the error.
  else if (BG_JOB_STATE_TRANSFERRING == State)
    //Call pJob->GetProgress(&Progress); to determine the number of bytes 
    //and files transferred.
} while (BG_JOB_STATE_TRANSFERRED != State && 
         BG_JOB_STATE_ERROR != State &&
         BG_JOB_STATE_TRANSIENT_ERROR != State);
CancelWaitableTimer(hTimer);
CloseHandle(hTimer);
```



 

 




