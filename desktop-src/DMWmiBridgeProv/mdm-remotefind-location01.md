---
title: MDM_RemoteFind_Location01-Klasse
description: Die MDM \_ remotefind \_ Location01-Klasse ruft die Speicherort Informationen für ein bestimmtes Gerät ab.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- MDM_RemoteFind_Location01-Klasse
- MDM_RemoteFind_Location01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e1b46a7b4a0c3439f78f38a5fb6cd5b865275c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475288"
---
# <a name="mdm_remotefind_location01-class"></a>MDM \_ remotefind \_ Location01-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ remotefind \_ Location01** -Klasse ruft die Speicherort Informationen für ein bestimmtes Gerät ab.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a>Member

Die **MDM \_ remotefind \_ Location01** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ remotefind \_ Location01** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Genauigkeit](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Age](/windows/client-management/mdm/remotefind-csp#age) (Alter)
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Höhe](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Altitudäaccuracy](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
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

Gibt den Namen des übergeordneten Knotens an. Für diese Klasse ist die Zeichenfolge "Location".

</dd> <dt>

[Latitude](/windows/client-management/mdm/remotefind-csp#latitude) (Breitengrad)
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Longitude](/windows/client-management/mdm/remotefind-csp#longitude) (Längengrad)
</dt> <dd> <dl> <dt>

Datentyp: **real32**
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

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/RemoteFind".

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                       |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

