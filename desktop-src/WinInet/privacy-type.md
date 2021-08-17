---
title: Datenschutztyp (Wininet.h)
description: Gibt an, dass Datenschutzeinstellungen für Erstanbieter- oder Drittanbietercookies gelten.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6f29461f57a2209fde00b30bce7914c207958f27e28062e2c3bd3d94d442e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743727"
---
# <a name="privacy-type"></a>Datenschutztyp

Gibt an, dass Datenschutzeinstellungen für Erstanbieter- oder Drittanbietercookies gelten.

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**\_DATENSCHUTZTYP \_ \_ ERSTANBIETER**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Bezieht sich auf Datenschutzeinstellungen für Erstanbietercookies.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**DATENSCHUTZTYP \_ \_ EINES \_ DRITTANBIETERS**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Bezieht sich auf Datenschutzeinstellungen für Cookies von Drittanbietern.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Cookies werden als Erstanbieter und Drittanbieter kategorisiert. Ein Erstanbietercookie stammt aus der Hostdomäne. Wenn https://www.blueyonderairlines.com "" in der Adressleiste von Microsoft Internet Explorer gefunden wird, ist "www.blueyonderairlines.com" die Hostdomäne. Wenn beim Besuch dieser Seite ein Cookie aus einer anderen Domäne als "www.blueyonderairlines.com" (z. B. "www.fourthcoffee.com" ) festgelegt wird, gilt dieses Cookie als Drittanbietercookie.

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

