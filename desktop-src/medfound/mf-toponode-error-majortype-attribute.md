---
description: Enthält den Haupt Medientyp für einen topologieknoten. Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, da der richtige Decoder nicht gefunden werden konnte.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: MF_TOPONODE_ERROR_MAJORTYPE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347832"
---
# <a name="mf_toponode_error_majortype-attribute"></a>MF- \_ toponode- \_ Fehler \_ majortype-Attribut

Enthält den Haupt Medientyp für einen topologieknoten. Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, da der richtige Decoder nicht gefunden werden konnte.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für alle Knoten Typen.

Das topologielader-Attribut kann das-Attribut festlegen. Anwendungen lesen dieses Attribut in der Regel, ohne es festzulegen.

Eine Liste möglicher Werte finden Sie unter [Hauptmedien Typen](media-type-guids.md).

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

[**Imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




