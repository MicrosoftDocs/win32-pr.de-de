---
title: UseWinLogonCredentials (EapType)-Element
description: Erfahren Sie mehr über das Element UseWinLogonCredentials (EapType). Dieses Element steuert die Verwendung von Winlogin-Anmeldeinformationen.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- UseWinLogonCredentials-Element EAPHost
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
ms.openlocfilehash: 2a407c505139562a155e5aa9d7ed57fed5d15077cf5d035ea8bb7bbe0e177363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086191"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>UseWinLogonCredentials (EapType)-Element

Das **Element UseWinLogonCredentials (EapType)** steuert die Verwendung der winlogin-Anmeldeinformationen.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

Das **UseWinLogonCredentials-Element** wird durch das [**EapType-Element**](mschapv2connectionpropertiesv1schema-eaptype-element.md) definiert.

## <a name="remarks"></a>Hinweise

True gibt an, dass EAP MS-CHAPv2 Anmeldeinformationen von winlogon erhält. False gibt an, dass EAP MS-CHAPv2 Anmeldeinformationen vom Benutzer erhält. Das **UseWinLogonCredentials -Element (EapType)** ist optional.

## <a name="requirements"></a>Anforderungen



| Rolle | Unterstützte Mindestversionen des Betriebssystems |
|------|-------------------------------|
| Client<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mschapv2connectionpropertiesv1-Schema](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





