---
title: Kontosperrung (WinNT-Anbieter)
description: Wenn die Anzahl der fehlgeschlagenen Anmeldeversuche überschritten wird, wird das Benutzerkonto für die im LockoutDuration-Attribut angegebene Anzahl von Minuten gesperrt.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Konto Sperre ADSI, WinNT-Anbieter
- WinNT-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Kontosperrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337873"
---
# <a name="account-lockout-winnt-provider"></a>Kontosperrung (WinNT-Anbieter)

Wenn die Anzahl der fehlgeschlagenen Anmeldeversuche überschritten wird, wird das Benutzerkonto für die im [**LockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) -Attribut angegebene Anzahl von Minuten gesperrt. Die Eigenschaft " [**IADsUser. isaccountlocked**](iadsuser-property-methods.md) " scheint die Eigenschaft zu sein, die zum Lesen und Ändern des Sperr Zustands eines Benutzerkontos verwendet werden soll, aber der WinNT ADSI-Anbieter weist Einschränkungen auf, die die Verwendung der Eigenschaft " **isaccountlocked** " einschränken.

## <a name="resetting-the-account-lockout-status"></a>Zurücksetzen des Konto Sperr Status

Bei Verwendung des WinNT-Anbieters kann die [**isaccountlocked**](iadsuser-property-methods.md) -Eigenschaft nur auf **false** festgelegt werden, wodurch das Konto entsperrt wird. Der Versuch, die **isaccountlocked** -Eigenschaft auf **true** festzulegen, schlägt fehl. Nur das System kann ein Konto sperren.

Im folgenden Codebeispiel wird veranschaulicht, wie Visual Basic mit ADSI verwendet wird, um ein Benutzerkonto zu entsperren.


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



Im folgenden Codebeispiel wird veranschaulicht, wie C++ mit ADSI verwendet wird, um ein Benutzerkonto zu entsperren.


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a>Lesen des Konto Sperr Status

Mit dem WinNT-Anbieter kann mithilfe der [**isaccountlocked**](iadsuser-property-methods.md) -Eigenschaft bestimmt werden, ob ein Konto gesperrt ist. Wenn ein Konto gesperrt ist, enthält die Eigenschaft " **isaccountlocked** " den Wert " **true**". Wenn ein Konto nicht gesperrt ist, enthält die Eigenschaft **isaccountlocked** den Wert **false**.

Im folgenden Codebeispiel wird veranschaulicht, wie Visual Basic mit ADSI verwendet wird, um zu bestimmen, ob ein Konto gesperrt ist.


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



Im folgenden Codebeispiel wird veranschaulicht, wie C++ mit ADSI verwendet wird, um zu bestimmen, ob ein Konto gesperrt ist.


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 