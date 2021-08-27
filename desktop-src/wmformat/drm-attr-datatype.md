---
title: DRM_ATTR_DATATYPE-Enumeration (Wmdrmsdk.h)
description: Die DRM \_ ATTR \_ DATATYPE-Enumeration definiert die Datentypen, die für DRM-Attribute und -Eigenschaften verwendet werden.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- DRM_ATTR_DATATYPE Enumerationsfenster Media Format
- Enumerationsfenster Medienformat
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
ms.openlocfilehash: 09f55c3d218aa86c33f699d4cb762e752a0bf4e1029e8ca42eee797aaf8ac721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110530"
---
# <a name="drm_attr_datatype-enumeration"></a>DRM \_ ATTR \_ DATATYPE-Enumeration

Die **DRM \_ ATTR \_ DATATYPE-Enumeration** definiert die Datentypen, die für DRM-Attribute und -Eigenschaften verwendet werden.

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

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**\_DRM-TYP \_ DWORD**
</dt> <dd>

Die -Eigenschaft ist ein **4-Byte-DWORD-Wert.**

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**\_ \_ DRM-TYPZEICHENFOLGE**
</dt> <dd>

Die -Eigenschaft ist eine auf NULL endende Unicode-Zeichenfolge.

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**\_DRM-TYP \_ BINARY**
</dt> <dd>

Die -Eigenschaft ist ein Bytearray.

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**\_DRM-TYP \_ BOOL**
</dt> <dd>

Die -Eigenschaft ist ein boolescher Wert mit 4 Byte.

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**\_DRM-TYP \_ QWORD**
</dt> <dd>

Die -Eigenschaft ist ein **8-Byte-QWORD-Wert.**

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**\_DRM-TYP \_ WORD**
</dt> <dd>

Die -Eigenschaft ist ein **2-Byte-WORD-Wert.**

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_ \_ DRM-TYP-GUID**
</dt> <dd>

Die -Eigenschaft ist ein 128-Bit-GUID-Wert (6 Byte).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





