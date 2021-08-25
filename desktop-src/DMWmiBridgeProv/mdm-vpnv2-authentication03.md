---
title: MDM_VPNv2_Authentication03-Klasse
description: Die MDM \_ VPNv2 \_ Authentication03-Klasse enthält Authentifizierungsinformationen für das native VPN-Profil.
ms.assetid: 931752a9-6de5-46d4-b9d9-2c59c49e8ed9
keywords:
- MDM_VPNv2_Authentication03-Klasse
- MDM_VPNv2_Authentication03, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03.InstanceID
- MDM_VPNv2_Authentication03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe1bda3b1b2448ae409e07605d2f8439e37872b78c161eac5051d0603269047
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874980"
---
# <a name="mdm_vpnv2_authentication03-class"></a>MDM \_ VPNv2 \_ Authentication03-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die [**MDM \_ VPNv2 \_ Authentication03-Klasse**](mdm-vpnv2-01.md) enthält Authentifizierungsinformationen für das native VPN-Profil.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Authentication03
{
  string InstanceID;
  string ParentID;
  string UserMethod;
  string MachineMethod;
};
```

## <a name="members"></a>Member

Die **MDM \_ VPNv2 \_ Authentication03-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ VPNv2 \_ Authentication03-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifiziert den Namen des übergeordneten Knotens.

</dd> <dt>

[MachineMethod](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-machinemethod)
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

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile".

</dd> <dt>

[UserMethod](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-usermethod)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

