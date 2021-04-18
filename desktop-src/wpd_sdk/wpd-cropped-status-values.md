---
description: Der Enumerationstyp der WPD-zugeschnittenen \_ \_ Status \_ Werte beschreibt den Zustellungs Status eines Bilds.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: WPD_CROPPED_STATUS_VALUES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361278"
---
# <a name="wpd_cropped_status_values-enumeration"></a>WPD-zugeschnittenen \_ \_ Status \_ Values-Enumeration

Der Enumerationstyp der WPD-zugeschnittenen **\_ \_ Status \_ Werte** beschreibt den Zustellungs Status eines Bilds.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**der WPD-zugeschnittenen \_ \_ Status wurde \_ nicht \_ beschnitten.**
</dt> <dd>

Das Bild wurde nicht abgeschnitten.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**ausgeschnittener WPD- \_ \_ Status \_**
</dt> <dd>

Das Bild wurde abgeschnitten.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**der WPD-zugeschnittenen \_ \_ Status \_ sollte \_ nicht zugeschnitten \_ werden \_ .**
</dt> <dd>

Das Bild wurde nicht, und sollte nicht, zugeschnitten werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Gibt den zugeschnittenen Status eines Bilds an. Diese Enumeration wird von der Eigenschaft " [Status des WPD- \_ Bilds \_ \_ ](image-properties.md) " verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




