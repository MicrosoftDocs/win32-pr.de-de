---
title: NAP-Datentypen (naptypes. h)
description: 'Beachten Sie, dass die Netzwerk Zugriffsschutz-Plattform ab Windows 10 nicht mehr verfügbar ist: die Datentypen für die NAP-API (Network Access Protection, Netzwerk Zugriffsschutz) lauten wie folgt.'
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- Probationtime
- Protocolmaxsize
- Napcomponentid
- Systemhealthentityid
- Enforcemententityid
- Systemhealthentitycount
- Enforcemententitycount
- Stringcorrelationid
- ConnectionId
- Prozentwert
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956966"
---
# <a name="nap-datatypes"></a>NAP-Datentypen

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die Datentypen für die NAP-API (Network Access Protection, Netzwerk Zugriffsschutz) lauten wie folgt.


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

**Probationtime**
</dt> <dd>

Eine [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, die eine Zeit im Zusammenhang mit der Bewährungsprobe eines Client Computers enthält.

</dd> <dt>

**Protocolmaxsize**
</dt> <dd>

Ein-Wert, der den Bereich möglicher Werte für die maximale Größe (in Bytes) eines [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Pakets angibt, wie nach Bereich definiert ([**minprotocolmaxsize, maxprotocolmaxsize**](nap-type-constants.md)).

</dd> <dt>

**Napcomponentid**
</dt> <dd>

Ein eindeutiger 4-Byte-Bezeichner, der von SHAs, SHVs und Erzwingungs Clients zur Identifizierung verwendet wird. Die ersten drei Bytes sind der durch IETF zugewiesene SMI-Code des Anbieters, und das letzte Byte identifiziert die Komponente selbst.

</dd> <dt>

**Systemhealthentityid**
</dt> <dd>

Ein **napcomponentid-** Wert, mit dem SHA/SHV-Paare identifiziert werden.

</dd> <dt>

**Enforcemententityid**
</dt> <dd>

Ein **napcomponentid-** Wert, mit dem Erzwingungs Clients identifiziert werden.

</dd> <dt>

**Systemhealthentitycount**
</dt> <dd>

Ein-Wert, der die Anzahl der registrierten SHAs im NAP-System im Bereich von 0 (null) bis [**maxsystemhealthentitycount**](nap-type-constants.md)angibt.

</dd> <dt>

**Enforcemententitycount**
</dt> <dd>

Ein-Wert, der die Anzahl der Erzwingungs Clients im NAP-System im Bereich von 0 (null) bis [**maxenforcercount**](nap-type-constants.md)angibt.

</dd> <dt>

**Stringcorrelationid**
</dt> <dd>

Die " [**waytedstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) "-Version einer [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) -Struktur, die für die Kopplung von [**sohrequests**](/windows/win32/api/naptypes/ns-naptypes-soh) an **sohantworten** verwendet wird.

</dd> <dt>

**ConnectionID**
</dt> <dd>

Eine eindeutige GUID (Global Unique Identifier) zum Identifizieren von NAP-Verbindungen, die von Erzwingungs Clients verwaltet werden.

</dd> <dt>

**Percentage**
</dt> <dd>

Ein-Wert, der den Prozentsatz von 0 (null) und 100 der abgeschlossenen Wiederherstellung enthält.

</dd> <dt>

**MessageId**
</dt> <dd>

Ein eindeutiger Wert, mit dem NAP-Systemmeldungen identifiziert werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                                |
| Header<br/>                   | <dl> <dt>Naptypes. h; </dt> <dt>Napforcementclient. h</dt> </dl> |



 

