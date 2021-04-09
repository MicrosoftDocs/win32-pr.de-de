---
title: MDM_AppLocker_EnterpriseDataProtection01_StoreApps03-Klasse
description: Die MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03-Klasse erfasst die Liste der Windows-apps, die zum Verarbeiten von Unternehmensdaten berechtigt sind. Sollte in Verbindung mit den Einstellungen in./Vendor/MSFT/Policy/configSource/DataProtection verwendet werden.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03-Klasse
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240f641e542bbbe0c71fd686e2d9df3908b9bab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957145"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a>MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** -Klasse erfasst die Liste der Windows-apps, die zum Verarbeiten von Unternehmensdaten berechtigt sind. Sollte in Verbindung mit den Einstellungen in./Vendor/MSFT/Policy/configSource/DataProtection verwendet werden.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a>Member

Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Legt Beschränkungen zum Ausführen von Apps vom Windows Store fest.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Gruppierung*".

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

 

