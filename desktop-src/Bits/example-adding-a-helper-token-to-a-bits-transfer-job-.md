---
title: Beispiel für das Hinzufügen eines hilfstokens zu einem Bits-Übertragungs Auftrag
description: Sie können einen Background Intelligent Transfer Service Übertragungs Auftrag (Bits) mit einem zusätzlichen Sicherheits Token konfigurieren. Der Bits-Übertragungs Auftrag verwendet dieses Hilfstoken für die Authentifizierung und für den Zugriff auf Ressourcen.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab12fe93ae54d91d02bef5e59e99d267571413e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039538"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a><span data-ttu-id="615b4-104">Beispiel: Hinzufügen eines Hilfsobjekts zu einem Bits-Übertragungs Auftrag</span><span class="sxs-lookup"><span data-stu-id="615b4-104">Example: Adding a Helper Token to a BITS Transfer Job</span></span>

<span data-ttu-id="615b4-105">Sie können einen Background Intelligent Transfer Service Übertragungs Auftrag (Bits) mit einem zusätzlichen Sicherheits Token konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="615b4-105">You can configure a Background Intelligent Transfer Service (BITS) transfer job with an additional security token.</span></span> <span data-ttu-id="615b4-106">Der Bits-Übertragungs Auftrag verwendet dieses Hilfstoken für die Authentifizierung und für den Zugriff auf Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="615b4-106">The BITS transfer job uses this helper token for authentication and to access resources.</span></span>

