---
description: Typspezifische Daten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: MF_MT_ARBITRARY_HEADER-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041955"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>Beliebiges "MF MT"- \_ \_ \_ Attribut

Typspezifische Daten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).

## <a name="data-type"></a>Datentyp

**[**MT \_ Beliebiger \_ Header**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** , gespeichert als **Byte \[ \]**

## <a name="getset"></a>Abrufen/Festlegen

Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.

## <a name="remarks"></a>Bemerkungen

ASF-Dateien können Streams mit Binärdaten enthalten. Das MF \_ MT \_ - \_ Attribut beliebiges Header im Medientyp enthält [**eine \_ beliebige MT- \_ Header**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) Struktur, die den Datenstrom beschreibt.

Zusätzlich zum "MF MT"- \_ \_ Attribut beliebiger \_ Header enthält der Medientyp für einen binären ASF-Stream die folgenden Attribute:



| Attribut                                                 | BESCHREIBUNG                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md) | Der Wert des-Attributs ist **MF MediaType \_ Binary**. |
| [\_ \_ beliebiges \_ Format der MF-MT](mf-mt-arbitrary-format.md)   | Enthält zusätzliche Formatierungsdaten.                       |



 

> [!Note]  
> Im Windows Media-Format-SDK werden binäre Streams als *beliebige Streams* oder *beliebige Datenströme* bezeichnet.

 

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




