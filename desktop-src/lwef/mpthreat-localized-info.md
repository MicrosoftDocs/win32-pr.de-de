---
title: MPTHREAT_LOCALIZED_INFO Struktur (mpclient. h)
description: Lokalisierte Informationen zu einer Bedrohung.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_LOCALIZED_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391883"
---
# <a name="mpthreat_localized_info-structure"></a>Lokalisierte mpthreat- \_ \_ Informationsstruktur

Lokalisierte Informationen zu einer Bedrohung.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Threatid**
</dt> <dd>

Typ: **mpthreat- \_ ID**

</dd> <dd>

Bedrohungs Bezeichner. Das obere Bit ist festgelegt, um antivirenbezogene Bedrohungen zu identifizieren.

</dd> <dt>

**CategoryName**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Bedrohungs Klassifizierung, z. b. ein Trojaner oder eine Keylogger.

</dd> <dt>

**Categorydescription**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Beschreibung der Bedrohungs Kategorie.

</dd> <dt>

**Schweregrad Name**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Bedrohungs Schweregrad, z. b. schwerwiegend oder Mittel.

</dd> <dt>

**"Severitydescription"**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Beschreibung des Bedrohungs schwere Grads.

</dd> <dt>

**Kurzbeschreibung**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Kurze Beschreibung der Bedrohung.

</dd> <dt>

**Defaultactionname;**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Der Name der Standardaktion, wie z. b. Remove oder Quarantäne, von der Engine vorgeschlagen.

</dd> <dt>

**Advice**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Ratschläge für eine bestimmte Bedrohung.

</dd> <dt>

**"-URL"**
</dt> <dd>

Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**

</dd> <dd>

Eine URL zu einer Webseite, die Informationen über die Bedrohung enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





