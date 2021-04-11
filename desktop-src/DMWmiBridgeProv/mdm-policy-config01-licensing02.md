---
title: MDM_Policy_Config01_Licensing02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Licensing02-Klasse stellt die verfügbaren Lizenzierungsrichtlinien dar.
ms.assetid: 7ec186e9-626e-4361-88fd-665b947ca23d
keywords:
- MDM_Policy_Config01_Licensing02-Klasse
- MDM_Policy_Config01_Licensing02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Licensing02
- MDM_Policy_Config01_Licensing02.InstanceID
- MDM_Policy_Config01_Licensing02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d654facc7ec3ba08d1f5b0f31497545945cc73d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956450"
---
# <a name="mdm_policy_config01_licensing02-class"></a>MDM- \_ Richtlinie \_ Config01 \_ Licensing02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM- \_ Richtlinie \_ Config01 \_ Licensing02** -Klasse stellt die verfügbaren Lizenzierungsrichtlinien dar.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Licensing02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsEntitlementReactivation;
  sint32 DisallowKMSClientOnlineAVSValidation;
};
```

## <a name="members"></a>Member

Die **MDM- \_ Richtlinie \_ Config01 \_ Licensing02** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM- \_ Richtlinie \_ Config01 \_ Licensing02** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Allowwindowsentitlementreactivation](/windows/client-management/mdm/policy-csp-licensing#licensing-allowwindowsentitlementreactivation)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Disallowkmsclientonlineavsvalidation](/windows/client-management/mdm/policy-csp-licensing#licensing-disallowkmsclientonlineavsvalidation)
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

Gibt den Namen des übergeordneten Knotens an. Für diese Klasse ist die Zeichenfolge "Licensing".

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



 

