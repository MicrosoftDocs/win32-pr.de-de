---
title: Angeben von Anmelde Informationen für die Server Authentifizierung für einen Bits-Übertragungs Auftrag
description: Sie können unterschiedliche Authentifizierungs Schemas für einen Background Intelligent Transfer Service Übertragungs Auftrag (Bits) angeben.
ms.assetid: 31db38f6-3639-4042-97f2-4f9d78942e15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4373cdf0c8b4c8afe7dff367fda9387eec0b54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039590"
---
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a><span data-ttu-id="d2983-103">Angeben von Anmelde Informationen für die Server Authentifizierung für einen Bits-Übertragungs Auftrag</span><span class="sxs-lookup"><span data-stu-id="d2983-103">Specify server authentication credentials for a BITS transfer job</span></span>

<span data-ttu-id="d2983-104">Sie können unterschiedliche Authentifizierungs Schemas für einen Background Intelligent Transfer Service Übertragungs Auftrag (Bits) angeben.</span><span class="sxs-lookup"><span data-stu-id="d2983-104">You can specify different authentication schemes for a Background Intelligent Transfer Service (BITS) transfer job.</span></span>

<span data-ttu-id="d2983-105">Mit dem folgenden Verfahren wird ein Authentifizierungsschema abgerufen und eine Authentifizierungs Identitäts Struktur erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2983-105">The following procedure gets an authentication scheme and creates an authentication identity structure.</span></span> <span data-ttu-id="d2983-106">Dann erstellt die Anwendung einen Bits-Download Auftrag und legt die Anmelde Informationen für den Auftrag fest.</span><span class="sxs-lookup"><span data-stu-id="d2983-106">Then the application creates a BITS download job and sets the credentials for the job.</span></span> <span data-ttu-id="d2983-107">Nachdem der Auftrag erstellt wurde, erhält die Anwendung einen Zeiger auf eine Rückruf Schnittstelle und fragt den Status des Bits-Übertragungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="d2983-107">After the job is created, the application gets a pointer to a callback interface and polls for the status of the BITS transfer job.</span></span> <span data-ttu-id="d2983-108">Nachdem der Auftrag fertiggestellt wurde, wird er aus der Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="d2983-108">After the job is complete, it is removed from the queue.</span></span>

<span data-ttu-id="d2983-109">In diesem Beispiel werden der Header und die Implementierung verwendet, die in [Beispiel: allgemeine Klassen](common-classes.md)definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d2983-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="d2983-110">**So geben Sie Anmelde Informationen für die Server Authentifizierung eines Bits-Übertragungs Auftrags an**</span><span class="sxs-lookup"><span data-stu-id="d2983-110">**To specify server authentication credentials for a BITS transfer job**</span></span>

1.  <span data-ttu-id="d2983-111">Erstellen Sie eine Containerstruktur, die die Werte des [**BG \_ auth- \_ Schemas**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) Schema Namen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="d2983-111">Create a container structure that maps [**BG\_AUTH\_SCHEME**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) values to scheme names.</span></span>

    ```C++
    struct
    {
        LPCWSTR        Name;
        BG_AUTH_SCHEME Scheme;
    }
    SchemeNames[] =
    {
        { L"basic",      BG_AUTH_SCHEME_BASIC },
        { L"digest",     BG_AUTH_SCHEME_DIGEST },
        { L"ntlm",       BG_AUTH_SCHEME_NTLM },
        { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
        { L"passport",   BG_AUTH_SCHEME_PASSPORT },

        { NULL,         BG_AUTH_SCHEME_BASIC }
    };
    ```

    

