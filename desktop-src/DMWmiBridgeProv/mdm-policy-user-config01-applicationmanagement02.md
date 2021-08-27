---
title: MDM_Policy_User_Config01_ApplicationManagement02-Klasse
description: Die MDM \_ Policy \_ User \_ Config01 ApplicationManagement02-Klasse stellt die verfügbaren Startrichtlinien dar, die pro \_ Benutzer festgelegt werden.
ms.assetid: 3dd20364-6723-4ed6-87c0-729789ddd948
keywords:
- MDM_Policy_User_Config01_ApplicationManagement02-Klasse
- MDM_Policy_User_Config01_ApplicationManagement02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_ApplicationManagement02
- MDM_Policy_User_Config01_ApplicationManagement02.InstanceID
- MDM_Policy_User_Config01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4044e73c2a466fed3bc69d877fe3bf0a6ebc3679450ddfd435aa8d22b5b3be5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109250"
---
# <a name="mdm_policy_user_config01_applicationmanagement02-class"></a>MDM \_ Policy \_ User \_ Config01 \_ ApplicationManagement02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM Policy User \_ \_ \_ Config01 \_ ApplicationManagement02-Klasse** stellt die verfügbaren Startrichtlinien dar, die pro Benutzer festgelegt werden.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 RequirePrivateStoreOnly;
};
```

## <a name="members"></a>Member

Die **MDM Policy User \_ \_ \_ Config01 \_ ApplicationManagement02-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM Policy User \_ \_ \_ Config01 \_ ApplicationManagement02-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifiziert den Namen des übergeordneten Knotens. Für diese Klasse ist die Zeichenfolge "ApplicationManagement".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./User/Vendor/MSFT/Policy/Config".

</dd> <dt>

[RequirePrivateStoreOnly](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
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

 