<span data-ttu-id="615b4-107">Weitere Informationen finden Sie unter [Helper Tokens für Bits-Übertragungs Aufträge](helper-tokens-for-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="615b4-107">For more information, see [Helper tokens for BITS transfer jobs](helper-tokens-for-bits-transfer-jobs.md).</span></span>

<span data-ttu-id="615b4-108">Mit der folgenden Prozedur wird ein Bits-Übertragungs Auftrag im Kontext des lokalen Benutzers erstellt, die Anmelde Informationen eines zweiten Benutzers abgerufen, ein Hilfsobjekt mit diesen Anmelde Informationen erstellt und dann das Hilfsobjekt für den Bits-Übertragungs Auftrag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="615b4-108">The following procedure creates a BITS transfer job in the context of the local user, gets credentials of a second user, creates a helper token with these credentials, and then sets the helper token on the BITS transfer job.</span></span>

<span data-ttu-id="615b4-109">In diesem Beispiel werden der Header und die Implementierung verwendet, die in [Beispiel: allgemeine Klassen](common-classes.md)definiert sind.</span><span class="sxs-lookup"><span data-stu-id="615b4-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="615b4-110">**So fügen Sie einem Bits-Übertragungs Auftrag ein Hilfsobjekt hinzu**</span><span class="sxs-lookup"><span data-stu-id="615b4-110">**To add a helper token to a BITS transfer job**</span></span>

1.  <span data-ttu-id="615b4-111">Initialisieren Sie com-Parameter, indem Sie die ccoinitializer-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="615b4-111">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="615b4-112">Weitere Informationen zur ccoinitializer-Funktion finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="615b4-112">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="615b4-113">Einen Zeiger auf die [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="615b4-113">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface.</span></span> <span data-ttu-id="615b4-114">In diesem Beispiel wird die [CComPtr-Klasse](/cpp/atl/reference/ccomptr-class?view=vs-2019) zum Verwalten von COM-Schnittstellen Zeigern verwendet.</span><span class="sxs-lookup"><span data-stu-id="615b4-114">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="615b4-115">Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="615b4-115">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="615b4-116">Bits erfordert mindestens die Identitätswechsel Ebene des Identitäts Wechsels.</span><span class="sxs-lookup"><span data-stu-id="615b4-116">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="615b4-117">Bits schlägt mit E \_ AccessDenied fehl, wenn die korrekte Identitätswechsel Ebene nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="615b4-117">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
4.  <span data-ttu-id="615b4-118">Rufen Sie einen Zeiger auf die [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle ab, und rufen Sie den anfänglichen Serverlocatorpunkt in Bits ab, indem Sie die [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="615b4-118">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
5.  <span data-ttu-id="615b4-119">Erstellen Sie einen Bits-Übertragungs Auftrag, indem Sie die [**ibackgroundcopymanager:: createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="615b4-119">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
6.  <span data-ttu-id="615b4-120">Rufen Sie einen Zeiger auf die cnotifyinterface-Rückruf Schnittstelle ab, und rufen Sie die [**ibackgroundcopyjob:: setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) -Methode auf, um Benachrichtigungen über auftragsbezogene Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="615b4-120">Get a pointer to the CNotifyInterface callback interface, and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="615b4-121">Weitere Informationen zu cnotifyinterface finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="615b4-121">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
7.  <span data-ttu-id="615b4-122">Aufrufen der [**ibackgroundcopyjob:: setnotifyflags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) -Methode, um die Benachrichtigungs Typen festzulegen, die empfangen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="615b4-122">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="615b4-123">In diesem Beispiel werden die **\_ \_ \_ Fehlerflags** **BG \_ Notify \_ Job \_ übertragen** und BG notify Job festgelegt.</span><span class="sxs-lookup"><span data-stu-id="615b4-123">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
8.  <span data-ttu-id="615b4-124">Rufen Sie einen Zeiger auf die [**ibitstokenoptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) -Schnittstelle ab, indem Sie die **ibackgroundcopyjob:: QueryInterface** -Methode mit dem richtigen Schnittstellen Bezeichner aufrufen.</span><span class="sxs-lookup"><span data-stu-id="615b4-124">Get a pointer to the [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) interface by calling the **IBackgroundCopyJob::QueryInterface** method with the proper interface identifier.</span></span>
9.  <span data-ttu-id="615b4-125">Versuchen Sie, den Benutzer des Hilfsobjekts anzumelden.</span><span class="sxs-lookup"><span data-stu-id="615b4-125">Attempt to log on the user of the helper token.</span></span> <span data-ttu-id="615b4-126">Erstellen Sie ein Identitätswechsel handle, und rufen Sie die [LogonUser-Funktion]( /windows/win32/api/winbase/nf-winbase-logonusera) auf, um das Identitätswechsel handle aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="615b4-126">Create an impersonation handle, and call the [LogonUser Function]( /windows/win32/api/winbase/nf-winbase-logonusera) to populate the impersonation handle.</span></span> <span data-ttu-id="615b4-127">Wenn der Vorgang erfolgreich ist, wird die Funktion "Identität [ateloggedonuser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="615b4-127">If successful, call the [ImpersonateLoggedOnUser Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span></span> <span data-ttu-id="615b4-128">Wenn nicht erfolgreich, wird im Beispiel die [RevertToSelf-Funktion](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufgerufen, um den Identitätswechsel des angemeldeten Benutzers zu beenden, ein Fehler wird ausgelöst, und das Handle ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="615b4-128">If unsuccessful, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
10. <span data-ttu-id="615b4-129">Um die Identität des Tokens des angemeldeten Benutzers anzunehmen, müssen Sie die [**ibitstokenoptions:: abspertoken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="615b4-129">Call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method to impersonate the token of the logged-on user.</span></span> <span data-ttu-id="615b4-130">Wenn diese Methode fehlschlägt, wird im Beispiel die [RevertToSelf-Funktion](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufgerufen, um den Identitätswechsel des angemeldeten Benutzers zu beenden, ein Fehler wird ausgelöst, und das Handle ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="615b4-130">If this method fails, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
    > [!Note]
    >
    > <span data-ttu-id="615b4-131">In unterstützten Versionen von Windows vor Windows 10, Version 1607, muss der Besitzer des Auftrags über Administrator Anmelde Informationen verfügen, um die [**ibitstokenoptions::**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) \*-Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="615b4-131">In supported versions of Windows before Windows 10, version 1607, the job owner must have administrative credentials to call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method.</span></span>
    >
    > <span data-ttu-id="615b4-132">Ab Windows 10, Version 1607, können nicht-Administrator-Auftrags Besitzer nicht-Administrator-Hilfstoken für BITS-Aufträge festlegen, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="615b4-132">Starting with Windows 10, version 1607, non-administrator job owners can set non-administrator helper tokens on BITS jobs they own.</span></span> <span data-ttu-id="615b4-133">Auftrags Besitzer müssen weiterhin über Administratorrechte verfügen, um Hilfstoken mit Administratorrechten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="615b4-133">Job owners must still have administrative credentials to set helper tokens with administrator privileges.</span></span>

     

11. <span data-ttu-id="615b4-134">Aufrufen der [**ibitstokenoptions:: tspertokenflags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) -Methode, um anzugeben, auf welche Ressourcen mithilfe des Sicherheits Kontexts des Hilfsobjekts zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="615b4-134">Call the [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) method to specify which resources to access using the helper token's security context.</span></span>
12. <span data-ttu-id="615b4-135">Nachdem der Identitätswechsel abgeschlossen ist, wird im Beispiel die [RevertToSelf-Funktion](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufgerufen, um den Identitätswechsel des angemeldeten Benutzers zu beenden, und das Handle ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="615b4-135">After the impersonation is complete, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of logged on user, and the handle is closed.</span></span>
13. <span data-ttu-id="615b4-136">Fügen Sie dem Bits-Übertragungs Auftrag Dateien hinzu, indem Sie [**ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="615b4-136">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span>
14. <span data-ttu-id="615b4-137">Nachdem die Datei hinzugefügt wurde, wenden Sie [**ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) an, um den Auftrag fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="615b4-137">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="615b4-138">Richten Sie eine while-Schleife ein, um auf die beendenmeldung von der Rückruf Schnittstelle zu warten, während der Auftrag übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="615b4-138">Set up a while loop to wait for the quit message from the callback interface while the job is transferring.</span></span> <span data-ttu-id="615b4-139">Die while-Schleife verwendet die [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) -Funktion, um die Anzahl der Millisekunden abzurufen, die seit Beginn der Übertragung des Auftrags verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="615b4-139">The while loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>
16. <span data-ttu-id="615b4-140">Nachdem der Bits-Übertragungs Auftrag fertiggestellt wurde, entfernen Sie den Auftrag aus der Warteschlange, indem Sie [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="615b4-140">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="615b4-141">Im folgenden Codebeispiel wird ein Hilfsobjekt zu einem Bits-Übertragungs Auftrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="615b4-141">The following code example adds a helper token to a BITS transfer job.</span></span>


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


void HelperToken(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &domain, const LPWSTR &username, const LPWSTR &password)
{
// If CoInitializeEx fails, the exception is unhandled and the program terminates   
CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);

CComPtr<IBackgroundCopyJob> pJob; 

    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(
            NULL,
            -1,
            NULL,
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL,
            EOAC_DYNAMIC_CLOAKING,
            0
            );

        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void **)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"HelperTokenSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);


        if(FAILED(hr))
        {   
            // Failed to create job.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;    
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to SetNotifyInterface.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to SetNotifyFlags.
            throw MyException(hr, L"SetNotifyFlags");
        }

        //Retrieve the IBitsTokenOptions interface pointer from the BITS transfer job.
        CComPtr<IBitsTokenOptions> pTokenOptions;
        hr = pJob->QueryInterface(__uuidof(IBitsTokenOptions), (void** ) &pTokenOptions);

        if (FAILED(hr))
        {
            // Failed to QueryInterface.
            throw MyException(hr, L"QueryInterface");
        }

        // Log on user of the helper token.
        wprintf(L"Credentials for helper token %s\\%s %s\n", domain, username, password);

        HANDLE hImpersonation = INVALID_HANDLE_VALUE;
        if(LogonUser(username, domain, password, LOGON32_LOGON_INTERACTIVE, LOGON32_PROVIDER_DEFAULT, &hImpersonation))
        {
            // Impersonate the logged-on user.
            if(ImpersonateLoggedOnUser(hImpersonation))
            {
                // Configure the impersonated logged-on user's token as the helper token.
                hr = pTokenOptions->SetHelperToken();        
                if (FAILED(hr))
                {
                    //Failed to set helper token.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperToken");
                }

                hr = pTokenOptions->SetHelperTokenFlags(BG_TOKEN_LOCAL_FILE);
                if (FAILED(hr))
                {
                    //Failed to set helper token flags.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperTokenFlags");
                }

                RevertToSelf();
            }               
            CloseHandle(hImpersonation);
        }

        // Add a file.
        // Replace parameters with variables that contain valid paths.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile,localFile);

        if(FAILED(hr))
        {   
            //Failed to add file to job.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Resume failed.                   
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
        wprintf(L"Error 0x%x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

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

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s ", argv[0]);
        wprintf(L"[remote name] [local name] [helpertoken domain] [helpertoken userrname] [helpertoken password]\n");
        return;
    }

    HelperToken(argv[1],argv[2],argv[3],argv[4],argv[5]);

}
```



## <a name="related-topics"></a><span data-ttu-id="615b4-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="615b4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="615b4-143">Hilfstoken für Bits-Übertragungs Aufträge</span><span class="sxs-lookup"><span data-stu-id="615b4-143">Helper tokens for BITS transfer jobs</span></span>](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[<span data-ttu-id="615b4-144">**Ibitstokenoptions**</span><span class="sxs-lookup"><span data-stu-id="615b4-144">**IBitsTokenOptions**</span></span>](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[<span data-ttu-id="615b4-145">Beispiel: allgemeine Klassen</span><span class="sxs-lookup"><span data-stu-id="615b4-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 