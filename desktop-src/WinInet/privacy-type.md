---
title: Daten Schutztyp (WinInet. h)
description: Gibt an, dass die Datenschutzeinstellungen entweder für Drittanbieter-oder Drittanbieter Cookies gelten.
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
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859295"
---
# <a name="privacy-type"></a>Daten Schutztyp

Gibt an, dass die Datenschutzeinstellungen entweder für Drittanbieter-oder Drittanbieter Cookies gelten.

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**Daten \_ Schutztyp \_ erste \_ Partei**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Bezieht sich auf die Datenschutzeinstellungen für Cookies von ersten Anbietern.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**Datenschutz von \_ \_ Dritt \_ Anbietern**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Bezieht sich auf Datenschutzeinstellungen für Cookies von Drittanbietern.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Cookies werden als erste Partei und als Drittanbieter kategorisiert. Ein erst Anbieter Cookie stammt aus der Host Domäne. Wenn " https://www.blueyonderairlines.com " in der Adressleiste von Microsoft Internet Explorer gefunden wird, ist "www.blueyonderairlines.com" die Host Domäne. Wenn Sie diese Seite aufrufen und ein Cookie aus einer anderen Domäne als "www.blueyonderairlines.com" (z. b. "www.fourthcoffee.com") festgelegt ist, wird dieses Cookie als Drittanbieter-Cookie angesehen.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Privacygetzonepreferencew**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**Privacysetzonepreferencew**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

