---
description: Gibt die Größe des Zielfensters für die Videowiedergabe an.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: MF_TOPOLOGY_PLAYBACK_MAX_DIMS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215136"
---
# <a name="mf_topology_playback_max_dims-attribute"></a>Maximal zulässige Anzahl von \_ \_ \_ \_ DiMS-Attributen

Gibt die Größe des Zielfensters für die Videowiedergabe an.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**mfgetattributesize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).

Um dieses Attribut festzulegen, muss [**mfsetattributesize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize)aufgerufen werden.

## <a name="applies-to"></a>Gilt für:

[**Imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Bemerkungen

Das topologielader verwendet dieses Attribut, um die Pipeline vor dem Start der Wiedergabe zu optimieren. Wenn Sie dieses Attribut festlegen, legen Sie auch das Attribut für die [ \_ \_ statische \_ Wiedergabe \_ der MF-Topologie](mf-topology-static-playback-optimizations.md) auf **true** fest.

Die oberen 32 Bits des Attribut Werts enthalten die Breite, und die unteren 32 Bits enthalten die Höhe, beide in Pixel.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> <dt>

[Video Qualitäts Verwaltung](video-quality-management.md)
</dt> </dl>

 

 




