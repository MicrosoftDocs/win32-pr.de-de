---
title: MDM_Policy_Result01_Games02-Klasse
description: Die Result01 Games02-Klasse der MDM- \_ Richtlinie ruft \_ \_ die Einstellungen der erweiterten Gaming-Dienste ab.
ms.assetid: c8d17de7-b645-4937-af9f-94bfc039b2fc
keywords:
- MDM_Policy_Result01_Games02-Klasse
- MDM_Policy_Result01_Games02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Games02
- MDM_Policy_Result01_Games02.InstanceID
- MDM_Policy_Result01_Games02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a0a9a216b8bb2610e25ffdbd4e233fc8b3f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104024"
---
# <a name="mdm_policy_result01_games02-class"></a>MDM- \_ Richtlinie \_ Result01 \_ Games02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die Result01 Games02-Klasse der MDM- \_ Richtlinie ruft \_ \_ die Einstellungen der erweiterten Gaming-Dienste ab.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Games02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAdvancedGamingServices;
};
```

## <a name="members"></a>Member

Die **MDM- \_ Richtlinie \_ Result01 \_ Games02** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM- \_ Richtlinie \_ Result01 \_ Games02** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Allowadvancedgamingservices](/windows/client-management/mdm/policy-csp-games#games-allowadvancedgamingservices)
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



 

