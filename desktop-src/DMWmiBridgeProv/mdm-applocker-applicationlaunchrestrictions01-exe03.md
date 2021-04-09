---
title: MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03-Klasse
description: Mit der MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03-Klasse können Sie angeben, welche exe-Anwendungen gestartet werden dürfen.
ms.assetid: 27f10b5c-bc3b-4344-afcf-5718ea13e909
keywords:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03-Klasse
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58aeb86edc21fec974c099fd8d25bd2e3fb244ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858818"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_exe03-class"></a>MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Mit der **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** -Klasse können Sie angeben, welche exe-Anwendungen gestartet werden dürfen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a>Member

Die **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[**Enforcementmode**](/windows/client-management/mdm/applocker-csp)
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

Definiert Einschränkungen für das Starten ausführbarer Anwendungen.

</dd> <dt>

[**Noninteractiveprocessenforcement**](/windows/client-management/mdm/applocker-csp)
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

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Gruppierung*".

</dd> <dt>

[**Policy**](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

