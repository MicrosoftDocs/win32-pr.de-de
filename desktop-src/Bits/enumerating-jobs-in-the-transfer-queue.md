---
title: Auflisten von Aufträgen in der Übertragungs Warteschlange
description: Um Aufträge aus der Übertragungs Warteschlange aufzulisten, müssen Sie die ibackgroundcopymanager-EnumJobs-Methode aufzurufen. Die-Methode gibt einen ienumbackgroundcopyjobs-Schnittstellen Zeiger zurück, den Sie zum Auflisten der Aufträge in der Warteschlange verwenden.
ms.assetid: ebeb1670-dedd-4791-914e-d035d3c22c5a
keywords:
- Übertragen von Auftrags Bits, aufzählen
- Auflisten von Aufträgen in den Bits der Übertragungs Warteschlange
- Warteschlangen Bits übertragen, enumerieren
- Auflisten von Bits
- Auflisten von Bits, Aufträgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9360043a9265248001dddb785edab3e8aac70abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309319"
---
# <a name="enumerating-jobs-in-the-transfer-queue"></a><span data-ttu-id="5b6b4-109">Auflisten von Aufträgen in der Übertragungs Warteschlange</span><span class="sxs-lookup"><span data-stu-id="5b6b4-109">Enumerating Jobs in the Transfer Queue</span></span>

<span data-ttu-id="5b6b4-110">Um Aufträge aus der Übertragungs Warteschlange aufzulisten, müssen Sie die [**ibackgroundcopymanager:: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-110">To enumerate jobs from the transfer queue, call the [**IBackgroundCopyManager::EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="5b6b4-111">Die-Methode gibt einen [**ienumbackgroundcopyjobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) -Schnittstellen Zeiger zurück, den Sie zum Auflisten der Aufträge in der Warteschlange verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-111">The method returns an [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) interface pointer that you use to enumerate the jobs in the queue.</span></span>

<span data-ttu-id="5b6b4-112">Legen Sie den ersten Parameter der [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) -Methode auf 0 fest, um die Aufträge des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-112">To retrieve the user's jobs, set the first parameter of the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method to 0.</span></span> <span data-ttu-id="5b6b4-113">Um alle Aufträge in der Warteschlange abzurufen, legen Sie den ersten Parameter der **EnumJobs** -Methode auf BG \_ Job \_ Enum \_ All \_ Users fest.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-113">To retrieve all jobs in the queue, set the first parameter of the **EnumJobs** method to BG\_JOB\_ENUM\_ALL\_USERS.</span></span> <span data-ttu-id="5b6b4-114">Nur Benutzer mit Administratorrechten können alle Aufträge in der Übertragungs Warteschlange abrufen.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-114">Only users with administrator privileges can retrieve all jobs in the transfer queue.</span></span>

<span data-ttu-id="5b6b4-115">Beachten Sie, dass es sich bei der aufgelisteten Liste um eine Momentaufnahme der Aufträge in der Übertragungs Warteschlange handelt, wenn Sie die [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-115">Note that the enumerated list is a snapshot of the jobs in the transfer queue at the time you call the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="5b6b4-116">Die Eigenschaftswerte dieser Aufträge entsprechen jedoch den aktuellen Werten des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-116">However, the property values of those jobs reflect the current values of the job.</span></span>

<span data-ttu-id="5b6b4-117">Wenn Sie einzelne Übertragungs Aufträge abrufen möchten, rufen Sie die [**ibackgroundcopymanager:: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-117">If you want to retrieve individual transfer jobs, call the [**IBackgroundCopyManager::GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) method.</span></span>

<span data-ttu-id="5b6b4-118">Informationen zum Aufzählen von Dateien in einem Auftrag finden Sie unter Auflisten von [Dateien in einem Auftrag](enumerating-files-in-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="5b6b4-118">To enumerate files in a job, see [Enumerating Files in a Job](enumerating-files-in-a-job.md).</span></span>

<span data-ttu-id="5b6b4-119">Im folgenden Beispiel wird gezeigt, wie Aufträge in der Übertragungs Warteschlange aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-119">The following example shows how to enumerate jobs in the transfer queue.</span></span> <span data-ttu-id="5b6b4-120">Die \_ Variable g xfermanager im Beispiel ist ein [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="5b6b4-120">The g\_XferManager variable in the example is an [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="5b6b4-121">Ausführliche Informationen zum Erstellen des **ibackgroundcopymanager** -Schnittstellen Zeigers finden Sie unter [Herstellen einer Verbindung mit dem BITS-Dienst](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="5b6b4-121">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


```C++
HRESULT hr = 0;
IEnumBackgroundCopyJobs* pJobs = NULL;
IBackgroundCopyJob* pJob = NULL;
ULONG cJobCount = 0;
ULONG idx = 0;

//This example enumerates all jobs in the transfer queue. This call fails if the 
//current user does not have administrator privileges. To enumerate jobs for only 
//the current user, replace BG_JOB_ENUM_ALL_USERS with 0.
hr = g_XferManager->EnumJobs(BG_JOB_ENUM_ALL_USERS, &pJobs);
if (SUCCEEDED(hr))
{
  //Get the count of jobs in the queue. 
  pJobs->GetCount(&cJobCount);

  //Enumerate the jobs in the queue.
  for (idx=0; idx<cJobCount; idx++)
  {
    hr = pJobs->Next(1, &pJob, NULL);
    if (S_OK == hr)
    {
      //Retrieve or set job properties.

      pJob->Release();
      pJob = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pJobs->Release();
  pJobs = NULL;
}
```



 

 




