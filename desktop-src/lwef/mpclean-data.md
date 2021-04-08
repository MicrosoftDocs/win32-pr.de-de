---
title: MPCLEAN_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten wurden an eine saubere Rückruffunktion übermittelt.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCLEAN_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741025"
---
# <a name="mpclean_data-structure"></a>Mpclean- \_ Datenstruktur

Benachrichtigungs Daten wurden an eine saubere Rückruffunktion übermittelt.

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

**Threatid**
</dt> <dd>

Typ: **mpthreat- \_ ID**

</dd> <dd>

Bedrohungs Bezeichner für die **mpnotify- \_ Bereinigung \_ \_** bereinigen, dass Fehler bei der Bereinigung der Clean Threat-Ereignisse aufgetreten sind / **\_ \_ \_** / **\_ \_ \_** . Das obere Bit ist festgelegt, um antivirenbezogene Bedrohungen zu identifizieren.

</dd> <dt>

**Maßnahme**
</dt> <dd>

Typ: **[ **mpthreat- \_ Aktion**](mpthreat-action.md)**

</dd> <dd>

Bedrohungs Aktion für den Fehler "mpnotify Clean Threat **\_ \_ \_ Start** / **mpnotify Clean \_ \_ Threat \_** failed", Fehler bei / **\_ Clean \_ Threat \_ failed** -Ereignissen. Siehe [**mpthreat- \_ Aktion**](mpthreat-action.md).

</dd> <dt>

**dwStatus**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Zusätzliche Status oder Aktionen, die der ausgeführten Aktion zugeordnet sind. Dies ist eine Kombination von Bitflags aus dem [**mpstatus- \_ Flag**](mpstatus-flag.md).

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Typ: **pmpresource- \_ Informationen**

</dd> <dd>

In den Ressourcen Informationen für die **mpnotify- \_ Bereinigung \_ \_** wurde ein Fehler bei der Bereinigung der Bereinigung von Clean Threat / **\_ \_ \_** / **\_ \_ \_ failed** -Ereignissen gemeldet. Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mpresource- \_ Informationen**](mpresource-info.md)
</dt> <dt>

[**\_mpstatusflag**](mpstatus-flag.md)
</dt> <dt>

[**mpthreat- \_ Aktion**](mpthreat-action.md)
</dt> </dl>

 

 





