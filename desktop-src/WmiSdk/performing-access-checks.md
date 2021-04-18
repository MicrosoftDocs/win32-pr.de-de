---
description: Eine Zugriffs Überprüfung bestimmt, ob eine Sicherheits Beschreibung einen angegebenen Satz von Zugriffsrechten für den Client oder Thread gewährt, der durch ein Zugriffs Token identifiziert wird.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Ausführen von Zugriffs Überprüfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9af65605b6e96a5ad8b820de876d553f8d19202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347700"
---
# <a name="performing-access-checks"></a><span data-ttu-id="2d4ad-103">Ausführen von Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="2d4ad-103">Performing Access Checks</span></span>

<span data-ttu-id="2d4ad-104">Eine Zugriffs Überprüfung bestimmt, ob eine Sicherheits Beschreibung einen angegebenen Satz von Zugriffsrechten für den Client oder Thread gewährt, der durch ein Zugriffs Token identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-104">An access check determines whether a security descriptor grants a specified set of access rights to the client or thread identified by an access token.</span></span> <span data-ttu-id="2d4ad-105">Sie können die Security-Funktion [**accescheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) von WMI-Client Anwendungen oder-Anbietern, die in C++ oder c# geschrieben wurden, abrufen.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-105">You can call the security function [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) from WMI client applications or providers written in C++ or C#.</span></span> <span data-ttu-id="2d4ad-106">Skripts und Visual Basic Anwendungen können mithilfe der hier beschriebenen Methode keine Zugriffs Überprüfungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-106">Scripts and Visual Basic applications cannot perform access checks using the method described here.</span></span>

<span data-ttu-id="2d4ad-107">Client Anwendungen sollten eine Zugriffs Überprüfung durchführen, um die Identität des Rückrufs zu ermitteln, wenn Ergebnisse an die Senke zurückgegeben werden, die durch den asynchronen Client aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-107">Client applications should do an access check to determine the identity of the callback when returning results to the sink provided by the client asynchronous call.</span></span>

<span data-ttu-id="2d4ad-108">Wenn Anbieter die Identität der Client Anwendung oder des Skripts, das Daten anfordert, nicht annehmen können, sollten Sie in den folgenden Situationen Zugriffs Überprüfungen durchführen:</span><span class="sxs-lookup"><span data-stu-id="2d4ad-108">When providers cannot impersonate the client application or script that is requesting data, they should perform access checks for the following situations:</span></span>

-   <span data-ttu-id="2d4ad-109">Beim Zugriff auf Ressourcen, die nicht durch Zugriffs Steuerungs Listen (Access Control Lists, ACL) geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-109">When accessing resources that are not protected by access control lists (ACL).</span></span>
-   <span data-ttu-id="2d4ad-110">Wenn der Client eine Verbindung mit der RPC-C-Ebene hergestellt hat, **\_ \_ \_ identifizieren** Sie die Identitätswechsel Ebene.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-110">When the client has connected at the **RPC\_C\_LEVEL\_IDENTIFY** impersonation level.</span></span>

> [!Note]  
> <span data-ttu-id="2d4ad-111">C++-und c#-Anwendungen können steuern, ob Zugriffs Überprüfungen von einem separaten Prozess ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-111">C++ and C# applications can control whether access checks are performed by a separate process.</span></span> <span data-ttu-id="2d4ad-112">Skripts und Visual Basic Anwendungen können einen Registrierungsschlüssel lesen oder ändern, um sicherzustellen, dass WMI Zugriffs Überprüfungen ausführt.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-112">Scripts and Visual Basic applications can read or change a registry key to ensure that WMI performs access checks.</span></span> <span data-ttu-id="2d4ad-113">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-113">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

 

