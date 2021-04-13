---
description: Die \_ WMI-Klasse der WMI-Klasse für die WMI-Klasse "Win32 systemsetting" verknüpft ein Computersystem und eine allgemeine Einstellung
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Win32_SystemSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e29b752d769cd347ce1cfdb729bf8c0c3959a4f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483894"
---
# <a name="win32_systemsetting-class"></a>Win32 \_ systemsetting-Klasse

Die [WMI-Klasse der WMI-Klasse für die WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemsetting** " verknüpft ein Computersystem und eine allgemeine Einstellung

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a>Member

Die **Win32- \_ systemsetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ systemsetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften eines Computer Systems darstellt, auf dem diese Einstellung angewendet werden kann.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Einstellung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM- \_ Einstellung")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften der Einstellung darstellt, die auf das Computersystem angewendet werden können.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ systemsetting** -Klasse wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.

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

[**CIM- \_ Element Setting**](cim-elementsetting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
