---
description: Die \_ WMI-Klasse für die Win32 wmielementsetting-Zuordnung verknüpft einen Dienst, der im Windows-System ausgeführt wird, und die verwendeten WMI-Einstellungen.
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Win32_WMIElementSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 41f79614fd0931759d502bbd61c7f4143e9e7dc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860687"
---
# <a name="win32_wmielementsetting-class"></a>Win32 \_ wmielementsetting-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32 \_ wmielementsetting** -Zuordnung verknüpft einen Dienst, der im Windows-System ausgeführt wird, und die verwendeten WMI-Einstellungen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a>Member

Die **Win32 \_ wmielementsetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ wmielementsetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Dienst**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32- \_ Dienst")
</dt> </dl>

Verweis auf die Instanz, die den Windows-Dienst mithilfe von WMI-Eigenschaften darstellt oder diese darstellt.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ wmisetting**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ wmisetting")
</dt> </dl>

Verweis auf die-Instanz, die die für den Windows-Dienst verfügbaren WMI-Einstellungen darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ wmielementsetting** -Klasse wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Element Setting**](cim-elementsetting.md)
</dt> <dt>

[WMI-Dienst Verwaltungs Klassen](./wmi-service-management-classes.md)
</dt> </dl>

 

 
