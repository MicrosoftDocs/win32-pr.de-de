---
title: Steuern eines Bits-Downloads über eine teure Verbindung
description: Blockieren Sie das Herunterladen über eine teure Verbindung, z. b. eine Roaming-Verbindung.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- Herunterladen von Bits, Vorgehensweise
- Herunterladen von Bits, kostenaufwendig vermeiden
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 6326838f08f1879929d9a6be67ef94c4aa035e00
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857867"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a><span data-ttu-id="50c23-105">Steuern eines Bits-Downloads über eine teure Verbindung</span><span class="sxs-lookup"><span data-stu-id="50c23-105">Control a BITS download over an expensive connection</span></span>

<span data-ttu-id="50c23-106">In diesem Thema wird gezeigt, wie Sie das Herunterladen eines Bits-Auftrags über eine teure Verbindung blockieren, z. b. eine Roaming-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="50c23-106">This topic shows how to block a BITS job from downloading over an expensive connection such as a roaming cellular link.</span></span> <span data-ttu-id="50c23-107">Bits ist eine asynchrone API, in der die Anwendung einen Auftrag erstellt, URLs zu diesem Auftrag hinzufügt und die Funktion zum fort [**setzen des Auftrags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) Objekts aufruft.</span><span class="sxs-lookup"><span data-stu-id="50c23-107">BITS is an asynchronous API where the application creates a job, adds URLs to that job, and calls the job object's [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) function.</span></span> <span data-ttu-id="50c23-108">Ab diesem Punkt wählt Bits aus, wann der Auftrag basierend auf Faktoren wie der Auftrags Priorität und der Übertragungs Richtlinie heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="50c23-108">From that point, BITS chooses when the job downloads based on factors such as job priority and the transfer policy.</span></span> <span data-ttu-id="50c23-109">Nachdem der Auftrag abgeschlossen ist, wird die Anwendung von Bits benachrichtigt, dass die URL heruntergeladen wurde (sofern die Anwendung für die Abschluss Benachrichtigung registriert wurde).</span><span class="sxs-lookup"><span data-stu-id="50c23-109">After the job has finished downloading, BITS notifies the application that the URL has been downloaded (if the application has registered for completion notification).</span></span> <span data-ttu-id="50c23-110">Wenn während der Lebensdauer des Vorgangs das Netzwerk des Endbenutzers geändert wird – z. b. wenn der Benutzer unterwegs ist und aktuell Roaminggebühren anfallen –, hält Bits den Auftrag an, bis die Netzwerkbedingungen optimal sind.</span><span class="sxs-lookup"><span data-stu-id="50c23-110">During the job's lifetime, if the end user's network changes—such as if the user is traveling and is currently incurring roaming fees—then BITS will suspend the job until network conditions are optimal.</span></span> <span data-ttu-id="50c23-111">Die folgenden schrittweisen Anleitungen zeigen, wie Sie den Auftrag erstellen und die entsprechenden Übertragungs Richtlinien Einstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="50c23-111">The following step-by-step instructions show how to create the job and specify the appropriate transfer policy settings.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="50c23-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="50c23-112">Prerequisites</span></span>

-   <span data-ttu-id="50c23-113">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="50c23-113">Microsoft Visual Studio</span></span>

## <a name="instructions"></a><span data-ttu-id="50c23-114">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="50c23-114">Instructions</span></span>

### <a name="step-1-include-the-required-bits-header-files"></a><span data-ttu-id="50c23-115">Schritt 1: einschließen der erforderlichen Bits-Header Dateien</span><span class="sxs-lookup"><span data-stu-id="50c23-115">Step 1: Include the required BITS header files</span></span>

<span data-ttu-id="50c23-116">Fügen Sie die folgenden Header Direktiven am Anfang der Quelldatei ein.</span><span class="sxs-lookup"><span data-stu-id="50c23-116">Insert the following header directives at the top of the source file.</span></span>


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a><span data-ttu-id="50c23-117">Schritt 2: Initialisieren von com</span><span class="sxs-lookup"><span data-stu-id="50c23-117">Step 2: Initialize COM</span></span>

