---
title: MDM_Policy_Config01_ApplicationDefaults02-Klasse
description: Die \_ \_ Config01 ApplicationDefaults02-Klasse der MDM-Richtlinie \_ ermöglicht einem Administrator das Festlegen von Standard Dateityp-und Protokoll Zuordnungen. Wenn festgelegt, werden Standard Zuordnungen auf die Anmeldung beim PC angewendet.
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- MDM_Policy_Config01_ApplicationDefaults02-Klasse
- MDM_Policy_Config01_ApplicationDefaults02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246278b1e4185337ebb63d9d23f74e2ff8753615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476035"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a>MDM- \_ Richtlinie \_ Config01 \_ ApplicationDefaults02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die \_ \_ Config01 ApplicationDefaults02-Klasse der MDM-Richtlinie \_ ermöglicht einem Administrator das Festlegen von Standard Dateityp-und Protokoll Zuordnungen. Wenn festgelegt, werden Standard Zuordnungen auf die Anmeldung beim PC angewendet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a>Member

Die **MDM- \_ Richtlinie \_ Config01 \_ ApplicationDefaults02** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM- \_ Richtlinie \_ Config01 \_ ApplicationDefaults02** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Defaultassociationsconfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
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

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

