---
title: Eap-Element (Benutzereigenschaft)
description: Erfahren Sie mehr über das Eap-Element. Dieses Element erfasst den ausgewählten Methodentyp und die methodenspezifische Konfiguration. | Eap-Element (Benutzereigenschaft)
ms.assetid: 4adef133-1d18-444a-baa3-5419b8cbe298
keywords:
- Eap-Element EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 877f7b00953bff6cbac585fc549e9fa44d1ba98e89720b2d1a8317c2538ed64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275693"
---
# <a name="eap-element-user-property"></a>Eap-Element (Benutzereigenschaft)

Das **Eap-Element** erfasst den ausgewählten Methodentyp und die methodenspezifische Konfiguration.

``` syntax
<xs:element name="Eap"
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Hinweise

Die -Methode kann die konstituierenden Elemente innerhalb des **Eap-Elements** definieren. Die -Methode führt auch eine Schemavalidierung für die Elemente in **Eap aus.**

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1-Schema](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





