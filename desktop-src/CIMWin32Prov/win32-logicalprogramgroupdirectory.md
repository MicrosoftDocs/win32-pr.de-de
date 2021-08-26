---
description: Die \_ WMI-Zuordnungsklasse Win32 LogicalProgramGroupDirectory bezieht sich auf logische Programmgruppen (Gruppierungen im Startmenü) und die Dateiverzeichnisse, in denen sie gespeichert sind.
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
ms.openlocfilehash: fa9bf70e82f5a46c8a9a346b33d18e3c9f4a12322ad10a5fca1233df5a36c1d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973310"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a>Win32 \_ LogicalProgramGroupDirectory-Klasse

Die **WMI-Zuordnungsklasse \_ Win32 LogicalProgramGroupDirectory** bezieht sich auf logische Programmgruppen (Gruppierungen im [](/windows/desktop/WmiSdk/retrieving-a-class) **Startmenü)** und die Dateiverzeichnisse, in denen sie gespeichert sind.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

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

Die **Win32 \_ LogicalProgramGroupDirectory-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ LogicalProgramGroupDirectory-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ LogicalProgramGroup**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroup")
</dt> </dl>

Verweis auf die -Instanz, die die logische Programmgruppe darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **\_ Win32-Verzeichnis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Directory")
</dt> </dl>

Verweis auf die -Instanz, die das Dateiverzeichnis für die logische Programmgruppe darstellt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ LogicalProgramGroupDirectory-Klasse** wird von der [**CIM-Abhängigkeit \_ abgeleitet.**](cim-dependency.md)

Der aufrufende Prozess, der diese Klasse verwendet, muss über SE **\_ RESTORE \_ NAME-Berechtigung** auf dem Computer verfügen, auf dem sich die Registrierung befindet. Wenn Sie diese Klasse beispielsweise auf dem lokalen Computer aufzählen, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen. Weitere Informationen finden Sie unter [Ausführen von privilegierten Vorgängen.](/windows/desktop/WmiSdk/executing-privileged-operations)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

