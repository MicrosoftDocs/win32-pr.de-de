---
description: Gibt die Zeit in Einheiten von 100 Nanosekunden an, die zum Senden einer ASF-Datei (Advanced Systems Format) benötigt wird. Eine Sendezeit für Pakete ist die Zeit, zu der das Paket über das Netzwerk übermittelt werden soll. Dies ist nicht die Präsentationszeit des Pakets.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: MF_PD_ASF_FILEPROPERTIES_SEND_DURATION-Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce635cd02766a3c9ca8b0a0d327db93a4bcaaca76bccd6ae54fda726684ec641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740942"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a>MF \_ PD \_ ASF \_ FILEPROPERTIES \_ SEND \_ DURATION-Attribut

Gibt die Zeit in Einheiten von 100 Nanosekunden an, die zum Senden einer ASF-Datei (Advanced Systems Format) benötigt wird. Die *Sendezeit* eines Pakets ist die Zeit, zu der das Paket über das Netzwerk übermittelt werden soll. Dies ist nicht die Präsentationszeit des Pakets.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalt.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) generiert dieses Attribut aus den ASF-Metadaten.

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

[**PRESENTPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Darstellungsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

[Präsentationsdeskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




