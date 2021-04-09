---
description: Enthält das Beispiel Beschreibungsfeld für eine MP4-oder 3GP-Datei.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: MF_MT_MPEG4_SAMPLE_DESCRIPTION-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867544"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>"MF \_ MT \_ MPEG4 \_ Sample \_ Description"-Attribut

Enthält das Beispiel Beschreibungsfeld für eine MP4-oder 3GP-Datei.

## <a name="data-type"></a>Datentyp

**Hobby\[\]**

## <a name="getset"></a>Abrufen/Festlegen

Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.

## <a name="applies-to"></a>Gilt für:

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Bemerkungen

Das Feld Beispiel Beschreibung beschreibt die Codierung, die für einen Datenstrom in der Datei verwendet wird.

Die MPEG-4-Datei Quelle legt dieses Attribut für den Medientyp für jeden Stream fest. Der Wert des-Attributs sind die Rohdaten im Feld für die Beispiel Beschreibung. Wenn die MPEG-4-Datei Quelle die Beispiel Beschreibung analysieren kann, werden auch die Format Details dem Medientyp hinzugefügt. Andernfalls muss die Anwendung oder der Decoder die Beispiel Beschreibung aus dem MF \_ MT \_ MPEG4 \_ Sample \_ Description-Attribut analysieren.

Beim Festlegen dieses Attributs für die MPEG-4-Senke über die [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) -Methode sollten sich die Daten für die Beschreibung des Attributs "MF \_ \_ \_ . MPEG4 Sample \_ Description" nicht ändern, nachdem mindestens ein Muster an die Senke in der [**imfstreamsink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) -Schnittstelle des entsprechenden Streams gesendet wurde

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




