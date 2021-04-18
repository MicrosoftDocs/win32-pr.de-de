---
description: Der \_ Enumerationstyp der WPD-SMS- \_ Codierungs \_ Typen beschreibt den Codierungstyp einer SMS (Short Message Service)-Nachricht.
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: WPD_SMS_ENCODING_TYPES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371487"
---
# <a name="wpd_sms_encoding_types-enumeration"></a>WPD- \_ SMS- \_ \_ Codierungstypen Enumeration

Der Enumerationstyp der **WPD- \_ SMS- \_ Codierungs \_ Typen** beschreibt den Codierungstyp einer SMS (Short Message Service)-Nachricht.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS- \_ Codierung ( \_ 7 \_ Bit)**
</dt> <dd>

7-Bit-Codierung.

</dd> <dt>

<span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS- \_ Codierung ( \_ 8 \_ Bit)**
</dt> <dd>

8-Bit-Codierung.

</dd> <dt>

<span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS- \_ Codierung \_ UTF \_ 16**
</dt> <dd>

16-Bit-Codierung (UTF).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird von der [WPD- \_ SMS- \_ Codierungs](sms-properties.md) Eigenschaft verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




