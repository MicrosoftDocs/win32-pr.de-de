---
title: Konto deaktiviert (WinNT-Anbieter)
description: Bei Verwendung des WinNT-Anbieters kann ein Konto mithilfe der IADsUser.AccountDisabled-Eigenschaft aktiviert oder deaktiviert werden.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Konto deaktiviert (WinNT-Anbieter)
- Account Disabled ADSI , WinNT provider
- WinNT-Anbieter ADSI , Benutzerverwaltungsbeispiele, Konto deaktiviert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1659bad4ab930615aed7d02e3c54fc3899b60eb476999676ff765fe2a2e94f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178505"
---
# <a name="account-disabled-winnt-provider"></a>Konto deaktiviert (WinNT-Anbieter)

Bei Verwendung des WinNT-Anbieters kann ein Konto mithilfe der [**IADsUser.AccountDisabled-Eigenschaft aktiviert oder deaktiviert**](iadsuser-property-methods.md) werden.

## <a name="example-1"></a>Beispiel 1

Das folgende Codebeispiel zeigt, wie Sie ein Konto mithilfe von Visual Basic ADSI deaktivieren.


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a>Beispiel 2

Das folgende Codebeispiel zeigt, wie Sie ein Konto mit C++ mit ADSI deaktivieren.


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




