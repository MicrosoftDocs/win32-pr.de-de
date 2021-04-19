---
description: Enthält den Wert eines Hardware Codecs.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: MFT_CODEC_MERIT_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353175"
---
# <a name="mft_codec_merit_attribute-attribute"></a>Attribut Attribut Attribut für MFT- \_ Codec \_ \_

Enthält den Wert eines Hardware Codecs.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird für das Aktivierungs Objekt für eine Media Foundation Transformation (MFT) festgelegt, die einen Hardwarecodec darstellt. Der Wert des-Attributs ist der Verdienst Wert des Codecs.

Dieses Attribut steuert die Reihenfolge, in der die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion Codecs auflistet, wenn das Flag **\_ \_ \_ sortandfilter für das MFT-Enum-Flag** festgelegt ist. MFTs mit einem Wert Wert werden in der Liste höher als andere MFTs angezeigt.

Dieses Attribut enthält keinen vertrauenswürdigen Wert. Um den tatsächlichen Wert des Codecs zu überprüfen, müssen Sie die [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) -Funktion aufrufen.

Wenn der Wert des Attributs für den MFT- \_ Codec- \_ Attribut Wert \_ nicht mit dem von [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)abgerufenen Verdienst Wert identisch ist, schlägt die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode fehl und gibt den von **MF \_ E \_ ungültigen \_ Codec- \_ Verdienst** zurück.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




