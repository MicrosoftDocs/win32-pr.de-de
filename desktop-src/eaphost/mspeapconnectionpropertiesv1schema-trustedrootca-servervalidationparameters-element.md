---
title: Treuhändrootca-Element (servervalidationparameters)
description: Zeichnet den Fingerabdruck der Stamm Zertifizierungsstellen (CAS) auf, die vom Client als vertrauenswürdig eingestuft werden. | Treuhändrootca-Element (servervalidationparameters)
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
keywords:
- Treuhändrootca-Element EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b691c5075f1a42f87e558a9a1f0795b90e8bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869684"
---
# <a name="trustedrootca-servervalidationparameters-element"></a>Treuhändrootca-Element (servervalidationparameters)

Das Element " **thumbdrootca (servervalidationparameters)** " erfasst den Fingerabdruck der Stamm Zertifizierungsstellen, die vom Client als vertrauenswürdig eingestuft werden.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

Das Element " **treuhändrootca** " wird durch den komplexen [**servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.

## <a name="remarks"></a>Bemerkungen

Der Thumb-Abdruck ist eine hexadezimale Zeichenfolge, die den SHA-1-Hash des Zertifikats enthält. Das Element " **treuhändrootca** " ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Mögliche direkt übergeordnete Elemente in der Schema Instanz**
</dt> <dt>

[**ServerValidation (eaptype)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema Elemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





