---
title: Kennwort läuft nie ab (WinNT-Anbieter)
description: Um diese Option mit dem WinNT ADSI-Anbieter zu aktivieren, legen Sie das FLAG ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD (0x10000) für das UserFlags-Attribut fest. Hinweis Für Windows 2000 und höher verwenden Sie den LDAP ADSI-Anbieter für Benutzerverwaltungsvorgänge wie gezeigt.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- Kennwort läuft nie ab (WinNT-Anbieter)
- Password Never Expires ADSI , WinNT provider
- WinNT-Anbieter ADSI , Benutzerverwaltungsbeispiele, Kennwort läuft nie ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47cdd7dc181c2875e8de06b66233d727c5b132963921b163b02fc09cbdc051d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082164"
---
# <a name="password-never-expires-winnt-provider"></a>Kennwort läuft nie ab (WinNT-Anbieter)

Um diese Option mithilfe des WinNT ADSI-Anbieters zu aktivieren, legen Sie das **FLAG ADS \_ UF \_ DONT EXPIRE \_ \_ PASSWD** (0x10000) für das **UserFlags-Attribut** fest.

> [!Note]  
> Verwenden Windows 2000 und höher den LDAP ADSI-Anbieter für Benutzerverwaltungsvorgänge wie gezeigt. Weitere Informationen finden Sie unter [Kennwort läuft nie ab (LDAP-Anbieter).](password-never-expires.md)

 

## <a name="example-1"></a>Beispiel 1

Das folgende Codebeispiel zeigt, wie Sie die Option Kennwort läuft nie ab mithilfe von Visual Basic ADSI festlegen.


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a>Beispiel 2

Das folgende Codebeispiel zeigt, wie Sie die Option Kennwort läuft nie ab mit C++ mit ADSI festlegen.


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




