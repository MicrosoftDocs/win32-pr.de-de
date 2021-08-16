---
title: BITS_FILE_PROPERTY_VALUE-Struktur (Deliveryoptimization.h)
description: Die BITS_FILE_PROPERTY_VALUE Union stellt den Eigenschaftswert der DO-Datei basierend auf einem Wert aus der BITS_FILE_PROPERTY_ID-Enumeration bereit.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- BITS_FILE_PROPERTY_VALUE-Struktur
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
ms.openlocfilehash: ba01a8c83cef842c40149b3fe8cbc586a7da5f819ffc387befb9f84182cbce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544625"
---
# <a name="bits_file_property_value-structure"></a>BITS_FILE_PROPERTY_VALUE-Struktur

Die **BITS_FILE_PROPERTY_VALUE** Union stellt den Eigenschaftswert der DO-Datei basierend auf einem Wert aus der [**BITS_FILE_PROPERTY_ID-Enumeration**](bits-file-property-id-.md) bereit.

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

Dieser Wert wird verwendet, wenn der Eigenschafts-ID-Enumerationswert **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS** verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5.GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5.SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





