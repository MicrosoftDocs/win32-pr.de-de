---
description: Gibt das Energiespar Niveau eines Video-Decoders an.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Avdecvideoswpowerlevel-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339666"
---
# <a name="avdecvideoswpowerlevel-property"></a>Avdecvideoswpowerlevel-Eigenschaft

Gibt das Energiespar Niveau eines Video-Decoders an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecvideoswpowerlevel**

## <a name="property-value"></a>Eigenschaftswert

Der Bereich möglicher Werte ist \[ 0.. 100 \] , einschließlich der folgenden Bedeutung.



| Wert | BESCHREIBUNG                 |
|-------|-----------------------------|
| 0     | Optimieren Sie die Akku Lebensdauer.  |
| 100   | Optimieren Sie die Videoqualität. |



 

Die [**eavdecvideoswpowerlevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) -Enumeration definiert einige bestimmte Konstanten innerhalb dieses Bereichs.

## <a name="remarks"></a>Bemerkungen

Sie können diese Eigenschaft während der Wiedergabe festlegen, um die Energiespar Stufe zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




