---
title: PROTOCOL_SPECIFIC_DATA Struktur (RTM. h)
description: Die Protokoll \_ spezifische \_ Datenstruktur enthält Arbeitsspeicher, der für spezifische Daten eines bestimmten Routing Protokolls reserviert ist.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA Struktur-RAS
- PPROTOCOL_SPECIFIC_DATA-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742192"
---
# <a name="protocol_specific_data-structure"></a>Protokoll \_ spezifische \_ Datenstruktur

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **Protokoll \_ spezifische \_ Daten** Struktur enthält Arbeitsspeicher, der für spezifische Daten eines bestimmten Routing Protokolls reserviert ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**PSD- \_ Daten**
</dt> <dd>

Gibt ein Array von **DWORD** -Variablen an. Dieser Speicher ist für Daten reserviert, die für Routing Protokolle spezifisch sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz für Routing Tabellen-Manager Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routing Tabellen-Manager, Version 1, Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ -IP- \_ Route**](rtm-ip-route.md)
</dt> <dt>

[**RTM- \_ IPX- \_ Route**](rtm-ipx-route.md)
</dt> </dl>

 

 





