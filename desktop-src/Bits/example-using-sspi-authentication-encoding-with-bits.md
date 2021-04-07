---
title: Beispiel für die Verwendung der SSPI-Authentifizierungs Codierung mit Bits
description: Sie können die SSPI-Authentifizierung (Security Support Provider Interface) und die Background Intelligent Transfer Service (Bits)-Methoden verwenden, um die Anmelde Informationen von einem Benutzer zu erhalten, die Anmelde Informationen zu codieren und die codierten Anmelde Informationen für einen Bits-Übertragungs Auftrag festzulegen.
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b86248c4782789010a817755d9bc27b3e5373b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730161"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a>Beispiel: Verwenden der SSPI-Authentifizierungs Codierung mit Bits

Sie können die SSPI-Authentifizierung (Security Support Provider Interface) und die Background Intelligent Transfer Service (Bits)-Methoden verwenden, um die Anmelde Informationen von einem Benutzer zu erhalten, die Anmelde Informationen zu codieren und die codierten Anmelde Informationen für einen Bits-Übertragungs Auftrag festzulegen. Die Codierung ist erforderlich, um die Anmelde Informationsstruktur in Zeichen folgen zu konvertieren, die an einen Bits-Übertragungs Auftrag übergeben werden können.

Weitere Informationen zur SSPI-Authentifizierung und zu Methoden finden Sie unter [SSPI](../secauthn/sspi.md).

Im folgenden Verfahren werden die Anmelde Informationen des Benutzers mithilfe des Aushandlungs Sicherheitspakets angefordert. Das Programm erstellt eine Authentifizierungs Identitäts Struktur und füllt die Struktur mit den codierten Zeichen folgen auf, die den Benutzernamen, die Domäne und das Kennwort des Benutzers darstellen. Das Programm erstellt dann einen Bits-Download Auftrag und legt den codierten Benutzernamen und das Kennwort als Anmelde Informationen für den Auftrag fest. Das Programm gibt die Authentifizierungs Identitäts Struktur frei, nachdem Sie nicht mehr benötigt wird.

In diesem Beispiel werden der Header und die Implementierung verwendet, die in [Beispiel: allgemeine Klassen](common-classes.md)definiert sind.

**So verwenden Sie die SSPI-Authentifizierungs Codierung mit Bits-Übertragungs Aufträgen**

1.  Initialisieren Sie com-Parameter, indem Sie die ccoinitializer-Funktion aufrufen. Weitere Informationen zur ccoinitializer-Funktion finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).
2.  Get-Zeiger für die [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)-, [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)-und [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) -Schnittstellen. In diesem Beispiel wird die [CComPtr-Klasse](/cpp/atl/reference/ccomptr-class?view=vs-2019) zum Verwalten von COM-Schnittstellen Zeigern verwendet.
3.  Erstellen Sie eine " [fordui \_ Info](/windows/win32/api/wincred/ns-wincred-credui_infoa) "-Struktur, die Informationen zum Anpassen des Erscheinungs Bilds des Dialog Felds für die [Funktion "sspipromptforanmelde](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)Informationen" enthält. Fordern Sie dann die Anmelde Informationen des Benutzers an. Weitere Informationen finden Sie unter der [Funktion "sspipromptforanmelde](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)Informationen".
4.  Codieren Sie die Struktur der Anmelde Informationen als Zeichen folgen, die mithilfe der [sspiencodeauthidentityasstrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) -Funktion an einen Bits-Übertragungs Auftrag übergeben werden können.
5.  Bereiten Sie eine [**BG \_ auth- \_ Anmelde**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) Informationsstruktur vor.
6.  Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Bits erfordert mindestens die Identitätswechsel Ebene des Identitäts Wechsels. Bits schlägt mit **E \_ AccessDenied** fehl, wenn die korrekte Identitätswechsel Ebene nicht festgelegt ist.
7.  Rufen Sie den anfänglichen Serverlocatorpunkt in Bits ab, indem Sie die [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen.
8.  Erstellen Sie einen Bits-Übertragungs Auftrag, indem Sie die [**ibackgroundcopymanager:: createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) -Methode aufrufen.
9.  Ruft den Bezeichner für die [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) -Schnittstelle ab und ruft die **ibackgroundcopyjob:: QueryInterface** -Methode auf.
10. Füllen Sie die [**BG \_ auth- \_ Anmelde**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) Informationsstruktur mit den codierten Benutzernamen-und Kenn Wort Zeichenfolgen auf, und legen Sie das Authentifizierungsschema auf Aushandeln (**BG \_ auth \_ Scheme-Schema \_ aushandeln**) fest
11. Verwenden Sie den [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) -Zeiger, um Anforderungen an Bits zu senden. Dieses Programm verwendet die [**IBackgroundCopyJob2:: setanmelde**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode, um die Anmelde Informationen für den Bits-Übertragungs Auftrag festzulegen.
12. Dateien hinzufügen, Eigenschaften ändern oder den Bits-Übertragungs Auftrag fortsetzen.
13. Nachdem der Bits-Übertragungs Auftrag fertiggestellt wurde, entfernen Sie den Auftrag aus der Warteschlange, indem Sie [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)aufrufen.
14. Schließlich können Sie die Authentifizierungs Identitäts Struktur durch Aufrufen der [sspifreeauthidentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) -Funktion freigeben.

Im folgenden Codebeispiel wird die Verwendung der SSPI-Authentifizierungs Codierung mit Bits-Übertragungs Aufträgen veranschaulicht.


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

[**Ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Beispiel: allgemeine Klassen](common-classes.md)
</dt> </dl>

 

 