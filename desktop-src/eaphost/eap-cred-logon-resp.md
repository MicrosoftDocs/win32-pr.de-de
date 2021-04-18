---
title: EAP- \_ Anmelde-e- \_ Mail-Anmeldung \_ (eaptypes. h)
description: Speichert EAP-Sicherheits Anmelde Informationen in einer EAP- \_ config- \_ Eingabe \_ Feld \_ Array-Struktur. | EAP- \_ Anmelde-e- \_ Mail-Anmeldung \_ (eaptypes. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351885"
---
# <a name="eap_cred_logon_resp"></a>EAP- \_ \_ Anmelde- \_ Anmeldedienst (e)

Die **EAP- \_ \_ Anmelde- \_** /Struktur-Anmeldeinformationen speichert EAP-Sicherheits Anmelde Informationen in einer [**EAP-config- \_ \_ Eingabe \_ Feld \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur.


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

**EAP- \_ \_ Anmelde- \_ Anmeldedienst (e)**
</dt> <dd>

Die **EAP- \_ \_ Anmelde- \_** /Struktur-Anmeldungs-Struktur speichert EAP-Sicherheits Anmelde Informationen, auf die der *pbuidata* -Parameter der [**\_ interaktiven \_ Benutzeroberflächen \_ Datenstruktur von EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) verweist, wenn der *dwDataType* -Parameter des [**interaktiven EAP-UI- \_ \_ \_ \_ Datentyps**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) einen Anforderungstyp Die Eingabefelder in dieser Struktur sind identisch mit den Eingabefeldern, die von [**eaphostpeer-querykredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)zurückgegeben werden. **EAP \_ Die \_ Anmelde \_** Informationen für die Anmelde Informationen werden in der ersten Anmelde Informationsanforderung verwendet, und EAP-Anmelde Informationen werden während einer Authentifizierung in der Wiederholungs Anforderung für Anmelde Informationen verwendet. [**\_ \_**](eap-cred-resp.md)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **EAP- \_ Anmelde- \_ /Struktur-Anmeldung \_** wird zur Unterstützung von einmaligem Anmelden (Single-Sign-on, SSO) verwendet.

Die **EAP- \_ \_ Anmelde- \_** /Struktur-Anmeldungs-Struktur ist identisch mit der [**EAP- \_ \_ Anmelde- \_ req-**](eap-cred-logon-req.md) Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eaphostpeer-querykredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[**\_ \_ Eingabe \_ Feld \_ Array der EAP-Konfiguration**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**EAP- \_ \_ Anmelde- \_ req**](eap-cred-logon-req.md)
</dt> <dt>

[**interaktive EAP- \_ \_ Benutzeroberflächen \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**interaktiver EAP- \_ \_ UI- \_ \_ Datentyp**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





