---
title: MDM_Reporting_SecurityAuditing01_RetrieveByCount02-Klasse
description: Die MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByCount02-Klasse wird verwendet, um eine angegebene Anzahl von Protokollen aus "StartTime" abzurufen.
ms.assetid: dfa50c04-99d6-4f6a-90ff-70a829bd317d
keywords:
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02-Klasse
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c979d25cdc9887a500307494218a6fc11f98bf86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740065"
---
# <a name="mdm_reporting_securityauditing01_retrievebycount02-class"></a>MDM- \_ Berichterstellung \_ SecurityAuditing01 RetrieveByCount02- \_ Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die [**MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByCount02**](mdm-reporting-enterprisedataprotection01-retrievebycount02.md) -Klasse wird verwendet, um eine angegebene Anzahl von Protokollen aus "StartTime" abzurufen. Der StartTime-Wert wird im ISO 8601-Format ausgedrückt. Sie können die Anzahl der erforderlichen Protokolle festlegen, indem Sie "logcount" und "StartTime" festlegen. Wenn die Gesamtzahl der Protokolle kleiner als logcount ist, wird die angegebene Anzahl von Protokollen oder weniger zurückgegeben.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
};
```

## <a name="members"></a>Member

Die **MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByCount02** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByCount02** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt den Namen des übergeordneten Knotens an. Für diese Klasse ist die Zeichenfolge "retrievebycount".

</dd> <dt>

[Logcount](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Protokolle](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**ParentID**
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

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                            |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. MOF</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dllfür die \\</dt> </dl> |



 

