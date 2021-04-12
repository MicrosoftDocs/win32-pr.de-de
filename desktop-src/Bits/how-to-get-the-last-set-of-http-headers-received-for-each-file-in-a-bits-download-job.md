---
title: So erhalten Sie den letzten Satz von HTTP-Headern, die für jede Datei in einem Bits-Download Auftrag empfangen wurden
description: In diesem Beispiel wird gezeigt, wie die GetProperty-Methode der neuen IBackgroundCopyJob5-Schnittstelle verwendet wird, um die letzten festgelegten HTTP-Header für jede Datei in einem Background Intelligent Transfer Service (Bits)-Download Auftrag abzurufen.
ms.assetid: 38808AB2-0D7A-46C6-A666-F3E0DB8A3009
keywords:
- Herunterladen von Bits, HTTP-Header
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 0b7858d5b2467f52681b325e2bfbe65b96889e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206359"
---
# <a name="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job"></a><span data-ttu-id="0832b-104">So erhalten Sie den letzten Satz von HTTP-Headern, die für jede Datei in einem Bits-Download Auftrag empfangen wurden</span><span class="sxs-lookup"><span data-stu-id="0832b-104">How to get the last set of HTTP headers received for each file in a BITS download job</span></span>

<span data-ttu-id="0832b-105">In diesem Beispiel wird gezeigt, wie die [**GetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-getproperty) -Methode der neuen [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) -Schnittstelle verwendet wird, um die letzten festgelegten HTTP-Header für jede Datei in einem Background Intelligent Transfer Service (Bits)-Download Auftrag abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0832b-105">This sample shows how to use the new [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface's [**GetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-getproperty) method to obtain the last set HTTP headers received for each file in a Background Intelligent Transfer Service (BITS) download job.</span></span> <span data-ttu-id="0832b-106">Die Informationen im HTTP-Header können z. b. verwendet werden, um den Dateityp oder den Zeitpunkt der letzten Änderung auf dem Server zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="0832b-106">The information in the HTTP header could be used, for example, to determine the file type or when it last changed on the server.</span></span> <span data-ttu-id="0832b-107">Vor Windows 8 und Windows Server 2012 bot Bits keine Methode, mit der die Anwendung die HTTP-Antwortheader eines abgeschlossenen Downloads abrufen und überprüfen konnte.</span><span class="sxs-lookup"><span data-stu-id="0832b-107">Prior to Windows 8 and Windows Server 2012, BITS did not provide a means by which the application could retrieve and inspect the HTTP response headers of a completed download.</span></span> <span data-ttu-id="0832b-108">Dieses Beispiel zeigt, wie Sie mit der Bits-API einen BITS-Auftrag mit mehreren zu ladenden URLs erstellen, die URLs in einem Auftrag auflisten und die HTTP-Antwortheader für jede URL abrufen.</span><span class="sxs-lookup"><span data-stu-id="0832b-108">This sample shows how to use the BITS API to create a BITS job with multiple URLs to download, list the URLs in a job, and retrieve the HTTP response headers for each URL.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0832b-109">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="0832b-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0832b-110">Technologien</span><span class="sxs-lookup"><span data-stu-id="0832b-110">Technologies</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0832b-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0832b-111">Prerequisites</span></span>

-   <span data-ttu-id="0832b-112">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0832b-112">Microsoft Visual Studio</span></span>

## <a name="instructions"></a><span data-ttu-id="0832b-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="0832b-113">Instructions</span></span>

### <a name="step-1-include-the-required-bits-header-files"></a><span data-ttu-id="0832b-114">Schritt 1: einschließen der erforderlichen Bits-Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0832b-114">Step 1: Include the required BITS header files</span></span>

<span data-ttu-id="0832b-115">Fügen Sie die folgenden Header Direktiven am Anfang der Quelldatei ein.</span><span class="sxs-lookup"><span data-stu-id="0832b-115">Insert the following header directives at the top of the source file.</span></span>


```C++
#include <bits.h>
```



