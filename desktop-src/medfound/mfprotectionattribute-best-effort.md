---
description: Legen Sie als Attribut für ein IMF OutputSchema-Objekt fest.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: MFPROTECTIONATTRIBUTE_BEST_EFFORT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215419"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a>MF Protection Attribute- \_ Attribut mit Best möglichen \_ Anstrengungen

Legen Sie als Attribut für ein [**IMF OutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) -Objekt fest. Wenn dieses Attribut vorhanden ist, wird ein fehlerhafter Versuch, den Schutz anzuwenden, ignoriert. Wenn der zugeordnete Attribut Wert **true** ist, sollte das Schutzschema mit dem [mfschutzattribute \_ \_](mfprotectionattribute-fail-over.md) -Attribut "Failover" angewendet werden.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Wenn **true**, erzwingen Sie das Schutzschema mit dem [mfschutzattribute \_ \_](mfprotectionattribute-fail-over.md) -Attribut "Failover", wenn das Festlegen dieses Schutzes fehlschlägt.

Legen Sie als Attribut für ein [**IMF OutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) -Objekt fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ UWP-apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ UWP-apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




