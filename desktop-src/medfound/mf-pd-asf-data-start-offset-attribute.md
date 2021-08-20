---
description: Gibt den Offset in Bytes vom Anfang einer ASF-Datei (Advanced Systems Format) bis zum Anfang des ersten Datenpakets an.
ms.assetid: 5145d952-19d9-4bf8-9046-0b5d28f5e641
title: MF_PD_ASF_DATA_START_OFFSET -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b848d83d32be7abc8c30cd41bf51959c25e4e784c1f5beab645a6ee5b0db381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741090"
---
# <a name="mf_pd_asf_data_start_offset-attribute"></a>MF \_ PD \_ ASF DATA START \_ \_ \_ OFFSET-Attribut

Gibt den Offset in Bytes vom Anfang einer ASF-Datei (Advanced Systems Format) bis zum Anfang des ersten Datenpakets an.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalte.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut aus den ASF-Metadaten.

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

[**ATTRIBUTEs::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEs::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**BESCHRIFTungDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentationsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> </dl>

 

 




