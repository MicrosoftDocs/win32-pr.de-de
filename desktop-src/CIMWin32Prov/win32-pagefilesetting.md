---
description: Win32 \_ PageFileSetting&\# 8194; Die WMI-Klasse stellt die Einstellungen einer Seitendatei dar.
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
ms.openlocfilehash: b860e5b9677b4d4774e0a3a01fb1cc27b336e7c1a02ebcfc40351f5eda21eb8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020188"
---
# <a name="win32_pagefilesetting-class"></a>Win32 \_ PageFileSetting-Klasse

Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ PageFileSetting** stellt die Einstellungen einer Seitendatei dar. Informationen in Objekten, die von dieser Klasse instanziiert werden, geben die Seitendateiparameter an, die beim Erstellen der Datei beim Systemstart verwendet werden. Die Eigenschaften in dieser Klasse können geändert und bis zum Start zurückgestellt werden. Diese Einstellungen unterscheiden sich vom Laufzeitzustand einer Seitendatei, ausgedrückt durch die zugeordnete [**Klasse Win32 \_ PageFileUsage.**](win32-pagefileusage.md)

Um eine Instanz dieser Klasse zu erstellen, aktivieren Sie die **SeCreatePagefilePrivilege-Berechtigung.** Weitere Informationen finden Sie unter [**Berechtigungskonstanten**](../wmisdk/privilege-constants.md) und [Ausführen privilegierter Vorgänge.](../wmisdk/executing-privileged-operations.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

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

Die **Win32 \_ PageFileSetting-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PageFileSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**InitialSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager Memory \\ \\ Management \\ \\ \| PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Anfangsgröße der Seitendatei.

Beispiel: 139

</dd> <dt>

**Maximumsize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager Memory \\ \\ Management \\ \\ \| PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Maximale Größe der Seitendatei.

Beispiel: 178

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Pfad und Dateiname der Seitendatei.

Beispiel: "C: \\PAGEFILE.SYS"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichner, durch den das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PageFileSetting-Klasse** wird von [**cim \_ setting**](cim-setting.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
