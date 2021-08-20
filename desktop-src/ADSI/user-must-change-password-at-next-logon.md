---
title: Benutzer muss Kennwort bei der nächsten Anmeldung ändern (LDAP-Anbieter)
description: Um zu erzwingen, dass ein Benutzer sein Kennwort bei der nächsten Anmeldung ändert, legen Sie das pwdLastSet-Attribut auf 0 (null) fest. Um diese Anforderung zu entfernen, legen Sie das pwdLastSet-Attribut auf -1 fest. Das pwdLastSet-Attribut kann nur vom System auf einen anderen Wert festgelegt werden.
ms.assetid: 0182151c-ddb7-4d08-98c6-c37e6e514cf0
ms.tgt_platform: multiple
keywords:
- Benutzer muss Kennwort bei der nächsten Anmeldung ADSI , LDAP-Anbieter ändern
- LDAP-Anbieter ADSI , Beispiele für die Benutzerverwaltung, Benutzer muss Kennwort bei der nächsten Anmeldung ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103703381512e82eee608d452b921429c87ef3ce6b7d59017fd07bc081e75ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648840"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a>Benutzer muss Kennwort bei der nächsten Anmeldung ändern (LDAP-Anbieter)

Um zu erzwingen, dass ein Benutzer sein Kennwort bei der nächsten Anmeldung ändert, legen Sie das **pwdLastSet-Attribut** auf 0 (null) fest. Um diese Anforderung zu entfernen, legen Sie das **pwdLastSet-Attribut** auf -1 fest. Das **pwdLastSet-Attribut** kann nur vom System auf einen anderen Wert festgelegt werden.

Im folgenden Codebeispiel wird veranschaulicht, wie die Option "Benutzer muss Kennwort bei der nächsten Anmeldung ändern" festgelegt wird.


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



Im folgenden Codebeispiel wird veranschaulicht, wie die Option "Benutzer muss Kennwort bei der nächsten Anmeldung ändern" festgelegt wird.


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



 

 




