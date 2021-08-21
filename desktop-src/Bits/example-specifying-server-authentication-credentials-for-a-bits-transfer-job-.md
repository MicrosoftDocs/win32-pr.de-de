---
title: Angeben von Anmeldeinformationen für die Serverauthentifizierung für einen BITS-Übertragungsauftrag
description: Sie können verschiedene Authentifizierungsschemas für einen BITS-Übertragungsauftrag (Background Intelligent Transfer Service) angeben.
ms.assetid: 31db38f6-3639-4042-97f2-4f9d78942e15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 844be330a34eaa5cfbe154fb3e22ec4a62aa807a355f54318fec207959baf5bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701820"
---
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a>Angeben von Anmeldeinformationen für die Serverauthentifizierung für einen BITS-Übertragungsauftrag

Sie können verschiedene Authentifizierungsschemas für einen BITS-Übertragungsauftrag (Background Intelligent Transfer Service) angeben.

Das folgende Verfahren ruft ein Authentifizierungsschema ab und erstellt eine Authentifizierungsidentitätsstruktur. Anschließend erstellt die Anwendung einen BITS-Downloadauftrag und legt die Anmeldeinformationen für den Auftrag fest. Nachdem der Auftrag erstellt wurde, ruft die Anwendung einen Zeiger auf eine Rückrufschnittstelle ab und fragt den Status des BITS-Übertragungsauftrags ab. Nach Abschluss des Auftrags wird er aus der Warteschlange entfernt.

In diesem Beispiel werden der Header und die Implementierung verwendet, die in [Beispiel: Allgemeine Klassen](common-classes.md)definiert sind.

**So geben Sie Anmeldeinformationen für die Serverauthentifizierung für einen BITS-Übertragungsauftrag an**

1.  Erstellen Sie eine Containerstruktur, die [**BG \_ AUTH \_ SCHEME-Werte**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) Schemanamen zuweist.

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

    

2.  Initialisieren Sie COM-Parameter, indem Sie die CCoInitializer-Funktion aufrufen. Weitere Informationen zur CCoInitializer-Funktion finden Sie unter [Beispiel: Allgemeine Klassen.](common-classes.md)
3.  Bereiten Sie eine [**BG \_ AUTH \_ CREDENTIALS-Struktur vor.**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) Im Beispiel wird die [SecureZeroMemory-Funktion]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) verwendet, um die Speicherplätze zu löschen, die den vertraulichen Informationen zugeordnet sind. Die [SecureZeroMemory-Funktion]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) ist in WinBase.h definiert.
4.  Verwenden Sie die GetScheme-Funktion, um das Authentifizierungsschema abzurufen, das zum Herstellen einer Verbindung mit dem Server verwendet werden soll.

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

    

5.  Füllen Sie die [**BG \_ AUTH \_ CREDENTIALS-Struktur**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) mit dem von der GetScheme-Funktion zurückgegebenen Authentifizierungsschema und dem Benutzernamen und Kennwort auf, die an die ServerAuthentication-Funktion übergeben wurden.
6.  Abrufen eines Zeigers auf die [**IBackgroundCopyJob-Schnittstelle**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) (pJob).
7.  Initialisieren Sie die COM-Prozesssicherheit, indem [Sie CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)aufrufen. BITS erfordert mindestens die IMPERSONATE-Ebene des Identitätswechsels. BITS schlägt mit E \_ ACCESSDENIED fehl, wenn die richtige Identitätswechselebene nicht festgelegt ist.
8.  Rufen Sie einen Zeiger auf die [**IBackgroundCopyManager-Schnittstelle**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) ab, und rufen Sie den ersten Locator zu BITS ab, indem Sie die [CoCreateInstance-Funktion]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen.
9.  Erstellen Sie einen BITS-Übertragungsauftrag, indem Sie die [**IBackgroundCopyManager::CreateJob-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) aufrufen.
10. Rufen Sie einen Zeiger auf die CNotifyInterface-Rückrufschnittstelle ab, und rufen Sie die [**IBackgroundCopyJob::SetNotifyInterface-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) auf, um Benachrichtigungen über auftragsbezogene Ereignisse zu empfangen. Weitere Informationen zu CNotifyInterface finden Sie unter [Beispiel: Allgemeine Klassen.](common-classes.md)
11. Rufen Sie die [**IBackgroundCopyJob::SetNotifyFlags-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) auf, um die zu empfangende Benachrichtigungstypen festzulegen. In diesem Beispiel werden die Flags **BG \_ NOTIFY JOB \_ \_ TRANSFERD** und **BG NOTIFY JOB \_ \_ \_ ERROR** festgelegt.
12. Abrufen eines Zeigers auf die [**IBackgroundCopyJob2-Schnittstelle.**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) Verwenden Sie den **IBackgroundCopyJob2-Zeiger,** um zusätzliche Eigenschaften für den Auftrag festzulegen. Dieses Programm verwendet die [**IBackgroundCopyJob2::SetCredentials-Methode,**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) um die Anmeldeinformationen für den BITS-Übertragungsauftrag festzulegen.
13. Fügen Sie dateien zum BITS-Übertragungsauftrag hinzu, indem [**Sie IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)aufrufen. In diesem Beispiel verwendet die **IBackgroundCopyJob::AddFile-Methode** die Variablen remoteFile und localFile, die an die ServerAuthentication-Funktion übergeben wurden.
14. Nachdem die Datei hinzugefügt wurde, rufen [**Sie IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) auf, um den Auftrag fortzusetzen.
15. Richten Sie eine while-Schleife ein, um während der Auftragsübertragung von der Rückrufschnittstelle auf Die Nachricht beenden zu warten.

    > [!Note]  
    > Dieser Schritt ist nur erforderlich, wenn das COM-Apartment ein Singlethread-Apartment ist. Weitere Informationen finden Sie unter [Singlethread-Apartment.](../com/single-threaded-apartments.md)

     

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

    

    Die vorangehende Schleife verwendet die [GetTickCount-Funktion,](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) um die Anzahl der Millisekunden abzurufen, die seit der Übertragung des Auftrags verstrichen sind.

16. Nachdem der BITS-Übertragungsauftrag abgeschlossen ist, entfernen Sie den Auftrag aus der Warteschlange, indem [**Sie IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)aufrufen.

Im folgenden Codebeispiel werden Anmeldeinformationen für die Serverauthentifizierung für einen BITS-Übertragungsauftrag angegeben.


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

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Beispiel: Allgemeine Klassen](common-classes.md)
</dt> </dl>

 

 