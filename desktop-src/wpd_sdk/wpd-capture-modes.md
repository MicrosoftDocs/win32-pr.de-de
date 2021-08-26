---
description: Der \_ WPD CAPTURE \_ MODES-Enumerationstyp beschreibt den Erfassungszeitmodus einer Standbilderfassung.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: WPD_CAPTURE_MODES-Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c8bc0d667e329db3afccf76497409350d7aa7250b0e6529d0b3f4ddae7a32370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927990"
---
# <a name="wpd_capture_modes-enumeration"></a>WPD \_ CAPTURE \_ MODES-Enumeration

Der **WPD \_ CAPTURE \_ MODES-Enumerationstyp** beschreibt den Erfassungszeitmodus einer Standbilderfassung.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD \_ CAPTURE \_ MODE \_ UNDEFINED**
</dt> <dd>

Der Erfassungsmodus wurde nicht definiert.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD \_ CAPTURE \_ MODE \_ NORMAL**
</dt> <dd>

Es sollte kein Verzögerungs- oder Burstmodus verwendet werden.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD \_ CAPTURE \_ MODE \_ BURST**
</dt> <dd>

Gibt an, dass eine definierte Anzahl von Bildern mit einem definierten Intervall zwischen ihnen erfasst werden soll. Die Anzahl der bilder, die erfasst werden sollen, und die Zeitverzögerung zwischen ihnen werden durch die EIGENSCHAFTEN [WPD \_ STILL IMAGE BURST \_ \_ \_ NUMBER](still-image-properties.md) und [WPD STILL IMAGE BURST \_ \_ \_ \_ INTERVAL](still-image-properties.md) angegeben.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD \_ CAPTURE \_ MODE \_ TIMELAPSE**
</dt> <dd>

Die Bildaufnahme sollte Zeitrafferfotos verwenden. Die Anzahl der Bilder und das Intervall zwischen ihnen werden in den Eigenschaften [WPD \_ STILL IMAGE \_ \_ TIMELAPSE \_ NUMBER](still-image-properties.md) und [WPD STILL IMAGE \_ \_ \_ TIMELAPSE \_ INTERVAL](still-image-properties.md) beschrieben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird von der [WPD \_ STILL IMAGE \_ CAPTURE \_ \_ MODE-Eigenschaft](still-image-properties.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




