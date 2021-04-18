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
# <a name="performing-access-checks"></a>Ausführen von Zugriffs Überprüfungen

Eine Zugriffs Überprüfung bestimmt, ob eine Sicherheits Beschreibung einen angegebenen Satz von Zugriffsrechten für den Client oder Thread gewährt, der durch ein Zugriffs Token identifiziert wird. Sie können die Security-Funktion [**accescheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) von WMI-Client Anwendungen oder-Anbietern, die in C++ oder c# geschrieben wurden, abrufen. Skripts und Visual Basic Anwendungen können mithilfe der hier beschriebenen Methode keine Zugriffs Überprüfungen durchführen.

Client Anwendungen sollten eine Zugriffs Überprüfung durchführen, um die Identität des Rückrufs zu ermitteln, wenn Ergebnisse an die Senke zurückgegeben werden, die durch den asynchronen Client aufgerufen wird.

Wenn Anbieter die Identität der Client Anwendung oder des Skripts, das Daten anfordert, nicht annehmen können, sollten Sie in den folgenden Situationen Zugriffs Überprüfungen durchführen:

-   Beim Zugriff auf Ressourcen, die nicht durch Zugriffs Steuerungs Listen (Access Control Lists, ACL) geschützt sind.
-   Wenn der Client eine Verbindung mit der RPC-C-Ebene hergestellt hat, **\_ \_ \_ identifizieren** Sie die Identitätswechsel Ebene.

> [!Note]  
> C++-und c#-Anwendungen können steuern, ob Zugriffs Überprüfungen von einem separaten Prozess ausgeführt werden. Skripts und Visual Basic Anwendungen können einen Registrierungsschlüssel lesen oder ändern, um sicherzustellen, dass WMI Zugriffs Überprüfungen ausführt. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

 

Das Codebeispiel in diesem Thema erfordert die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.


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



Im folgenden Codebeispiel wird veranschaulicht, wie Sie überprüfen, ob das Sicherheits Token eines Client Anwendungs Threads Berechtigungen enthält, die für eine angegebene Sicherheits Beschreibung geeignet sind. Die Funktion übernimmt die Zeichenfolge "Domain \\ User" und gibt die SID zurück. Wenn der Aufruf fehlschlägt, gibt die Funktion **null** zurück, andernfalls muss der Aufrufer den zurückgegebenen Zeiger freigeben.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auswählen der richtigen Registrierung](choosing-correct-registration.md)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Sichern Ihres Anbieters](securing-your-provider.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
