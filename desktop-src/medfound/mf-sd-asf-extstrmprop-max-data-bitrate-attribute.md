---
description: Gibt die maximale Datenbitrate eines Streams in einer ASF-Datei (Advanced Systems Format) in Bits pro Sekunde an.
ms.assetid: d20d374a-a259-4e89-8eeb-942bbe53e959
title: MF_SD_ASF_EXTSTRMPROP_MAX_DATA_BITRATE -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9bb445724c15604ab30e353315769f78a71c0d6dd94291392e4c34ee05a70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714360"
---
# <a name="mf_sd_asf_extstrmprop_max_data_bitrate-attribute"></a>MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX DATA \_ \_ BITRATE-Attribut

Gibt die maximale Datenbitrate eines Streams in einer ASF-Datei (Advanced Systems Format) in Bits pro Sekunde an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Streamdeskriptoren für ASF-Inhalte. Sie entspricht dem Feld Alternate Data Bit Rate (Alternative Datenbitrate) im Objekt Extended Stream Properties (Erweiterte Streameigenschaften). Weitere Informationen finden Sie in der ASF-Spezifikation.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut aus den ASF-Metadaten. Die Anwendung kann den Streamdeskriptor für den Stream aus dem Präsentationsdeskriptor erstellen, indem [**SIE DENTPRESENTATIONDescriptor::GetStreamDescriptorByIndex aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**JAVASCRIPTStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> </dl>

 

 




