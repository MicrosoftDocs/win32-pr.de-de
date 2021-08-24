---
title: MDM_EnterpriseDataProtection-Klasse
description: Die MDM \_ EnterpriseDataProtection-Klasse wird verwendet, um den aktuellen Status von spezifischen Einstellungen für Windows Information Protection (WIP) (früher als Enterprise Data Protection bezeichnet) zu bestimmen.
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
ms.openlocfilehash: 0c9ab641873f95f3b7d7b60772dd10ed0a38c12f57497304478a4c469ee1c645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694880"
---
# <a name="mdm_enterprisedataprotection-class"></a>MDM \_ EnterpriseDataProtection-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ EnterpriseDataProtection-Klasse** wird verwendet, um den aktuellen Status von spezifischen Einstellungen für Windows Information Protection (WIP) (früher als Enterprise Data Protection bezeichnet) zu bestimmen.

Weitere Informationen zu WIP finden Sie unter [Schützen Ihrer Unternehmensdaten mit enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).

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

Die **MDM \_ EnterpriseDataProtection-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ EnterpriseDataProtection-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifiziert den Namen des übergeordneten Knotens. Für diese Klasse lautet die Zeichenfolge "EnterpriseDataProtection".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse lautet die Zeichenfolge "./Vendor/MSFT/".

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                            |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\Mofs-DMWmiBridgeProv.dll</dt> </dl> |



 

