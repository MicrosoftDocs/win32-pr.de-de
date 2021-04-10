---
title: Korrelations Element (systempropertiestype)
description: Die Aktivitäts Bezeichner, mit denen Consumer verwandte Ereignisse gruppieren können.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Korrelations Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956917"
---
# <a name="correlation-systempropertiestype-element"></a>Korrelations Element (systempropertiestype)

Die Aktivitäts Bezeichner, mit denen Consumer verwandte Ereignisse gruppieren können.

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

Das **Korrelations** Element wird durch den komplexen [**systempropertiestype**](eventschema-systempropertiestype-complextype.md) -Typ definiert.

## <a name="attributes"></a>Attributes



| Name              | type                                                | BESCHREIBUNG                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktivitäts-ID        | [**Guidtype**](eventschema-guidtype-simpletype.md) | Ein-Globally Unique Identifier, der die aktuelle Aktivität bezeichnet. Die mit diesem Bezeichner veröffentlichten Ereignisse sind Teil derselben Aktivität.<br/>                              |
| RelatedActivityID | [**Guidtype**](eventschema-guidtype-simpletype.md) | Ein-Globally Unique Identifier, der die Aktivität identifiziert, an die das Steuerelement übertragen wurde. Die zugehörigen Ereignisse haben dann diesen Bezeichner als ActivityId-Bezeichner.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





