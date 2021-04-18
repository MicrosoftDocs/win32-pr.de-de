---
description: Win32 \_ pagefilesetting&\# 8194; WMI-Klasse stellt die Einstellungen einer Auslagerungs Datei dar.
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Win32_PageFileSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339703"
---
# <a name="win32_pagefilesetting-class"></a>Win32- \_ pagefilesetting-Klasse

Die **Win32 \_ pagefilesetting**- [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt die Einstellungen einer Auslagerungs Datei dar. Informationen, die in Objekten enthalten sind, die von dieser Klasse instanziiert werden, geben die Auslagerungs Datei Parameter an, die beim Systemstart erstellt werden. Die Eigenschaften in dieser Klasse können geändert und bis zum Start verzögert werden. Diese Einstellungen unterscheiden sich vom Lauf Zeit Zustand einer Auslagerungs Datei, die durch die zugeordnete [**Win32- \_ PageFileUsage**](win32-pagefileusage.md)-Klasse ausgedrückt wird.

Um eine Instanz dieser Klasse zu erstellen, aktivieren Sie die Berechtigung **secreatepagefileprivilege** . Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](../wmisdk/privilege-constants.md) und [Ausführen privilegierter Vorgänge](../wmisdk/executing-privileged-operations.md).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a>Member

Die **Win32-Klasse \_ pagefilesetting** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32-Klasse \_ pagefilesetting** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**InitialSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("Megabytes")
</dt> </dl>

Anfängliche Größe der Auslagerungs Datei.

Beispiel: 139

</dd> <dt>

**MaximumSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("Megabytes")
</dt> </dl>

Maximale Größe der Auslagerungs Datei.

Beispiel: 178

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Der Pfad und der Dateiname der Auslagerungs Datei.

Beispiel: "C: \\PAGEFILE.SYS"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ pagefilesetting** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

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

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
