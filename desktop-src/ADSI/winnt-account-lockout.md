---
title: Kontosperrung (WinNT-Anbieter)
description: Wenn die Anzahl fehlgeschlagener Anmeldeversuche überschritten wird, wird das Benutzerkonto für die vom lockoutDuration-Attribut angegebene Anzahl von Minuten gesperrt.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Kontosperrung ADSI, WinNT-Anbieter
- WinNT-Anbieter ADSI , Benutzerverwaltungsbeispiele, Kontosperrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e28c2a4bf58f5559070af78ca55235e8b10c16b2b856a63a256767d4d67a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838360"
---
# <a name="account-lockout-winnt-provider"></a>Kontosperrung (WinNT-Anbieter)

Wenn die Anzahl fehlgeschlagener Anmeldeversuche überschritten wird, wird das Benutzerkonto für die vom [**lockoutDuration-Attribut**](/windows/desktop/ADSchema/a-lockoutduration) angegebene Anzahl von Minuten gesperrt. Die [**IADsUser.IsAccountLocked-Eigenschaft**](iadsuser-property-methods.md) scheint die Eigenschaft zu sein, die zum Lesen und Ändern des Sperrstatus eines Benutzerkontos verwendet werden soll. Der WinNT ADSI-Anbieter verfügt jedoch über Einschränkungen, die die Verwendung der **IsAccountLocked-Eigenschaft** einschränken.

## <a name="resetting-the-account-lockout-status"></a>Zurücksetzen des Kontosperrungsstatus

Bei Verwendung des WinNT-Anbieters kann die [**IsAccountLocked-Eigenschaft**](iadsuser-property-methods.md) nur auf **FALSE** festgelegt werden, wodurch das Konto entsperrt wird. Beim Festlegen der **IsAccountLocked-Eigenschaft** auf **TRUE** ist ein Fehler zu sehen. Nur das System kann ein Konto sperren.

Im folgenden Codebeispiel wird veranschaulicht, wie sie Visual Basic ADSI verwenden, um ein Benutzerkonto zu entsperren.


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



Im folgenden Codebeispiel wird veranschaulicht, wie C++ mit ADSI zum Entsperren eines Benutzerkontos verwendet wird.


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



## <a name="reading-the-account-lockout-status"></a>Lesen des Kontosperrungsstatus

Mit dem WinNT-Anbieter kann die [**IsAccountLocked-Eigenschaft**](iadsuser-property-methods.md) verwendet werden, um zu bestimmen, ob ein Konto gesperrt ist. Wenn ein Konto gesperrt ist, enthält die **IsAccountLocked-Eigenschaft** **TRUE**. Wenn ein Konto nicht gesperrt ist, enthält die **IsAccountLocked-Eigenschaft** **FALSE**.

Im folgenden Codebeispiel wird veranschaulicht, wie sie Visual Basic ADSI verwenden, um zu bestimmen, ob ein Konto gesperrt ist.


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



 

 