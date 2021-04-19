---
description: Erzwingt, dass der erweiterte Videorenderer (EVR) Bob Deinterlacing verwendet.
ms.assetid: 56f808b3-c2eb-46e4-84a1-c478a5db78e7
title: EVRConfig_ForceBob-Attribut (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afeeb1e7fb57f956d378e71ac4452ea2e4f168be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343020"
---
# <a name="evrconfig_forcebob-attribute"></a>Evrconfig \_ forcebob-Attribut

Erzwingt, dass der erweiterte Videorenderer (EVR) Bob Deinterlacing verwendet.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann in der EVR-Medien Senke festgelegt werden. Zum Festlegen des-Attributs verwenden Sie **QueryInterface** , um die EVR-Medien Senke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle abzufragen.

Das Festlegen dieses Attributs hat denselben Effekt wie das Festlegen des **MF videomixprefs \_ forcebob** -Flags für den EVR. Eine Beschreibung dieses Flags finden Sie unter [**MF videomixprefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .

Die GUID-Konstante für dieses Attribut wird aus "straumiids. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>UUIDs. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR-Attribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Video Qualitäts Verwaltung](video-quality-management.md)
</dt> </dl>

 

 




