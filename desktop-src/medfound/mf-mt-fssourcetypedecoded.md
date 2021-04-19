---
description: Gibt an, ob ein Decoder beim Festlegen von Zeitstempeln decodierungszeit Stempel (DTS) verwenden kann.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366248"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>MF \_ MT- \_ Attribut "f"

Gibt an, dass ein Medientyp automatisch decodiert wird.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**


## <a name="remarks"></a>Bemerkungen
Ein Medientyp ist als Attribut gekennzeichnet, um anzugeben, dass dieser nicht in der physischen Quelle vorhanden ist und von der Pipeline synthetisiert wird. Der Wert 1 (true) gibt an, dass der Medientyp synthetisiert ist. Der Wert 0 (false) oder der Wert, der nicht vorhanden ist, gibt an, dass dies nicht der Fall ist.

In der aktuellen Version sollte dieses Attribut anstelle der MD_MT_FSSourceTypeDecoded Konstante mit dem folgenden GUID-Wert angegeben werden:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




