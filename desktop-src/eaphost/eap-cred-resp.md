---
title: EAP- \_ Kred \_ (eaptypes. h)
description: Speichert EAP-Sicherheits Anmelde Informationen in einer EAP- \_ config- \_ Eingabe \_ Feld \_ Array-Struktur. | EAP- \_ Kred \_ (eaptypes. h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c2176377dbde0f7c02d2a7d8083ad1bcff9e71
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106370368"
---
# <a name="eap_cred_resp"></a>EAP-Benutzer \_ -e/a \_

Die EAP-Struktur von "|" speichert EAP-Sicherheits Anmelde Informationen in einer [**EAP- \_ config- \_ Eingabe \_ Feld \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur. **\_ \_**


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

**EAP-Benutzer \_ -e/a \_**
</dt> <dd>

In der **EAP-Struktur \_ -.- \_** Struktur werden sowohl die alten als auch die neuen EAP-Sicherheits Anmelde Informationen gespeichert, auf die durch den *pbuidata* -Parameter der [**interaktiven Datenstruktur der EAP- \_ \_ Benutzeroberfläche \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) verwiesen wird, wenn der *dwDataType* -Parameter des [**interaktiven EAP-UI- \_ \_ \_ \_ Datentyps**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) einen Anmelde

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **EAP \_ -Struktur \_** von "|" wird zur Unterstützung von einmaligem Anmelden (Single-Sign-on, SSO) verwendet.

Die **EAP \_ -Struktur \_** "|" ist mit der [**EAP-Struktur " \_ \_ req req**](eap-cred-req.md) " identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost-Supplicant-Strukturen](eap-host-supplicant-structures.md)
</dt> <dt>

[**EAP- \_ Kred- \_ req**](eap-cred-req.md)
</dt> <dt>

[**EAP- \_ \_ ablaufungsablauf- \_ req**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**EAP- \_ \_ Ablaufs Ablauf (e) \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**interaktive EAP- \_ \_ Benutzeroberflächen \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

