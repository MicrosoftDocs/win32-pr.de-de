---
title: Treuhändrootca (servervalidationparameters)-Element-Verbindung
description: Erfasst den Fingerabdruck der Stamm Zertifizierungsstellen, die vom Client als vertrauenswürdig eingestuft werden. | Treuhändrootca-Element (servervalidationparameters)
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
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
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106364403"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a>Treuhänder-Element (servervalidationparameters) für Verbindungs Eigenschaften

Das Element " **Treuhänder" (servervalidationparameters)** erfasst den Fingerabdruck der Stamm Zertifizierungsstellen, die vom Client als vertrauenswürdig eingestuft werden.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

Das Element " **treuhändrootca** " wird durch den komplexen [**servervalidationparameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.

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

[**Servervalidationparameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Mögliche direkt übergeordnete Elemente in der Schema Instanz**
</dt> <dt>

[**ServerValidation (eaptype)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema Elemente](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





