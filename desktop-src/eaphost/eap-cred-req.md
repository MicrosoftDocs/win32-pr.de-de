---
title: EAP- \_ Kred \_ req (eaptypes. h)
description: Speichert EAP-Sicherheits Anmelde Informationen in einer EAP- \_ config- \_ Eingabe \_ Feld \_ Array-Struktur. | EAP- \_ Kred \_ req (eaptypes. h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106367320"
---
# <a name="eap_cred_req"></a>EAP- \_ Kred- \_ req

Die **EAP-Struktur " \_ \_ req req** " speichert EAP-Sicherheits Anmelde Informationen in einer [**EAP- \_ config- \_ Eingabe \_ Feld \_ Array**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) -Struktur.


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

**EAP- \_ Kred- \_ req**
</dt> <dd>

Die **EAP-Struktur " \_ \_ req req** " speichert sowohl die alten als auch die neuen EAP-Sicherheits Anmelde Informationen, auf die durch den *pbuidata* -Parameter der [**interaktiven Datenstruktur der EAP- \_ \_ Benutzeroberfläche \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) verwiesen wird, wenn der *dwDataType* -Parameter des [**interaktiven EAP-Benutzeroberflächen- \_ \_ \_ \_ Datentyps**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) einen

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **EAP-Struktur " \_ \_ req req** " wird zur Unterstützung von einmaligem Anmelden (Single Sign-on, SSO) verwendet.

Die **EAP-Struktur " \_ \_ req req** " ist identisch mit der " [**EAP" \_ - \_**](eap-cred-resp.md) Struktur "|".

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

[**EAP-Benutzer \_ -e/a \_**](eap-cred-resp.md)
</dt> <dt>

[**EAP- \_ \_ ablaufungsablauf- \_ req**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**EAP- \_ \_ Ablaufs Ablauf (e) \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**interaktive EAP- \_ \_ Benutzeroberflächen \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

