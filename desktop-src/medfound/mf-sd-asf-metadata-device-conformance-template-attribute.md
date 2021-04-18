---
description: Gibt die Konformitäts Vorlage für Geräte für einen Datenstrom in einer ASF-Datei (Advanced Systems Format) an.
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347404"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a>Vorlagen Attribut für das SD-Datei- \_ \_ ASF- \_ \_ metadatengerät \_ \_

Gibt die Konformitäts Vorlage für Geräte für einen Datenstrom in einer ASF-Datei (Advanced Systems Format) an.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für streamdeskriptoren für den ASF-Inhalt. Weitere Informationen zu den Vorlagen für die Geräte Konformität finden Sie im Thema "Geräte Übereinstimmungs-Vorlagen Parameter" im SDK für den Windows Media-Format.

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

[**Imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMF-Deskriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> </dl>

 

 




