---
title: Erstellen eines Auftrags
description: Um einen Übertragungs Auftrag zu erstellen, rufen Sie die Methode ibackgroundcopymanager kreatejob auf.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- Übertragen von Auftrags Bits
- Übertragen von Auftrags Bits, erstellen
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8dddb2427fde43014a31e81f72711ca74e69de34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470997"
---
# <a name="creating-a-job"></a><span data-ttu-id="3f583-105">Erstellen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="3f583-105">Creating a Job</span></span>

<span data-ttu-id="3f583-106">Um einen Übertragungs Auftrag zu erstellen, rufen Sie die [**ibackgroundcopymanager:: kreatejob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3f583-106">To create a transfer job, call the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span> <span data-ttu-id="3f583-107">Nachdem Bits den Auftrag erstellt hat, [fügen Sie dem Auftrag Dateien hinzu](adding-files-to-a-job.md) , und [Ändern Sie die Auftrags Eigenschaften](setting-and-retrieving-the-properties-of-a-job.md) entsprechend Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3f583-107">After BITS creates the job, [add files to the job](adding-files-to-a-job.md) and [modify the job's properties](setting-and-retrieving-the-properties-of-a-job.md) as appropriate for your application.</span></span> <span data-ttu-id="3f583-108">Um den Auftrag in der Warteschlange zu aktivieren, müssen Sie die [**ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="3f583-108">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method.</span></span>

<span data-ttu-id="3f583-109">Die Methode " [**kreatejob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) " erstellt eine GUID, die den Auftrag eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3f583-109">The [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method creates a GUID that uniquely identifies the job.</span></span> <span data-ttu-id="3f583-110">Verwenden Sie die GUID, um [den Auftrag aus der Übertragungs Warteschlange abzurufen](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="3f583-110">You use the GUID to [retrieve the job from the transfer queue](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span> <span data-ttu-id="3f583-111">Der Anzeige Name, den Sie beim Erstellen des Auftrags angeben, ist nicht eindeutig. mehrere Aufträge können denselben Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f583-111">The display name that you provide when you create the job is not unique; more than one job can use the same name.</span></span>

<span data-ttu-id="3f583-112">Bits schränkt die Anzahl der Aufträge in der Warteschlange auf 300 Aufträge und die Anzahl der Aufträge ein, die ein Benutzer in 60 Auftrag erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="3f583-112">BITS limits the number of jobs in the queue to 300 jobs and the number of jobs that a user can create to 60 job.</span></span> <span data-ttu-id="3f583-113">Diese Grenzwerte gelten nicht für Administratoren oder Dienste.</span><span class="sxs-lookup"><span data-stu-id="3f583-113">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="3f583-114">Informationen zum Ändern dieser Standard Limits finden Sie unter [Gruppenrichtlinien](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="3f583-114">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="3f583-115">Im folgenden Beispiel wird gezeigt, wie ein Download Auftrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3f583-115">The following example shows how to create a download job.</span></span> <span data-ttu-id="3f583-116">Im Beispiel wird davon ausgegangen, dass die g \_ pbcm-Variable ein gültiger [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstellen Zeiger ist.</span><span class="sxs-lookup"><span data-stu-id="3f583-116">The example assumes the g\_pbcm variable is a valid [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="3f583-117">Ausführliche Informationen zum Erstellen des **ibackgroundcopymanager** -Schnittstellen Zeigers finden Sie unter [Herstellen einer Verbindung mit dem BITS-Dienst](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="3f583-117">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


```C++
HRESULT hr;
GUID JobId;
IBackgroundCopyJob* pJob = NULL;

//To create an upload job, replace BG_JOB_TYPE_DOWNLOAD with 
//BG_JOB_TYPE_UPLOAD or BG_JOB_TYPE_UPLOAD_REPLY.
hr = g_pbcm->CreateJob(L"MyJobName", BG_JOB_TYPE_DOWNLOAD, &JobId, &pJob);
if (SUCCEEDED(hr))
{
  //Save the JobId for later reference. 
  //Modify the job's property values.
  //Add files to the job.
  //Activate (resume) the job in the transfer queue.
}
```



<span data-ttu-id="3f583-118">Um die aktuelle [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstelle abzurufen, nennen Sie die **ibackgroundcopyjob:: QueryInterface** -Methode.</span><span class="sxs-lookup"><span data-stu-id="3f583-118">To get the latest [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface, call the **IBackgroundCopyJob::QueryInterface** method.</span></span> <span data-ttu-id="3f583-119">Im folgenden Beispiel wird gezeigt, wie Sie die [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) -Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="3f583-119">The following example shows how to get the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface.</span></span>


```C++
  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJob5* pJob5 = NULL;

  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob5), (void**)&pJob5);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }
```



 

 




