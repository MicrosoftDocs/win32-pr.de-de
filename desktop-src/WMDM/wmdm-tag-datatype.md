---
title: WMDM_TAG_DATATYPE Enumeration
description: Der WMDM \_ TAG \_ DATATYPE-Enumerationstyp definiert einen Datentyp.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- WMDM_TAG_DATATYPE windows Media Geräte-Manager
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd725e6d8a0e1baef8a6dfc98cb5d3056f5d67b2d7babd07c919692d96248881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862670"
---
# <a name="wmdm_tag_datatype-enumeration"></a>WMDM \_ TAG \_ DATATYPE-Enumeration

Der **WMDM \_ TAG \_ DATATYPE-Enumerationstyp** definiert einen Datentyp.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM \_ TYPE \_ DWORD**
</dt> <dd>

Gibt einen **DWORD-Wert** mit 4 Byte an.

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**\_WMDM-TYPZEICHENFOLGE \_**
</dt> <dd>

Gibt eine mit NULL beendete Unicode-Zeichenfolge an (2 Bytes pro Zeichen).

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**\_WMDM-TYP BINARY \_**
</dt> <dd>

Gibt ein Bytearray an.

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**\_WMDM-TYP \_ BOOL**
</dt> <dd>

Gibt einen booleschen 4-Byte-Wert an.

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM \_ TYPE \_ QWORD**
</dt> <dd>

Gibt einen **QWORD-Wert** mit 8 Byte an.

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**\_WMDM-TYP \_ WORD**
</dt> <dd>

Gibt einen 2-Byte-WORD-Wert an. 

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_ \_ WMDM-TYP-GUID**
</dt> <dd>

Gibt eine 128-Bit-GUID (16 Byte) an.

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM \_ TYPE \_ DATE**
</dt> <dd>

Gibt ein Datum an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





