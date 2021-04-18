---
description: Gibt an, ob ein gemeinsam verwendeter Schlüssel verschlüsselt ist.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: geschütztes-Element (sharedkey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344059"
---
# <a name="protected-sharedkey-element"></a>geschütztes-Element (sharedkey)

Das geschützte (sharedkey)-Element gibt an, ob ein gemeinsam verwendeter Schlüssel verschlüsselt ist.

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

Das-Element wird durch das [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Für Windows Vista und Windows Server 2008 hat **Protected** immer den Wert true, wenn das Profil aus dem Profil Speicher abgerufen wurde (z. b. durch Aufrufen von [**wlangetprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).

Für Profile, die für die Verwendung unter Windows XP mit Service Pack 3 (SP3) oder der Wireless LAN-API für Windows XP mit Service Pack 2 (SP2) vorgesehen sind, muss **Protected** den Wert false aufweisen.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **geschützte** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**sharedkey (Sicherheit)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




