---
description: Die CIM \_ processexecutable-Klasse stellt einen Link zwischen einem Prozess und einer Datendatei dar und gibt an, dass die Datei an der Ausführung des Prozesses beteiligt ist.
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: CIM_ProcessExecutable-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aedb1e79ad842e4cb04746ff47bfab142a536f43
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041524"
---
# <a name="cim_processexecutable-class"></a>CIM \_ processexecutable-Klasse

Die **CIM \_ processexecutable** -Klasse stellt einen Link zwischen einem Prozess und einer Datendatei dar und gibt an, dass die Datei an der Ausführung des Prozesses beteiligt ist.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a>Member

Die **CIM \_ processexecutable** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ processexecutable** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ DataFile**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung (Vorgänger), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Eine [**CIM \_**](cim-datafile.md) -Datendatei, die die Datendatei beschreibt, die an der Ausführung des Prozesses beteiligt ist.

</dd> <dt>

**BaseAddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Die Basisadresse des Moduls im Adressraum des zugeordneten Prozesses.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Prozess**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung (abhängig), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ein [**CIM- \_ Prozess**](cim-process.md) , der den Prozess beschreibt.

</dd> <dt>

**Globalprocesscount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Aktuelle Anzahl der Prozesse, bei denen die Datei in den Arbeitsspeicher geladen wurde.

</dd> <dt>

**ModuleInstance**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Win32-Instanzhandle. Diese Eigenschaft ist veraltet, und es gibt keinen Ersatzwert.

</dd> <dt>

**ProcessCount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Verweis Zähler der Datei im zugeordneten Prozess.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM \_ processexecutable** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

WMI implementiert die **CIM \_ processexecutable** -Klasse. Die **CIM \_ processexecutable** -Klasse ist eine dynamische Klasse.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

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
</dt> </dl>

 

