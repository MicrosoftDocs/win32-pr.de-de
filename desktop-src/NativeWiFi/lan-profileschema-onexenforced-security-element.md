---
description: Gibt an, ob der automatische Konfigurationsdienst für kabelgebundene Netzwerke die Verwendung von 802.1X für die Portauthentifizierung erfordert.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: OneXEnforced(security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bcaa8604fb8b813417299725133e9c6e51f7d7510b540cf8495ff9009b9d1c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798440"
---
# <a name="onexenforced-security-element"></a>OneXEnforced(security)-Element

Das **OneXEnforced** -Element (Sicherheit) gibt an, ob der automatische Konfigurationsdienst für kabelgebundene Netzwerke die Verwendung von 802.1X für die Portauthentifizierung erfordert. Wenn **OneXEnforced** true ist, muss der automatische Konfigurationsdienst 802.1X für die Portauthentifizierung verwenden. Wenn **OneXEnforced** auf FALSE festgelegt ist, versucht der automatische Konfigurationsdienst, 802.1X für die Portauthentifizierung zu verwenden, aber der Dienst wird auf keine Authentifizierung zurückgreifen, wenn die 802.1X-Authentifizierung aus irgendeinem Grund fehlschlägt.

Dieses Element ist optional. Der Standardwert ist FALSE.

Dieses Element hat nur dann einen aussagekräftigen Wert, wenn [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) TRUE ist. Wenn **OneXEnabled** auf FALSE festgelegt ist, wird der Wert dieses Elements ignoriert.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

Das **OneXEnforced-Element** wird durch das [**Sicherheitselement**](lan-profileschema-security-msm-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Sicherheit**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Sicherheit (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




