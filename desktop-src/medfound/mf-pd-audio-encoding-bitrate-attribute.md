---
description: Gibt die Audiocodierungsbitrate für die Präsentation in Bits pro Sekunde an. Dieses Attribut gilt für Präsentationsdeskriptoren.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: MF_PD_AUDIO_ENCODING_BITRATE Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041e92eb71621d1f42d2b800557d204215bbca40f346a2afa4627863fc1a2206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102877"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a>MF \_ PD AUDIO ENCODING \_ \_ \_ BITRATE-Attribut

Gibt die Audiocodierungsbitrate für die Präsentation in Bits pro Sekunde an. Dieses Attribut gilt für Präsentationsdeskriptoren.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Das Attribut ist optional. Einige Formate verfügen über komplexere Codierungsschemas, die nicht mit diesem Attribut zusammengefasst werden können. Für ASF-Dateien (Advanced Systems Format) beschreiben die folgenden Attribute zusammen die Codierungsbitrate:

-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATE**](mf-sd-asf-streambitrates-bitrate-attribute.md)

Formate von Drittanbietern können andere benutzerdefinierte Attribute verwenden.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Darstellungsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




