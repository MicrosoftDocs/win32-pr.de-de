---
title: Festlegen und Abrufen der Eigenschaften eines Auftrags
description: Der Besitzer des Auftrags oder ein Benutzer mit Administratorrechten kann die Eigenschaften des Auftrags jederzeit festlegen und abrufen.
ms.assetid: 5d0ab96b-b818-4b41-8317-cf50ad17c12d
keywords:
- Übertragen von Auftrags Bits, Eigenschaften
- Festlegen von Auftrags Eigenschaften Bits
- Abrufen von Auftrags Eigenschaften Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609299e3e7bdee477e2008f3f4ce83ae24583ffd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855468"
---
# <a name="setting-and-retrieving-the-properties-of-a-job"></a><span data-ttu-id="4c1f0-106">Festlegen und Abrufen der Eigenschaften eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="4c1f0-106">Setting and Retrieving the Properties of a Job</span></span>

<span data-ttu-id="4c1f0-107">Der Besitzer des Auftrags oder ein Benutzer mit Administratorrechten kann die Eigenschaften des Auftrags jederzeit festlegen und abrufen.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-107">The owner of the job or a user with administrator privileges can set and retrieve the properties of the job at any time.</span></span> <span data-ttu-id="4c1f0-108">Eine umfassende Liste der Eigenschaften, die Sie festlegen und abrufen können, finden Sie unter [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)-, [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)-, [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)-und [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-108">For a complete list of properties that you can set and retrieve, see the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2), [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3), and [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) interfaces.</span></span>

<span data-ttu-id="4c1f0-109">Dateien enthalten außerdem Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-109">Files also contain properties.</span></span> <span data-ttu-id="4c1f0-110">Informationen zum Abrufen einer Datei und ihrer Eigenschaften aus einem Auftrag finden Sie unter Auflisten von [Dateien in einem Auftrag](enumerating-files-in-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="4c1f0-110">For information on how to retrieve a file and its properties from a job, see [Enumerating Files in a Job](enumerating-files-in-a-job.md).</span></span>

<span data-ttu-id="4c1f0-111">Um Dateien zu übertragen, müssen Sie die Standardwerte der Eigenschaften des Auftrags nicht ändern – Bits verwendet die Standardwerte, die für die typische Anwendung geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-111">To transfer files, you do not need to change the default values of the job's properties—BITS uses default values that are appropriate for the typical application.</span></span>

## <a name="setting-the-properties-of-a-job"></a><span data-ttu-id="4c1f0-112">Festlegen der Eigenschaften eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="4c1f0-112">Setting the properties of a job</span></span>

<span data-ttu-id="4c1f0-113">Im folgenden Beispiel wird gezeigt, wie die Eigenschaften festgelegt werden, die am wahrscheinlichsten von Ihrer Anwendung geändert werden: [Priorität](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority), [Benachrichtigungs Schnittstelle](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface), [Benachrichtigungs-Flags](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)und [Antwort Dateiname](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setreplyfilename).</span><span class="sxs-lookup"><span data-stu-id="4c1f0-113">The following example shows how to set the properties that your application is most likely to change: [priority](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority), [notify interface](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface), [notify flags](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags), and [reply file name](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setreplyfilename).</span></span> <span data-ttu-id="4c1f0-114">Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger, pjob, gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-114">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob4* pJob4 = NULL;
CNotifyInterface *pNotify = new CNotifyInterface();

hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob4), (void**)&pJob4);
pJob->Release();

//The default priority level for a job is BG_JOB_PRIORITY_NORMAL. 
hr = pJob4->SetPriority(BG_JOB_PRIORITY_HIGH);
if (FAILED(hr))
{
  //Handle error
}

//By default, an application must poll BITS for the status of a job.
//To specify an IBackgroundCopyCallback interface pointer that receives event 
//notification based on the value of the notify flags property, set the notify 
//interface property. For details on the CNotifyInterface example class, see the 
//IBackgroundCopyCallback interface in the reference section.
hr = pJob4->SetNotifyInterface(pNotify);
if (SUCCEEDED(hr))
{
  hr = pJob4->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                            BG_NOTIFY_JOB_ERROR);
}
pNotify->Release();
if (FAILED(hr))
{
  //Handle error - failed to setup notification callbacks
}

