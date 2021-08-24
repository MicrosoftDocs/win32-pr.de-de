---
title: MDM_Policy_User_Result01_Start02-Klasse
description: Die Mdm \_ Policy \_ User \_ Result01 Start02-Klasse stellt die verfügbaren Startrichtlinien dar, die pro \_ Benutzer festgelegt werden.
ms.assetid: f7b63db4-f48d-44d2-b343-88cbc8f89cbe
keywords:
- MDM_Policy_User_Result01_Start02-Klasse
- MDM_Policy_User_Result01_Start02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Start02
- MDM_Policy_User_Result01_Start02.InstanceID
- MDM_Policy_User_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6a8c969af7fbe22645ab47c31448c8e2604562f39561a350f9d2e40bf80ca7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698440"
---
# <a name="mdm_policy_user_result01_start02-class"></a>MDM \_ Policy \_ User \_ Result01 \_ Start02-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **Mdm Policy User \_ \_ \_ Result01 \_ Start02-Klasse** stellt die verfügbaren Startrichtlinien dar, die pro Benutzer festgelegt werden.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a>Member

Die **MDM Policy User \_ \_ \_ Result01 \_ Start02-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM Policy User \_ \_ \_ Result01 \_ Start02-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

[HidePeopleBar](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
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

Identifiziert den Namen des übergeordneten Knotens. Für diese Klasse ist die Zeichenfolge "Start".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./User/Vendor/MSFT/Policy/Result".

</dd> <dt>

[StartLayout](/windows/client-management/mdm/policy-csp-start#start-startlayout)
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

 

