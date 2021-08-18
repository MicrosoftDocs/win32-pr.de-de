---
description: Gibt die durchschnittliche Lautstärke des Audioinhalts an.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: MFPKEY_WMADRC_AVGREF-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7d3575b81ca878c610aed95ca25f73fa94c292ec16f9245a72a3a9515198c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973239"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>MFPKEY \_ WMADRC \_ AVGREF-Eigenschaft

Gibt die durchschnittliche Lautstärke des Audioinhalts an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMADRCAverageReference

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Hinweise

Sie können diesen Wert vom Encoder erhalten, nachdem der Inhalt verarbeitet wurde. Dieser Wert kann auch für den Decoder für die dynamische Bereichssteuerung festgelegt werden, hat jedoch nur dann Auswirkungen, wenn die [ \_ MFPKEY WFPC \_ DRCMODE-Eigenschaft](mfpkey-wmadec-drcmodeproperty.md) festgelegt ist.

Weitere Informationen zur Dynamischen Bereichssteuerung finden Sie im Webartikel [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
