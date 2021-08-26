---
title: MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02-Klasse
description: Die Mdm \_ Reporting \_ SecurityAuditing01 RetrieveByTimeRange02-Klasse wird verwendet, um die Protokolle abzurufen, die \_ in StartTime und StopTime vorhanden sind.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02-Klasse
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02, beschrieben
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c307f2b5ddcad1631cd5981a0ea25d8b9fb43566a482de20a2d050a0f3e8db57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913572"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a>MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **Mdm \_ Reporting \_ SecurityAuditing01-Klasse \_ RetrieveByTimeRange02** wird verwendet, um die Protokolle abzurufen, die in StartTime und StopTime vorhanden sind. StartTime und StopTime werden im ISO 8601-Format ausgedrückt. Wenn StartTime und StopTime nicht angegeben sind, werden die Werte entweder als erste vorhandene oder letzte vorhandene Zeit interpretiert.

Hier sind die anderen möglichen Szenarien:

-   Wenn StartTime und StopTime nicht angegeben sind, werden alle vorhandenen Protokolle zurückgegeben.
-   Wenn StopTime angegeben wird, startTime jedoch nicht angegeben ist, werden alle Protokolle zurückgegeben, die vor StopTime vorhanden sind.
-   Wenn StartTime angegeben wird, stoptime jedoch nicht angegeben ist, werden alle Protokolle zurückgegeben, die aus StartTime vorhanden sind.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a>Member

Die **Mdm \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifiziert den Namen des übergeordneten Knotens. Für diese Klasse ist die Zeichenfolge "RetrieveByTimeRange".

</dd> <dt>

[Protokolle](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/SecurityAuditing".

</dd> <dt>

[StartTime](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                            |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\Mofs-DMWmiBridgeProv.dll</dt> </dl> |



 

