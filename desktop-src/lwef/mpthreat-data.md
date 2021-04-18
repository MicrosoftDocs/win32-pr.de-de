---
title: MPTHREAT_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten wurden aufgrund von Bedrohungserkennung oder-Änderung übermittelt.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344720"
---
# <a name="mpthreat_data-structure"></a>Mpthreat- \_ Datenstruktur

Benachrichtigungs Daten wurden aufgrund von Bedrohungserkennung oder-Änderung übermittelt.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**Threatid**
</dt> <dd>

Typ: **mpthreat- \_ ID**

</dd> <dd>

Bedrohungs Bezeichner. Das obere Bit ist festgelegt, um antivirenbezogene Bedrohungen zu identifizieren.

</dd> <dt>

**dwsessionid**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die der Bedrohung zugeordnete Sitzung. Auf-1 festgelegt, wenn keine Sitzungs spezifischen Informationen verfügbar sind.

</dd> <dt>

**Maßnahme**
</dt> <dd>

Typ: **[ **mpthreat- \_ Aktion**](mpthreat-action.md)**

</dd> <dd>

Es wurde versucht, die Bedrohungs Aktion für den Fehler "mpnotify Threat Clean failed-Ereignisse **\_ \_ \_ erfolgreich**" zu beheben / **\_ \_ \_** .

</dd> <dt>

**dwStatus**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Zusätzliche Status oder Aktionen, die der ausgeführten Aktion zugeordnet sind. Dies ist eine Kombination von Bitflags aus dem [**mpstatus- \_ Flag**](mpstatus-flag.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_mpstatusflag**](mpstatus-flag.md)
</dt> <dt>

[**mpthreat- \_ Aktion**](mpthreat-action.md)
</dt> </dl>

 

 





