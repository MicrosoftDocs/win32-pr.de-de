---
title: MDM_AppLocker_EnterpriseDataProtection01_StoreApps03-Klasse
description: Die MDM \_ AppLocker \_ EnterpriseDataProtection01 StoreApps03-Klasse erfasst die Liste der Windows-Apps, die \_ Unternehmensdaten verarbeiten dürfen. Sollte in Verbindung mit den Einstellungen in ./Vendor/MSFT/Policy/ConfigSource/DataProtection verwendet werden.
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
ms.openlocfilehash: cf5b0c3af455e501695cb7a2093b841159f5755ac54e1de97a370c7dc7f2d6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077411"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a>MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03-Klasse** erfasst die Liste der Windows Apps, die Unternehmensdaten verarbeiten dürfen. Sollte in Verbindung mit den Einstellungen in ./Vendor/MSFT/Policy/ConfigSource/DataProtection verwendet werden.

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

Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Legt Beschränkungen zum Ausführen von Apps vom Windows Store fest.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"

</dd> <dt>

[**Richtlinie**](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | \\ \\ Stamm-CIMv2-MDM-DMMap \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

