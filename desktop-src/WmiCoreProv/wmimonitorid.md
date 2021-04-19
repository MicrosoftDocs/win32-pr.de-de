---
description: Stellt die identifizierenden Informationen zu einem Videomonitor dar, z. b. Herstellername, Jahr der Fertigung oder Seriennummer.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Wmimonitorid-Klasse
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
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106367508"
---
# <a name="wmimonitorid-class"></a>Wmimonitorid-Klasse

Die **wmimonitorid-** WMI-Klasse stellt die identifizierenden Informationen zu einem Videomonitor dar, z. b. Herstellername, Jahr der Fertigung oder Seriennummer. Die Daten in dieser Klasse entsprechen den Daten im Anbieter-/Produktions-Identifikations-Block der Videoeingabe Definition des standardmäßigen Enhanced Display Identification Data (E-EDID)-Standards von Video Electronics Standard Association (VESA).

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

Die **wmimonitorid-** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmimonitorid-** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der Name der spezifischen Monitor Instanz.

</dd> <dt>

**ManufacturerName**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Herstellers.

</dd> <dt>

**Manufacturernamelength**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Länge des Hersteller namens in der **ManufacturerName** -Eigenschaft.

</dd> <dt>

**Productcodeid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vom Hersteller zugewiesene Produktcode-ID.

</dd> <dt>

**Serialzahlkennung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Seriennummer.

</dd> <dt>

UserFriendlyName
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeige Name des Monitors. Die Größe des Namens entspricht der Länge, die von der userfriendlynamelength-Eigenschaft angegeben wird.

</dd> <dt>

Userfriendlynamelength
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Zeichen im Namen in der userfriendlyname-Eigenschaft.

</dd> <dt>

**Weekof-Hersteller**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Woche der Fertigung nach Wochen Nummer. Der Bereich liegt zwischen 1 und 53. NULL (0) ist nicht definiert.

</dd> <dt>

**Yearomamanufacturing**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Jahr der Fertigung.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Erläuterung dazu, wie die Arrays übersetzt werden, in denen die Seriennummern-IDs gespeichert sind, finden Sie im Artikel [Bericht über Monitor Informationen mit Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) .

## <a name="examples"></a>Beispiele

Das folgende PowerShell-Beispiel ruft die Seriennummer mehrerer Monitore ab.


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



Der folgende VBScript-Code ruft außerdem Monitor-ID-Informationen von einem System ab.


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
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

