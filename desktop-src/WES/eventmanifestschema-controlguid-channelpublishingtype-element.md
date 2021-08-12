---
title: controlGuid (ChannelPublishingType)-Element
description: Identifiziert die Sitzungs-GUID für eine ETW-Sitzung, die WPP-Ereignisse enthält.
ms.assetid: a9e86468-8a97-4689-a258-85d253debf55
keywords:
- controlGuid-Element EventLog
topic_type:
- apiref
api_name:
- controlGuid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bd831592d7b01f8ffca102c2cab6626d74d6b666bf6f0d6cfc6e6311c4aa7eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589951"
---
# <a name="controlguid-channelpublishingtype-element"></a>controlGuid (ChannelPublishingType)-Element

Identifiziert die Sitzungs-GUID für eine ETW-Sitzung, die WPP-Ereignisse enthält.

``` syntax
<xs:element name="controlGuid"
    type="GUIDType"
 />
```

Das **controlGuid-Element** wird durch den komplexen [**ChannelPublishingType-Typ**](eventmanifestschema-channelpublishingtype-complextype.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**publishing (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





