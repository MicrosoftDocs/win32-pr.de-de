---
title: BITS_FILE_PROPERTY_VALUE-Struktur (deliveryoptimization. h)
description: Die BITS_FILE_PROPERTY_VALUE Union stellt den Eigenschafts Wert der do-Datei auf Grundlage eines Werts aus der BITS_FILE_PROPERTY_ID Enumeration bereit.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- BITS_FILE_PROPERTY_VALUE Struktur
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337493"
---
# <a name="bits_file_property_value-structure"></a>BITS_FILE_PROPERTY_VALUE Struktur

Die **BITS_FILE_PROPERTY_VALUE** Union stellt den Eigenschafts Wert der do-Datei auf Grundlage eines Werts aus der [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) Enumeration bereit.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a>Member

<dl> <dt>

**String**
</dt> <dd>

Dieser Wert wird verwendet, wenn der Enumerationswert **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS** der Eigenschaft ID verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





