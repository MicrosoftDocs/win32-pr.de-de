---
description: Der \_ Enumerationstyp des WPD-Erfassungs \_ Modus beschreibt den Erfassungs Zeit Steuerungs Modus einer immer noch Abbild Erfassung.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: WPD_CAPTURE_MODES-Enumeration (portabledevice. h)
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
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356406"
---
# <a name="wpd_capture_modes-enumeration"></a>WPD- \_ Erfassungs \_ Modi-Enumeration

Der Enumerationstyp des **WPD- \_ Erfassungs \_** Modus beschreibt den Erfassungs Zeit Steuerungs Modus einer immer noch Abbild Erfassung.

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

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD- \_ Erfassungs \_ Modus nicht \_ definiert**
</dt> <dd>

Der Erfassungs Modus wurde nicht definiert.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD- \_ Erfassungs \_ Modus \_ Normal**
</dt> <dd>

Es sollte keine Verzögerung oder kein Burst Modus verwendet werden.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**Burst für WPD- \_ Erfassungs \_ Modus \_**
</dt> <dd>

Gibt an, dass eine definierte Anzahl von Bildern mit einem definierten Intervall zwischen Ihnen aufgezeichnet werden soll. Die Anzahl der zu erfassenden Abbilder und die Zeitverzögerung zwischen Ihnen werden von der [WPD- \_ Image- \_ \_ Burst \_ Nummer](still-image-properties.md) und der WPD-Eigenschaft für das [ \_ \_ \_ Burst \_ Intervall](still-image-properties.md) für Images angegeben.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD- \_ Erfassungs \_ Modus ( \_ Timelapse)**
</dt> <dd>

Die Abbild Erfassung sollte Zeitverlaufs Fotos verwenden. Die Anzahl der Abbilder und des Intervalls zwischen Ihnen wird von der [WPD- \_ Anzahl der nach wie vor \_ Abbild- \_ \_ Timelapse](still-image-properties.md) und von WPD-Eigenschaften für das Zeit [ \_ \_ \_ \_ Intervall Image](still-image-properties.md) beschrieben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der WPD-Eigenschaft für die [ \_ \_ Image \_ Erfassungs \_ Modus](still-image-properties.md) -Eigenschaft verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