<span data-ttu-id="2d4ad-114">Das Codebeispiel in diesem Thema erfordert die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-114">The code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#include <lmcons.h>
#define _WIN32_DCOM
#define SECURITY_WIN32
#include <wbemidl.h>
#include <security.h>
#include <safestr.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "Secur32.lib")
```



<span data-ttu-id="2d4ad-115">Im folgenden Codebeispiel wird veranschaulicht, wie Sie überprüfen, ob das Sicherheits Token eines Client Anwendungs Threads Berechtigungen enthält, die für eine angegebene Sicherheits Beschreibung geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-115">The following code example shows how to check that the security token of a client application thread contains permissions appropriate to a specified security descriptor.</span></span> <span data-ttu-id="2d4ad-116">Die Funktion übernimmt die Zeichenfolge "Domain \\ User" und gibt die SID zurück.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-116">The function takes the string "domain\\user" and returns the SID.</span></span> <span data-ttu-id="2d4ad-117">Wenn der Aufruf fehlschlägt, gibt die Funktion **null** zurück, andernfalls muss der Aufrufer den zurückgegebenen Zeiger freigeben.</span><span class="sxs-lookup"><span data-stu-id="2d4ad-117">If the call fails, the function returns **NULL**, otherwise the caller must free the returned pointer.</span></span>


```C++
BYTE * GetSid(LPWSTR pwcUserName)
{
    DWORD dwSidSize = 0, dwDomainSize = 0;
    SID_NAME_USE use;

    // first call is to get the size
    BOOL bRet = LookupAccountNameW(

      NULL,            // system name
      pwcUserName,     // account name
      NULL,            // security identifier
      &dwSidSize,      // size of security identifier
      NULL,            // domain name
      &dwDomainSize,   // size of domain name
      &use             // SID-type indicator
      );    

    if(bRet == FALSE && ERROR_INSUFFICIENT_BUFFER 
        != GetLastError())\
        return NULL;

    BYTE * buff = new BYTE[dwSidSize];

    if(buff == NULL)
        return NULL;

    WCHAR * pwcDomain = new WCHAR[dwDomainSize];

    if(pwcDomain == NULL)

    {
        delete [] buff;
        return FALSE;
    }

    // Call to LookupAccountNameW actually gets the SID
    bRet = LookupAccountNameW(

      NULL,           // system name
      pwcUserName,    // account name
      buff,           // security identifier
      &dwSidSize,     // size of security identifier
      pwcDomain,      // domain name
      &dwDomainSize,  // size of domain name
      &use            // SID-type indicator
      );    

    delete [] pwcDomain;

    if(bRet == FALSE)
    {
        delete [] buff;
        return NULL;
    }

    return buff;
}

// This returns true if the caller is coming 
//   from the expected computer in the expected domain.

BOOL IsAllowed(LPWSTR pwsExpectedDomain, 
   LPWSTR pwsExpectedMachine)
{

    WCHAR wCallerName[UNLEN + 1];
    DWORD nSize = UNLEN + 1;

// Impersonate the caller and get its name

    HRESULT hr = CoImpersonateClient();
    if(FAILED(hr))

        return FALSE;

    BOOL bRet = GetUserNameExW(NameSamCompatible, 
       wCallerName, &nSize);

    CoRevertToSelf();

    if(bRet == FALSE)

        return FALSE;


    // take the expected domain and lan manager 
    //   style name and create a SID.  In actual
    // production code, it would be more efficient 
    //   to do this only when necessary

    WCHAR wExpectedName[UNLEN + 1];

    HRESULT hrCopyCat;
    hrCopyCat = StringCchCopy(wExpectedName,
        sizeof(pwsExpectedDomain)*sizeof(WCHAR)+1, 
        pwsExpectedDomain);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = 
        StringCchCat(wExpectedName,sizeof(wExpectedName)
        + 2*sizeof(WCHAR)+1, L"\\");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(pwsExpectedMachine)*sizeof(WCHAR)+1, 
        pwsExpectedMachine);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(WCHAR)+1, L"$");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
  

    // convert the two names to SIDs and compare.  
    // Note that SIDs are used since 
    //   the format of the names might vary.  

    BYTE * pCaller = GetSid(wCallerName);

    if(pCaller == NULL)

        return FALSE;

    BYTE * pExpected = GetSid(wExpectedName);

    if(pExpected == NULL)
    {
        delete [] pCaller;

        return FALSE;
    }

    bRet = EqualSid((PSID)pCaller, (PSID)pExpected);

    delete [] pCaller;
    delete [] pExpected;

    return bRet;
}
```



## <a name="related-topics"></a><span data-ttu-id="2d4ad-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d4ad-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d4ad-119">Auswählen der richtigen Registrierung</span><span class="sxs-lookup"><span data-stu-id="2d4ad-119">Choosing Correct Registration</span></span>](choosing-correct-registration.md)
</dt> <dt>

[<span data-ttu-id="2d4ad-120">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="2d4ad-120">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="2d4ad-121">Sichern Ihres Anbieters</span><span class="sxs-lookup"><span data-stu-id="2d4ad-121">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="2d4ad-122">Zugriff auf WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="2d4ad-122">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
