---
description: Stellt die identifizierenden Informationen zu einem Videomonitor dar, z. B. Herstellername, Herstellungsjahr oder Seriennummer.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: WmiMonitorID-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 552e66a4e3a0c6f120bcc95123e3a2674fc579457de16c9ef8cd1e80161f175e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051148"
---
# <a name="wmimonitorid-class"></a>WmiMonitorID-Klasse

Die **WMI-Klasse WmiMonitorID** stellt die identifizierenden Informationen zu einem Videomonitor dar, z. B. Herstellername, Herstellungsjahr oder Seriennummer. Die Daten in dieser Klasse entsprechen den Daten im Block Vendor/Product Identification der Videoeingabedefinition des VESA-Standards (Video Electronics Standard Association) Enhanced Extended Display Identification Data (E-EDID).

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a>Member

Die **WmiMonitorID-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **WmiMonitorID-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Name der spezifischen Überwachungsinstanz.

</dd> <dt>

**ManufacturerName**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Herstellers.

</dd> <dt>

**ManufacturerNameLength**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Länge des Herstellernamens in der **ManufacturerName-Eigenschaft.**

</dd> <dt>

**ProductCodeID**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vom Anbieter zugewiesene Produktcode-ID.

</dd> <dt>

**SerialNumberID**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Seriennummer.

</dd> <dt>

UserFriendlyName
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeigename des Monitors. Die Größe des Namens entspricht der Länge, die von der UserFriendlyNameLength-Eigenschaft angegeben wird.

</dd> <dt>

UserFriendlyNameLength
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Zeichen im Namen, die sich in der UserFriendlyName-Eigenschaft befinden.

</dd> <dt>

**WeekOfManufacture**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Herstellungswoche nach Wochennummer. Der Bereich liegt zwischen 1 und 53. Null (0) ist nicht definiert.

</dd> <dt>

**YearOfManufacture**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Herstellungsjahr.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Erläuterung zum Übersetzen der Arrays, in denen Seriennummern-IDs gespeichert werden, finden Sie im Blogartikel [Berichterstellungsmonitorinformationen mit Konfigurations-Manager.](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager)

## <a name="examples"></a>Beispiele

Im folgenden PowerShell-Beispiel wird die Seriennummer mehrerer Monitore abgerufen.


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



Der folgende VBScript-Code ruft auch Überwachungs-ID-Informationen von einem System ab.


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

