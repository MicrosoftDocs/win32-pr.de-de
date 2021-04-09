---
description: Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Avdecaudiodualmono-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 107adb00eb68cbb9ec19331b0c0f3f9db916a306
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860421"
---
# <a name="avdecaudiodualmono-property"></a>Avdecaudiodualmono (Eigenschaft)

Gibt an, ob die zwei-Kanal-Audiodaten als Stereo oder Dual Mono codiert werden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecaudiodualmono**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eavdecaudiodualmono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) -Enumeration.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nur angewendet, wenn der Eingabe-Bit-Stream des Decoders zwei Kanal-Audiodaten enthält. Ein Audiodatenstrom mit zwei Kanälen kann als Stereo oder als dualer Mono codiert werden. Wenn das Audio Dual Mono ist, können Sie die [**avdecaudiodualmonorepromode**](avdecaudiodualmonorepromode-property.md) -Eigenschaft festlegen, um zu konfigurieren, wie der Decoder die Audiodatei wiederherstellt.

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

 

 




