---
description: Gibt den Leistungspegel für den Decoder an.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce376a370ea6488c87c0266319de7e9bde0a94edab7137a81f015f416ea9fc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874064"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>MFPKEY \_ AVDecVideoSWPowerLevel-Eigenschaft

Gibt den Leistungspegel für den Decoder an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="default-value"></a>Standardwert

**100**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft muss auf einen der folgenden Werte festgelegt werden.



| Wert | Bedeutung                                                             |
|-------|---------------------------------------------------------------------|
| 0     | Der Decoder verwendet eine Energiestufe, die für die Akkulebensdauer optimiert ist.  |
| 50    | Der Decoder verwendet einen ausgeglichenen Energiepegel.                            |
| 100   | Der Decoder verwendet eine Energiestufe, die für die Videoqualität optimiert ist. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
