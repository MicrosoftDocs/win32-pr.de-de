---
title: Konto deaktiviert (WinNT-Anbieter)
description: Wenn Sie den WinNT-Anbieter verwenden, kann ein Konto mithilfe der IADsUser. accountdeaktiviert-Eigenschaft aktiviert oder deaktiviert werden.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Konto deaktiviert (WinNT-Anbieter)
- Konto deaktiviert ADSI, WinNT-Anbieter
- WinNT-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Konto deaktiviert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99b1fe45b71eda14547703f8721b2a13d581b8e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104394034"
---
# <a name="account-disabled-winnt-provider"></a>Konto deaktiviert (WinNT-Anbieter)

Wenn Sie den WinNT-Anbieter verwenden, kann ein Konto mithilfe der [**IADsUser. accountdeaktiviert**](iadsuser-property-methods.md) -Eigenschaft aktiviert oder deaktiviert werden.

## <a name="example-1"></a>Beispiel 1

Im folgenden Codebeispiel wird gezeigt, wie Sie ein Konto mit Visual Basic mit ADSI deaktivieren.


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

Im folgenden Codebeispiel wird gezeigt, wie Sie ein Konto mit C++ mit ADSI deaktivieren.


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




