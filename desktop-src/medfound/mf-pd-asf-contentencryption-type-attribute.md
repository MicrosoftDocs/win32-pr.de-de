---
description: Gibt den Typ des Schutzmechanismus an, der in einer ASF-Datei (Advanced Systems Format) verwendet wird.
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: MF_PD_ASF_CONTENTENCRYPTION_TYPE-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862500"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a>MF \_ - \_ \_ \_ Attribut vom Typ "MF-Attribut"

Gibt den Typ des Schutzmechanismus an, der in einer ASF-Datei (Advanced Systems Format) verwendet wird.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode ruft das Schutztyp Feld ab, konvertiert es in eine Zeichenfolge mit breit Zeichen und füllt dann ein mit Null endendes Array von **WCHAR** s auf. Falls vorhanden, muss der Wert "DRM" lauten. Die Größe des Arrays ist mit dem Feldlängen Feld der Schutzart des Inhalts Verschlüsselungs Headers Gleichheits.

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

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> <dt>

[Präsentations Deskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




