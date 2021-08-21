---
title: MDM_EnterpriseAPN_01-Klasse
description: Die MDM \_ EnterpriseAPN \_ 01-Klasse wird vom Unternehmen zum Bereitstellen eines APNs für das Internet verwendet.
ms.assetid: c5fc0a86-98b7-4d0c-aae5-be836e48eee7
keywords:
- MDM_EnterpriseAPN_01-Klasse
- MDM_EnterpriseAPN_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01.InstanceID
- MDM_EnterpriseAPN_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3661328e3e7d9854a2d298e2226a56838af652dc3732010baf95bd9c634f540
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104290"
---
# <a name="mdm_enterpriseapn_01-class"></a>MDM \_ EnterpriseAPN \_ 01-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ EnterpriseAPN \_ 01-Klasse** wird vom Unternehmen zum Bereitstellen eines APNs für das Internet verwendet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_01
{
  string  InstanceID;
  string  ParentID;
  string  APNName;
  string  IPType;
  boolean IsAttachAPN;
  string  ClassId;
  string  AuthType;
  string  UserName;
  string  Password;
  string  IccId;
  boolean AlwaysOn;
  boolean Enabled;
  string  Roaming;
};
```

## <a name="members"></a>Member

Die **MDM \_ EnterpriseAPN \_ 01-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ EnterpriseAPN \_ 01-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

[AlwaysOn](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-alwayson)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[APNName](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-apnname)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Authtype](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-authtype)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Classid](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-classid)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Aktiviert](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-enabled)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[LapId](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iccid)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name der Verbindung, wie er von Windows Verbindungs-Manager angezeigt wird.

</dd> <dt>

[IPType](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iptype)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[IsAttachAPN](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-isattachapn)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse lautet die Zeichenfolge "./Vendor/MSFT/EnterpriseAPN".

</dd> <dt>

[Kennwort](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-password)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Roaming](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-roaming)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[UserName](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-username)
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

 

