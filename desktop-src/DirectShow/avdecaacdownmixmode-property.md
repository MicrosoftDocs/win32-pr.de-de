---
description: Gibt an, ob ein AAC-Decoder standardmäßige MPEG-2/MPEG-4-Stereo Abmischungs Gleichungen verwendet oder eine nicht standardmäßige downmischungs-verwendet.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Avdecaacdownmixmode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340088"
---
# <a name="avdecaacdownmixmode-property"></a>Avdecaacdownmixmode (Eigenschaft)

Gibt an, ob ein AAC-Decoder standardmäßige MPEG-2/MPEG-4-Stereo Abmischungs Gleichungen verwendet oder eine nicht standardmäßige downmischungs-verwendet.

Ein Beispiel für eine nicht standardmäßige Downmix ist die, die durch das ARIB-Dokument Std-B21 Version 4,4 definiert wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecaacdownmixmode**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eavdecaacdownmixmode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) -Enumeration.

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

 

