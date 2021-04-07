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
# <a name="example-using-sspi-authentication-encoding-with-bits"></a><span data-ttu-id="4abfc-103">Beispiel: Verwenden der SSPI-Authentifizierungs Codierung mit Bits</span><span class="sxs-lookup"><span data-stu-id="4abfc-103">Example: Using SSPI Authentication Encoding with BITS</span></span>

<span data-ttu-id="4abfc-104">Sie können die SSPI-Authentifizierung (Security Support Provider Interface) und die Background Intelligent Transfer Service (Bits)-Methoden verwenden, um die Anmelde Informationen von einem Benutzer zu erhalten, die Anmelde Informationen zu codieren und die codierten Anmelde Informationen für einen Bits-Übertragungs Auftrag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4abfc-104">You can use Security Support Provider Interface (SSPI) Authentication and Background Intelligent Transfer Service (BITS) methods to get the credentials from a user, encode the credentials, and set the encoded credentials on a BITS transfer job.</span></span> <span data-ttu-id="4abfc-105">Die Codierung ist erforderlich, um die Anmelde Informationsstruktur in Zeichen folgen zu konvertieren, die an einen Bits-Übertragungs Auftrag übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="4abfc-105">Encoding is required to convert credentials structure into strings that can be passed to a BITS transfer job.</span></span>

<span data-ttu-id="4abfc-106">Weitere Informationen zur SSPI-Authentifizierung und zu Methoden finden Sie unter [SSPI](../secauthn/sspi.md).</span><span class="sxs-lookup"><span data-stu-id="4abfc-106">For more information about SSPI authentication and methods, see [SSPI](../secauthn/sspi.md).</span></span>

<span data-ttu-id="4abfc-107">Im folgenden Verfahren werden die Anmelde Informationen des Benutzers mithilfe des Aushandlungs Sicherheitspakets angefordert.</span><span class="sxs-lookup"><span data-stu-id="4abfc-107">The following procedure prompts for credentials from the user by using the Negotiate security package.</span></span> <span data-ttu-id="4abfc-108">Das Programm erstellt eine Authentifizierungs Identitäts Struktur und füllt die Struktur mit den codierten Zeichen folgen auf, die den Benutzernamen, die Domäne und das Kennwort des Benutzers darstellen.</span><span class="sxs-lookup"><span data-stu-id="4abfc-108">The program creates an authentication identity structure and populates the structure with the encoded strings that represent the user name, domain, and password of the user.</span></span> <span data-ttu-id="4abfc-109">Das Programm erstellt dann einen Bits-Download Auftrag und legt den codierten Benutzernamen und das Kennwort als Anmelde Informationen für den Auftrag fest.</span><span class="sxs-lookup"><span data-stu-id="4abfc-109">Then the program creates a BITS download job and sets the encoded user name and password as the credentials for the job.</span></span> <span data-ttu-id="4abfc-110">Das Programm gibt die Authentifizierungs Identitäts Struktur frei, nachdem Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="4abfc-110">The program frees the authentication identity structure after it is no longer needed.</span></span>

<span data-ttu-id="4abfc-111">In diesem Beispiel werden der Header und die Implementierung verwendet, die in [Beispiel: allgemeine Klassen](common-classes.md)definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4abfc-111">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="4abfc-112">**So verwenden Sie die SSPI-Authentifizierungs Codierung mit Bits-Übertragungs Aufträgen**</span><span class="sxs-lookup"><span data-stu-id="4abfc-112">**To use SSPI authentication encoding with BITS transfer jobs**</span></span>

