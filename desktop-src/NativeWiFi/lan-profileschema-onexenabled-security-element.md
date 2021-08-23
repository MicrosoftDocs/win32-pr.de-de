---
description: Gibt an, ob der automatische Konfigurationsdienst für kabelgebundene Netzwerke versucht, die Portauthentifizierung mit 802.1X zu versuchen.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: OneXEnabled -Element (Sicherheit)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aaaf5344078e4c8da2e5ee2118eed84563ebeb4daa8aebd700a29630b2fe4301
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801090"
---
# <a name="onexenabled-security-element"></a>OneXEnabled -Element (Sicherheit)

Das **OneXEnabled-Element** (Sicherheit) gibt an, ob der automatische Konfigurationsdienst für kabelgebundene Netzwerke versucht, die Portauthentifizierung mit 802.1X zu versuchen. Wenn **OneXEnabled** false ist, verwendet der automatische Konfigurationsdienst nie 802.1X für die Portauthentifizierung. Wenn **OneXEnabled** true ist, versucht der automatische Konfigurationsdienst die Portauthentifizierung mit 802.1X.

Dieses Element ist optional. Der Standardwert ist TRUE. Wenn **OneXEnabled** nicht in einem Profil angegeben ist, kann 802.1X für die Portauthentifizierung verwendet werden.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

Das **OneXEnabled-Element** wird durch das [**Sicherheitselement**](lan-profileschema-security-msm-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Sicherheit**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Sicherheit (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




