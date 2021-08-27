---
description: Gibt an, ob ein Algorithmus verwendet werden soll, der videos mit höherer Qualität erzeugt, oder einen schnelleren Algorithmus.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: MFPKEY_RESIZE_QUALITY-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8aeb59935c8fc3462b713967ed2b14a0adfcf731fa1a71fec434b0e07d4309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973409"
---
# <a name="mfpkey_resize_quality-property"></a>MFPKEY \_ RESIZE \_ QUALITY-Eigenschaft

Gibt an, ob ein Algorithmus verwendet werden soll, der videos mit höherer Qualität erzeugt, oder einen schnelleren Algorithmus.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="applies-to"></a>Gilt für

-   [Video Resizer DSP](videoresizer.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie einen der folgenden Werte:



| Wert     | Beschreibung          |
|-----------|----------------------|
| VT \_ FALSE | Schnellerer Algorithmus     |
| VT \_ TRUE  | Video mit höherer Qualität |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
