---
title: Accept-Servername (Peer-extensionstype)-Element
description: Gibt an, ob der Servername anhand der im Server Ames (servervalidationparameters)-Element angegebenen Namens Zeichenfolge validiert wird. | Accept-Servername (Peer-extensionstype)-Element
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Accept-Servername-Element EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d085122104c2764896801015c58fcbc9f72a1580
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961478"
---
# <a name="acceptservername-peapextensionstype-element"></a>Accept-Servername (Peer-extensionstype)-Element

Das Element "Accepted Servername **(Peer-extensionstype)** " gibt an, ob der Servername anhand der im Servername [**(servervalidationparameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) -Element angegebenen Namens Zeichenfolge validiert wird.

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

Das Element " **Accept Servername** " wird vom Element " [**Peer Name extensionstype**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) " definiert.

## <a name="remarks"></a>Bemerkungen

Das Element " **Accept Servername** " ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Peer-extensionstype**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**"Peer Erweiterungen"**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema Elemente](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