### <a name="step-2-initialize-com-and-instantiate-a-bits-background-copy-manager-object-interface"></a><span data-ttu-id="0832b-116">Schritt 2: Initialisieren von com und Instanziieren einer BITS-Background-Kopier-Manager-Objektschnittstelle</span><span class="sxs-lookup"><span data-stu-id="0832b-116">Step 2: Initialize COM and instantiate a BITS Background Copy Manager object interface</span></span>

<span data-ttu-id="0832b-117">Vor dem Instanziieren der [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle (die zum Erstellen eines Bits-Auftrags verwendet wird) müssen Sie com initialisieren und das gewünschte com-Threading Modell festlegen.</span><span class="sxs-lookup"><span data-stu-id="0832b-117">Before instantiating the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface (used to create a BITS job), you must initialize COM and set the desired COM threading model.</span></span>


```C++
// Initialize COM and specify the appropriate COM threading model for your application.
IBackgroundCopyManager* pManager;

HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
 hr = CoCreateInstance(__uuidof(BackgroundCopyManager), 
                       NULL,
                       CLSCTX_LOCAL_SERVER,
                       __uuidof(IBackgroundCopyManager),
                       (void**) &pManager);
}
```



### <a name="step-3-create-the-bits-job"></a><span data-ttu-id="0832b-118">Schritt 3: Erstellen des Bits-Auftrags</span><span class="sxs-lookup"><span data-stu-id="0832b-118">Step 3: Create the BITS job</span></span>

<span data-ttu-id="0832b-119">Nur der Benutzer, der den Auftrag erstellt, oder ein Benutzer mit Administratorrechten kann dem Auftrag Dateien hinzufügen und die Eigenschaften des Auftrags ändern.</span><span class="sxs-lookup"><span data-stu-id="0832b-119">Only the user who creates the job or a user with administrator privileges can add files to the job and change the job's properties.</span></span>


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pManager->CreateJob(L"TransferPolicy",
                         BG_JOB_TYPE_DOWNLOAD,
                         &guidJob,
                         (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-4-add-the-files-to-the-bits-job"></a><span data-ttu-id="0832b-120">Schritt 4: Hinzufügen der Dateien zum BITS-Auftrag</span><span class="sxs-lookup"><span data-stu-id="0832b-120">Step 4: Add the files to the BITS job</span></span>

<span data-ttu-id="0832b-121">Im folgenden Beispiel werden öffentlich verfügbare Dokumente aus dem Microsoft Download Center heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="0832b-121">The following example downloads publicly available documents from the Microsoft Download Center.</span></span> <span data-ttu-id="0832b-122">Sie müssen diese Werte für Ihre jeweilige Umgebung ändern.</span><span class="sxs-lookup"><span data-stu-id="0832b-122">You'll need to change these values for your specific environment.</span></span>


```C++
// Array that contains multiple DOWNLOAD_FILE data structures that represent the 
// files that will be added to the download job.
DOWNLOAD_FILE FileList[] =
{
 {
  L"https://download.microsoft.com/download/0/2/8/02809141-3329-4412-8AC4-AA41B406055C/WinRT81-HttpClient-BT-Socket-Poster.pdf",
  L"c:\\temp\\data\\WinRT81-HttpClient-BT-Socket-Poster.pdf"
 },
 {
  L"https://download.microsoft.com/download/6/6/2/662DD05E-BAD7-46EF-9431-135F9BAE6332/9781509302963_Microsoft%20Azure%20Essentials%20Fundamentals%20of%20Azure%202nd%20ed%20pdf.pdf",
  L"c:\\temp\\data\\Fundamentals of Azure.pdf"
 },
 {
  L"https://aka.ms/WinServ16/StndPDF",
  L"c:\\temp\\data\\IntroducingWindowsServer2016.pdf"
 }
};

...

// Add the files to the job.
for (int i=0; i < ARRAY_LENGTH(FileList); ++i)
{
 hr = Job->AddFile(FileList[i].RemoteFile,
                   FileList[i].LocalFile);
 ...
}
```



### <a name="step-5-start-the-bits-job"></a><span data-ttu-id="0832b-123">Schritt 5: Starten des Bits-Auftrags</span><span class="sxs-lookup"><span data-stu-id="0832b-123">Step 5: Start the BITS job</span></span>

<span data-ttu-id="0832b-124">Nach dem Einrichten des Bits-Auftrags können Sie die Funktion " [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) " der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstelle zum Starten oder Fortsetzen des Downloads abrufen.</span><span class="sxs-lookup"><span data-stu-id="0832b-124">After setting up the BITS job, call the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface's [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) function to start or continue the download.</span></span>


```C++
// Start the BITS job. 
hr = pBackgroundJob->Resume();
```



### <a name="step-6-monitor-and-display-the-bits-jobs-progress"></a><span data-ttu-id="0832b-125">Schritt 6: überwachen und Anzeigen des Status des Bits-Auftrags</span><span class="sxs-lookup"><span data-stu-id="0832b-125">Step 6: Monitor and display the BITS job's progress</span></span>

<span data-ttu-id="0832b-126">Die `MonitorJobProgress` Hilfsfunktion nimmt ein [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Objekt als einzigen Parameter an und fragt den Auftrag für einen Status alle 500 Millisekunden ab.</span><span class="sxs-lookup"><span data-stu-id="0832b-126">The `MonitorJobProgress` helper function takes an [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) object as its only parameter and polls the job for a status every 500 milliseconds.</span></span> <span data-ttu-id="0832b-127">Diese Funktion wird erst zurückgegeben, wenn der Auftrag abgeschlossen oder abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="0832b-127">This function does not return until the job has completed or been canceled.</span></span>


```C++
HRESULT MonitorJobProgress(__in IBackgroundCopyJob* Job)
{ 
 HRESULT hr;
 LPWSTR JobName;
 BG_JOB_STATE State;
 int PreviousState = -1;
 bool Exit = false;
 int ProgressCounter = 0;
 hr = Job->GetDisplayName(&JobName);
 printf("Progress report for download job '%ws'.\n", JobName);
 CoTaskMemFree(JobName);

 // Display the download progress.
 while (!Exit)
 {
  hr = Job->GetState(&State);
  if (State != PreviousState)
  {
   switch(State)
   {
    case BG_JOB_STATE_QUEUED:
     printf("Job is in the queue and waiting to run.\n");
    break;
    case BG_JOB_STATE_CONNECTING:
     printf("BITS is trying to connect to the remote server.\n");    
    break;

    case BG_JOB_STATE_TRANSFERRING:
     printf("BITS has started downloading data.\n");  
     DisplayProgress( Job );
    break;

    case BG_JOB_STATE_ERROR:
     wprintf(L"ERROR: BITS has encountered a non-recoverable error.\n");
     DisplayError(Job);
     wprintf(L"       Exiting job.\n");
     Exit = true;
     break;

    case BG_JOB_STATE_TRANSIENT_ERROR:
     wprintf(L"ERROR: BITS has encountered a recoverable error.\n");
     DisplayError(Job);
     wprintf(L"       Continuing to retry.\n");
     break;

    case BG_JOB_STATE_TRANSFERRED:
     DisplayProgress(Job);
     printf("The job has been successfully completed.\n");
     printf("Finalizing local files.\n");
     Job->Complete();
    break;

    case BG_JOB_STATE_ACKNOWLEDGED:
     printf("Finalization complete.\n");
     Exit = true;
    break;

    case BG_JOB_STATE_CANCELLED:
     printf("WARNING: The job has been cancelled.\n");   
     Exit = true;
    break;

    default:
     printf("WARNING: Unknown BITS state %d.\n", State);    
     Exit = true;
   }

   PreviousState = State;
  }
  else if (State == BG_JOB_STATE_TRANSFERRING)
  {
   // Display job progress every 2 seconds.
   if (++ProgressCounter % TWO_SECOND_LOOP == 0)
   {
    DisplayProgress( Job );
   } 
  }
  Sleep(HALF_SECOND_AS_MILLISECONDS);
 }
 printf("\n");
 return hr;
}

// Display the current progress of the job in terms of the amount of data
// and number of files transferred.
VOID DisplayProgress(__in IBackgroundCopyJob *Job)
{
 HRESULT hr;
 BG_JOB_PROGRESS Progress;
 hr = Job->GetProgress(&Progress);
 if (SUCCEEDED(hr))
 {
  printf("%llu of %llu bytes transferred (%lu of %lu files).\n",
         Progress.BytesTransferred, Progress.BytesTotal,
         Progress.FilesTransferred, Progress.FilesTotal);
 }
}
```



### <a name="step-7-display-the-downloaded-file-headers"></a><span data-ttu-id="0832b-128">Schritt 7: Anzeigen der heruntergeladenen Dateiheader</span><span class="sxs-lookup"><span data-stu-id="0832b-128">Step 7: Display the downloaded file headers</span></span>

<span data-ttu-id="0832b-129">Die `DisplayFileHeaders` Hilfsfunktion listet die Aufträge auf, die für ein [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Objekt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0832b-129">The `DisplayFileHeaders` helper function enumerates the jobs defined for an [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) object.</span></span>


```C++
// For each file in the job, obtain and display the HTTP header received server.
HRESULT DisplayFileHeaders(__in IBackgroundCopyJob *Job)
{
 HRESULT hr;
 IEnumBackgroundCopyFiles *FileEnumerator;
 
 hr = Job->EnumFiles(&FileEnumerator);
 if (SUCCEEDED(hr))
 {
  ULONG Count;

  hr = FileEnumerator->GetCount(&Count);
  if (SUCCEEDED(hr))
  {
   for (ULONG i=0; i < Count; ++i)
   {
    IBackgroundCopyFile *TempFile;

    hr = FileEnumerator->Next(1, &TempFile, NULL);
    if (SUCCEEDED(hr))
    {
     IBackgroundCopyFile5 *File;
     hr = TempFile->QueryInterface(__uuidof( IBackgroundCopyFile5 ), (void **) &File);
     if (SUCCEEDED(hr))
     {
      LPWSTR RemoteFileName;
      hr = File->GetRemoteName(&RemoteFileName);
      if (SUCCEEDED(hr))
      {
       printf("HTTP headers for remote file '%ws'\n", RemoteFileName );
       CoTaskMemFree( RemoteFileName );
       RemoteFileName = NULL;
      }

      BITS_FILE_PROPERTY_VALUE Value;
      hr = File->GetProperty(BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS, &Value);
      if (SUCCEEDED(hr) && Value.String)
      {
       printf("Headers: %ws\n", Headers );

       CoTaskMemFree(Value.String);
       Value.String = NULL;
      }

      File->Release();
      File = NULL;
     }

     TempFile->Release();
     TempFile = NULL;
    }
   }
  }

   FileEnumerator->Release();
   FileEnumerator = NULL;
 }

 return S_OK;
}
```



## <a name="example"></a><span data-ttu-id="0832b-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0832b-130">Example</span></span>

<span data-ttu-id="0832b-131">Das folgende Codebeispiel ist eine voll Funktions volle Konsolenanwendung, die zeigt, wie Sie mit der Bits-API einen BITS-Auftrag mit mehreren URLs zum Herunterladen erstellen, die URLs in einem Auftrag auflisten und die HTTP-Antwortheader für jede URL abrufen.</span><span class="sxs-lookup"><span data-stu-id="0832b-131">The following code example is a fully working console application that shows how to use the BITS API to create a BITS job with multiple URLs to download, list the URLs in a job, and retrieve the HTTP response headers for each URL.</span></span>


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

#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <stdio.h> // needed for wprintf
#include <strsafe.h>

#define ARRAY_LENGTH(x) (sizeof(x) / sizeof( *(x) ))

// Definition of constants.
static const unsigned int HALF_SECOND_AS_MILLISECONDS = 500;
static const unsigned int TWO_SECOND_LOOP = 2000 / HALF_SECOND_AS_MILLISECONDS;

// Simple data structure that contains the remote and local names for a file.
typedef struct
{
 LPCWSTR RemoteFile;
 LPCWSTR LocalFile;
} DOWNLOAD_FILE;

// Array that contains sample DOWNLOAD_FILE data structures that represent the files
// that will be added to the download job.
DOWNLOAD_FILE FileList[] =
{
 {
  L"https://download.microsoft.com/download/0/2/8/02809141-3329-4412-8AC4-AA41B406055C/WinRT81-HttpClient-BT-Socket-Poster.pdf",
  L"c:\\temp\\data\\WinRT81-HttpClient-BT-Socket-Poster.pdf"
 },
 {
  L"https://download.microsoft.com/download/6/6/2/662DD05E-BAD7-46EF-9431-135F9BAE6332/9781509302963_Microsoft%20Azure%20Essentials%20Fundamentals%20of%20Azure%202nd%20ed%20pdf.pdf",
  L"c:\\temp\\data\\Fundamentals of Azure.pdf"
 },
 {
  L"https://aka.ms/WinServ16/StndPDF",
  L"c:\\temp\\data\\IntroducingWindowsServer2016.pdf"
 }
};

// Forward declaration of functions.
HRESULT GetBackgroundCopyManager(__out IBackgroundCopyManager **Manager);
HRESULT CreateDownloadJob(__in LPCWSTR Name, __in IBackgroundCopyManager *Manager, __out IBackgroundCopyJob **Job);
HRESULT MonitorJobProgress(__in IBackgroundCopyJob *Job);
HRESULT DisplayFileHeaders(__in IBackgroundCopyJob *Job);
VOID    DisplayProgress(__in IBackgroundCopyJob *Job);
VOID    DisplayHeaders(__in LPWSTR Headers);
VOID    DisplayError(__in IBackgroundCopyJob *Job);

// Main program entry point.
int wmain(int argc, wchar_t* argv[])
{
 HRESULT hr;
 IBackgroundCopyManager *Manager;

 // Get the BITS Background Copy Manager.
 hr = GetBackgroundCopyManager(&Manager);
 if (SUCCEEDED(hr))
 {
  IBackgroundCopyJob *Job;

  // Create a new download job.
  hr = CreateDownloadJob(L"MyJob", Manager, &Job);
  if (SUCCEEDED(hr))
  {
   // Add files to the job.
   for (int i = 0; i < ARRAY_LENGTH(FileList); ++i)
   {
    hr = Job->AddFile(FileList[i].RemoteFile, FileList[i].LocalFile);
    if (FAILED(hr))
    {
     wprintf(L"Error: Unable to add remote file '%ws' to the download job (error %08X).\n",
      FileList[i].RemoteFile,
      hr);
    }
    else
    {
     wprintf(L"Downloading remote file '%ws' to local file '%ws'\n",
      FileList[i].RemoteFile, FileList[i].LocalFile);
    }
   }

   // Start the job and display its progress.
   hr = Job->Resume();
   if (FAILED(hr))
   {
    wprintf(L"ERROR: Unable to start the BITS download job (error code %08X).\n", hr);
   }
   else
   {
    MonitorJobProgress(Job);
   }

   // Release the BITS IBackgroundCopyJob interface.
   Job->Release();
   Job = NULL;
  }

  // Release the IBackgroundCopyManager interface.
  Manager->Release();
  Manager = NULL;
 }

 return 0;
}

/**
 * Gets a pointer to the BITS Background Copy Manager.
 *
 * If successful, this function returns a success code and sets the
 * referenced IBackgroundCopyFileManager interface pointer to a
 * reference counted instance of the Background Copy Manager interface.
 */
HRESULT GetBackgroundCopyManager(__out IBackgroundCopyManager **Manager)
{
 HRESULT hr;

 //Specify the appropriate COM threading model for your application.
 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 if (SUCCEEDED(hr))
 {
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
   NULL,
   CLSCTX_LOCAL_SERVER,
   __uuidof(IBackgroundCopyManager),
   (void**)Manager);
 }
 else
 {
  wprintf(L"ERROR: Unable to initialize COM (error code %08X).\n", hr);
 }

 return hr;
}

/**
 * Creates a new download job with the specified name.
 */
HRESULT CreateDownloadJob(__in LPCWSTR Name, __in IBackgroundCopyManager *Manager, __out IBackgroundCopyJob **Job)
{
 GUID guid;
 return Manager->CreateJob(Name, BG_JOB_TYPE_DOWNLOAD, &guid, Job);
}

/**
 * Monitors and displays the progress of the download job.
 *
 * A new status message is output whenever the job's status changes or,
 * when transferring data, every 2 seconds displays how much data
 * has been transferred.
 */
HRESULT MonitorJobProgress(__in IBackgroundCopyJob *Job)
{
 HRESULT hr;
 LPWSTR JobName;
 BG_JOB_STATE State;
 int PreviousState = -1;
 bool Exit = false;
 int ProgressCounter = 0;

 hr = Job->GetDisplayName(&JobName);
 wprintf(L"Progress report for download job '%ws'.\n", JobName);
 CoTaskMemFree(JobName);

 // Display the download progress.
 while (!Exit)
 {
  hr = Job->GetState(&State);

  if (State != PreviousState)
  {
   switch (State)
   {
   case BG_JOB_STATE_QUEUED:
    wprintf(L"Job is in the queue and waiting to run.\n");
    break;

   case BG_JOB_STATE_CONNECTING:
    wprintf(L"BITS is trying to connect to the remote server.\n");
    break;

   case BG_JOB_STATE_TRANSFERRING:
    wprintf(L"BITS has started downloading data.\n");
    DisplayProgress(Job);
    break;

   case BG_JOB_STATE_ERROR:
    wprintf(L"ERROR: BITS has encountered a non-recoverable error.\n");
    DisplayError(Job);
    wprintf(L"       Exiting job.\n");
    Exit = true;
    break;

   case BG_JOB_STATE_TRANSIENT_ERROR:
    wprintf(L"ERROR: BITS has encountered a recoverable error.\n");
    DisplayError(Job);
    wprintf(L"       Continuing to retry.\n");
    break;

   case BG_JOB_STATE_TRANSFERRED:
    DisplayProgress(Job);
    wprintf(L"The job has been successfully completed.\n");
    wprintf(L"Finalizing local files.\n");
    Job->Complete();
    break;

   case BG_JOB_STATE_ACKNOWLEDGED:
    wprintf(L"Finalization complete.\n");
    Exit = true;
    break;

   case BG_JOB_STATE_CANCELLED:
    wprintf(L"WARNING: The job has been cancelled.\n");
    Exit = true;
    break;

   default:
    wprintf(L"WARNING: Unknown BITS state %d.\n", State);
    Exit = true;
   }

   PreviousState = State;
  }
  else if (State == BG_JOB_STATE_TRANSFERRING)
  {
   // Display job progress every 2 seconds.
   if (++ProgressCounter % TWO_SECOND_LOOP == 0)
   {
    DisplayProgress(Job);
   }
  }
  Sleep(HALF_SECOND_AS_MILLISECONDS);
 }

 wprintf(L"\n");

 if (SUCCEEDED(hr))
 {
  hr = DisplayFileHeaders(Job);
 }

 return hr;
}

/**
 * For each file in the job, obtains the (final) HTTP headers received from the
 * remote server that hosts the files and then displays the HTTP headers.
 */
HRESULT DisplayFileHeaders(__in IBackgroundCopyJob *Job)
{
 HRESULT hr;
 IEnumBackgroundCopyFiles *FileEnumerator;

 wprintf(L"Individual file information.\n");

 hr = Job->EnumFiles(&FileEnumerator);
 if (FAILED(hr))
 {
  wprintf(L"WARNING: Unable to obtain an IEnumBackgroundCopyFiles interface.\n");
  wprintf(L"         No further information can be provided about the files in the job.\n");
 }
 else
 {
  ULONG Count;

  hr = FileEnumerator->GetCount(&Count);
  if (FAILED(hr))
  {
   wprintf(L"WARNING: Unable to obtain a count of the number of files in the job.\n");
   wprintf(L"        No further information can be provided about the files in the job.\n");
  }
  else
  {
   for (ULONG i = 0; i < Count; ++i)
   {
    IBackgroundCopyFile *TempFile;

    hr = FileEnumerator->Next(1, &TempFile, NULL);
    if (FAILED(hr))
    {
     wprintf(L"WARNING: Unable to obtain an IBackgroundCopyFile interface for the next file in the job.\n");
     wprintf(L"        No further information can be provided about this file.\n");
    }
    else
    {
     IBackgroundCopyFile5 *File;
     hr = TempFile->QueryInterface(__uuidof(IBackgroundCopyFile5), (void **)&File);
     if (FAILED(hr))
     {
      wprintf(L"WARNING: Unable to obtain an IBackgroundCopyFile5 interface for the file.\n");
      wprintf(L"        No further information can be provided about this file.\n");
     }
     else
     {
      LPWSTR RemoteFileName;
      hr = File->GetRemoteName(&RemoteFileName);
      if (FAILED(hr))
      {
       wprintf(L"WARNING: Unable to obtain the remote file name for this file.\n");
      }
      else
      {
       wprintf(L"HTTP headers for remote file '%ws'\n", RemoteFileName);
       CoTaskMemFree(RemoteFileName);
       RemoteFileName = NULL;
      }

      BITS_FILE_PROPERTY_VALUE Value;
      hr = File->GetProperty(BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS, &Value);
      if (FAILED(hr))
      {
       wprintf(L"WARNING: Unable to obtain the HTTP headers for this file.\n");
      }
      else
      {
       if (Value.String)
       {
        DisplayHeaders(Value.String);
        CoTaskMemFree(Value.String);
        Value.String = NULL;
       }
      }

      File->Release();
      File = NULL;
     }

     TempFile->Release();
     TempFile = NULL;
    }
   }
  }

  FileEnumerator->Release();
  FileEnumerator = NULL;
 }

 return S_OK;
}


/**
 * Displays the current progress of the job in terms of the amount of data
 * and number of files transferred.
 */
VOID DisplayProgress(__in IBackgroundCopyJob *Job)
{
 HRESULT hr;
 BG_JOB_PROGRESS Progress;

 hr = Job->GetProgress(&Progress);
 if (SUCCEEDED(hr))
 {
  wprintf(L"%llu of %llu bytes transferred (%lu of %lu files).\n",
   Progress.BytesTransferred, Progress.BytesTotal,
   Progress.FilesTransferred, Progress.FilesTotal);
 }
 else
 {
  wprintf(L"ERROR: Unable to get job progress (error code %08X).\n", hr);
 }
}

/**
 * Parses the provided string that contains HTTP headers,
 * splits them apart and displays them to the user.
 */
VOID DisplayHeaders(__in LPWSTR Headers)
{
 wprintf(L"Headers: %ws\n", Headers);
}

VOID DisplayError(__in IBackgroundCopyJob *Job)
{
 HRESULT hr;
 IBackgroundCopyError *Error;
 LPWSTR ErrorDescription;

 hr = Job->GetError(&Error);
 if (FAILED(hr))
 {
  wprintf(L"WARNING: Unable to get job error information (code %08X)\n", hr);
 }
 else
 {
  BG_ERROR_CONTEXT ErrorContext;
  HRESULT ErrorResult;
  hr = Error->GetError(&ErrorContext, &ErrorResult);
  if (FAILED(hr))
  {
   wprintf(L"WARNING: Unable to get job error code information (code %08X)\n", hr);
  }
  else
  {
   hr = Error->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &ErrorDescription);
   if (FAILED(hr))
   {
    wprintf(L"WARNING: Unable to get job error description (code %08X) for %08X\n", hr, ErrorResult);
   }
   else
   {
    wprintf(L"   Error details: code %08X %ws\n", ErrorResult, ErrorDescription);
    CoTaskMemFree(ErrorDescription);
   }
  }

  Error->Release();
 }
}
```



 

 




