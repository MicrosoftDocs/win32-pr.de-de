---
title: MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02-Klasse
description: Die MDM \_ Reporting \_ EnterpriseDataProtection01 RetrieveByTimeRange02-Klasse wird verwendet, um die Protokolle abzurufen, die \_ in StartTime und StopTime vorhanden sind.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02-Klasse
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60952e10f437b75edb4edf5a9465d4926b7e0615cc736f19f31520e02997d5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045610"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a>MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02-Klasse** wird verwendet, um die Protokolle abzurufen, die in StartTime und StopTime vorhanden sind. StartTime und StopTime werden im ISO 8601-Format ausgedrückt. Wenn StartTime und StopTime nicht angegeben sind, werden die Werte entweder als erste vorhandene oder letzte vorhandene Zeit interpretiert.

Hier sind die anderen möglichen Szenarien:

-   Wenn StartTime und StopTime nicht angegeben sind, werden alle vorhandenen Protokolle zurückgegeben.
-   Wenn StopTime angegeben wird, startTime jedoch nicht angegeben ist, werden alle Protokolle zurückgegeben, die vor StopTime vorhanden sind.
-   Wenn StartTime angegeben wird, stoptime jedoch nicht angegeben ist, werden alle Protokolle zurückgegeben, die aus StartTime vorhanden sind.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a>Member

Die **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ Reporting \_ EnterpriseDataProtection01-Klasse \_ RetrieveByTimeRange02** verfügt über diese Eigenschaften.

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

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseDataProtection".

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

</dd> <dt>

[Typ](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
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



 

