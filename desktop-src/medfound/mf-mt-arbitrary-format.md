---
description: Zusätzliche Formatdaten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: MF_MT_ARBITRARY_FORMAT -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7629e92eea07059f562d553985628f2099df1da03bd371617f0eed5183dd69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973609"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>MF \_ MT \_ ARBITRARY \_ FORMAT-Attribut

Zusätzliche Formatdaten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).

## <a name="data-type"></a>Datentyp

**Byte\[\]**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="remarks"></a>Hinweise

Anwendungen können binäre Datenströme verwenden, um benutzerdefinierte Datentypen zu halten. Die ASF-Medienquelle behandelt den Wert dieses Attributs als nicht transparentes Blob. Der **formattype-Member** der [**MT \_ ARBITRARY \_ HEADER-Struktur**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) definiert das Layout der Formatdaten.

Diese Struktur entspricht dem Feld Formatdaten der typspezifischen Daten im Stream Properties-Objekt in Dateien, in denen der Streamtyp **ASF \_ Binary Media \_ ist.** Weitere Informationen finden Sie in der ASF-Spezifikation.

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
</dt> <dt>

[MF \_ MT \_ ARBITRARY \_ HEADER](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




