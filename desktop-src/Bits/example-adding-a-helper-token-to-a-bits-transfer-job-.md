---
title: Beispiel zum Hinzufügen eines Hilfstokens zu einem BITS-Übertragungsauftrag
description: Sie können einen auftragsbasierten Background Intelligent Transfer Service (BITS) mit einem zusätzlichen Sicherheitstoken konfigurieren. Der BITS-Übertragungsauftrag verwendet dieses Hilfstoken für die Authentifizierung und den Zugriff auf Ressourcen.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4adab6ca8cebeeca9b9883e89db28205dfdab1ea43e05c01fd119c14c26d374
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528820"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a>Beispiel: Hinzufügen eines Hilfstokens zu einem BITS-Übertragungsauftrag

Sie können einen auftragsbasierten Background Intelligent Transfer Service (BITS) mit einem zusätzlichen Sicherheitstoken konfigurieren. Der BITS-Übertragungsauftrag verwendet dieses Hilfstoken für die Authentifizierung und den Zugriff auf Ressourcen.

Weitere Informationen finden Sie unter [Hilfstoken für BITS-Übertragungsaufträge.](helper-tokens-for-bits-transfer-jobs.md)

Das folgende Verfahren erstellt einen BITS-Übertragungsauftrag im Kontext des lokalen Benutzers, ruft Anmeldeinformationen eines zweiten Benutzers ab, erstellt ein Hilfstoken mit diesen Anmeldeinformationen und legt dann das Hilfstoken für den BITS-Übertragungsauftrag fest.

In diesem Beispiel werden der Header und die Implementierung verwendet, die in [Beispiel: Allgemeine Klassen definiert sind.](common-classes.md)

**So fügen Sie einem BITS-Übertragungsauftrag ein Hilfstoken hinzu**

1.  Initialisieren Sie COM-Parameter, indem Sie die CCoInitializer-Funktion aufrufen. Weitere Informationen zur CCoInitializer-Funktion finden Sie unter [Beispiel: Allgemeine Klassen](common-classes.md).
2.  Sie erhalten einen Zeiger auf die [**IBackgroundCopyJob-Schnittstelle.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) In diesem Beispiel wird die [CComPtr-Klasse verwendet,](/cpp/atl/reference/ccomptr-class?view=vs-2019) um COM-Schnittstellenzeiger zu verwalten.
3.  Initialisieren Sie die COM-Prozesssicherheit, indem [Sie CoInitializeSecurity aufrufen.](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) BITS erfordert mindestens die IMPERSONATE-Ebene des Identitätswechsels. BITS schlägt mit E \_ ACCESSDENIED fehl, wenn die richtige Identitätswechselebene nicht festgelegt ist.
4.  Rufen Sie einen Zeiger auf die [**IBackgroundCopyManager-Schnittstelle**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) ab, und rufen Sie den anfänglichen Locator auf BITS ab, indem Sie die [CoCreateInstance-Funktion]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen.
5.  Erstellen Sie einen BITS-Übertragungsauftrag, indem Sie [**die IBackgroundCopyManager::CreateJob-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) aufrufen.
6.  Rufen Sie einen Zeiger auf die CNotifyInterface-Rückrufschnittstelle ab, und rufen Sie die [**IBackgroundCopyJob::SetNotifyInterface-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) auf, um Benachrichtigungen über auftragsbezogene Ereignisse zu empfangen. Weitere Informationen zu CNotifyInterface finden Sie unter [Beispiel: Allgemeine Klassen](common-classes.md).
7.  Rufen Sie die [**IBackgroundCopyJob::SetNotifyFlags-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) auf, um die Typen der zu empfangenden Benachrichtigungen festlegen. In diesem Beispiel werden die **Flags BG \_ NOTIFY JOB \_ \_ TRANSFERD** und **BG NOTIFY JOB \_ \_ \_ ERROR** festgelegt.
8.  Rufen Sie einen Zeiger auf die [**IBitsTokenOptions-Schnittstelle**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) ab, indem Sie die **IBackgroundCopyJob::QueryInterface-Methode** mit dem richtigen Schnittstellenbezeichner aufrufen.
9.  Versuchen Sie, den Benutzer des Hilfstokens zu anmelden. Erstellen Sie ein Identitätswechselhand handle, und rufen Sie die [LogonUser-Funktion auf,]( /windows/win32/api/winbase/nf-winbase-logonusera) um das Identitätswechselhand handle zu füllen. Wenn dies erfolgreich ist, rufen Sie [die ImpersonateLoggedOnUser-Funktion auf.](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) Wenn dies nicht erfolgreich ist, ruft das Beispiel die [RevertToSelf-Funktion](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) auf, um den Identitätswechsel des angemeldeten Benutzers zu beenden. Es wird ein Fehler ausgelöst, und das Handle wird geschlossen.
10. Rufen Sie [**die IBitsTokenOptions::SetHelperToken-Methode**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) auf, um die Identität des Tokens des angemeldeten Benutzers zu angenommen. Wenn diese Methode fehlschlägt, ruft das Beispiel die [RevertToSelf-Funktion](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) auf, um den Identitätswechsel des angemeldeten Benutzers zu beenden. Es wird ein Fehler ausgelöst, und das Handle wird geschlossen.
    > [!Note]
    >
    > In unterstützten Versionen von Windows vor Windows 10, Version 1607, muss der Auftragsbesitzer über Administratoranmeldeinformationen verfügen, um die [**IBitsTokenOptions::SetHelperToken-Methode aufrufen**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) zu können.
    >
    > Ab Windows 10 Version 1607 können Auftragsbesitzer ohne Administratorrechte Hilfstoken für BITS-Aufträge festlegen, die sie besitzen. Auftragsbesitzer müssen weiterhin über Administratoranmeldeinformationen verfügen, um Hilfstoken mit Administratorrechten festlegen zu können.

     

11. Rufen Sie [**die IBitsTokenOptions::SetHelperTokenFlags-Methode**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) auf, um mithilfe des Sicherheitskontexts des Hilfstokens anzugeben, auf welche Ressourcen sie zugreifen sollen.
12. Nach Abschluss des Identitätswechsels ruft das Beispiel die [RevertToSelf-Funktion](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) auf, um den Identitätswechsel des angemeldeten Benutzers zu beenden, und das Handle wird geschlossen.
13. Fügen Sie dem BITS-Übertragungsauftrag Dateien hinzu, indem [**Sie IBackgroundCopyJob::AddFile aufrufen.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
14. Nachdem die Datei hinzugefügt wurde, rufen Sie [**IBackgroundCopyJob::Resume auf,**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) um den Auftrag wieder aufzunehmen.
15. Richten Sie eine while-Schleife ein, um auf die Nachricht zum Beenden von der Rückrufschnittstelle zu warten, während der Auftrag übertragen wird. Die while-Schleife verwendet die [GetTickCount-Funktion,](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) um die Anzahl der Millisekunden abzurufen, die seit beginn der Übertragung des Auftrags verstrichen sind.
16. Entfernen Sie den Auftrag nach Abschluss des BITS-Übertragungsauftrags aus der Warteschlange, indem Sie [**IBackgroundCopyJob::Complete aufrufen.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)

Im folgenden Codebeispiel wird einem BITS-Übertragungsauftrag ein Hilfstoken hinzufügt.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hilfstoken für BITS-Übertragungsaufträge](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[Beispiel: Allgemeine Klassen](common-classes.md)
</dt> </dl>

 

 