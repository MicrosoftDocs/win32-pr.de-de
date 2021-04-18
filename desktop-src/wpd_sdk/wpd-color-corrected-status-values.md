---
description: Der \_ \_ Enumerationstyp "korrigierte WPD-Farben" \_ beschreibt den Status der \_ Farbkorrektur eines Bilds oder einer Videodatei.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: WPD_COLOR_CORRECTED_STATUS_VALUES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371231"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a>Mit der WPD- \_ Farbe \_ korrigierte \_ Status \_ Werte Enumeration

Der Enumerationstyp " **korrigierte WPD- \_ Farben \_ \_ \_** " beschreibt den Status der Farbkorrektur eines Bilds oder einer Videodatei.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**Status der \_ korrigierten WPD-Farbe \_ \_ \_ nicht \_ korrigiert**
</dt> <dd>

Das Bild wurde nicht farblich korrigiert.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**korrigierter Status der WPD- \_ Farbe \_ \_ \_ korrigiert**
</dt> <dd>

Das Bild wurde farblich korrigiert.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**der Status der korrigierten WPD- \_ Farbe \_ \_ \_ sollte \_ nicht \_ \_ korrigiert werden.**
</dt> <dd>

Das Bild wurde nicht, und sollte nicht sein, dass die Farbe korrigiert wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Gibt den Status der Farbkorrektur eines Bilds an. Diese Enumeration wird von der Eigenschaft " [Status der WPD- \_ Image \_ Farbe \_ korrigiert \_ ](image-properties.md) " verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




