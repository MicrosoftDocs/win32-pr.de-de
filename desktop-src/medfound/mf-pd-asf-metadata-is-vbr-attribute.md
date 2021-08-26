---
description: Gibt an, ob eine ASF-Datei (Advanced Systems Format) eine VBR-Codierung (Variable Bit Rate) verwendet.
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: MF_PD_ASF_METADATA_IS_VBR-Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e97d471c6a6466290c5b2ac490f88ae33de29aa3823af420ef8b8116a81192a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955420"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a>MF \_ PD \_ ASF METADATA IS \_ \_ \_ VBR attribute

Gibt an, ob eine ASF-Datei (Advanced Systems Format) eine VBR-Codierung (Variable Bit Rate) verwendet.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalt. Wenn der Wert **TRUE** ist, wurde die Datei mit VBR codiert. Wenn der Wert **FALSE** ist oder das Attribut nicht vorhanden ist, verwendet die Datei keine VBR-Codierung.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut und legt es für den Präsentationsdeskriptor fest.

> [!Note]  
> Dieses Attribut entspricht dem **IsVBR-Attribut** im Windows Media Format SDK.

 

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

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Darstellungsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

[Präsentationsdeskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




