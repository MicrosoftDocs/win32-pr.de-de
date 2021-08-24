---
title: MDM_DeviceStatus_CellularIdentities01_01-Klasse
description: Mit der MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01-Klasse können Sie abfragen, ob das Gerät mit der Unternehmensverschlüsselungsrichtlinie konform ist.
ms.assetid: e117ff72-48c0-4b25-8b09-c096851c18ac
keywords:
- MDM_DeviceStatus_CellularIdentities01_01-Klasse
- MDM_DeviceStatus_CellularIdentities01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_CellularIdentities01_01
- MDM_DeviceStatus_CellularIdentities01_01.InstanceID
- MDM_DeviceStatus_CellularIdentities01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8ee53bb06be0cf5bce11cdcc26be49d86b15f3bb79aa58237ce258f8ee1a05c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655690"
---
# <a name="mdm_devicestatus_cellularidentities01_01-class"></a>MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Mit **der MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01-Klasse** können Sie abfragen, ob das Gerät mit der Unternehmensverschlüsselungsrichtlinie konform ist.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_CellularIdentities01_01
{
  string  InstanceID;
  string  ParentID;
  string  IMSI;
  string  ICCID;
  string  PhoneNumber;
  string  CommercializationOperator;
  boolean RoamingStatus;
  boolean RoamingCompliance;
};
```

## <a name="members"></a>Member

Die **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ DeviceStatus \_ CellularIdentities01 \_ 01-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

[CommercializationOperator](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-commercializationoperator)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[ICCID](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-iccid)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Imsi](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-imsi)
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

Knoten für Abfragen auf SIM-Karten.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse lautet die Zeichenfolge "./Vendor/MSFT/DeviceStatus".

</dd> <dt>

[Phonenumber](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-phonenumber)
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[RoamingCompliance](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingcompliance)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[RoamingStatus](/windows/client-management/mdm/devicestatus-csp#devicestatus-cellularidentities-imei-roamingstatus)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
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

 

