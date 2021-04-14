---
description: Gibt die Lizenz Erwerbs-URL für eine verschlüsselte ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Feld "License URL" des Content Encryption Headers, das in der ASF-Spezifikation definiert ist.
ms.assetid: fe431c38-8227-4385-ac6f-72b9982cde62
title: MF_PD_ASF_CONTENTENCRYPTION_LICENSE_URL-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5245ebbc5bfeac8b363898b4913c82b94990fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484819"
---
# <a name="mf_pd_asf_contentencryption_license_url-attribute"></a>Lizenz-URL-Attribut für MF \_ PD- \_ \_ \_ Lizenz \_

Gibt die Lizenz Erwerbs-URL für eine verschlüsselte ASF-Datei (Advanced Systems Format) an. Dieses Attribut entspricht dem Feld "License URL" des Content Encryption Headers, das in der ASF-Spezifikation definiert ist.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Präsentations Deskriptoren für den ASF-Inhalt.

Die [**imfasf ContentInfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) -Methode ruft das Lizenz-URL-Feld ab, konvertiert es in eine Zeichenfolge mit breit Zeichen und füllt dann ein mit Null endendes Array von **WCHAR** s auf. Die Größe des Arrays gleicht dem Feld für die Lizenz-URL-Länge des Content Encryption-Headers.

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

 

 




