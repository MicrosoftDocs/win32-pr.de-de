---
title: Beispiel für die Verwendung der SSPI-Authentifizierungscodierung mit BITS
description: Sie können die Methoden security support provider interface (SSPI) authentication and Background Intelligent Transfer Service (BITS) verwenden, um die Anmeldeinformationen von einem Benutzer abzurufen, die Anmeldeinformationen zu codieren und die codierten Anmeldeinformationen für einen BITS-Übertragungsauftrag festzulegen.
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db13abe9b0bb6d8d4252575f70738f7b2f1a5c42b4cae1a4f042725c7bae15ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528800"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a>Beispiel: Verwenden der SSPI-Authentifizierungscodierung mit BITS

Sie können die Methoden security support provider interface (SSPI) authentication and Background Intelligent Transfer Service (BITS) verwenden, um die Anmeldeinformationen von einem Benutzer abzurufen, die Anmeldeinformationen zu codieren und die codierten Anmeldeinformationen für einen BITS-Übertragungsauftrag festzulegen. Die Codierung ist erforderlich, um die Anmeldeinformationsstruktur in Zeichenfolgen zu konvertieren, die an einen BITS-Übertragungsauftrag übergeben werden können.

Weitere Informationen zur SSPI-Authentifizierung und zu SSPI-Methoden finden Sie unter [SSPI](../secauthn/sspi.md).

Im folgenden Verfahren wird der Benutzer mithilfe des Sicherheitspakets Negotiate zur Eingabe von Anmeldeinformationen aufgefordert. Das Programm erstellt eine Authentifizierungsidentitätsstruktur und füllt die Struktur mit den codierten Zeichenfolgen auf, die den Benutzernamen, die Domäne und das Kennwort des Benutzers darstellen. Anschließend erstellt das Programm einen BITS-Downloadauftrag und legt den codierten Benutzernamen und das Kennwort als Anmeldeinformationen für den Auftrag fest. Das Programm gibt die Authentifizierungsidentitätsstruktur frei, nachdem sie nicht mehr benötigt wird.

In diesem Beispiel werden der Header und die Implementierung verwendet, die in [Beispiel: Allgemeine Klassen](common-classes.md)definiert sind.

**So verwenden Sie die SSPI-Authentifizierungscodierung mit BITS-Übertragungsaufträgen**

