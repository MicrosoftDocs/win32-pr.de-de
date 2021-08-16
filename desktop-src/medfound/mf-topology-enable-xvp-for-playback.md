---
description: Gibt an, ob das Topologieladeprogramm den Transcode Video Processor (XVP) aktiviert. für Konvertierungen, wodurch die hardwarebeschleunigte Farbkonvertierung aktiviert wird.
title: MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: 3f315463ce1719617c5a48066401219f4b971f0a555cadf2af43b055a2b0e9a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875730"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>MF \_ TOPOLOGY \_ ENABLE \_ XVP FOR \_ \_ PLAYBACK-Attribut

Gibt an, ob das Topologieladeprogramm den Transcode Video Processor (XVP) aktiviert. für Konvertierungen, wodurch die hardwarebeschleunigte Farbkonvertierung aktiviert wird.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**TOPOLOGIE**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut festgelegt ist, pullt das Topologieladeprogramm den Videoprozessor bei Bedarf während der Topologieauflösung ohne Transcodierung. Wenn Sie die Topologie verwenden, um ihre eigene [CONVERTERTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) zu erstellen, weist dieses Attribut das Ladeprogramm an, XVP für Konvertierungen anstelle des Legacyfarbkonverters zu verwenden, sodass die hardwarebeschleunigte Farbkonvertierung aktiviert wird. Der Legacyfarbkonverter ist nur Software.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Direct3D-Geräte-Manager](direct3d-device-manager.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




