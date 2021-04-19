---
description: Gibt die Zeit in 100-Nanosekunden-Einheiten an, die zum Senden einer ASF-Datei (Advanced Systems Format) benötigt werden. Eine Sende Zeit für Pakete ist die Zeit, zu der das Paket über das Netzwerk übermittelt werden soll. Es handelt sich nicht um die Präsentationszeit des Pakets.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: MF_PD_ASF_FILEPROPERTIES_SEND_DURATION-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deed3f78208a0f0c7e555e8113f05ac0800cdb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362607"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a>MF \_ PD \_ ASF \_ FileProperties \_ Send \_ Duration-Attribut

Gibt die Zeit in 100-Nanosekunden-Einheiten an, die zum Senden einer ASF-Datei (Advanced Systems Format) benötigt werden. Die *Sendezeit* eines Pakets ist die Zeit, zu der das Paket über das Netzwerk übermittelt werden soll. Es handelt sich nicht um die Präsentationszeit des Pakets.

## <a name="data-type"></a>Datentyp

**UINT64**

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

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> <dt>

[Präsentations Deskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




