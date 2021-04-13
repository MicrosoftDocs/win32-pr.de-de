---
title: Kennwort läuft nie ab (LDAP-Anbieter)
description: Wenn Sie die Option Kennwort läuft nie ab mithilfe des LDAP-Anbieters aktivieren möchten, legen Sie \_ \_ für das \_ \_ userAccountControl-Attribut der userAccountControl-Eigenschaft das Kennwort für die Werbung
ms.assetid: b8d7e7fe-c846-45c4-9c5f-770530453836
ms.tgt_platform: multiple
keywords:
- Kennwort läuft nie ab ADSI, LDAP-Anbieter
- LDAP-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Kennwort läuft nie ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c0d9eb42d37c1bcc7d65495fa0d72609060407
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391010"
---
# <a name="password-never-expires-ldap-provider"></a>Kennwort läuft nie ab (LDAP-Anbieter)

Wenn Sie die Option Kennwort läuft nie ab mithilfe des LDAP-Anbieters aktivieren möchten, legen Sie für das [**userAccountControl-Attribut der userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) -Eigenschaft das Kennwort für die [**\_ \_ \_ \_ Werbung**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000

Set usr = GetObject("LDAP://CN=jeffsmith,OU=Sales,DC=Fabrikam,DC=Com")
flag = usr.Get("userAccountControl")
newFlag = flag Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "userAccountControl", newFlag
usr.SetInfo
```




```C++
#include <activeds.h>

IADsUser *pUser;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath = L"LDAP://serv1/cn=Jeff Smith,cn=Users,dc=Fabrikam,dc=com";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->Get(_bstr_t("userAccountControl"), &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(_bstr_t("userAccountControl"), var);

hr = pUser->SetInfo();
VariantClear(&var);
hr = pUser->Release();
```



 

 