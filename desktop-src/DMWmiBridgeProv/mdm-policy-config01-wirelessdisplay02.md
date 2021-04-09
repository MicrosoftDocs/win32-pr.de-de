---
title: MDM_Policy_Config01_WirelessDisplay02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02-Klasse stellt die verfügbaren drahtlos Anzeige Richtlinien dar.
ms.assetid: 24b72ed9-cc14-4318-a9d1-597976083242
keywords:
- MDM_Policy_Config01_WirelessDisplay02-Klasse
- MDM_Policy_Config01_WirelessDisplay02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WirelessDisplay02
- MDM_Policy_Config01_WirelessDisplay02.InstanceID
- MDM_Policy_Config01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b99183f8fdf599df8b5c1b4e82b9b536f47019
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956532"
---
# <a name="mdm_policy_config01_wirelessdisplay02-class"></a>MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02** -Klasse stellt die verfügbaren drahtlos Anzeige Richtlinien dar.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WirelessDisplay02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMdnsDiscovery;
  sint32 AllowMdnsAdvertisement;
  sint32 AllowProjectionFromPCOverInfrastructure;
  sint32 AllowProjectionFromPC;
  sint32 AllowProjectionToPC;
  sint32 AllowProjectionToPCOverInfrastructure;
  sint32 AllowUserInputFromWirelessDisplayReceiver;
  sint32 RequirePinForPairing;
};
```

## <a name="members"></a>Member

Die **MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM- \_ Richtlinie \_ Config01 \_ WirelessDisplay02** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Allowmdnsankündigung](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Allowmdnsdiscovery](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Allowprojectionfrompc](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Allowprojectionfrompcoverinfrastructure](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Allowprojectiontopc](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Allowprojectiontopcoverinfrastructure](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Zuordnung von "zugeerteninputfromwirelessdisplayreceiver"](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
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

Gibt den Namen des übergeordneten Knotens an. Für diese Klasse ist die Zeichenfolge "wirelessdisplay".

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

</dd> <dt>

[Requirements pinforkopplung](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
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
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dllfür die \\</dt> </dl> |



 

