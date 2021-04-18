---
title: DRM_ATTR_DATATYPE-Enumeration (wmdrmsdk. h)
description: Die DRM \_ attr \_ DataType-Enumeration definiert die Datentypen, die für DRM-Attribute und-Eigenschaften verwendet werden.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- DRM_ATTR_DATATYPE-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e684ba1c09a86c65a13adbd189bb185f65598b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371738"
---
# <a name="drm_attr_datatype-enumeration"></a>DRM- \_ attr- \_ DataType-Enumeration

Die **DRM \_ attr \_ DataType** -Enumeration definiert die Datentypen, die für DRM-Attribute und-Eigenschaften verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM- \_ Typ \_ DWORD**
</dt> <dd>

Die-Eigenschaft ist ein 4-Byte- **DWORD** -Wert.

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM \_ - \_ Zeichenfolge**
</dt> <dd>

Die-Eigenschaft ist eine NULL-terminierte Unicode-Zeichenfolge.

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM \_ - \_ typbinär Datei**
</dt> <dd>

Die-Eigenschaft ist ein Bytearray.

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM- \_ Typ \_ bool**
</dt> <dd>

Die-Eigenschaft ist ein boolescher Wert mit 4 Bytes.

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM- \_ Typ \_ QWORD**
</dt> <dd>

Die-Eigenschaft ist ein 8-Byte- **QWORD** -Wert.

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM \_ - \_ typwort**
</dt> <dd>

Die-Eigenschaft ist ein 2-Byte- **Wort** Wert.

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM- \_ Typ- \_ GUID**
</dt> <dd>

Die-Eigenschaft ist ein 128-Bit-GUID-Wert (6-Byte).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





