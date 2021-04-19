---
description: Gibt den Datei Bezeichner einer ASF-Datei (Advanced Systems Format) an.
ms.assetid: 096c2e1a-7fd7-49ab-aa24-7d7c779d9e79
title: MF_PD_ASF_FILEPROPERTIES_FILE_ID-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92d20351c11df4feebd732c670cbacabf3bd67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356600"
---
# <a name="mf_pd_asf_fileproperties_file_id-attribute"></a>Datei-ID-Attribut für MF \_ PD- \_ \_ \_ Dateieigenschaften \_

Gibt den Datei Bezeichner einer ASF-Datei (Advanced Systems Format) an.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.

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

[**Imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> <dt>

[Präsentations Deskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




