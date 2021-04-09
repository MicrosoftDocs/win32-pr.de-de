---
description: Die \_ WMI-Klasse "Win32 operatingsystemqfe Association" bezieht sich auf ein Betriebssystem und die in der Win32- \_ quickfixengineering dargestellten Produktupdates.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Win32_OperatingSystemQFE-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3b357e3c6efb62217c137bc6c785185154ed984
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958542"
---
# <a name="win32_operatingsystemqfe-class"></a>Win32 \_ operatingsystemqfe-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ operatingsystemqfe** Association" bezieht sich auf ein Betriebssystem und die in der [**Win32- \_ quickfixengineering**](win32-quickfixengineering.md)dargestellten Produktupdates.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ operatingsystemqfe** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ operatingsystemqfe** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ OperatingSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")
</dt> </dl>

Verweis auf die-Instanz, die das System darstellt, das durch das Produkt Update in dieser Zuordnung betroffen ist.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ quickfixengineering**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ quickfixengineering")
</dt> </dl>

Verweis auf die-Instanz, die die Objektinstanz darstellt, die in dieser Zuordnung auf das Betriebssystem angewendet wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ operatingsystemqfe** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.

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

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
