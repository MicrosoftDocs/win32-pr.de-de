---
description: Gibt an, ob die Medien Senke, die diesem topologieknoten zugeordnet ist, ratlos ist.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: MF_TOPONODE_RATELESS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5c5ded4d8d09e8d45f766b03737954329c9202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345785"
---
# <a name="mf_toponode_rateless-attribute"></a>Attribut "MF- \_ toponode- \_ Attribut"

Gibt an, ob die Medien Senke, die diesem topologieknoten zugeordnet ist, ratlos ist.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Ausgabe Knoten (**MF- \_ topologieausgabe- \_ \_ Knoten**).

Wenn der Wert dieses Attributs ungleich 0 (null) ist, behandelt die Medien Sitzung die Medien Senke als ratlose Senke, unabhängig davon, ob die Medien Senke das **mediasink \_** -Attribut zurückgibt. Wenn dieses Attribut nicht festgelegt ist, wird davon ausgegangen, dass die Medien Senke nicht ratlos ist.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Imfmediasink:: getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




