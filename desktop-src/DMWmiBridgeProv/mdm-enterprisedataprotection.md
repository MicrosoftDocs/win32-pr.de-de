---
title: MDM_EnterpriseDataProtection-Klasse
description: Die MDM \_ enterprisedataprotection-Klasse wird verwendet, um den aktuellen Status von Windows Information Protection (WIP)-spezifischen Einstellungen zu bestimmen.
ms.assetid: 2b97de12-76d1-4b74-a979-f0484807b840
keywords:
- MDM_EnterpriseDataProtection-Klasse
- MDM_EnterpriseDataProtection-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection.InstanceID
- MDM_EnterpriseDataProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b4a3a1d9d491b6970ee95a081de8bb240d54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478063"
---
# <a name="mdm_enterprisedataprotection-class"></a>MDM \_ enterprisdataprotection-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ enterprisedataprotection** -Klasse wird verwendet, um den aktuellen Status von Windows Information Protection (WIP)-spezifischen Einstellungen zu bestimmen.

Weitere Informationen zu WIP finden Sie unter [Schützen von Unternehmensdaten mithilfe von Enterprise Data Protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a>Member

Die **MDM \_ enterpritardataprotection** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ enterprigendataprotection** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Gibt den Namen des übergeordneten Knotens an. Für diese Klasse ist die Zeichenfolge "enterprisdataprotection".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".

</dd> <dt>

[Status](/windows/client-management/mdm/enterprisedataprotection-csp#status)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
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



 

