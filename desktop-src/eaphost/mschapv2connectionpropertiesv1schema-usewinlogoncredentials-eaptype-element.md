---
title: Usewinlogonanmeldeinformationen (eaptype)-Element
description: Erfahren Sie mehr über das usewinlogonanmelde-Element (eaptype)-Element. Dieses Element steuert die Verwendung von winlogin-Anmelde Informationen.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Usewinlogon-Anmelde Informationen-Element EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730369"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Usewinlogonanmeldeinformationen (eaptype)-Element

Das **usewinlogonanmeldeinformationen (eaptype)** -Element steuert die Verwendung der winlogin-Anmelde Informationen.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

Das **usewinlogonanmelde** -Element wird durch das [**eaptype**](mschapv2connectionpropertiesv1schema-eaptype-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Wenn der Wert true ist, erhält der EAP-MS-CHAPv2 Anmelde Informationen von Winlogon. Wenn der Wert false ist, erhält EAP MS-CHAPv2 Anmelde Informationen vom Benutzer. Das **usewinlogon-Anmelde Informationen-Element (eaptype)** ist optional.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversionen |
|------|-------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Eaptype**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Eaptype**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mschapv2connectionpropertiesv1-Schema](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