1.  Initialisieren Sie COM-Parameter, indem Sie die CCoInitializer-Funktion aufrufen. Weitere Informationen zur CCoInitializer-Funktion finden Sie unter [Beispiel: Allgemeine Klassen.](common-classes.md)
2.  Abrufen von Zeigern für die Schnittstellen [**IBackgroundCopyManager,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)und [**IBackgroundCopyJob2.**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) In diesem Beispiel wird die [CComPtr-Klasse](/cpp/atl/reference/ccomptr-class?view=vs-2019) verwendet, um COM-Schnittstellenzeiger zu verwalten.
3.  Erstellen Sie eine [CREDUI \_ INFO-Struktur,](/windows/win32/api/wincred/ns-wincred-credui_infoa) die Informationen zum Anpassen der Darstellung des Dialogfelds für die [SspiPromptForCredentials-Funktion](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)enthält. Fordern Sie dann den Benutzer zur Eingabe von Anmeldeinformationen auf. Weitere Informationen finden Sie unter [SspiPromptForCredentials-Funktion.](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)
4.  Codieren Sie die Anmeldeinformationsstruktur als Zeichenfolgen, die mithilfe der [SspiEncodeAuthIdentityAsStrings-Funktion](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) an einen BITS-Übertragungsauftrag übergeben werden können.
5.  Bereiten Sie eine [**BG \_ AUTH \_ CREDENTIALS-Struktur vor.**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials)
6.  Initialisieren Sie die COM-Prozesssicherheit, indem [Sie CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)aufrufen. BITS erfordert mindestens die IMPERSONATE-Ebene des Identitätswechsels. BITS schlägt mit **E \_ ACCESSDENIED fehl,** wenn die richtige Identitätswechselebene nicht festgelegt ist.
7.  Rufen Sie den anfänglichen Locator zu BITS ab, indem Sie die [CoCreateInstance-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen.
8.  Erstellen Sie einen BITS-Übertragungsauftrag, indem Sie die [**IBackgroundCopyManager::CreateJob-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) aufrufen.
9.  Rufen Sie den Bezeichner für die [**IBackgroundCopyJob2-Schnittstelle**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) ab, und rufen Sie die **IBackgroundCopyJob::QueryInterface-Methode** auf.
10. Füllen Sie die [**BG \_ AUTH \_ CREDENTIALS-Struktur**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) mit den codierten Benutzernamen- und Kennwortzeichenfolgen auf, und legen Sie das Authentifizierungsschema auf Negotiate **(BG \_ AUTH \_ SCHEME \_ NEGOTIATE)** fest.
11. Verwenden Sie den [**IBackgroundCopyJob2-Zeiger,**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) um Anforderungen an BITS zu stellen. Dieses Programm verwendet die [**IBackgroundCopyJob2::SetCredentials-Methode,**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) um die Anmeldeinformationen für den BITS-Übertragungsauftrag festzulegen.
12. Fügen Sie Dateien hinzu, ändern Sie Eigenschaften, oder setzen Sie den BITS-Übertragungsauftrag fort.
13. Nachdem der BITS-Übertragungsauftrag abgeschlossen ist, entfernen Sie den Auftrag aus der Warteschlange, indem [**Sie IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)aufrufen.
14. Schließlich können Sie die Authentifizierungsidentitätsstruktur freigeben, indem Sie die [SspiFreeAuthIdentity-Funktion](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) aufrufen.

Im folgenden Codebeispiel wird die Verwendung der SSPI-Authentifizierungscodierung mit BITS-Übertragungsaufträgen veranschaulicht.


```C++
#define SECURITY_WIN32
#define _SEC_WINNT_AUTH_TYPES

#include <windows.h>
#include <ntsecapi.h>
#include <bits.h>
#include <sspi.h>
#include <wincred.h>
#include <iostream>
#include <atlbase.h>
#include "CommonCode.h"

void PromptForCredentials(PWSTR pwTargetName)
{
    HRESULT hr;
    
    // If CoInitializeEx fails, the exception is unhandled and the program terminates
    CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    CComPtr<IBackgroundCopyManager> pQueueMgr;
    CComPtr<IBackgroundCopyJob> pJob;
    CComPtr<IBackgroundCopyJob2> pJob2;

    PSEC_WINNT_AUTH_IDENTITY_OPAQUE pAuthIdentityEx2 = NULL;
    DWORD dwFlags = 0;
    BOOL fSave = FALSE;
    BOOL bReturn = TRUE;

    CREDUI_INFO creduiInfo = { 0 };
    creduiInfo.cbSize = sizeof(creduiInfo);
    // Change the message text and caption to the actual text for your dialog.
    creduiInfo.pszMessageText = pwTargetName;
    creduiInfo.pszCaptionText = L"SSPIPFC title for the dialog box";

    try {
        // Prompt for credentials from user using Negotiate security package.
        DWORD dwRet = SspiPromptForCredentials(
            pwTargetName,
            &creduiInfo,
            0,
            L"Negotiate", 
            NULL,
            &pAuthIdentityEx2,
            &fSave,
            dwFlags
            );

        if (SEC_E_OK != dwRet) 
        {
            // Prompt for credentials failed.
            throw MyException(dwRet, L"SspiPromptForCredentials");
        }

        if (NULL != pAuthIdentityEx2) 
        {
            GUID guidJob;
            BG_AUTH_CREDENTIALS authCreds;

            PCWSTR pwUserName = NULL;
            PCWSTR pwDomainName = NULL;
            PCWSTR pwPassword = NULL;

            // Encode credential structure as strings that can
            // be passed to a BITS job.
            SECURITY_STATUS secStatus = SspiEncodeAuthIdentityAsStrings(
                pAuthIdentityEx2,
                &pwUserName,
                &pwDomainName,
                &pwPassword
                );

            if(SEC_E_OK != secStatus) 
            {
                // Encode authentication identity as strings.
                throw MyException(secStatus, L"SspiEncodeAuthIdentityAsStrings");   
            }

            // Show the encoded user name and domain name.
            wprintf(
                L"User Name: %s\nDomain Name: %s",
                pwUserName,
                pwDomainName
                );

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
            hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                CLSCTX_LOCAL_SERVER,
                __uuidof(IBackgroundCopyManager),
                (void**) &pQueueMgr);

            if (FAILED(hr))
            {
                // Failed to connect.
                throw MyException(hr, L"CoCreateInstance");
            }

            // Create a job.
            hr = pQueueMgr->CreateJob(
                L"EncodeSample", 
                BG_JOB_TYPE_DOWNLOAD, 
                &guidJob, 
                &pJob
                );

            if(FAILED(hr))
            {   
                // Failed to create a BITS job.
                throw MyException(hr, L"CreateJob");
            }

            // Get IBackgroundCopyJob2 interface.
            hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
            if (FAILED(hr)) 
            {
                // Failed to get a reference to the IBackgroundCopyJob2 interface.
                throw MyException(hr, L"QueryInterface(IBackgroundCopyJob2)");
            }

            // Create a BITS authentication structure from the encoded strings.
            authCreds.Target = BG_AUTH_TARGET_SERVER;
            authCreds.Scheme = BG_AUTH_SCHEME_NEGOTIATE;
            authCreds.Credentials.Basic.UserName = (LPWSTR)pwUserName;
            authCreds.Credentials.Basic.Password = (LPWSTR)pwPassword;

            // Set the credentials for the job.
            hr = pJob2->SetCredentials(&authCreds);
            if (FAILED(hr)) 
            {
                // Failed to set credentials.
                throw MyException(hr, L"SetCredentials");
            }

            // Modify the job's property values.
            // Add files to the job.
            // Activate (resume) the job in the transfer queue.

            // Remove the job from the transfer queue.
            hr = pJob->Complete();
            if (FAILED(hr)) 
            {
                // Failed to complete the job.
                throw MyException(hr, L"Complete");
            }
        }
    }
    catch(std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }
    catch(MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }

    // Free the auth identity structure.
    if (NULL != pAuthIdentityEx2)
    {
        SspiFreeAuthIdentity(pAuthIdentityEx2);
        pAuthIdentityEx2 = NULL;
    }

    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{
    PromptForCredentials(L"Target");
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SSPI](../secauthn/sspi.md)
</dt> <dt>

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Beispiel: Allgemeine Klassen](common-classes.md)
</dt> </dl>

 

 