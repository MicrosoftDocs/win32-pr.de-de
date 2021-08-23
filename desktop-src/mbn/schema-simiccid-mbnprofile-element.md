---
description: Identifiziert die SIM-Identifikationsnummer für GSM-Geräte.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: SimIccID (MBNProfile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: 8a6e4a20d93396337e2af0f0533486618dc707760f1ccd5c4f20f399cbdbf203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777860"
---
# <a name="simiccid-mbnprofile-element"></a>SimIccID (MBNProfile)-Element

Das **SimIccID -Element (MBNProfile)** identifiziert die SIM-Identifikationsnummer für GSM-Geräte.

Dieses Element ist optional und wird vom Mobilen Breitbanddienst für die interne Verwendung festgelegt. Eine Anwendung sollte dieses Feld beim Erstellen oder Aktualisieren eines Profils nicht festlegen.

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

Das **SimIccID-Element** wird durch das [**MBNProfile-Element**](schema-mbnprofile-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




