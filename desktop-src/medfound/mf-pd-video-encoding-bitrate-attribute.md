---
description: Gibt die Video Codierungs Bitrate für die Präsentation in Bits pro Sekunde an. Dieses Attribut gilt für Präsentations Deskriptoren.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: MF_PD_VIDEO_ENCODING_BITRATE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355400"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a>MF \_ PD- \_ Video \_ Codierung- \_ Bitrate-Attribut

Gibt die Video Codierungs Bitrate für die Präsentation in Bits pro Sekunde an. Dieses Attribut gilt für Präsentations Deskriptoren.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist optional. Einige Formate verfügen über komplexere Codierungs Schemas, die nicht mithilfe dieses Attributs zusammengefasst werden können. Bei ASF-Dateien (Advanced Systems Format) beschreiben die folgenden Attribute kollektiv die Codierungs Bitrate:

-   [**MF \_ PD \_ ASF \_ File Properties \_ Max. \_ Bitrate**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**MF SD-Datei (in Bytes) \_ \_ \_ \_ \_ \_**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**MF \_ SD \_ , \_ \_ maximal zulässige \_ Daten \_ Bitrate**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**MF \_ SD, \_ ASF \_ streambitraten \_ Bitrate**](mf-sd-asf-streambitrates-bitrate-attribute.md)

Formate von Drittanbietern können andere benutzerdefinierte Attribute verwenden.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




