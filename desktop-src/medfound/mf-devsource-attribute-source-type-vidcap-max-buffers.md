---
description: Gibt die maximale Anzahl von Frames an, die von der Video Erfassungs Quelle gepuffert werden.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346986"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a>MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ Maximales \_ Puffer Attribut

Gibt die maximale Anzahl von Frames an, die von der Video Erfassungs Quelle gepuffert werden.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Standardmäßig puffert die Video Erfassungs Quelle maximal einen Frame gleichzeitig. Sie können das Puffer Limit erhöhen, indem Sie dieses Attribut festlegen.

Die richtige Methode zum Festlegen dieses Attributs hängt von der Funktion ab, die zum Erstellen der Medienquelle verwendet wird:

-   [**MF | atedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Legen Sie das Attribut über den *pattributes* -Parameter der Funktion fest.
-   [**MF | atedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Legen Sie das Attribut über den *pattributes* -Parameter der Funktion fest.
-   [**Mfenumdebug**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Legen Sie das-Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, der von der-Funktion zurückgegeben wird. Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.

Das-Attribut gilt nur für Video Erfassungsgeräte.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Geräte Attribute erfassen](capture-device-attributes.md)
</dt> </dl>

 

 




