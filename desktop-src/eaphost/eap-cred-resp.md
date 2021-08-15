---
title: EAP \_ CRED \_ RESP (Eaptypes.h)
description: Speichert EAP-Sicherheitsanmeldeinformationen in einer EAP \_ CONFIG \_ INPUT FIELD \_ \_ ARRAY-Struktur. | EAP \_ CRED \_ RESP (Eaptypes.h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b9bda55ed1b4aee9a9847740b25d46418c6ec3544dfdd6ba71b2c282042b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904637"
---
# <a name="eap_cred_resp"></a>EAP \_ CRED \_ RESP

Die **EAP \_ CRED \_ RESP-Struktur** speichert EAP-Sicherheitsanmeldeinformationen in einer [**EAP \_ CONFIG \_ INPUT FIELD \_ \_ ARRAY-Struktur.**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

**EAP \_ CRED \_ RESP**
</dt> <dd>

Die **EAP \_ CRED \_ RESP-Struktur** speichert sowohl die alten als auch die neuen EAP-Sicherheitsanmeldeinformationen, auf die der *pbUiData-Parameter* der [**EAP \_ INTERACTIVE UI \_ \_ DATA-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) verweist, wenn der *dwDataType-Parameter* von [**EAP INTERACTIVE UI \_ DATA \_ \_ \_ TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) einen Antworttyp für Anmeldeinformationen angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **EAP \_ CRED \_ RESP-Struktur** wird verwendet, um einmaliges Anmelden (Single Sign-On, SSO) zu unterstützen.

Die **EAP \_ CRED \_ RESP-Struktur** ist mit der [**EAP \_ CRED \_ REQ-Struktur**](eap-cred-req.md) identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost-Suppliplizierungsstrukturen](eap-host-supplicant-structures.md)
</dt> <dt>

[**EAP \_ CRED \_ REQ**](eap-cred-req.md)
</dt> <dt>

[**EAP \_ CRED \_ EXPIRY \_ REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**EAP \_ INTERACTIVE \_ UI \_ DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

