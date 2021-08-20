---
description: Gibt den Schlüsselbezeichner für eine verschlüsselte ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Feld Schlüssel-ID des Content Encryption-Headers, das in der ASF-Spezifikation definiert ist.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: MF_PD_ASF_CONTENTENCRYPTION_KEYID -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edae0f324e7ab4889b21ae69714da16bfa88803db1d3aef808e4ba715522f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876433"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a>MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID-Attribut

Gibt den Schlüsselbezeichner für eine verschlüsselte ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Feld Schlüssel-ID des Content Encryption-Headers, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Präsentationsdeskriptoren für ASF-Inhalte.

Die [**IMFASFContentInfo::GeneratePresentationDescriptor-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) ruft das Feld Schlüssel-ID ab, konvertiert es in eine Breitzeichenzeichenfolge und füllt dann ein auf NULL terminiertes Array von **WCHAR-Werten** auf. Die Größe des Arrays entspricht dem Feld Schlüssel-ID-Länge des Content Encryption-Headers.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**ZEICHENFOLGEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**BESCHRIFTungDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentationsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

[Präsentationsdeskriptoren](presentation-descriptors.md)
</dt> </dl>

 

 




