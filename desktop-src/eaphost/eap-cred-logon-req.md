---
title: EAP \_ CRED \_ LOGON \_ REQ (Eaptypes.h)
description: Speichert EAP-Sicherheitsanmeldeinformationen in einer EAP \_ CONFIG \_ INPUT FIELD \_ \_ ARRAY-Struktur.
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719abbed6c16deb6d3bfd61811f3f24253181364fe89f5823ee682bafef001e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785623"
---
# <a name="eap_cred_logon_req"></a>REQ \_ DER EAP-CRED-ANMELDUNG \_ \_

Die **EAP \_ CRED \_ LOGON \_ REQ-Struktur** speichert EAP-Sicherheitsanmeldeinformationen innerhalb einer [**EAP \_ CONFIG \_ INPUT FIELD \_ \_ ARRAY-Struktur.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**REQ \_ DER EAP-CRED-ANMELDUNG \_ \_**
</dt> <dd>

Die **EAP \_ CRED \_ LOGON \_ REQ-Struktur** speichert EAP-Sicherheitsanmeldeinformationen, auf die der *pbUiData-Parameter* der [**EAP \_ INTERACTIVE UI \_ \_ DATA-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) verweist, wenn der *dwDataType-Parameter* von [**EAP INTERACTIVE UI \_ DATA \_ \_ \_ TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) einen Anforderungstyp für Anmeldeinformationen angibt. Die Eingabefelder in dieser Struktur sind identisch mit den Eingabefeldern, die von [**EapHostPeerQueryCredentialInputFields zurückgegeben werden.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) **EAP \_ CRED \_ LOGON \_ REQ** wird in der anfänglichen Anforderung von Anmeldeinformationen verwendet, [**und EAP \_ CRED \_ REQ**](eap-cred-req.md) wird während einer Authentifizierung in der Anforderung zur Wiederholung von Anmeldeinformationen verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **EAP \_ CRED \_ LOGON \_ REQ-Struktur** wird verwendet, um einmaliges Anmelden (Single Sign-On, SSO) zu unterstützen.

Die **EAP \_ CRED \_ LOGON \_ REQ-Struktur** ist identisch mit der [**EAP \_ CRED \_ LOGON \_ RESP-Struktur.**](eap-cred-logon-resp.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EAP \_ CONFIG \_ INPUT \_ FIELD \_ ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**EAP \_ CRED \_ REQ**](eap-cred-req.md)
</dt> <dt>

[**INTERAKTIVE \_ \_ EAP-BENUTZEROBERFLÄCHENDATEN \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**EAP \_ INTERACTIVE \_ \_ \_ UI-DATENTYP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





