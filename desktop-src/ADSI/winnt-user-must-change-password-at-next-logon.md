---
title: Benutzer muss Kennwort bei der nächsten Anmeldung ändern (WinNT-Anbieter)
description: Um diese Option zu aktivieren, legen Sie das PasswordExpired-Attribut des Benutzers auf eins (1) fest. Durch Festlegen dieses Attributs auf 0 (null) kann sich der Benutzer anmelden, ohne das Kennwort zu ändern.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- Benutzer muss Kennwort bei der nächsten Anmeldung (WinNT-Anbieter) ADSI ändern
- Benutzer muss Kennwort bei der nächsten Anmeldung ADSI , WinNT-Anbieter ändern
- WinNT-Anbieter ADSI , Beispiele für die Benutzerverwaltung, Benutzer muss Kennwort bei der nächsten Anmeldung ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be50e5cdccb4969e59a5b32516a35278b867062e8cced2e80d96b26c56c6173b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023038"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a>Benutzer muss Kennwort bei der nächsten Anmeldung ändern (WinNT-Anbieter)

Um diese Option zu aktivieren, legen Sie das **PasswordExpired-Attribut** des Benutzers auf eins (1) fest. Durch Festlegen dieses Attributs auf 0 (null) kann sich der Benutzer anmelden, ohne das Kennwort zu ändern.

## <a name="example-1"></a>Beispiel 1

Das folgende Codebeispiel zeigt, wie Sie das Kennwort bei der nächsten Anmeldung ändern mithilfe von Visual Basic mit ADSI festlegen.


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a>Beispiel 2

Das folgende Codebeispiel zeigt, wie Sie das Kennwort bei der nächsten Anmeldungsoption mithilfe von C++ mit ADSI ändern.


```C++
IADsUser *pUser = NULL;
HRESULT hr;

hr=ADsGetObject(L"WinNT://Fabrikam/jeffsmith,user",
                IID_IADsUser,
                (void**)&pUser);
VARIANT var;
VariantInit(&var);
V_I4(&var)=1;
V_VT(&var)=VT_I4;
hr = pUser->Put(_bstr_t("PasswordExpired"),var); // User must change password.
hr = pUser->SetInfo();

VariantClear(&var);
pUser->Release();
```



 

 




