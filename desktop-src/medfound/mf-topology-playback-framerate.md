---
description: Gibt die Aktualisierungsrate des Monitors an.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: MF_TOPOLOGY_PLAYBACK_FRAMERATE-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ada0743900629308b1f622881d545bfbc1648b1811b36ff1640e2df5b9b83b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875657"
---
# <a name="mf_topology_playback_framerate-attribute"></a>MF \_ TOPOLOGY \_ PLAYBACK \_ FRAMERATE-Attribut

Gibt die Aktualisierungsrate des Monitors an.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)auf, um dieses Attribut abzurufen.

Um dieses Attribut festzulegen, rufen Sie [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio)auf.

## <a name="applies-to"></a>Gilt für:

[**TOPOLOGIE**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Hinweise

Das Topologieladeprogramm verwendet dieses Attribut, um die Pipeline zu optimieren, bevor die Wiedergabe gestartet wird. Wenn Sie dieses Attribut festlegen, legen Sie auch das [MF \_ TOPOLOGY \_ STATIC PLAYBACK \_ \_ OPTIMIZATIONS-Attribut](mf-topology-static-playback-optimizations.md) auf **TRUE** fest.

Die Bildfrequenz wird als Verhältnis ausgedrückt. Die oberen 32 Bits des Attributwerts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner.

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

 

 




