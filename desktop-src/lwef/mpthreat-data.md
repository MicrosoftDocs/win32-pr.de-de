---
title: MPTHREAT_DATA -Struktur (MpClient.h)
description: Benachrichtigungsdaten, die aufgrund von Bedrohungserkennung oder -änderung übergeben werden.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA struktur Legacy-Windows Umgebungsfeatures
- PMPTHREAT_DATA strukturzeiger Legacy-Windows-Umgebungsfeatures
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
ms.openlocfilehash: 2bd6338a027e3b03971f357950bbc351acef0d3fcdca83b72130e0ea475164d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883230"
---
# <a name="mpthreat_data-structure"></a>\_MPTHREAT-DATENstruktur

Benachrichtigungsdaten, die aufgrund von Bedrohungserkennung oder -änderung übergeben werden.

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

**ThreatID**
</dt> <dd>

Typ: **MPTHREAT-ID \_**

</dd> <dd>

Bedrohungsbezeichner. Oberes Bit wird festgelegt, um Bedrohungen im Zusammenhang mit Antivirensoftware zu identifizieren.

</dd> <dt>

**dwSessionID**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Sitzung, die der Bedrohung zugeordnet ist. Legen Sie auf -1 fest, wenn keine sitzungsspezifischen Informationen verfügbar sind.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Typ: **[ **MPTHREAT \_ ACTION**](mpthreat-action.md)**

</dd> <dd>

Es wurde eine Bedrohungsaktion für **die MPNOTIFY \_ THREAT CLEAN \_ \_ SUCCEEDED** / **MPNOTIFY \_ THREAT CLEAN \_ \_ FAILED-Ereignisse** versucht.

</dd> <dt>

**dwStatus**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Zusätzliche Status oder Aktionen, die der durchgeführten Aktion zugeordnet sind. Dies ist eine Kombination von Bitflags von [**MPSTATUS \_ FLAG**](mpstatus-flag.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_MPSTATUS-FLAG**](mpstatus-flag.md)
</dt> <dt>

[**MPTHREAT-AKTION \_**](mpthreat-action.md)
</dt> </dl>

 

 





