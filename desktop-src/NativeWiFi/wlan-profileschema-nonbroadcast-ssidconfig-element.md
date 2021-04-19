---
description: Gibt an, ob eine Verbindung mit einem verborgenen Netzwerk hergestellt werden soll.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Nonbroadcast-Element (ssidconfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355557"
---
# <a name="nonbroadcast-ssidconfig-element"></a>Nonbroadcast-Element (ssidconfig)

Das Nonbroadcast (ssidconfig)-Element gibt an, ob eine Verbindung mit einem verborgenen Netzwerk hergestellt werden soll. Wenn ein Netzwerk seine SSID nicht überträgt, wird es als ausgeblendetes Netzwerk bezeichnet. Wenn mehrere SSIDs innerhalb des Profils festgelegt sind, müssen alle den gleichen nicht Broadcast Wert aufweisen.

Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf **ESS** festgelegt ist, kann dieser Wert entweder "true" oder "false" lauten. Wenn dieses Element nicht vorhanden ist, ist der Standardwert "false".

Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf **IBSS** festgelegt ist, muss dieser Wert "false" lauten. Wenn dieses Element nicht vorhanden ist, ist der Standardwert "false".

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

Das-Element wird durch das [**ssidconfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) -Element definiert.

## <a name="examples"></a>Beispiele

Ein Beispiel Profil, das das **Nonbroadcast** -Element verwendet, finden Sie unter [Beispiel für nicht-Broadcast profile](non-broadcast-profile-sample.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Ssidconfig (wlanprofile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




