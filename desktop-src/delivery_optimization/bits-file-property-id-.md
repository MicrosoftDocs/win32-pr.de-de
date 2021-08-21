---
title: BITS_FILE_PROPERTY_ID -Enumeration (Deliveryoptimization.h)
description: Die BITS_FILE_PROPERTY_ID-Enumeration gibt Werte an, die ID-Werte definieren, die backgroundCopyFile-Eigenschaften entspricht.
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- BITS_FILE_PROPERTY_ID Enumeration
- BITS_FILE_PROPERTY_ID Enumeration
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
ms.openlocfilehash: 5eb8593e018a5c38c6788dfffefe827ed2e086774aedca1d051680b9cb6a433a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810774"
---
# <a name="bits_file_property_id-enumeration"></a>BITS_FILE_PROPERTY_ID Enumeration

Die **BITS_FILE_PROPERTY_ID-Enumeration** gibt Werte an, die ID-Werte definieren, die **backgroundCopyFile-Eigenschaften** entspricht.

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

Der vollständige Satz von HTTP-Antwortheadern aus dem letzten HTTP-Antwortpaket des Servers.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



 

 





