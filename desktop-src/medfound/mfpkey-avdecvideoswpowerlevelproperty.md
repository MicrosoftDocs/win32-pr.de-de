---
description: Gibt die Leistungs Ebene für den Decoder an.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372868"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>Mfpkey \_ avdecvideoswpowerlevel-Eigenschaft

Gibt die Leistungs Ebene für den Decoder an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="default-value"></a>Standardwert

**100**

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft muss auf einen der folgenden Werte festgelegt werden.



| Wert | Bedeutung                                                             |
|-------|---------------------------------------------------------------------|
| 0     | Der Decoder verwendet einen Energiepegel, der für die Akku Lebensdauer optimiert ist.  |
| 50    | Der Decoder verwendet einen ausgeglichenen Energie Stand.                            |
| 100   | Der Decoder verwendet einen Energiepegel, der für die Videoqualität optimiert ist. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
