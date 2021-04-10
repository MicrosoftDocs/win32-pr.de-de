---
title: Einfache ADSI-Datentypen (IADs. h)
description: Mit Active Directory Service Interfaces (ADSI) werden die folgenden einfachen Datentypen definiert und verwendet.
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
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040246"
---
# <a name="adsi-simple-data-types"></a>Einfache ADSI-Datentypen

Mit Active Directory Service Interfaces (ADSI) werden die folgenden einfachen Datentypen definiert und verwendet.


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

**ADS \_ boolescher Wert**
</dt> <dd>

DWORD

</dd> <dt>

**\_ \_ akdie exakte \_ Zeichenfolge**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ - \_ \_ Zeichenfolge ignorieren**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ DN- \_ Zeichenfolge**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS- \_ Ganzzahl**
</dt> <dd>

DWORD

</dd> <dt>

**Werbung für \_ große \_ ganze Zahlen**
</dt> <dd>

[**große \_ ganze Zahl**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**\_numerische \_ Zeichenfolge ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS- \_ Objekt \_ Klasse**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_Druck druckbare \_ Zeichenfolge**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS- \_ Such \_ handle**
</dt> <dd>

HANDLE

</dd> <dt>

**Anzeigen der \_ UTC- \_ Zeit**
</dt> <dd>

[**System Time**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn ADSI ein Attribut liest, das im LDAP-Schema als **Integer** definiert wurde, wird die ganze Zahl immer als 32-Bit-Wert behandelt, und die Daten können abgeschnitten werden. Dies ist nur bei LDAP-Servern von Bedeutung, die ganzzahlige Werte beliebig groß sind. Wenn das Attribut ein durch die Erweiterung des Schemas definiertes benutzerdefiniertes Attribut ist, kann dieses Problem vermieden werden, indem das benutzerdefinierte Attribut als Zeichenfolge definiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                    |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl> |



 

