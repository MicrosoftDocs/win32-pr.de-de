---
description: Gibt die Sprache an, die von einem Datenstrom in einer ASF-Datei (Advanced Systems Format) verwendet wird.
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349317"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a>\_Benutzer- \_ ID- \_ \_ \_ \_ Index Attribut der MF SD-Datei

Gibt die Sprache an, die von einem Datenstrom in einer ASF-Datei (Advanced Systems Format) verwendet wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für streamdeskriptoren für den ASF-Inhalt. Der Wert ist ein Index in der Sprachliste, die im [**MF PD-Attribut " \_ \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) " enthalten ist.

Dieses Attribut entspricht dem Feld "Stream Language ID Index" im erweiterten Stream Properties-Objekt. Weitere Informationen finden Sie in der ASF-Spezifikation.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten. Die Anwendung kann den Datenstrom Deskriptor für den Stream aus dem Präsentations Deskriptor erstellen, indem Sie [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)aufrufen.

Sie können das Sprachtag auch abrufen, indem Sie den Datenstrom Deskriptor für das [**MF \_ SD- \_ sprach**](mf-sd-language-attribute.md) Attribut Abfragen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF-Deskriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> </dl>

 

 




