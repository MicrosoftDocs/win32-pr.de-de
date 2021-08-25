---
description: Gibt den Ursprung von 802.1X-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: useMSOneX-Element (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4a62f2f25ef2a4a52fae82e2ce8ddb097a4b434d7c2f8f35a2783703a617ad8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912640"
---
# <a name="usemsonex-ihv-element"></a>useMSOneX-Element (IHV)

Das **useMSOneX-Element** (IHV) gibt den Ursprung von 802.1X-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden.

Wenn **useMSOneX** true ist, verwenden IHV-Sicherheitskomponenten von Microsoft definierte 802.1X-Einstellungen. Wenn **useMSOneX** false ist, verwenden IHV-Sicherheitskomponenten vom Anbieter bereitgestellte 802.1X-Einstellungen.

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

Das -Element wird durch das [**IHV-Element**](wlan-profileschema-ihv-wlanprofile-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Ihv**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




