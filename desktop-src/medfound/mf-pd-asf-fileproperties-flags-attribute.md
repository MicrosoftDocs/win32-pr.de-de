---
description: Gibt an, ob eine ASF-Datei (Advanced Systems Format) übertragen oder durchsuchbar ist. Dieser Wert entspricht dem Feld Flags des Dateieigenschaften Objekts, das in der ASF-Spezifikation definiert ist.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: MF_PD_ASF_FILEPROPERTIES_FLAGS-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348740"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a>MF-Attribut für das "MF- \_ \_ \_ \_ Attribut"

Gibt an, ob eine ASF-Datei (Advanced Systems Format) übertragen oder durchsuchbar ist. Dieser Wert entspricht dem Feld Flags des Dateieigenschaften Objekts, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt. Der Wert des-Attributs ist ein bitweises OR der folgenden Flags:



| Flag | Beschreibung                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x01 | Broadcast-Flag. Die Datei wird gerade erstellt.                                                                                                                                                                                                                                      |
| 0x02 | Suchbares Flag. Die Datei ist suchbar.<br/> Eine Datei kann durchsuchbar sein, wenn ein Audiodatenstrom vorhanden ist und die maximale Datenpaket Größe der minimalen Datenpaket Größe entspricht. Sie kann auch durchsuchbar sein, wenn die Datei einen Audiostream und einen Videostream mit einem entsprechenden einfachen Index Objekt aufweist.<br/> |



 

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode generiert dieses Attribut aus den ASF-Metadaten.

Wenn das Broadcast-Flag festgelegt ist, sind die folgenden Attribute im Präsentations Deskriptor ungültig:

-   [**Datei-ID für MF \_ PD \_ ASF \_ File Properties \_ \_**](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [**Zeitpunkt der Erstellung der MF \_ PD- \_ \_ Dateieigenschaften \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [**MF-,-Paket- \_ \_ \_ Dateieigenschaften \_ Pakete**](mf-pd-asf-fileproperties-packets-attribute.md)
-   [**\_Dauer der \_ \_ \_ Wiedergabe \_ Dauer von MF PD ASF File Properties**](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [**\_Dauer der \_ \_ \_ Sende \_ Dauer von MF PD ASF File Properties**](mf-pd-asf-fileproperties-send-duration-attribute.md)

Außerdem werden die Attributwerte für die [**\_ \_ \_ \_ Maximale \_ \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) Paketgröße für das MF-Attribut und das Attribut "MF [**\_ PD \_ ASF \_ File Properties \_ Min \_ Packet \_ size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) " auf die tatsächliche Paketgröße festgelegt.

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

 

 




