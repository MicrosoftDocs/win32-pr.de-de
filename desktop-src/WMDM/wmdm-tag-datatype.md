---
title: WMDM_TAG_DATATYPE-Enumeration
description: Der \_ \_ DataType-Enumerationstyp des WMDM-Tags definiert einen-Datentyp.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- Device Manager der WMDM_TAG_DATATYPE-Enumeration Windows Media
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
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354037"
---
# <a name="wmdm_tag_datatype-enumeration"></a>\_DataType-Enumeration des WMDM-Tags \_

Der **\_ \_ DataType** -Enumerationstyp des WMDM-Tags definiert einen-Datentyp.

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

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM- \_ Typ \_ DWORD**
</dt> <dd>

Gibt einen 4-Byte- **DWORD** -Wert an.

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM \_ - \_ Typzeichenfolge**
</dt> <dd>

Gibt eine NULL-terminierte Unicode-Zeichenfolge (2 Bytes pro Zeichen) an.

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM \_ - \_ typbinär Datei**
</dt> <dd>

Gibt ein Bytearray an.

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM- \_ Typ \_ bool**
</dt> <dd>

Gibt einen booleschen Wert mit 4 Byte an.

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM- \_ Typ \_ QWORD**
</dt> <dd>

Gibt einen 8-Byte- **QWORD** -Wert an.

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM- \_ Typ \_ Wort**
</dt> <dd>

Gibt einen 2-Byte- **Wort** Wert an.

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM- \_ Typ- \_ GUID**
</dt> <dd>

Gibt eine 128-Bit-GUID (16-Byte-GUID) an.

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**Datum des WMDM- \_ Typs \_**
</dt> <dd>

Gibt ein Datum an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





