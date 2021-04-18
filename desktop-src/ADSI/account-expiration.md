---
title: Konto Ablauf (LDAP-Anbieter)
description: Um das Ablaufdatum des Kontos festzulegen, legen Sie die IADsUser. AccountExpirationDate-Eigenschaft auf den gewünschten Datumswert fest.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- Konto Ablauf ADSI, LDAP-Anbieter
- LDAP-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Konto Ablauf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03ea33d8d5abb219c2b562aa05058b5dec45919
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337253"
---
# <a name="account-expiration-ldap-provider"></a>Konto Ablauf (LDAP-Anbieter)

Um das Ablaufdatum des Kontos festzulegen, legen Sie die [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) -Eigenschaft auf den gewünschten Datumswert fest. Um das Ablaufdatum des Kontos zu deaktivieren, legen Sie das [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires) -Attribut auf NULL fest. In den folgenden Codebeispielen wird gezeigt, wie das Ablaufdatum festgelegt wird.


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
> Das [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires) -Attribut enthält das Ablaufdatum des Kontos. Das MMC-Snap-in "Active Directory-Benutzer und-Computer" zeigt das Datum an, an dem das Konto am Ende von abläuft. Das heißt, das MMC-Snap-in "Active Directory-Benutzer und-Computer" zeigt das Ablaufdatum des Kontos als einen Tag vor dem Datum im **AccountExpires** -Attribut an.

 

 

 