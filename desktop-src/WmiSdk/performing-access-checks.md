---
description: Eine Zugriffsüberprüfung bestimmt, ob ein Sicherheitsdeskriptor dem Client oder Thread, der durch ein Zugriffstoken identifiziert wird, einen angegebenen Satz von Zugriffsrechten gewährt.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Durchführen von Zugriffsüberprüfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e06f2bccab886b38b53ecc3592371555b8c93a0ed12cdad0a4f039b62d62752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050508"
---
# <a name="performing-access-checks"></a>Durchführen von Zugriffsüberprüfungen

Eine Zugriffsüberprüfung bestimmt, ob ein Sicherheitsdeskriptor dem Client oder Thread, der durch ein Zugriffstoken identifiziert wird, einen angegebenen Satz von Zugriffsrechten gewährt. Sie können die Sicherheitsfunktion [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) von WMI-Clientanwendungen oder -Anbietern aufrufen, die in C++ oder C# geschrieben sind. Skripts und Visual Basic Anwendungen können keine Zugriffsüberprüfungen mithilfe der hier beschriebenen Methode durchführen.

Clientanwendungen sollten eine Zugriffsüberprüfung durchführen, um die Identität des Rückrufs zu ermitteln, wenn Ergebnisse an die vom asynchronen Clientaufruf bereitgestellte Senke zurückgegeben werden.

Wenn Anbieter die Identität der Clientanwendung oder des Skripts, die Bzw. das Daten anfordert, nicht annehmen können, sollten sie Zugriffsüberprüfungen für die folgenden Situationen durchführen:

-   Beim Zugriff auf Ressourcen, die nicht durch Zugriffssteuerungslisten (Access Control Lists, ACL) geschützt sind.
-   Wenn der Client eine Verbindung auf **\_ RPC-C-EBENE hergestellt \_ \_ hat, identifizieren Sie** den Identitätswechsel.

> [!Note]  
> C++- und C#-Anwendungen können steuern, ob Zugriffsüberprüfungen von einem separaten Prozess ausgeführt werden. Skripts und Visual Basic Anwendungen können einen Registrierungsschlüssel lesen oder ändern, um sicherzustellen, dass WMI Zugriffsüberprüfungen durchführt. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)

 

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



Das folgende Codebeispiel zeigt, wie Sie überprüfen, ob das Sicherheitstoken eines Clientanwendungsthreads Berechtigungen enthält, die für einen angegebenen Sicherheitsdeskriptor geeignet sind. Die Funktion verwendet die Zeichenfolge \\ "Domänenbenutzer" und gibt die SID zurück. Wenn der Aufruf fehlschlägt, gibt die Funktion **NULL** zurück, andernfalls muss der Aufrufer den zurückgegebenen Zeiger freigeben.


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

[Schützen Ihres Anbieters](securing-your-provider.md)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
