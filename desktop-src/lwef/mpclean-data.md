---
title: MPCLEAN_DATA -Struktur (MpClient.h)
description: Benachrichtigungsdaten, die an eine bereinigte Rückruffunktion übergeben werden.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA struktur Legacy Windows Umgebungsfeatures
- PMPCLEAN_DATA Strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece20324fc06fb68a813b374a698b2e27264068c9051bb2a5fff328c7ad328d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476338"
---
# <a name="mpclean_data-structure"></a>MPCLEAN \_ DATA-Struktur

Benachrichtigungsdaten, die an eine bereinigte Rückruffunktion übergeben werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**ThreatID**
</dt> <dd>

Typ: **MPTHREAT-ID \_**

</dd> <dd>

Bedrohungsbezeichner für **die MPNOTIFY \_ CLEAN THREAT \_ \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED-Ereignisse.** Oberes Bit wird festgelegt, um Bedrohungen im Zusammenhang mit Antivirensoftware zu identifizieren.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Typ: **[ **MPTHREAT \_ ACTION**](mpthreat-action.md)**

</dd> <dd>

Bedrohungsaktion für **die MPNOTIFY \_ CLEAN THREAT \_ \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED-Ereignisse.** Siehe [**MPTHREAT \_ ACTION**](mpthreat-action.md).

</dd> <dt>

**dwStatus**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Zusätzliche Status oder Aktionen, die der durchgeführten Aktion zugeordnet sind. Dies ist eine Kombination von Bitflags von [**MPSTATUS \_ FLAG**](mpstatus-flag.md).

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Typ: **PMPRESOURCE \_ INFO**

</dd> <dd>

Ressourceninformationen für die **MPNOTIFY \_ CLEAN \_ THREAT \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED-Ereignisse.** Weitere Informationen [**finden Sie unter MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MPRESOURCE-INFORMATIONEN \_**](mpresource-info.md)
</dt> <dt>

[**\_MPSTATUS-FLAG**](mpstatus-flag.md)
</dt> <dt>

[**MPTHREAT-AKTION \_**](mpthreat-action.md)
</dt> </dl>

 

 





