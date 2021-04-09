---
title: Lesevorgang kann das Kennwort nicht ändern (WinNT-Anbieter)
description: Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- Lesen des Benutzers kann das Kennwort nicht ändern (WinNT-Anbieter) ADSI
- Der Benutzer kann das Kennwort (WinNT-Anbieter) ADSI nicht ändern, lesen
- WinNT-Anbieter ADSI, Benutzer Verwaltungs Beispiele, Benutzer kann Kennwort nicht ändern, lesen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab257f620d3e103866639f8ecacb57cc924efec4
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2020
ms.locfileid: "103948477"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>Lesevorgang kann das Kennwort nicht ändern (WinNT-Anbieter)

Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann. Um zu ermitteln, ob der Benutzer diese Berechtigung mit dem WinNT-Anbieter erhalten hat, lesen Sie das ADS-Flag "ADS-Flag nicht **\_ \_ \_ \_ ändern** " der **UserFlags** -Eigenschaft des User-Objekts. Das Flag " **\_ \_ inserpasswd \_ cant \_ Change** " in der [**ADS- \_ \_ benutzerflag \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) -Enumeration ist definiert.

## <a name="example-code"></a>Beispielcode

Im folgenden Codebeispiel wird veranschaulicht, wie das **ADS \_ - \_ \_ \_** Flag für die Kennung "" mit der Eigenschaft " **UserFlags** " eines Benutzer Objekts abgerufen wird.


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Function UserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
    Dim oUser As IADs
    
    strPath = "WinNT://" + strDomain + "/" + strUser
    
    If "" <> strUserCred Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("WinNT:")
        Set oUser = dso.OpenDSObject(strPath, strUserCred, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strPath)
    End If
    
    If (oUser.Get("userFlags") And ADS_UF_PASSWD_CANT_CHANGE) <> 0 Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



Im folgenden Codebeispiel wird veranschaulicht, wie das **ADS \_ - \_ \_ \_** Flag für die Kennung "" mit der Eigenschaft " **UserFlags** " eines Benutzer Objekts abgerufen wird.


```C++
//***************************************************************************
//
//  UserCannotChangePassword()
//
//***************************************************************************

HRESULT UserCannotChangePassword(LPCWSTR pwszDomain, 
                                 LPCWSTR pwszUser, 
                                 LPCWSTR pwszUserCred, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
{
    if(NULL == pwszDomain || NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
    *pfCannotChangePassword = FALSE;

    HRESULT hr;
    IADs *pads;

    CComBSTR sbstrADsPath = L"WinNT://";
    sbstrADsPath += pwszDomain;
    sbstrADsPath += "/";
    sbstrADsPath += pwszUser;

    hr = ADsOpenObject( sbstrADsPath,
                        pwszUserCred,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("userFlags"), &svar);
        if(SUCCEEDED(hr))
        {
            if(ADS_UF_PASSWD_CANT_CHANGE & svar.lVal)
            {
                *pfCannotChangePassword = TRUE;
            }
            else
            {
                *pfCannotChangePassword = FALSE;
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




