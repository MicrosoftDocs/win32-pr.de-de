---
title: Benutzer muss Kennwort bei der nächsten Anmeldung ändern (LDAP-Anbieter)
description: Legen Sie das pwdLastSet-Attribut auf 0 (null) fest, um zu erzwingen, dass ein Benutzer sein Kennwort bei der nächsten Anmeldung ändert. Um diese Anforderung zu entfernen, legen Sie das pwdLastSet-Attribut auf-1 fest. Das pwdLastSet-Attribut kann nicht auf einen anderen Wert festgelegt werden, außer durch das System.
ms.assetid: 0182151c-ddb7-4d08-98c6-c37e6e514cf0
ms.tgt_platform: multiple
keywords:
- Benutzer muss das Kennwort bei der nächsten Anmeldung ändern ADSI, LDAP Provider
- LDAP-Anbieter ADSI, Benutzer Verwaltungs Beispiele, Benutzer muss Kennwort bei der nächsten Anmeldung ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784ee0defbe3c8ec9abe2d110c2532b8c9688019
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036296"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a>Benutzer muss Kennwort bei der nächsten Anmeldung ändern (LDAP-Anbieter)

Legen Sie das **pwdLastSet** -Attribut auf 0 (null) fest, um zu erzwingen, dass ein Benutzer sein Kennwort bei der nächsten Anmeldung ändert. Um diese Anforderung zu entfernen, legen Sie das **pwdLastSet** -Attribut auf-1 fest. Das **pwdLastSet** -Attribut kann nicht auf einen anderen Wert festgelegt werden, außer durch das System.

Im folgenden Codebeispiel wird gezeigt, wie die Option "Benutzer muss Kennwort bei der nächsten Anmeldung ändern" festgelegt wird.


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



Im folgenden Codebeispiel wird gezeigt, wie die Option "Benutzer muss Kennwort bei der nächsten Anmeldung ändern" festgelegt wird.


```C++
/***************************************************************************

    SetUserMustChangePassword()

***************************************************************************/

HRESULT SetUserMustChangePassword(LPCWSTR pwszUserADsPath, 
                                  LPCWSTR pwszUsername, 
                                  LPCWSTR pwszPassword)
{
    IADs *pUser;
    HRESULT hr;

    hr = ADsOpenObject(pwszUserADsPath,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs,
                        (void**)&pUser);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        hr = pUser->Put(CComBSTR("pwdLastSet"), var);
        hr = pUser->SetInfo();

        VariantClear(&var);
        pUser->Release();
    }

    return hr;
}
```



 

 