1.  <span data-ttu-id="4abfc-113">Initialisieren Sie com-Parameter, indem Sie die ccoinitializer-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4abfc-113">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="4abfc-114">Weitere Informationen zur ccoinitializer-Funktion finden Sie unter [Beispiel: allgemeine Klassen](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="4abfc-114">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="4abfc-115">Get-Zeiger für die [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)-, [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)-und [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4abfc-115">Get pointers for the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interfaces.</span></span> <span data-ttu-id="4abfc-116">In diesem Beispiel wird die [CComPtr-Klasse](/cpp/atl/reference/ccomptr-class?view=vs-2019) zum Verwalten von COM-Schnittstellen Zeigern verwendet.</span><span class="sxs-lookup"><span data-stu-id="4abfc-116">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="4abfc-117">Erstellen Sie eine " [fordui \_ Info](/windows/win32/api/wincred/ns-wincred-credui_infoa) "-Struktur, die Informationen zum Anpassen des Erscheinungs Bilds des Dialog Felds für die [Funktion "sspipromptforanmelde](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)Informationen" enthält.</span><span class="sxs-lookup"><span data-stu-id="4abfc-117">Create a [CREDUI\_INFO](/windows/win32/api/wincred/ns-wincred-credui_infoa) structure that contains information for customizing the appearance of the dialog box for the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span> <span data-ttu-id="4abfc-118">Fordern Sie dann die Anmelde Informationen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="4abfc-118">Then prompt for credentials from the user.</span></span> <span data-ttu-id="4abfc-119">Weitere Informationen finden Sie unter der [Funktion "sspipromptforanmelde](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)Informationen".</span><span class="sxs-lookup"><span data-stu-id="4abfc-119">For more information, see the [SspiPromptForCredentials Function](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).</span></span>
4.  <span data-ttu-id="4abfc-120">Codieren Sie die Struktur der Anmelde Informationen als Zeichen folgen, die mithilfe der [sspiencodeauthidentityasstrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) -Funktion an einen Bits-Übertragungs Auftrag übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="4abfc-120">Encode credential structure as strings that can be passed to a BITS transfer job by using the [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) function.</span></span>
5.  <span data-ttu-id="4abfc-121">Bereiten Sie eine [**BG \_ auth- \_ Anmelde**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) Informationsstruktur vor.</span><span class="sxs-lookup"><span data-stu-id="4abfc-121">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span>
6.  <span data-ttu-id="4abfc-122">Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="4abfc-122">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="4abfc-123">Bits erfordert mindestens die Identitätswechsel Ebene des Identitäts Wechsels.</span><span class="sxs-lookup"><span data-stu-id="4abfc-123">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="4abfc-124">Bits schlägt mit **E \_ AccessDenied** fehl, wenn die korrekte Identitätswechsel Ebene nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4abfc-124">BITS fails with **E\_ACCESSDENIED** if the correct impersonation level is not set.</span></span>
7.  <span data-ttu-id="4abfc-125">Rufen Sie den anfänglichen Serverlocatorpunkt in Bits ab, indem Sie die [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4abfc-125">Obtain the initial locator to BITS by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
8.  <span data-ttu-id="4abfc-126">Erstellen Sie einen Bits-Übertragungs Auftrag, indem Sie die [**ibackgroundcopymanager:: createjob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4abfc-126">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
9.  <span data-ttu-id="4abfc-127">Ruft den Bezeichner für die [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) -Schnittstelle ab und ruft die **ibackgroundcopyjob:: QueryInterface** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="4abfc-127">Get the identifier for the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface, and call the **IBackgroundCopyJob::QueryInterface** method.</span></span>
10. <span data-ttu-id="4abfc-128">Füllen Sie die [**BG \_ auth- \_ Anmelde**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) Informationsstruktur mit den codierten Benutzernamen-und Kenn Wort Zeichenfolgen auf, und legen Sie das Authentifizierungsschema auf Aushandeln (**BG \_ auth \_ Scheme-Schema \_ aushandeln**) fest</span><span class="sxs-lookup"><span data-stu-id="4abfc-128">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) structure with the encoded user name and password strings, and set the authentication scheme to Negotiate (**BG\_AUTH\_SCHEME\_NEGOTIATE**).</span></span>
11. <span data-ttu-id="4abfc-129">Verwenden Sie den [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) -Zeiger, um Anforderungen an Bits zu senden.</span><span class="sxs-lookup"><span data-stu-id="4abfc-129">Use the [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) pointer to make requests to BITS.</span></span> <span data-ttu-id="4abfc-130">Dieses Programm verwendet die [**IBackgroundCopyJob2:: setanmelde**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) -Methode, um die Anmelde Informationen für den Bits-Übertragungs Auftrag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4abfc-130">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
12. <span data-ttu-id="4abfc-131">Dateien hinzufügen, Eigenschaften ändern oder den Bits-Übertragungs Auftrag fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="4abfc-131">Add files, modify properties, or resume the BITS transfer job.</span></span>
13. <span data-ttu-id="4abfc-132">Nachdem der Bits-Übertragungs Auftrag fertiggestellt wurde, entfernen Sie den Auftrag aus der Warteschlange, indem Sie [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4abfc-132">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>
14. <span data-ttu-id="4abfc-133">Schließlich können Sie die Authentifizierungs Identitäts Struktur durch Aufrufen der [sspifreeauthidentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="4abfc-133">Finally, free the authentication identity structure by calling the [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) function.</span></span>

<span data-ttu-id="4abfc-134">Im folgenden Codebeispiel wird die Verwendung der SSPI-Authentifizierungs Codierung mit Bits-Übertragungs Aufträgen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4abfc-134">The following code example demonstrates how to use SSPI Authentication Encoding with BITS transfer jobs.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4abfc-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4abfc-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4abfc-136">SSPI</span><span class="sxs-lookup"><span data-stu-id="4abfc-136">SSPI</span></span>](../secauthn/sspi.md)
</dt> <dt>

[<span data-ttu-id="4abfc-137">**Ibackgroundcopymanager**</span><span class="sxs-lookup"><span data-stu-id="4abfc-137">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="4abfc-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="4abfc-138">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="4abfc-139">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="4abfc-139">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="4abfc-140">Beispiel: allgemeine Klassen</span><span class="sxs-lookup"><span data-stu-id="4abfc-140">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 