---
title: Benutzer muss das Kennwort bei der nächsten Anmeldung ändern (WinNT-Anbieter)
description: Um diese Option zu aktivieren, legen Sie das passwordexpired-Attribut des Benutzers auf eins (1) fest. Wenn dieses Attribut auf NULL (0) festgelegt wird, kann sich der Benutzer anmelden, ohne das Kennwort zu ändern.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- Benutzer muss das Kennwort bei der nächsten Anmeldung (WinNT-Anbieter) ADSI ändern
- Benutzer muss das Kennwort bei der nächsten Anmeldung ändern ADSI, WinNT Provider
- WinNT-Anbieter ADSI, Benutzer Verwaltungs Beispiele, Benutzer muss Kennwort bei der nächsten Anmeldung ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787be5f5f4e1534574a68c179bb699ac68c61e3e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106370393"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a>Benutzer muss das Kennwort bei der nächsten Anmeldung ändern (WinNT-Anbieter)

Um diese Option zu aktivieren, legen Sie das **passwordexpired** -Attribut des Benutzers auf eins (1) fest. Wenn dieses Attribut auf NULL (0) festgelegt wird, kann sich der Benutzer anmelden, ohne das Kennwort zu ändern.

## <a name="example-1"></a>Beispiel 1

Im folgenden Codebeispiel wird gezeigt, wie die Option Kennwort bei der nächsten Anmeldung ändern mithilfe von Visual Basic mit ADSI festgelegt wird.


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a>Beispiel 2

Im folgenden Codebeispiel wird gezeigt, wie die Option Kennwort bei der nächsten Anmeldung ändern mithilfe von C++ mit ADSI festgelegt wird.


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



 

 




