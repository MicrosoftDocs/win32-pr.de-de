---
title: Kontoablauf (LDAP-Anbieter)
description: Legen Sie zum Festlegen des Ablaufdatums des Kontos die IADsUser.AccountExpirationDate-Eigenschaft auf den gewünschten Datumswert fest.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- Kontoablauf ADSI, LDAP-Anbieter
- LDAP-Anbieter ADSI , Benutzerverwaltungsbeispiele, Kontoablauf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645ce5e2e1ae72ace0a8a642642eb5c15e7eabd63d51dba3f03596869bfb9efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024068"
---
# <a name="account-expiration-ldap-provider"></a>Kontoablauf (LDAP-Anbieter)

Legen Sie zum Festlegen des Ablaufdatums des Kontos die [**IADsUser.AccountExpirationDate-Eigenschaft**](iadsuser-property-methods.md) auf den gewünschten Datumswert fest. Um das Ablaufdatum des Kontos zu deaktivieren, legen Sie das [**AccountExpires-Attribut**](/windows/desktop/ADSchema/a-accountexpires) auf 0 (null) fest. In den folgenden Codebeispielen wird gezeigt, wie das Ablaufdatum festgelegt wird.


```VB
Public Sub SetUserAccountExpirationDate(User As IADsUser, ExpirationDate As Date)
    If 0 = ExpirationDate Then
        ' Disable the account expiration date.
        User.Put "accountExpires", 0
    Else
        ' Set the new account expiration date.
        User.AccountExpirationDate = ExpirationDate
    End If
    
    User.SetInfo
 
End Sub
```




```C++
/***************************************************************************

    SetUserAccountExpirationDate()

***************************************************************************/

HRESULT SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
    if(!pUser) 
    {
        return E_INVALIDARG;
    }

    HRESULT hr;

    if(!date || date < 0) 
    {
        // Account never expires. Set the accountExpires attribute to zero.
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        
        hr = pUser->Put(CComBSTR("accountExpires"), var); 

        VariantClear(&var);
    }
    else 
    {
        // Account expires on date.
        hr = pUser->put_AccountExpirationDate(date); 
    }

    if(S_OK == hr)
    {
        hr = pUser->SetInfo();
    }

    return hr;
}
```



> [!Note]  
> Das [**AccountExpires-Attribut**](/windows/desktop/ADSchema/a-accountexpires) enthält das Ablaufdatum des Kontos. Das Active Directory-Benutzer und -Computer MMC-Snap-In zeigt das Datum an, an dem das Konto am Ende abläuft. Das heißt, das Active Directory-Benutzer und -Computer MMC-Snap-In zeigt das Ablaufdatum des Kontos als einen Tag vor dem Im **accountExpires-Attribut enthaltenen Datum** an.

 

 

 