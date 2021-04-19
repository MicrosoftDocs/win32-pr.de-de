---
description: Die \_ WMI-Klasse "Win32 logicalprogramgroupdirectory Association" bezieht logische Programm Gruppen (Gruppierungen im Startmenü) und die Datei Verzeichnisse, in denen Sie gespeichert sind.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupDirectory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342578"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a>Win32 \_ logicalprogramgroupdirectory-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ logicalprogramgroupdirectory** Association" bezieht logische Programm Gruppen (Gruppierungen im **Startmenü** ) und die Datei Verzeichnisse, in denen Sie gespeichert sind.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ logicalprogramgroupdirectory** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ logicalprogramgroupdirectory** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ logicalprogramgroup**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ logicalprogramgroup")
</dt> </dl>

Verweis auf die Instanz, die die logische Programmgruppe darstellt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Verzeichnis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32- \_ Verzeichnis")
</dt> </dl>

Verweis auf die-Instanz, die das Datei Verzeichnis für die logische Programmgruppe darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ logicalprogramgroupdirectory** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen. Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).

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

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

