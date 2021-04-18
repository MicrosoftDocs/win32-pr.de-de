---
description: Zusätzliche Formatierungsdaten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: MF_MT_ARBITRARY_FORMAT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348099"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>\_ \_ Beliebiges Format von MF MT \_

Zusätzliche Formatierungsdaten für einen binären Stream in einer ASF-Datei (Advanced Systems Format).

## <a name="data-type"></a>Datentyp

**Hobby\[\]**

## <a name="getset"></a>Abrufen/Festlegen

Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.

## <a name="remarks"></a>Bemerkungen

Anwendungen können binäre Datenströme verwenden, um benutzerdefinierte Datentypen zu speichern. Der Wert dieses Attributs wird von der ASF-Medienquelle als undurchsichtiges BLOB behandelt. Der **Format Type** -Member der [**willkürlichen MT- \_ \_ Header**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) Struktur definiert das Layout der Formatierungsdaten.

Diese Struktur entspricht dem Format Daten Feld der typspezifischen Daten im Stream Properties-Objekt in Dateien, bei denen der Streamtyp ein ASF- **\_ Binär \_ Medium** ist. Weitere Informationen finden Sie in der ASF-Spezifikation.

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
</dt> <dt>

[\_ \_ beliebiger Header von MF MT \_](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




