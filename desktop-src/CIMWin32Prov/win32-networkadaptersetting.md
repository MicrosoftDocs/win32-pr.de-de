---
description: Die \_ WMI-Klasse "Win32 networkadaptersetting Association" verknüpft einen Netzwerkadapter und seine Konfigurationseinstellungen.
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Win32_NetworkAdapterSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340128"
---
# <a name="win32_networkadaptersetting-class"></a>Win32 \_ networkadaptersetting-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ networkadaptersetting** Association" verknüpft einen Netzwerkadapter und seine Konfigurationseinstellungen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a>Member

Die **Win32 \_ networkadaptersetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ networkadaptersetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ NetworkAdapter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Network Adapter")
</dt> </dl>

Ein [**Win32- \_ NetworkAdapter**](win32-networkadapter.md) , der die Eigenschaften des Netzwerkadapters beschreibt, der eine bestimmte Netzwerkadapter Einstellung verwendet.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ networkadapterconfiguration**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ networkadapterconfiguration")
</dt> </dl>

Eine [**Win32- \_ networkadapterconfiguration**](win32-networkadapterconfiguration.md) , die die auf dem Netzwerkadapter verwendeten Konfigurationseinstellungen beschreibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ networkadaptersetting** -Klasse wird von [**Win32- \_ devicesettings**](win32-devicesettings.md)abgeleitet.

Weitere Informationen zum Verwenden von Zuordnungs Klassen finden Sie unter [ASSOCIATORS of Statement](../wmisdk/associators-of-statement.md).

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Beispiel wird **Win32 \_ networkadaptersetting** verwendet, um die IP-Adresse in der LAN-Verbindung zu identifizieren.


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Geräte-Manager \_**](win32-devicesettings.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> <dt>

[WMI-Tasks: Netzwerk](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
