---
description: Gibt die früheren Merkmale der Medienquelle an.
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: MF_EVENT_SOURCE_CHARACTERISTICS_OLD-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347880"
---
# <a name="mf_event_source_characteristics_old-attribute"></a>Eigenschaften der MF- \_ Ereignis \_ Quelle \_ \_ Altes Attribut

Gibt die früheren Merkmale der Medienquelle an. Bei den Attributdaten handelt es sich um ein bitweises **or** von-Flags aus der [**mfmediasource- \_ Eigenschaften**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) -Enumeration.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird mit dem [mesourcecharakteristicschangi-Ereignis](mesourcecharacteristicschanged.md) verwendet.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




