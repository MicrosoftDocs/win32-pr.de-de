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
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a>Beispiel: Hinzufügen eines Hilfsobjekts zu einem Bits-Übertragungs Auftrag

Sie können einen Background Intelligent Transfer Service Übertragungs Auftrag (Bits) mit einem zusätzlichen Sicherheits Token konfigurieren. Der Bits-Übertragungs Auftrag verwendet dieses Hilfstoken für die Authentifizierung und für den Zugriff auf Ressourcen.

Weitere Informationen finden Sie unter [Helper Tokens für Bits-Übertragungs Aufträge](helper-tokens-for-bits-transfer-jobs.md).

Mit der folgenden Prozedur wird ein Bits-Übertragungs Auftrag im Kontext des lokalen Benutzers erstellt, die Anmelde Informationen eines zweiten Benutzers abgerufen, ein Hilfsobjekt mit diesen Anmelde Informationen erstellt und dann das Hilfsobjekt für den Bits-Übertragungs Auftrag festgelegt.

In diesem Beispiel werden der Header und die Implementierung verwendet, die in [Beispiel: allgemeine Klassen](common-classes.md)definiert sind.

**So fügen Sie einem Bits-Übertragungs Auftrag ein Hilfsobjekt hinzu**

1.  Initialisieren Sie com-Parameter, indem Sie die ccoinitializer-Funktion aufrufen. Weitere Informationen zur ccoinitializer-Funktion finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).
2.  Einen Zeiger auf die [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstelle erhalten. In diesem Beispiel wird die [CComPtr-Klasse](/cpp/atl/reference/ccomptr-class?view=vs-2019) zum Verwalten von COM-Schnittstellen Zeigern verwendet.
3.  Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Bits erfordert mindestens die Identitätswechsel Ebene des Identitäts Wechsels. Bits schlägt mit E \_ AccessDenied fehl, wenn die korrekte Identitätswechsel Ebene nicht festgelegt ist.
4.  Rufen Sie einen Zeiger auf die [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle ab, und rufen Sie den anfänglichen Serverlocatorpunkt in Bits ab, indem Sie die [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen.
5.  Erstellen Sie einen Bits-Übertragungs Auftrag, indem Sie die [**ibackgroundcopymanager:: createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) -Methode aufrufen.
6.  Rufen Sie einen Zeiger auf die cnotifyinterface-Rückruf Schnittstelle ab, und rufen Sie die [**ibackgroundcopyjob:: setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) -Methode auf, um Benachrichtigungen über auftragsbezogene Ereignisse zu empfangen. Weitere Informationen zu cnotifyinterface finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).
7.  Aufrufen der [**ibackgroundcopyjob:: setnotifyflags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) -Methode, um die Benachrichtigungs Typen festzulegen, die empfangen werden sollen. In diesem Beispiel werden die **\_ \_ \_ Fehlerflags** **BG \_ Notify \_ Job \_ übertragen** und BG notify Job festgelegt.
8.  Rufen Sie einen Zeiger auf die [**ibitstokenoptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) -Schnittstelle ab, indem Sie die **ibackgroundcopyjob:: QueryInterface** -Methode mit dem richtigen Schnittstellen Bezeichner aufrufen.
9.  Versuchen Sie, den Benutzer des Hilfsobjekts anzumelden. Erstellen Sie ein Identitätswechsel handle, und rufen Sie die [LogonUser-Funktion]( /windows/win32/api/winbase/nf-winbase-logonusera) auf, um das Identitätswechsel handle aufzufüllen. Wenn der Vorgang erfolgreich ist, wird die Funktion "Identität [ateloggedonuser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)" aufgerufen. Wenn nicht erfolgreich, wird im Beispiel die [RevertToSelf-Funktion](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufgerufen, um den Identitätswechsel des angemeldeten Benutzers zu beenden, ein Fehler wird ausgelöst, und das Handle ist geschlossen.
10. Um die Identität des Tokens des angemeldeten Benutzers anzunehmen, müssen Sie die [**ibitstokenoptions:: abspertoken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) -Methode abrufen. Wenn diese Methode fehlschlägt, wird im Beispiel die [RevertToSelf-Funktion](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufgerufen, um den Identitätswechsel des angemeldeten Benutzers zu beenden, ein Fehler wird ausgelöst, und das Handle ist geschlossen.
    > [!Note]
    >
    > In unterstützten Versionen von Windows vor Windows 10, Version 1607, muss der Besitzer des Auftrags über Administrator Anmelde Informationen verfügen, um die [**ibitstokenoptions::**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) *-Methode aufzurufen.
    >
    > Ab Windows 10, Version 1607, können nicht-Administrator-Auftrags Besitzer nicht-Administrator-Hilfstoken für BITS-Aufträge festlegen, die Sie besitzen. Auftrags Besitzer müssen weiterhin über Administratorrechte verfügen, um Hilfstoken mit Administratorrechten festzulegen.

     

11. Aufrufen der [**ibitstokenoptions:: tspertokenflags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) -Methode, um anzugeben, auf welche Ressourcen mithilfe des Sicherheits Kontexts des Hilfsobjekts zugegriffen werden soll.
12. Nachdem der Identitätswechsel abgeschlossen ist, wird im Beispiel die [RevertToSelf-Funktion](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufgerufen, um den Identitätswechsel des angemeldeten Benutzers zu beenden, und das Handle ist geschlossen.
13. Fügen Sie dem Bits-Übertragungs Auftrag Dateien hinzu, indem Sie [**ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)aufrufen.
14. Nachdem die Datei hinzugefügt wurde, wenden Sie [**ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) an, um den Auftrag fortzusetzen.
15. Richten Sie eine while-Schleife ein, um auf die beendenmeldung von der Rückruf Schnittstelle zu warten, während der Auftrag übertragen wird. Die while-Schleife verwendet die [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) -Funktion, um die Anzahl der Millisekunden abzurufen, die seit Beginn der Übertragung des Auftrags verstrichen sind.
16. Nachdem der Bits-Übertragungs Auftrag fertiggestellt wurde, entfernen Sie den Auftrag aus der Warteschlange, indem Sie [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)aufrufen.

Im folgenden Codebeispiel wird ein Hilfsobjekt zu einem Bits-Übertragungs Auftrag hinzugefügt.


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

[Hilfstoken für Bits-Übertragungs Aufträge](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[**Ibitstokenoptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[Beispiel: allgemeine Klassen](common-classes.md)
</dt> </dl>

 

 