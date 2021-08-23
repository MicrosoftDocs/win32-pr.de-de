---
title: MDM_EnterpriseModernAppManagement_AppSettingPolicy04-Klasse
description: Die MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04-Klasse gibt alle Einstellungswerte für verwaltete Apps an.
ms.assetid: 65e2d2aa-31fd-4733-a1f7-8a572700a562
keywords:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04-Klasse
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.InstanceID
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba82be4653266c94465917857eb47b014399594525a6f0f18264e4f73651684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077254"
---
# <a name="mdm_enterprisemodernappmanagement_appsettingpolicy04-class"></a>MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04-Klasse** gibt alle Einstellungswerte für verwaltete Apps an.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppSettingPolicy04
{
  string  InstanceID;
  string  ParentID;
  string  Value;
  boolean IsVariableLeaf;
};
```

## <a name="members"></a>Member

Die **MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifiziert den Namen des übergeordneten Knotens. Für diese Klasse die Zeichenfolge "AppSettingPolicy".

</dd> <dt>

[IsVariableLeaf](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hinzugefügt in Windows 10 Version 1511. **SettingValue und** die Daten stellen ein Schlüssel-Wert-Paar dar, das für die App konfiguriert werden soll. Der Knoten stellt den Namen des Schlüssels dar, und die Daten stellen den Wert dar. Sie finden diesen Wert in LocalSettings im Managed.App. Einstellungen Container.

Diese Einstellung funktioniert nur für Apps, die das Feature unterstützen, und wird nur im Benutzerkontext unterstützt.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*"

</dd> <dt>

[**Wert**](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
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
| Namespace<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge-Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

