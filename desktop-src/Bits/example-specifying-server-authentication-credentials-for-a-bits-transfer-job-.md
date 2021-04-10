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
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a>Angeben von Anmelde Informationen für die Server Authentifizierung für einen Bits-Übertragungs Auftrag

Sie können unterschiedliche Authentifizierungs Schemas für einen Background Intelligent Transfer Service Übertragungs Auftrag (Bits) angeben.

Mit dem folgenden Verfahren wird ein Authentifizierungsschema abgerufen und eine Authentifizierungs Identitäts Struktur erstellt. Dann erstellt die Anwendung einen Bits-Download Auftrag und legt die Anmelde Informationen für den Auftrag fest. Nachdem der Auftrag erstellt wurde, erhält die Anwendung einen Zeiger auf eine Rückruf Schnittstelle und fragt den Status des Bits-Übertragungs Auftrags ab. Nachdem der Auftrag fertiggestellt wurde, wird er aus der Warteschlange entfernt.

In diesem Beispiel werden der Header und die Implementierung verwendet, die in [Beispiel: allgemeine Klassen](common-classes.md)definiert sind.

**So geben Sie Anmelde Informationen für die Server Authentifizierung eines Bits-Übertragungs Auftrags an**

1.  Erstellen Sie eine Containerstruktur, die die Werte des [**BG \_ auth- \_ Schemas**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) Schema Namen zuordnet.

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

    

2.  Initialisieren Sie com-Parameter, indem Sie die ccoinitializer-Funktion aufrufen. Weitere Informationen zur ccoinitializer-Funktion finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).
3.  Bereiten Sie eine [**BG \_ auth- \_ Anmelde**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) Informationsstruktur vor. Im Beispiel wird die [securezeromemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion verwendet, um die Speicherorte zu löschen, die den vertraulichen Informationen zugeordnet sind. Die [securezeromemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion ist in Winbase. h definiert.
4.  Verwenden Sie die getscheme-Funktion, um das Authentifizierungsschema für die Verbindung mit dem Server zu erhalten.

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

    

5.  Füllen Sie die [**BG \_ auth- \_ Anmelde**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) Informationsstruktur mit dem Authentifizierungsschema, das von der getscheme-Funktion zurückgegeben wird, und dem Benutzernamen und dem Kennwort, die an die Funktion ServerAuthentication übermittelt wurden
6.  Einen Zeiger auf die [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstelle (pjob) erhalten.
7.  Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Bits erfordert mindestens die Identitätswechsel Ebene des Identitäts Wechsels. Bits schlägt mit E \_ AccessDenied fehl, wenn die korrekte Identitätswechsel Ebene nicht festgelegt ist.
8.  Rufen Sie einen Zeiger auf die [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle ab, und rufen Sie den anfänglichen Serverlocatorpunkt in Bits ab, indem Sie die [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen.
9.  Erstellen Sie einen Bits-Übertragungs Auftrag, indem Sie die [**ibackgroundcopymanager:: createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) -Methode aufrufen.
10. Rufen Sie einen Zeiger auf die cnotifyinterface-Rückruf Schnittstelle ab, und rufen Sie die [**ibackgroundcopyjob:: setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) -Methode auf, um Benachrichtigungen über auftragsbezogene Ereignisse zu empfangen. Weitere Informationen zu cnotifyinterface finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).
11. Aufrufen der [**ibackgroundcopyjob:: setnotifyflags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) -Methode, um die Benachrichtigungs Typen festzulegen, die empfangen werden sollen. In diesem Beispiel werden die **\_ \_ \_ Fehlerflags** **BG \_ Notify \_ Job \_ übertragen** und BG notify Job festgelegt.
12. Einen Zeiger auf die [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) -Schnittstelle erhalten. Verwenden Sie den **IBackgroundCopyJob2** -Zeiger, um zusätzliche Eigenschaften für den Auftrag festzulegen. Dieses Programm verwendet die [**IBackgroundCopyJob2:: setanmelde**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode, um die Anmelde Informationen für den Bits-Übertragungs Auftrag festzulegen.
13. Fügen Sie dem Bits-Übertragungs Auftrag Dateien hinzu, indem Sie [**ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)aufrufen. In diesem Beispiel verwendet die **ibackgroundcopyjob:: AddFile** -Methode die remotefile-und LocalFile-Variablen, die an die Funktion ServerAuthentication übermittelt wurden.
14. Nachdem die Datei hinzugefügt wurde, wenden Sie [**ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) an, um den Auftrag fortzusetzen.
15. Richten Sie eine while-Schleife ein, um auf die beendenmeldung von der Rückruf Schnittstelle zu warten, während der Auftrag übertragen wird.

    > [!Note]  
    > Dieser Schritt ist nur erforderlich, wenn es sich bei dem com-Apartment um ein Single Thread-Apartment handelt. Weitere Informationen finden Sie unter [Single Thread Apartments](../com/single-threaded-apartments.md).

     

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

    

    Die vorhergehende Schleife verwendet die [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) -Funktion, um die Anzahl der Millisekunden abzurufen, die seit Beginn der Übertragung des Auftrags verstrichen sind.

16. Nachdem der Bits-Übertragungs Auftrag fertiggestellt wurde, entfernen Sie den Auftrag aus der Warteschlange, indem Sie [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)aufrufen.

Im folgenden Codebeispiel werden Anmelde Informationen für die Server Authentifizierung für einen Bits-Übertragungs Auftrag angegeben.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Beispiel: allgemeine Klassen](common-classes.md)
</dt> </dl>

 

 