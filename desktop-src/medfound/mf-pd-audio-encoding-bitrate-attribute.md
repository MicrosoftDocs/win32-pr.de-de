---
description: Gibt die audiocodierungs-Bitrate für die Präsentation in Bits pro Sekunde an. Dieses Attribut gilt für Präsentations Deskriptoren.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: MF_PD_AUDIO_ENCODING_BITRATE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49566ecb225482ef6513e056de8ba11763de603e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216881"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a>MF \_ PD \_ - \_ Attribut für die Audiocodierung- \_ Bitrate

Gibt die audiocodierungs-Bitrate für die Präsentation in Bits pro Sekunde an. Dieses Attribut gilt für Präsentations Deskriptoren.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Das-Attribut ist optional. Einige Formate verfügen über komplexere Codierungs Schemas, die nicht mithilfe dieses Attributs zusammengefasst werden können. Bei ASF-Dateien (Advanced Systems Format) beschreiben die folgenden Attribute kollektiv die Codierungs Bitrate:

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

 

 




