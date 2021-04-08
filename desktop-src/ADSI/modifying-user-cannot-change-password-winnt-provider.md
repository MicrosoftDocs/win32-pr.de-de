---
title: Ändern des Benutzers kann das Kennwort nicht ändern (WinNT-Anbieter)
description: Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann.
ms.assetid: 071a817b-087e-49ee-af1a-6f190493cac0
ms.tgt_platform: multiple
keywords:
- Ändern des Benutzers kann das Kennwort nicht ändern (WinNT-Anbieter)
- Benutzer kann Kennwort nicht ändern (WinNT-Anbieter), ändern
- WinNT-Anbieter ADSI, Benutzer Verwaltungs Beispiele, Benutzer kann Kennwort nicht ändern, ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e14e9bac51bae2edf4b9f6f571f20c75563a4d03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707403"
---
# <a name="modifying-user-cannot-change-password-winnt-provider"></a>Ändern des Benutzers kann das Kennwort nicht ändern (WinNT-Anbieter)

Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann. Um diese Berechtigung zu verweigern, fügen Sie der **UserFlags** -Eigenschaft des User-Objekts das ADS-Flag "-Kennwort für die Kenn **\_ \_ Wort \_ \_ Änderung** " hinzu. Um diese Berechtigung zu erteilen, entfernen Sie das Flag " **ADS- \_ \_ Kennwort nicht \_ \_ ändern** " aus der **UserFlags** -Eigenschaft des User-Objekts.

## <a name="example-code"></a>Beispielcode

Im folgenden Codebeispiel wird veranschaulicht, wie das ADS-Flag "- **\_ \_ Kennwort nicht \_ \_ ändern** " der **UserFlags** -Eigenschaft eines User-Objekts geändert wird.


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Sub SetUserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String, fUserCannotChangePassword As Boolean)
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
    
    lUserFlags = oUser.Get("userFlags")
    
    If fUserCannotChangePassword Then
        lUserFlags = lUserFlags Or ADS_UF_PASSWD_CANT_CHANGE
    Else
        lUserFlags = lUserFlags And Not ADS_UF_PASSWD_CANT_CHANGE
    End If
    
    ' Modify the userFlags property.
    oUser.Put "userFlags", lUserFlags
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



Im folgenden Codebeispiel wird veranschaulicht, wie das ADS-Flag "- **\_ \_ Kennwort nicht \_ \_ ändern** " der **UserFlags** -Eigenschaft eines User-Objekts geändert wird.


```C++
//***************************************************************************
//  SetUserCannotChangePassword()
//***************************************************************************

HRESULT SetUserCannotChangePassword(LPCWSTR pwszDomain,
                                    LPCWSTR pwszUser, 
                                    LPCWSTR pwszUserCred, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    if(NULL == pwszDomain || 
        NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
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
        CComBSTR sbstrPropName = "userFlags";
        CComVariant svar;
        
        hr = pads->Get(sbstrPropName, &svar);
        if(SUCCEEDED(hr))
        {
            if(fCannotChangePassword)
            {
                svar.lVal |= ADS_UF_PASSWD_CANT_CHANGE;
            }
            else
            {
                svar.lVal &= ~ADS_UF_PASSWD_CANT_CHANGE;
            }

            // Perform the change.
            hr = pads->Put(sbstrPropName, svar);

            // Commit the change.
            hr = pads->SetInfo();
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




