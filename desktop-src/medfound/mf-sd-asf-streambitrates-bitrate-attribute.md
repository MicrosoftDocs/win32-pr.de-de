---
description: Gibt die durchschnittliche Bitrate eines Streams in einer ASF-Datei (Advanced Systems Format) in Bits pro Sekunde an. Dieses Attribut entspricht dem In der ASF-Spezifikation definierten Eigenschaftenobjekt der StreamBitrate.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: MF_SD_ASF_STREAMBITRATES_BITRATE-Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4190ed64a1d241e17a4fad1481977a27dd62ba0f293f686b55a45f417e89d3d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605170"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a>MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATE-Attribut

Gibt die durchschnittliche Bitrate eines Streams in einer ASF-Datei (Advanced Systems Format) in Bits pro Sekunde an. Dieses Attribut entspricht dem In der ASF-Spezifikation definierten Eigenschaftenobjekt der StreamBitrate.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut und legt es im Streamdeskriptor fest. Die Anwendung kann den Streamdeskriptor für den Stream aus dem Präsentationsdeskriptor erstellen, indem [**SIE DENKPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)aufrufen.

Der Attributwert entspricht dem Feld Average Bit Rate im Stream Bit Rate Properties -Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ÜBERSCHREIBENStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> </dl>

 

 




