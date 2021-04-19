---
description: Gibt an, ob für den automatischen Konfigurations Dienst für verkabelte Netzwerke die Verwendung von 802.1 x für die Port Authentifizierung erforderlich ist.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Onexerzwungene (Security)-Element
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
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362592"
---
# <a name="onexenforced-security-element"></a>Onexerzwungene (Security)-Element

Das **onexerzwungene** (Security)-Element gibt an, ob für den automatischen Konfigurations Dienst für verkabelte Netzwerke die Verwendung von 802.1 x für die Port Authentifizierung erforderlich ist. Wenn " **onexerzwungene** " den Wert "true" hat, muss der automatische Konfigurations Dienst 802.1 x für die Port Authentifizierung verwenden. Wenn " **onexerzwungene** " den Wert "false" hat, versucht der automatische Konfigurations Dienst, 802.1 x für die Port Authentifizierung zu verwenden. der Dienst wird jedoch auf keine Authentifizierung zurückgreifen, wenn die 802.1 x-Authentifizierung aus irgendeinem Grund fehlschlägt.

Dieses Element ist optional. Der Standardwert ist FALSE.

Dieses Element hat nur einen sinnvollen Wert, wenn [**onexaktivierte**](lan-profileschema-onexenabled-security-element.md) true ist. Wenn " **onexaktivierte** " den Wert "false" hat, wird der Wert dieses Elements ignoriert.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

Das **onexerzwungene** -Element wird durch das [**Security**](lan-profileschema-security-msm-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Sicherung**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Sicherheit (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




