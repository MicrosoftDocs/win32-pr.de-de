---
description: Typspezifische Daten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: MF_MT_ARBITRARY_HEADER -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d824aad4f76947786f991807d2f7b301703e3e356d2d1cfb416aa634d49f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826520"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>MF \_ MT \_ ARBITRARY \_ HEADER-Attribut

Typspezifische Daten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).

## <a name="data-type"></a>Datentyp

**[**MT \_ ARBITRARY \_ HEADER als**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** **BYTE gespeichert \[ \]**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="remarks"></a>Hinweise

ASF-Dateien können Streams mit Binärdaten enthalten. Das MF \_ MT \_ ARBITRARY \_ HEADER-Attribut im Medientyp enthält eine [**MT \_ ARBITRARY \_ HEADER-Struktur,**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) die den Stream beschreibt.

Zusätzlich zum MF MT ARBITRARY HEADER-Attribut enthält der Medientyp für einen \_ \_ \_ ASF-Binärdatenstrom die folgenden Attribute:



| attribute                                                 | Beschreibung                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md) | Der Wert des Attributs ist **MFMediaType \_ Binary**. |
| [MF \_ MT \_ ARBITRARY \_ FORMAT](mf-mt-arbitrary-format.md)   | Enthält zusätzliche Formatdaten.                       |



 

> [!Note]  
> Im Windows Media Format SDK werden binäre Streams als *beliebige Streams* oder *beliebige Datenströme bezeichnet.*

 

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




