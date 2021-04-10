---
title: EAP- \_ \_ Anmelde- \_ req (eaptypes. h)
description: Speichert EAP-Sicherheits Anmelde Informationen in einer EAP- \_ config- \_ Eingabe \_ Feld \_ Array-Struktur.
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040376"
---
# <a name="eap_cred_logon_req"></a>EAP- \_ \_ Anmelde- \_ req

Die **EAP- \_ \_ Anmelde- \_ req-** Struktur speichert EAP-Sicherheits Anmelde Informationen in einer [**EAP-config- \_ \_ Eingabe \_ Feld \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur.


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**EAP- \_ \_ Anmelde- \_ req**
</dt> <dd>

Die **EAP- \_ \_ Anmelde- \_ req-** Struktur speichert EAP-Sicherheits Anmelde Informationen, auf die durch den *pbuidata* -Parameter der [**interaktiven Datenstruktur der EAP- \_ \_ Benutzeroberfläche \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) verwiesen wird, wenn der *dwDataType* -Parameter des [**interaktiven EAP-UI- \_ \_ \_ \_ Datentyps**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) einen Anforderungstyp Die Eingabefelder in dieser Struktur sind identisch mit den Eingabefeldern, die von [**eaphostpeer-querykredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)zurückgegeben werden. **EAP \_ Die \_ Anmelde \_** Informationen für die Anmelde Informationen werden in der anfänglichen Anmelde Informationsanforderung verwendet, und EAP-Anmelde Informationen werden während einer Authentifizierung in der Wiederholungs Anforderung für Anmelde Informationen verwendet. [**\_ \_**](eap-cred-req.md)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **EAP- \_ \_ Anmelde- \_ req-** Struktur wird zur Unterstützung von einmaligem Anmelden (Single-Sign-on, SSO) verwendet.

Die **EAP- \_ \_ Anmelde- \_ req-** Struktur ist identisch mit der [**EAP- \_ \_ Anmelde \_ -**](eap-cred-logon-resp.md) /Struktur-Anmeldungs-Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_ \_ Eingabe \_ Feld \_ Array der EAP-Konfiguration**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**EAP- \_ Kred- \_ req**](eap-cred-req.md)
</dt> <dt>

[**interaktive EAP- \_ \_ Benutzeroberflächen \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**interaktiver EAP- \_ \_ UI- \_ \_ Datentyp**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**Eaphostpeer-querykredentialinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





