---
description: Enthält das Beispielbeschreibungsfeld für eine MP4- oder 3GP-Datei.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: MF_MT_MPEG4_SAMPLE_DESCRIPTION-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c59827fa5d2ba6c6621c7e251cf319478fd621d24639e105dcd44863495b364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741796"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>MF \_ MT \_ MPEG4 SAMPLE \_ \_ DESCRIPTION-Attribut

Enthält das Beispielbeschreibungsfeld für eine MP4- oder 3GP-Datei.

## <a name="data-type"></a>Datentyp

**Byte\[\]**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="applies-to"></a>Gilt für:

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Hinweise

Im Beispielbeschreibungsfeld wird die Codierung beschrieben, die für einen Stream in der Datei verwendet wird.

Die MPEG-4-Dateiquelle legt dieses Attribut für den Medientyp für jeden Stream fest. Der Wert des Attributs sind die Rohdaten im Feld mit der Beispielbeschreibung. Wenn die MPEG-4-Dateiquelle die Beispielbeschreibung analysieren kann, werden dem Medientyp auch die Formatdetails hinzugefügt. Andernfalls muss die Anwendung oder der Decoder die Beispielbeschreibung aus dem MF \_ MT \_ MPEG4 \_ SAMPLE \_ DESCRIPTION-Attribut analysieren.

Beim Festlegen dieses Attributs für die MPEG-4-Senke mithilfe der [**METHODE "MPEGMediaTypeHandler::SetCurrentMediaType"**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) sollten sich die Daten für das Attribut MF \_ MT \_ MPEG4 SAMPLE DESCRIPTION nicht \_ \_ ändern, nachdem ein oder mehrere Beispiele an die Senke der [**ENTSPRECHENDEN SCHNITTSTELLE VON STREAMSTREAMSink::P rocessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) gesendet wurden.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




