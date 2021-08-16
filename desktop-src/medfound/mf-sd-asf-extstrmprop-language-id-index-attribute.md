---
description: Gibt die Sprache an, die von einem Stream in einer ASF-Datei (Advanced Systems Format) verwendet wird.
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f77b53a4156cf21a23680618da010db781e0c7c75d7d4decb2f9e1136c5dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474068"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a>MF \_ SD \_ ASF \_ EXTSTRMPROP \_ LANGUAGE ID \_ \_ INDEX-Attribut

Gibt die Sprache an, die von einem Stream in einer ASF-Datei (Advanced Systems Format) verwendet wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Streamdeskriptoren für ASF-Inhalt. Der Wert ist ein Index in der Sprachliste, die im [**MF \_ PD \_ ASF \_ LANGLIST-Attribut**](mf-pd-asf-langlist-attribute.md) enthalten ist.

Dieses Attribut entspricht dem Feld Stream Language ID Index im Extended Stream Properties-Objekt. Weitere Informationen finden Sie in der ASF-Spezifikation.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut aus den ASF-Metadaten. Die Anwendung kann den Streamdeskriptor für den Stream aus dem Präsentationsdeskriptor erstellen, indem [**SIE DENKPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)aufrufen.

Sie können das Sprachtag auch abrufen, indem Sie den Streamdeskriptor für das [**MF \_ SD \_ LANGUAGE-Attribut**](mf-sd-language-attribute.md) abfragen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ÜBERSCHREIBENStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> </dl>

 

 




