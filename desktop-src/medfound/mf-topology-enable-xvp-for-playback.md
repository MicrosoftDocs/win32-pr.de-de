---
description: Gibt an, ob der topologielader den Transcode-Video Prozessor (xvp) aktiviert. für Konvertierungen, Aktivieren der Hardware beschleunigten Farbkonvertierung.
title: MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK-Attribut (mspdl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350629"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>MF- \_ Topologie \_ \_ xvp \_ für \_ Wiedergabe Attribut aktivieren

Gibt an, ob der topologielader den Transcode-Video Prozessor (xvp) aktiviert. für Konvertierungen, Aktivieren der Hardware beschleunigten Farbkonvertierung.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**Imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut festgelegt ist, ruft das topologielader ggf. bei Bedarf während der nicht-transcode-topologieauflösung einen Pull in den Videoprozessor ab. Wenn Sie die Topologie zum Erstellen einer eigenen [imftopologie](/windows/win32/api/mfidl/nn-mfidl-imftopology) verwenden, weist das Attribut das Lade Modul an, anstelle des Legacy Farb Konverters xvp für Konvertierungen zu verwenden, sodass die hardwarebeschleunigte Farbkonvertierung aktiviert werden kann. der Legacy Farb Konverter ist nur Software.

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

[Direct3D Device Manager](direct3d-device-manager.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