//Only set the reply file name if the job's type is BG_JOB_TYPE_UPLOAD_REPLY.
//If you do not set the file name before calling the IBackgroundCopyJob::Resume 
//method, BITS generates a file name for you; the directory is the same as that
//specified for the local file name (the file being uploaded). To retrieve the 
//file name, call the IBackgroundCopyJob2::GetReplyFileName method.
hr = pJob4->SetReplyFileName(L"<REPLYPATHGOESHERE>");
if (FAILED(hr))
{
  //Handle error
}
pJob4->Release();
```



<span data-ttu-id="4c1f0-115">Standardmäßig lädt Bits Inhalt vom Ursprungsserver herunter.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-115">By default, BITS downloads content from the origin server.</span></span> <span data-ttu-id="4c1f0-116">Zum Herunterladen von Inhalten von einem Peer müssen der Computer und der Auftrag das Peer Caching aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-116">To download content from a peer, both the computer and the job must enable peer caching.</span></span> <span data-ttu-id="4c1f0-117">Um Peer Caching auf dem Computer zu aktivieren, legen Sie die Gruppenrichtlinien Einstellung enablepeercaching fest.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-117">To enable peer caching on the computer, set the EnablePeerCaching group policy setting.</span></span> <span data-ttu-id="4c1f0-118">Sie können auch die [**ibitspeercacheadministration:: setconfigurationflags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) -Methode aufrufen, um das Peer Caching auf dem Computer zu aktivieren. die Einstellungs Einstellung wird jedoch von der Richtlinie überschrieben, sofern festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-118">You can also call the [**IBitsPeerCacheAdministration::SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) method to enable peer caching on the computer; however, the preference setting is overridden by the policy, if set.</span></span> <span data-ttu-id="4c1f0-119">Um Peer Caching für den Auftrag zu aktivieren, müssen Sie die [**IBackgroundCopyJob4:: setpeercachingflags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-119">To enable peer caching for the job, you must call the [**IBackgroundCopyJob4::SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) method.</span></span>

<span data-ttu-id="4c1f0-120">Um benutzerdefinierte Header, ein Client Zertifikat für die Client Authentifizierung und http-Optionen wie Umleitungs Richtlinie, CRL-Prüfung und anzugeben, welche Zertifikat Fehler ignoriert werden sollen, verwenden Sie die [**ibackgroundcopyjobhttpoptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-120">To specify custom headers, a client certificate for client authentication, and HTTP options like redirection policy, CRL checking, and specifying which certificate errors to ignore, use the [**IBackgroundCopyJobHttpOptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) interface.</span></span> <span data-ttu-id="4c1f0-121">Um die **ibackgroundcopyjobhttpoptions** -Schnittstelle zu erhalten, Fragen Sie eine beliebige [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-121">To get the **IBackgroundCopyJobHttpOptions** interface, query any of the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interfaces.</span></span>

## <a name="retrieving-the-properties-of-a-job"></a><span data-ttu-id="4c1f0-122">Abrufen der Eigenschaften eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="4c1f0-122">Retrieving the properties of a job</span></span>

<span data-ttu-id="4c1f0-123">Das folgende Beispiel zeigt, wie Sie die Eigenschaftswerte " [Anzeige Name](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)", " [Besitzer](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner) [", "](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)Status" und " [Status](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) " eines Auftrags abrufen.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-123">The following example shows how to retrieve the [display name](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname), [owner](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner), [progress](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress), and [state](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) property values of a job.</span></span> <span data-ttu-id="4c1f0-124">Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger, pjob, gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4c1f0-124">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
WCHAR* pszJobName = NULL;
WCHAR* pszOwnerSid = NULL;
BOOL bResult;
DWORD dwNameSize = 0;
DWORD dwDomainSize = 0;
WCHAR* pszName = NULL;
WCHAR* pszDomain = NULL;
WCHAR* pszFullOwnerName = NULL;
PSID pSid = NULL;
SID_NAME_USE eNameUse;
BG_JOB_PROGRESS Progress;
int PercentOfFiles = 0;
BG_JOB_PRIORITY Priority;
BG_JOB_STATE State;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

//Name of the job to use in the user interface. The name is set when you 
//create the job. You can use the SetDisplayName method to change the name. 
hr = pJob->GetDisplayName(&pszJobName);
if (SUCCEEDED(hr))
{
  //Use the name in a user interface or output.
  CoTaskMemFree(pszJobName);       
}

//The owner property contains the SID of the job's owner. The following code
//shows how to get the domain and user names associated with the SID.
hr = pJob->GetOwner(&pszOwnerSID);
if (SUCCEEDED(hr))
{
  bResult = ConvertStringSidToSid(pszOwnerSid, &pSid);
  CoTaskMemFree(pszOwnerSid);
  if (bResult)
  {
    //Call LookupAccountSid twice. The first call retrieves the buffer size 
    //for name and domain and the second call retrieves the actual name and domain.
    LookupAccountSid(NULL, pSid, NULL, &cbNameSize, 
                               NULL, &cbDomainSize, &eNameUse);
    LastError = GetLastError();
    if (ERROR_INSUFFICIENT_BUFFER == LastError)
    {
      pszName = (WCHAR*)malloc(sizeof(WCHAR) * cbNameSize);
      pszDomain = (WCHAR*)malloc(sizeof(WCHAR) * cbDomainSize);
      if (pszName && pszDomain)
      {
        bResult = LookupAccountSid(NULL, pSid, pszName, &cbNameSize, 
                                   pszDomain, &cbDomainSize, &eNameUse);
        if (bResult)
        {
          pszFullName = (WCHAR*)malloc(sizeof(WCHAR)*(cbDomainSize+1+cbNameSize+1));
          if (pszFullName)
          {
            StringCchPrintf(pszFullName, cbDomainSize+1+cbNameSize+1, L"%s\\%s", pszDomain, pszName);
            //Do something with pszFullName. 
            free(pszFullName);
          }
        }
      }
      if (pszDomain)
        free(pszDomain);
      if(pszName)
        free(pszName);
    }
    else
    {
      //Handle error - most likely ERROR_NONE_MAPPED, could not find the SID.
    }
    LocalFree(pSid);
  }
}

//The state property identifies the current state of the job. For example, the 
//state of the job is BG_JOB_STATE_TRANSFERRING or BG_JOB_STATE_ERROR. 
hr = pJob->GetState(&State);
if (SUCCEEDED(hr))
{
  //Use JobStates[State] to set the text representation of the job's 
  //state in a user interface.
}

//Use the information contained in the BG_JOB_PROGRESS structure to determine the 
//overall progress of the job. The structure contains information on the number of 
//bytes and files transferred. 
hr = pJob->GetProgress(&Progress);
if (SUCCEEDED(hr))
{
  //Determine the progress of the job based on the number of files transferred.
  if (Progress.FilesTotal > 0)
  {
    PercentOfFiles = 100*Progress.FilesTransferred/Progress.FilesTotal
  }
  //For an example that shows determining the progress of the job based on the 
  //number of bytes transferred, see the topic Determing the Progress of a Job.
}
```



 

 




