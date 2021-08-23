---
title: ADSI Simple Data Types (Iads.h)
description: Active Directory Service Interfaces (ADSI) definiert und verwendet die folgenden einfachen Datentypen.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422fc0e20195e576f3ade8b39948992d61a376b58fd22f399ca1009db79cbdb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023698"
---
# <a name="adsi-simple-data-types"></a>EINFACHE ADSI-Datentypen

Active Directory Service Interfaces (ADSI) definiert und verwendet die folgenden einfachen Datentypen.


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

**ADS \_ BOOLEAN**
</dt> <dd>

DWORD

</dd> <dt>

**ADS \_ CASE \_ EXACT \_ STRING**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ CASE \_ IGNORE \_ STRING**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ DN \_ STRING**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ INTEGER**
</dt> <dd>

DWORD

</dd> <dt>

**ADS \_ LARGE \_ INTEGER**
</dt> <dd>

[**GROßE \_ GANZE ZAHL**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**ADS \_ NUMERIC \_ STRING**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_ \_ ADS-OBJEKTKLASSE**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ PRINTABLE \_ STRING**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ SEARCH \_ HANDLE**
</dt> <dd>

HANDLE

</dd> <dt>

**ADS \_ UTC \_ TIME**
</dt> <dd>

[**Systemtime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn ADSI ein Attribut liest, das im LDAP-Schema als **INTEGER** definiert wurde, verarbeitet es die ganze Zahl immer als 32-Bit-Wert und kann die Daten abschneiden. Dies ist nur ein Problem für LDAP-Server, die ganzzahlige Werte beliebiger Größe zulassen. Wenn das Attribut ein benutzerdefiniertes Attribut ist, das durch Erweitern des Schemas definiert wird, kann dieses Problem vermieden werden, indem das benutzerdefinierte Attribut als Zeichenfolge definiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                    |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl> |



 

