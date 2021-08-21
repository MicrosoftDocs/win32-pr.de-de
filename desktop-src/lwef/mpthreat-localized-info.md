---
title: MPTHREAT_LOCALIZED_INFO-Struktur (MpClient.h)
description: Lokalisierte Informationen für eine Bedrohung.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO struktur legacy Windows Environment Features (Legacy-Windows-Umgebungsfeatures)
- PMPTHREAT_LOCALIZED_INFO Strukturzeiger Legacy Windows Umgebungsfeatures
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
ms.openlocfilehash: 4ff28c77c60421fcaabe31580400ad87823ad3edf3536d96ba3ba5eec177ad94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555950"
---
# <a name="mpthreat_localized_info-structure"></a>MPTHREAT \_ LOCALIZED \_ INFO-Struktur

Lokalisierte Informationen für eine Bedrohung.

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

**ThreatID**
</dt> <dd>

Typ: **\_ MPTHREAT-ID**

</dd> <dd>

Bedrohungsbezeichner. Das obere Bit ist festgelegt, um Bedrohungen im Zusammenhang mit Antivirensoftware zu identifizieren.

</dd> <dt>

**Categoryname**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Bedrohungsklassifizierung, z. B. ein Trojaner oder ein Keylogger.

</dd> <dt>

**CategoryDescription**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Beschreibung der Bedrohungskategorie.

</dd> <dt>

**SeverityName**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Schweregrad der Bedrohung, z. B. schwerwiegend oder mittel.

</dd> <dt>

**SeverityDescription**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Beschreibung des Schweregrads der Bedrohung.

</dd> <dt>

**ShortDescription**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Kurze Beschreibung der Bedrohung.

</dd> <dt>

**DefaultActionName;**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Name der Standardaktion, z. B. entfernen oder unter Quarantäne stellen, die von der Engine vorgeschlagen wird.

</dd> <dt>

**Advice**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Hinweise zur jeweiligen Bedrohung.

</dd> <dt>

**ThreatUrl**
</dt> <dd>

Typ: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Eine URL zu einer Webseite, die Informationen über die Bedrohung enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





