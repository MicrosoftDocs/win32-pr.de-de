---
description: Gibt den Ursprung der 802.1 x-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: usemsonex (IHV)-Element
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
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959974"
---
# <a name="usemsonex-ihv-element"></a>usemsonex (IHV)-Element

Das **usemsonex** (IHV)-Element gibt den Ursprung der 802.1 x-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden.

Wenn **usemsonex** auf true festgelegt ist, verwenden die IHV-Sicherheitskomponenten von Microsoft definierte 802.1 x-Einstellungen. Wenn **usemsonex** den Wert false hat, verwenden IHV-Sicherheitskomponenten vom Hersteller bereitgestellte 802.1 x-Einstellungen.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

Das-Element wird durch das [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**IHV (wlanprofile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




