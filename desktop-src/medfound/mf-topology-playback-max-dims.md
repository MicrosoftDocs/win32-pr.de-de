---
description: Gibt die Größe des Zielfensters für die Videowiedergabe an.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: MF_TOPOLOGY_PLAYBACK_MAX_DIMS-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98575a32b1d68414cb4d94a547273aa4986e03dc707023d5c40f9860b77b5a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604780"
---
# <a name="mf_topology_playback_max_dims-attribute"></a>MF \_ TOPOLOGY \_ PLAYBACK MAX \_ \_ DIMS-Attribut

Gibt die Größe des Zielfensters für die Videowiedergabe an.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize)auf, um dieses Attribut abzurufen.

Um dieses Attribut festzulegen, rufen Sie [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize)auf.

## <a name="applies-to"></a>Gilt für:

[**TOPOLOGIE**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Hinweise

Das Topologieladeprogramm verwendet dieses Attribut, um die Pipeline zu optimieren, bevor die Wiedergabe gestartet wird. Wenn Sie dieses Attribut festlegen, legen Sie auch das [MF \_ TOPOLOGY \_ STATIC PLAYBACK \_ \_ OPTIMIZATIONS-Attribut](mf-topology-static-playback-optimizations.md) auf **TRUE** fest.

Die oberen 32 Bits des Attributwerts enthalten die Breite und die unteren 32 Bits die Höhe in Pixel.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> <dt>

[Videoqualitätsverwaltung](video-quality-management.md)
</dt> </dl>

 

 




