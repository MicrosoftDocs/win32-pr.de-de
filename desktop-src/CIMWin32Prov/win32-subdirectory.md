---
description: Die \_ WMI-Klasse der Win32-Unterverzeichnis Zuordnung bezieht sich auf ein Verzeichnis (Ordner) und eines der Unterverzeichnisse (Unterordner).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Win32_SubDirectory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127316"
---
# <a name="win32_subdirectory-class"></a>Win32- \_ Unterverzeichnis Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32- \_ Unterverzeichnis** Zuordnung bezieht sich auf ein Verzeichnis (Ordner) und eines der Unterverzeichnisse (Unterordner).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a>Member

Die **Win32- \_ Unterverzeichnis** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ Unterverzeichnis** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Verzeichnis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32- \_ Verzeichnis")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften des übergeordneten Verzeichnisses (Ordner) in dieser Zuordnung darstellt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Verzeichnis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32- \_ Verzeichnis")
</dt> </dl>

Verweis auf die-Instanz, die das Unterverzeichnis (Unterordner) der Zuordnung darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ Unterverzeichnis** Klasse wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.

Zum Zurückgeben einer Auflistung von Unterordnern für einen Ordner erstellen Sie eine Zuordnungs Abfrage, mit der das *RESULTROLE* auf *PartComponent* festgelegt wird. Dies gibt an, dass alle Elemente in der zurückgegebenen Auflistung die Rolle einer PartComponent oder eines unter Ordners des Ordner Objekts spielen müssen. Um den übergeordneten Ordner für einen Ordner zurückzugeben, legen Sie das *RESULTROLE* auf *GroupComponent* fest.

Die **Win32- \_ Unterverzeichnis** Klasse funktioniert nur auf Dateisystem Ebene direkt oberhalb oder direkt unterhalb des angegebenen Ordners.

## <a name="examples"></a>Beispiele

Das folgende VBScript-Beispiel gibt eine Liste aller Unterordner im Ordner C: \\ Scripts zurück.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
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

[**CIM- \_ Komponente**](cim-component.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
