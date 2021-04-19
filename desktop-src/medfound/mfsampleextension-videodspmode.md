---
description: Gibt an, ob die Videostabilisierung auf einen Videoframe angewendet wurde.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: MFSampleExtension_VideoDSPMode-Attribut (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350581"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>MF Sample Extension \_ videodspmode-Attribut

Gibt an, ob die Videostabilisierung auf einen Videoframe angewendet wurde.

## <a name="data-type"></a>Datentyp

**MF videodspmode** gespeichert als **UInt32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Das [**Videostabilisierung-MFT**](video-stabilization-mft.md) legt dieses Attribut auf die Ausgabe Beispiele fest, die es erzeugt. Der Wert des-Attributs ist ein [**MF videodspmode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) -Enumerationswert. Wenn der Wert **mfvideodspmode- \_ Stabilisierung** ist, bedeutet dies, dass die MFT die Bildstabilisierung auf den Frame angewendet hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> <dt>

[Medien Beispiele](media-samples.md)
</dt> <dt>

[**Videostabilisierung-MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




