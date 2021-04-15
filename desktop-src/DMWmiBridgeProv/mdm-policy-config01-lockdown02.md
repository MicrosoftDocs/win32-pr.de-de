---
title: MDM_Policy_Config01_LockDown02-Klasse
description: Die Config01 Lockdown02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die verfügbaren Sperr Richtlinien dar.
ms.assetid: 1d744400-70db-4f6b-97d0-7799fdfda44f
keywords:
- MDM_Policy_Config01_LockDown02-Klasse
- MDM_Policy_Config01_LockDown02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_LockDown02
- MDM_Policy_Config01_LockDown02.InstanceID
- MDM_Policy_Config01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf9914573c1a3f693d88da8b35b2d577e1f21f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476614"
---
# <a name="mdm_policy_config01_lockdown02-class"></a>MDM- \_ Richtlinie \_ Config01 \_ LockDown02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **\_ \_ Config01 \_ Lockdown02-Klasse der MDM-Richtlinie** stellt die verfügbaren Sperr Richtlinien dar.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a>Member

Die **MDM- \_ Richtlinie \_ Config01 \_ LockDown02** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM- \_ Richtlinie \_ Config01 \_ LockDown02** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

["Zuweisung"](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt den Namen des übergeordneten Knotens an. Für diese Klasse ist die Zeichenfolge "Lockdown".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                            |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dllfür die \\</dt> </dl> |



 

