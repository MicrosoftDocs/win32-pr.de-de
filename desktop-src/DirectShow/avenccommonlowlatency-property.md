---
description: Gibt an, ob der Ausgabestream so strukturiert werden soll, dass der codierte Stream eine geringe Decodierungs Latenz aufweist.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Avenccommonlowlatency-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213987"
---
# <a name="avenccommonlowlatency-property"></a>Avenccommonlowlatency (Eigenschaft)

Gibt an, ob der Ausgabestream so strukturiert werden soll, dass der codierte Stream eine geringe Decodierungs Latenz aufweist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**Variant \_ bool** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonlowlatency**

## <a name="remarks"></a>Bemerkungen

Die Decodierungs Latenz ist definiert als die Menge der Daten, die der Decoder Puffern muss. Wenn Sie diese Eigenschaft beispielsweise auf **Variant \_ true** für einen MPEG-Video Encoder festlegen, werden die Typen von GOP-Strukturen, die der Encoder verwenden kann, eingeschränkt.

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

 

 