<span data-ttu-id="50c23-118">Vor dem Instanziieren der [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle (die zum Erstellen eines Bits-Auftrags verwendet wird) müssen Sie com initialisieren, das COM-Threading Modell festlegen und eine Identitätswechsel Ebene von mindestens RPC- \_ C \_ IMP- \_ Ebenen annehmen \_ .</span><span class="sxs-lookup"><span data-stu-id="50c23-118">Before instantiating the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface (used to create a BITS job), you must initialize COM, set the COM threading model, and specify an impersonation level of at least RPC\_C\_IMP\_LEVEL\_IMPERSONATE.</span></span>


```C++
// Initialize COM and specify the COM threading model.
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
 // Specify an impersonation level of at least RPC_C_IMP_LEVEL_IMPERSONATE.
 hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                           RPC_C_AUTHN_LEVEL_CONNECT,
                           RPC_C_IMP_LEVEL_IMPERSONATE,
                           NULL, EOAC_NONE, 0);
 if (SUCCEEDED(hr))
 {
  ...
```



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a><span data-ttu-id="50c23-119">Schritt 3: Instanziieren der ibackgroundcopymanager-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="50c23-119">Step 3: Instantiate the IBackgroundCopyManager interface</span></span>

<span data-ttu-id="50c23-120">Verwenden Sie die [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle zum Erstellen von Übertragungs Aufträgen, rufen Sie ein Enumeratorobjekt ab, das die Aufträge in der Warteschlange enthält, und rufen Sie einzelne Aufträge aus der Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="50c23-120">Use the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to create transfer jobs, retrieve an enumerator object that contains the jobs in the queue, and retrieve individual jobs from the queue.</span></span>


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a><span data-ttu-id="50c23-121">Schritt 4: Erstellen des Bits-Auftrags</span><span class="sxs-lookup"><span data-stu-id="50c23-121">Step 4: Create the BITS job</span></span>

<span data-ttu-id="50c23-122">Nur der Benutzer, der den Auftrag erstellt, oder ein Benutzer mit Administratorrechten kann dem Auftrag Dateien hinzufügen und die Eigenschaften des Auftrags ändern.</span><span class="sxs-lookup"><span data-stu-id="50c23-122">Only the user who creates the job or a user with administrator privileges can add files to the job and change the job's properties.</span></span>


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a><span data-ttu-id="50c23-123">Schritt 5: Angeben der Übertragungs Richtlinien Einstellung für den Auftrag</span><span class="sxs-lookup"><span data-stu-id="50c23-123">Step 5: Specify the transfer policy setting for the job</span></span>

<span data-ttu-id="50c23-124">An dieser Stelle geben Sie die Datenübertragungs Richtlinie für den Kosten Zustand an.</span><span class="sxs-lookup"><span data-stu-id="50c23-124">This is where you specify the cost state transfer policy.</span></span> <span data-ttu-id="50c23-125">\_ \_ Um die gewünschten Ergebnisse zu erzielen, können Sie mehrere Bits-Cost-State-Flags festlegen, indem Sie eine bitweise **or** -Kombination verwenden.</span><span class="sxs-lookup"><span data-stu-id="50c23-125">You can set several BITS\_COST\_STATE flags by using a bitwise **OR** combination to achieve the desired results.</span></span>


```C++
BITS_JOB_PROPERTY_VALUE propval;
IBackgroundCopyJob5* pBackgroundCopyJob5;

propval.Dword = BITS_COST_STATE_USAGE_BASED
              | BITS_COST_STATE_OVERCAP_THROTTLED
              | BITS_COST_STATE_BELOW_CAP
              | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
              | BITS_COST_STATE_UNRESTRICTED;

hr = pBackgroundCopyJob->QueryInterface(__uuidof(IBackgroundCopyJob5),
                                        reinterpret_cast<void**>(&pBackgroundCopyJob5));
if(SUCCEEDED(hr))
{
 pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);
}
```



## <a name="example"></a><span data-ttu-id="50c23-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="50c23-126">Example</span></span>

<span data-ttu-id="50c23-127">Im folgenden Codebeispiel wird gezeigt, wie die Übertragungs Richtlinie eines Bits-Auftrags so festgelegt wird, dass die Verarbeitung des Auftrags nicht stattfindet, während bestimmte Bedingungen erfüllt werden – z. b. wenn der Benutzer ein Roaming durchführt oder das monatliche Datenübertragungs Limit überschritten hat.</span><span class="sxs-lookup"><span data-stu-id="50c23-127">The following code example shows how to set a BITS job's transfer policy so that the processing of the job doesn't occur while certain conditions are met—such as when the user is roaming or has exceeded their monthly data transfer limit.</span></span>


```C++
//*********************************************************
//
//    Copyright (c) Microsoft. All rights reserved.
//    This code is licensed under the Microsoft Public License.
//    THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF
//    ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY
//    IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR
//    PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.
//
//*********************************************************

#define WIN32_LEAN_AND_MEAN             // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <stdio.h> // define wprintf


int main()
{
 HRESULT hr = S_OK;
 GUID guidJob;
 IBackgroundCopyJob5* pBackgroundCopyJob5;  
 IBackgroundCopyJob* pBackgroundCopyJob;
 IBackgroundCopyManager* pQueueMgr;
 BITS_JOB_PROPERTY_VALUE propval;

 // Specify the COM threading model.
 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 if (SUCCEEDED(hr))
 {
  // The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
  hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                            RPC_C_AUTHN_LEVEL_CONNECT,
                            RPC_C_IMP_LEVEL_IMPERSONATE,
                            NULL, EOAC_NONE, 0);

  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(__uuidof(BackgroundCopyManager), 
                         NULL,
                         CLSCTX_LOCAL_SERVER,
                         __uuidof(IBackgroundCopyManager),
                         (void **)&pQueueMgr);

   if (FAILED(hr))
   {
    // Failed to connect to BITS.
    wprintf(L"Failed to connect to BITS with error %x\n",hr);
    goto done;
   }

   // Create a BITS job.
   wprintf(L"Creating Job...\n");

   hr = pQueueMgr->CreateJob(L"TransferPolicy",
                             BG_JOB_TYPE_DOWNLOAD,
                             &guidJob,
                             (IBackgroundCopyJob **)&pBackgroundCopyJob);

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }

   wprintf(L" Job is succesfully created ...\n");

   // Set the Transfer Policy for the job.
   propval.Dword = BITS_COST_STATE_USAGE_BASED 
                 | BITS_COST_STATE_OVERCAP_THROTTLED
                 | BITS_COST_STATE_BELOW_CAP
                 | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
                 | BITS_COST_STATE_UNRESTRICTED;

   hr = pBackgroundCopyJob->QueryInterface(
         __uuidof(IBackgroundCopyJob5),
         reinterpret_cast<void**>(&pBackgroundCopyJob5)
        );

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }
   pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);

   // Get the Transfer Policy for the new job.
   BITS_JOB_PROPERTY_VALUE actual_propval;

   wprintf(L"Getting TransferPolicy Property ...\n");

   hr = pBackgroundCopyJob5->GetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, 
                                         &actual_propval);
   if (FAILED(hr))
   {
    // SetSSLSecurityFlags failed.
    wprintf(L"GetProperty failed with error %x\n",hr);
    goto cancel;
   }

   DWORD job_transferpolicy = actual_propval.Dword;
   wprintf(L"get TransferPolicy Property returned %#x\n", job_transferpolicy);
  }
done:
  CoUninitialize();
 }
 return 1;

cancel:
 pBackgroundCopyJob->Cancel(); 
 pBackgroundCopyJob->Release();
 goto done;
}
```



 

 




