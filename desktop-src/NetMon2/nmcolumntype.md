---
description: Gibt die Member der nmcolumnvariant-Struktur an.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: Nmcolumntype-Enumeration (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3c88d001ce3ccf1ebfe1e28855ae9df9fca5d327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760123"
---
# <a name="nmcolumntype-enumeration"></a>Nmcolumntype-Enumeration

Die **nmcolumntype** -Enumeration gibt die Member der [**nmcolumnvariant**](nmcolumnvariant.md) -Struktur an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**Nmcolumntype \_ Uint8**
</dt> <dd>

8-Bit-Ganzzahl ohne Vorzeichen.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**Nmcolumntype \_ SINT8**
</dt> <dd>

8-Bit-Ganzzahl mit Vorzeichen.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**Nmcolumntype \_ UInt16**
</dt> <dd>

16-Bit-Ganzzahl ohne Vorzeichen.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**Nmcolumntype \_ SINT16**
</dt> <dd>

16-Bit-Ganzzahl mit Vorzeichen.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**Nmcolumntype \_ UInt32**
</dt> <dd>

32-Bit-Ganzzahl ohne Vorzeichen.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**Nmcolumntype \_ SINT32**
</dt> <dd>

Ganze 32-Bit-Zahl mit Vorzeichen:

</dd> <dt>

<span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**Nmcolumntype \_ float64**
</dt> <dd>

64-Bit Float.

</dd> <dt>

<span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**nmcolumntype- \_ Frame**
</dt> <dd>

Frame Nummer.

</dd> <dt>

<span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**nmcolumntype \_ YesNo**
</dt> <dd>

"Yes" oder "No".

</dd> <dt>

<span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**nmcolumntype \_ onoff**
</dt> <dd>

"On" oder "Off"

</dd> <dt>

<span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**nmcolumntype \_ truefalse**
</dt> <dd>

"True" oder "false".

</dd> <dt>

<span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**nmcolumntype \_ MACADDR**
</dt> <dd>

MAC-Adresse

</dd> <dt>

<span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**nmcolumntype \_ ipxaddr**
</dt> <dd>

IPX-Adresse

</dd> <dt>

<span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**nmcolumntype \_ ipaddr**
</dt> <dd>

IP-Adresse.

</dd> <dt>

<span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**nmcolumntype \_ vartime**
</dt> <dd>

Variant-Zeit.

</dd> <dt>

<span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**nmcolumntype- \_ Zeichenfolge**
</dt> <dd>

Zeiger auf eine Zeichenfolge.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