2.  <span data-ttu-id="d2983-112">Initialisieren Sie com-Parameter, indem Sie die ccoinitializer-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d2983-112">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="d2983-113">Weitere Informationen zur ccoinitializer-Funktion finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="d2983-113">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
3.  <span data-ttu-id="d2983-114">Bereiten Sie eine [**BG \_ auth- \_ Anmelde**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) Informationsstruktur vor.</span><span class="sxs-lookup"><span data-stu-id="d2983-114">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span> <span data-ttu-id="d2983-115">Im Beispiel wird die [securezeromemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion verwendet, um die Speicherorte zu löschen, die den vertraulichen Informationen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d2983-115">The example uses the [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function to clear the memory locations associated with the sensitive information.</span></span> <span data-ttu-id="d2983-116">Die [securezeromemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion ist in Winbase. h definiert.</span><span class="sxs-lookup"><span data-stu-id="d2983-116">The [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function is defined in WinBase.h.</span></span>
4.  <span data-ttu-id="d2983-117">Verwenden Sie die getscheme-Funktion, um das Authentifizierungsschema für die Verbindung mit dem Server zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2983-117">Use the GetScheme function to get the authentication scheme to use to connect to the server.</span></span>

    ```C++
    bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
    {
        int i;

        i = 0;
        while (SchemeNames[i].Name != NULL)
        {
            if (0 == _wcsicmp( s, SchemeNames[i].Name ))
            {

                *scheme = SchemeNames[i].Scheme;
                return true;
            }

            ++i;
        }

        return false;
    }
    ```

    

5.  <span data-ttu-id="d2983-118">Füllen Sie die [**BG \_ auth- \_ Anmelde**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) Informationsstruktur mit dem Authentifizierungsschema, das von der getscheme-Funktion zurückgegeben wird, und dem Benutzernamen und dem Kennwort, die an die Funktion ServerAuthentication übermittelt wurden</span><span class="sxs-lookup"><span data-stu-id="d2983-118">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure with the authentication scheme returned by the GetScheme function and the user name and password that were passed into the ServerAuthentication function.</span></span>
6.  <span data-ttu-id="d2983-119">Einen Zeiger auf die [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstelle (pjob) erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2983-119">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface (pJob).</span></span>
7.  <span data-ttu-id="d2983-120">Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="d2983-120">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="d2983-121">Bits erfordert mindestens die Identitätswechsel Ebene des Identitäts Wechsels.</span><span class="sxs-lookup"><span data-stu-id="d2983-121">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="d2983-122">Bits schlägt mit E \_ AccessDenied fehl, wenn die korrekte Identitätswechsel Ebene nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d2983-122">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
8.  <span data-ttu-id="d2983-123">Rufen Sie einen Zeiger auf die [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle ab, und rufen Sie den anfänglichen Serverlocatorpunkt in Bits ab, indem Sie die [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d2983-123">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
9.  <span data-ttu-id="d2983-124">Erstellen Sie einen Bits-Übertragungs Auftrag, indem Sie die [**ibackgroundcopymanager:: createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d2983-124">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
10. <span data-ttu-id="d2983-125">Rufen Sie einen Zeiger auf die cnotifyinterface-Rückruf Schnittstelle ab, und rufen Sie die [**ibackgroundcopyjob:: setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) -Methode auf, um Benachrichtigungen über auftragsbezogene Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d2983-125">Get a pointer to the CNotifyInterface callback interface and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="d2983-126">Weitere Informationen zu cnotifyinterface finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="d2983-126">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
11. <span data-ttu-id="d2983-127">Aufrufen der [**ibackgroundcopyjob:: setnotifyflags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) -Methode, um die Benachrichtigungs Typen festzulegen, die empfangen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d2983-127">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="d2983-128">In diesem Beispiel werden die **\_ \_ \_ Fehlerflags** **BG \_ Notify \_ Job \_ übertragen** und BG notify Job festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2983-128">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
12. <span data-ttu-id="d2983-129">Einen Zeiger auf die [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) -Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2983-129">Get a pointer to the [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface.</span></span> <span data-ttu-id="d2983-130">Verwenden Sie den **IBackgroundCopyJob2** -Zeiger, um zusätzliche Eigenschaften für den Auftrag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d2983-130">Use the **IBackgroundCopyJob2** pointer to set additional properties on the job.</span></span> <span data-ttu-id="d2983-131">Dieses Programm verwendet die [**IBackgroundCopyJob2:: setanmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode, um die Anmelde Informationen für den Bits-Übertragungs Auftrag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d2983-131">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
13. <span data-ttu-id="d2983-132">Fügen Sie dem Bits-Übertragungs Auftrag Dateien hinzu, indem Sie [**ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d2983-132">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span> <span data-ttu-id="d2983-133">In diesem Beispiel verwendet die **ibackgroundcopyjob:: AddFile** -Methode die remotefile-und LocalFile-Variablen, die an die Funktion ServerAuthentication übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="d2983-133">In this example, the **IBackgroundCopyJob::AddFile** method uses the remoteFile and localFile variables that were passed into the ServerAuthentication function.</span></span>
14. <span data-ttu-id="d2983-134">Nachdem die Datei hinzugefügt wurde, wenden Sie [**ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) an, um den Auftrag fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d2983-134">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="d2983-135">Richten Sie eine while-Schleife ein, um auf die beendenmeldung von der Rückruf Schnittstelle zu warten, während der Auftrag übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="d2983-135">Set up a while loop to wait for Quit Message from the callback interface while the job is transferring.</span></span>

    > [!Note]  
    > <span data-ttu-id="d2983-136">Dieser Schritt ist nur erforderlich, wenn es sich bei dem com-Apartment um ein Single Thread-Apartment handelt.</span><span class="sxs-lookup"><span data-stu-id="d2983-136">This step is necessary only if the COM apartment is a single-threaded apartment.</span></span> <span data-ttu-id="d2983-137">Weitere Informationen finden Sie unter [Single Thread Apartments](../com/single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="d2983-137">For more information, see [Single-Threaded Apartments](../com/single-threaded-apartments.md).</span></span>

     

    ```C++
    // Wait for QuitMessage from CallBack
        DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
        while (dwLimit > GetTickCount())
        {
            MSG msg;

            while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
            { 
                // If it is a quit message, exit.
                if (msg.message == WM_QUIT) 
                {
                    return;
                }

                // Otherwise, dispatch the message.
                DispatchMessage(&msg); 
            } // End of PeekMessage while loop
        }
    ```

    

    <span data-ttu-id="d2983-138">Die vorhergehende Schleife verwendet die [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) -Funktion, um die Anzahl der Millisekunden abzurufen, die seit Beginn der Übertragung des Auftrags verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="d2983-138">The preceding loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>

16. <span data-ttu-id="d2983-139">Nachdem der Bits-Übertragungs Auftrag fertiggestellt wurde, entfernen Sie den Auftrag aus der Warteschlange, indem Sie [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d2983-139">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="d2983-140">Im folgenden Codebeispiel werden Anmelde Informationen für die Server Authentifizierung für einen Bits-Übertragungs Auftrag angegeben.</span><span class="sxs-lookup"><span data-stu-id="d2983-140">The following code example specifies server authentication credentials for a BITS transfer job.</span></span>


```C++
#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"

//
// Retrieve BG_AUTH_SCHEME from scheme name.
//
//
struct
{
    LPCWSTR        Name;
    BG_AUTH_SCHEME Scheme;
}
SchemeNames[] =
{
    { L"basic",      BG_AUTH_SCHEME_BASIC },
    { L"digest",     BG_AUTH_SCHEME_DIGEST },
    { L"ntlm",       BG_AUTH_SCHEME_NTLM },
    { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
    { L"passport",   BG_AUTH_SCHEME_PASSPORT },

    { NULL,         BG_AUTH_SCHEME_BASIC }
};

bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
{
    int i;

    i = 0;
    while (SchemeNames[i].Name != NULL)
    {
        if (0 == _wcsicmp( s, SchemeNames[i].Name ))
        {

            *scheme = SchemeNames[i].Scheme;
            return true;
        }

        ++i;
    }

    return false;
}

void ServerAuthentication(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &scheme, const LPWSTR &username, const LPWSTR &password)
{

 // If CoInitializeEx fails, the exception is unhandled and the program terminates  
 CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    // Prepare the credentials structure.
    BG_AUTH_CREDENTIALS cred;
    ZeroMemory(&cred, sizeof(cred));
    if (!GetScheme(scheme,&cred.Scheme))
    {
        wprintf(L"Invalid authentication scheme specified\n");
        return;
    }

    cred.Target = BG_AUTH_TARGET_SERVER;
    cred.Credentials.Basic.UserName = username;
    if (0 == _wcsicmp(cred.Credentials.Basic.UserName, L"NULL"))
    {
        cred.Credentials.Basic.UserName = NULL;
    }

    cred.Credentials.Basic.Password = password;
    if (0 == _wcsicmp(cred.Credentials.Basic.Password, L"NULL"))
    {
        cred.Credentials.Basic.Password = NULL;
    }

    CComPtr<IBackgroundCopyJob> pJob;
    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(NULL, 
            -1, 
            NULL, 
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL, 
            EOAC_DYNAMIC_CLOAKING, 
            0);
        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void**)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"BitsAuthSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyFlags");
        }

        // Set credentials.
        CComPtr<IBackgroundCopyJob2> job2;
        hr = pJob.QueryInterface(&job2);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"QueryInterface");
        }

        hr = job2->SetCredentials(&cred);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetCredentials");
        }

        // Add a file.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile, localFile);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"Resume");
        }
    }
    catch(const std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }
    catch(const MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack.
    DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
    while (dwLimit > GetTickCount())
    {
        MSG msg;

        while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
        { 
            // If it is a quit message, exit.
            if (msg.message == WM_QUIT) 
            {
                return;
            }

            // Otherwise, dispatch the message.
            DispatchMessage(&msg); 
        } // End of PeekMessage while loop
    }

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s", argv[0]);
        wprintf(L" [remote name] [local name] [server authentication scheme =\"NTLM\"|\"NEGOTIATE\"|\"BASIC\"|\"DIGEST\"] [username] [password]\n");
        return;
    }

    ServerAuthentication(argv[1], argv[2], argv[3], argv[4], argv[5]); 

}
```



## <a name="related-topics"></a><span data-ttu-id="d2983-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2983-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2983-142">**Ibackgroundcopymanager**</span><span class="sxs-lookup"><span data-stu-id="d2983-142">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="d2983-143">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="d2983-143">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="d2983-144">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="d2983-144">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="d2983-145">Beispiel: allgemeine Klassen</span><span class="sxs-lookup"><span data-stu-id="d2983-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 