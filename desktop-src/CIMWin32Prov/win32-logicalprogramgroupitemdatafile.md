---
description: Die WMI-Zuordnungsklasse Win32 LogicalProgramGroupItemDataFile bezieht sich auf die Programmgruppenelemente der Startmenü und die Dateien, in denen \_ sie gespeichert sind.
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItemDataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6f69c23ae545de837e9d6578ba2f64eed51ecbc6f10780e40c809cb2e362b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973051"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a>Win32 \_ LogicalProgramGroupItemDataFile-Klasse

Die **WMI-Zuordnungsklasse \_ Win32 LogicalProgramGroupItemDataFile** bezieht sich auf die Programmgruppenelemente des **Startmenüs** und die Dateien, in denen sie gespeichert sind. [](/windows/desktop/WmiSdk/retrieving-a-class)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ LogicalProgramGroupItemDataFile-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ LogicalProgramGroupItemDataFile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ LogicalProgramGroupItem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroupItem")
</dt> </dl>

Verweis auf die -Instanz, die die Programmgruppen im **Startmenü** darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ DataFile**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")
</dt> </dl>

Verweis auf die -Instanz, die die klasse darstellt, die der Programmgruppe zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ LogicalProgramGroupItemDataFile-Klasse** wird von der [**CIM-Abhängigkeit \_ abgeleitet.**](cim-dependency.md)

Der aufrufende Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über SE **\_ RESTORE \_ NAME-Berechtigung** verfügen. Wenn Sie diese Klasse beispielsweise auf dem lokalen Computer aufzählen, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen. Weitere Informationen finden Sie unter [Ausführen von privilegierten Vorgängen.](/windows/desktop/WmiSdk/executing-privileged-operations)

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

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

