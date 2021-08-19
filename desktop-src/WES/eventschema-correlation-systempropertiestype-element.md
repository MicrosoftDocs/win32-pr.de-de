---
title: Correlation (SystemPropertiesType)-Element
description: Die Aktivitätsbezeichner, die Consumer zum Gruppieren verwandter Ereignisse verwenden können.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Correlation-Element EventLog
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc301c43bbc8ba834949ae2a5056fb4359b5c8db3125da3d1729b18ac7aa1b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120358"
---
# <a name="correlation-systempropertiestype-element"></a>Correlation (SystemPropertiesType)-Element

Die Aktivitätsbezeichner, die Consumer zum Gruppieren verwandter Ereignisse verwenden können.

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Das **Correlation-Element** wird vom komplexen [**SystemPropertiesType-Typ**](eventschema-systempropertiestype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name              | type                                                | Beschreibung                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktivitäts-ID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Ein global eindeutiger Bezeichner, der die aktuelle Aktivität identifiziert. Die Ereignisse, die mit diesem Bezeichner veröffentlicht werden, sind Teil derselben Aktivität.<br/>                              |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Ein global eindeutiger Bezeichner, der die Aktivität identifiziert, an die das Steuerelement übertragen wurde. Die zugehörigen Ereignisse verfügen dann über diesen Bezeichner als ActivityID-Bezeichner.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





