---
description: Gibt an, ob der Dienst für die automatische Konfiguration von Kabel Netzwerken mithilfe von 802.1 x eine Port Authentifizierung durchführen soll.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Onexaktiviertes (Security)-Element
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
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216923"
---
# <a name="onexenabled-security-element"></a>Onexaktiviertes (Security)-Element

Das **onexaktivierte** (Security)-Element gibt an, ob der automatische Konfigurations Dienst für verkabelte Netzwerke mithilfe von 802.1 x eine Port Authentifizierung durchführen soll. Wenn " **onexaktivierte** " den Wert "false" hat, verwendet der automatische Konfigurations Dienst 802.1 x nie für die Port Authentifizierung. Wenn " **onexaktivierte** " den Wert "true" hat, versucht der automatische Konfigurations Dienst mithilfe von 802.1 x die Port Authentifizierung.

Dieses Element ist optional. Der Standardwert ist TRUE. Wenn **onexused** nicht in einem Profil angegeben ist, kann 802.1 x für die Port Authentifizierung verwendet werden.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

Das **onexaktivierte** -Element wird durch das [**Security**](lan-profileschema-security-msm-element.md) -Element definiert.

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

 

 




