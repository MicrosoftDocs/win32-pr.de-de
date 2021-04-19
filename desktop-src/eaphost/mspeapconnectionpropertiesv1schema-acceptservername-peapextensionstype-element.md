---
title: Accept Servername (papextensionstype)-Element (EAPHost)
description: Gibt an, ob der Servername anhand der im Server Ames (servervalidationparameters)-Element angegebenen Namens Zeichenfolge validiert wird. | Accept-Servername (Peer-extensionstype)-Element
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- EAPHost-Element
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba4874b7c8761f35fa93387b23eaf5463a31bcf4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314603"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a>Accept Servername (papextensionstype)-Element (EAPHost)

Das Element "Accepted Servername **(Peer-extensionstype)** " gibt an, ob der Servername anhand der im Servername [**(servervalidationparameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) -Element angegebenen Namens Zeichenfolge validiert wird.

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

Das-Element wird durch das-Element von " [**Peer**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) Type" definiert.

## <a name="remarks"></a>Bemerkungen

Das Element " **Accept Servername** " ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

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

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema Elemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**Akzeptservername**](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





