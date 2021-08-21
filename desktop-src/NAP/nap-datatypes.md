---
title: NAP-Datentypen (NapTypes.h)
description: Hinweis Die Network Access Protection-Plattform ist ab Windows 10 nicht verfügbar. Die Datentypen für die NAP-API (Network Access Protection) sind wie folgt.
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- ProbationTime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Prozentsatz
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550baa14779ccefaec14605938edb6076e7cc332aa9d1a2390ab430f7568e844
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802620"
---
# <a name="nap-datatypes"></a>NAP-Datentypen

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die Datentypen für die NAP-API (Network Access Protection) sind wie folgt.


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

**ProbationTime**
</dt> <dd>

Eine [FILETIME-Struktur,](/windows/win32/api/minwinbase/ns-minwinbase-filetime) die eine Zeit im Zusammenhang mit der Testdauer eines Clientcomputers enthält.

</dd> <dt>

**ProtocolMaxSize**
</dt> <dd>

Ein -Wert, der den Bereich der möglichen Werte für die maximale Größe eines [**SoH-Pakets**](/windows/win32/api/naptypes/ns-naptypes-soh) in Bytes angibt, wie durch range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)) definiert.

</dd> <dt>

**NapComponentId**
</dt> <dd>

Ein eindeutiger 4-Byte-Bezeichner, der von SHAs, SHVs und Erzwingungsclients verwendet wird, um sich selbst zu identifizieren. Die ersten drei Bytes sind der IETF-zugewiesene SMI-Code des Anbieters, und das letzte Byte identifiziert die Komponente selbst.

</dd> <dt>

**SystemHealthEntityId**
</dt> <dd>

Ein **NapComponentId-Wert,** der zum Identifizieren von SHA/SHV-Paaren verwendet wird.

</dd> <dt>

**EnforcementEntityId**
</dt> <dd>

Ein **NapComponentId-Wert,** der zum Identifizieren von Erzwingungsclients verwendet wird.

</dd> <dt>

**SystemHealthEntityCount**
</dt> <dd>

Ein -Wert, der die Anzahl der registrierten SHAs im NAP-System im Bereich von 0 (null) bis [**maxSystemHealthEntityCount**](nap-type-constants.md)angibt.

</dd> <dt>

**EnforcementEntityCount**
</dt> <dd>

Ein -Wert, der die Anzahl der Erzwingungsclients im NAP-System im Bereich von 0 (null) bis [**maxEnforcerCount**](nap-type-constants.md)angibt.

</dd> <dt>

**StringCorrelationId**
</dt> <dd>

Die [**CountedString-Version**](/windows/win32/api/naptypes/ns-naptypes-countedstring) einer [**CorrelationId-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-correlationid) die verwendet wird, um [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) mit **SoHResponses** zu koppeln.

</dd> <dt>

**ConnectionId**
</dt> <dd>

Ein eindeutiger GUID (Globally Unique Identifier), der zum Identifizieren von NAP-Verbindungen verwendet wird, die von Erzwingungsclients verwaltet werden.

</dd> <dt>

**Percentage**
</dt> <dd>

Ein -Wert, der den Prozentsatz zwischen 0 (null) und 100 abgeschlossener Korrektur enthält.

</dd> <dt>

**MessageId**
</dt> <dd>

Ein eindeutiger Wert, der zum Identifizieren von NAP-Systemmeldungen verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                                |
| Header<br/>                   | <dl> <dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt> </dl> |



 

