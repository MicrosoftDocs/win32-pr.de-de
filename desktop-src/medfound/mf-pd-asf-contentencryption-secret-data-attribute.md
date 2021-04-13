---
description: Enthält geheime Daten für eine verschlüsselte ASF-Datei (Advanced Systems Format). Dieses Attribut entspricht dem Geheimnis Daten Feld des Content Encryption Headers, das in der ASF-Spezifikation definiert ist.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526000"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a>MF \_ PD \_ - \_ Attribut für \_ Geheimnis Daten (Secret contentencryption \_ )

Enthält geheime Daten für eine verschlüsselte ASF-Datei (Advanced Systems Format). Dieses Attribut entspricht dem Geheimnis Daten Feld des Content Encryption Headers, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode füllt ein Bytearray mit dem geheimen Datenfeld auf. Die Größe des Arrays ist mit dem Feld für die geheime Daten Länge des Content Encryption-Headers Gleichheits.

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

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> <dt>

[Präsentations Deskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




