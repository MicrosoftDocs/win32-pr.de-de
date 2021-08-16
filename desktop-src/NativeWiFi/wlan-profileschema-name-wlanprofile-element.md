---
description: Enthält den Namen eines WLAN-Profils.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: name (WLANProfile)-Element
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
ms.openlocfilehash: 6a6d19c043f7cc2e42ca8221e98b05e4afe7628b143bd572465f00e1d3652275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984113"
---
# <a name="name-wlanprofile-element"></a>name (WLANProfile)-Element

Das Element name (WLANProfile) enthält den Namen eines WLAN-Profils.

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

Das **Name-Element** wird durch das [**WLANProfile-Element**](wlan-profileschema-wlanprofile-element.md) definiert.

## <a name="remarks"></a>Hinweise

Bei Namen wird die Groß-/Kleinschreibung beachtet.

Bei Windows XP mit Service Pack 3 (SP3) und der Wlan-API für Windows XP mit Service Pack 2 (SP2) wird das Name-Element ignoriert, wenn das Profil im Profilspeicher gespeichert wird. Der Name des Profils wird von der SSID des Netzwerks abgeleitet. Bei Infrastrukturnetzwerkprofilen ist der Name des Profils die SSID des Netzwerks. Bei Ad-hoc-Netzwerkprofilen ist der Name des Profils die SSID des Ad-hoc-Netzwerks gefolgt von `-adhoc` . XML-Escapezeichen wie & werden nicht angezeigt. Vermeiden Sie die Verwendung von XML-Escapezeichen in SSID-Namen für Profile, die auf Windows XP mit SP3 oder der Wireless LAN-API für Windows XP mit SP2 bereitgestellt werden.

Für jedes Netzwerkprofil, das nur für Windows Vista oder Windows Server 2008 vorgesehen ist, kann der Name eine beliebige Zeichenfolge sein.

## <a name="examples"></a>Beispiele

Beispielprofile, die das **Name-Element** verwenden, finden Sie unter [Beispiele für Funkprofile.](wireless-profile-samples.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




