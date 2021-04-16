---
description: Enthält den Namen eines drahtlosen LAN-Profils.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Name (wlanprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527788"
---
# <a name="name-wlanprofile-element"></a>Name (wlanprofile)-Element

Das Elementname (wlanprofile) enthält den Namen eines drahtlosen LAN-Profils.

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

Das **Name** -Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Bei Namen wird Groß-/Kleinschreibung beachtet.

Für Windows XP mit Service Pack 3 (SP3) und Wireless LAN API für Windows XP mit Service Pack 2 (SP2) wird das Name-Element ignoriert, wenn das Profil im Profil Speicher gespeichert wird. Der Name des Profils wird von der SSID des Netzwerks abgeleitet. Bei Infrastrukturnetzwerk Profilen ist der Name des Profils die SSID des Netzwerks. Bei Ad-hoc-Netzwerk Profilen ist der Name des Profils die SSID des Ad-hoc-Netzwerks gefolgt von `-adhoc` . XML-Escapezeichen, wie z. b. &, werden nicht angezeigt. Vermeiden Sie die Verwendung von XML-Escapezeichen in SSID-Namen für Profile, die unter Windows XP mit SP3 oder Wireless LAN API für Windows XP mit SP2 bereitgestellt werden

Für alle Netzwerk Profile, die ausschließlich für Windows Vista oder Windows Server 2008 vorgesehen sind, kann der Name eine beliebige Zeichenfolge sein.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **Name** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




