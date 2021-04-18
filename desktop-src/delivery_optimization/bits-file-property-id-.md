---
title: BITS_FILE_PROPERTY_ID-Enumeration (deliveryoptimization. h)
description: Die BITS_FILE_PROPERTY_ID-Enumeration gibt Werte an, die ID-Werte definieren, die den backgroundcopyfile-Eigenschaften entsprechen.
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- BITS_FILE_PROPERTY_ID-Enumeration
- BITS_FILE_PROPERTY_ID-Enumeration
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b6c6b8a4de359e8313e3127080f2cc17ae6478c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340324"
---
# <a name="bits_file_property_id-enumeration"></a>BITS_FILE_PROPERTY_ID-Enumeration

Die **BITS_FILE_PROPERTY_ID** -Enumeration gibt Werte an, die ID-Werte definieren, die den **backgroundcopyfile** -Eigenschaften entsprechen.

## <a name="syntax"></a>Syntax


```C++
typedef enum _BITS_FILE_PROPERTY_ID { 
  BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS  = 1
} BITS_FILE_PROPERTY_ID;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**
</dt> <dd>

Der vollständige Satz von HTTP-Antwort Headern aus dem letzten http-Antwortpaket des Servers.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





