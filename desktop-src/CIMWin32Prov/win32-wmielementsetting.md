---
description: Die WMI-Zuordnungsklasse "Win32 WMIElementSetting" bezieht sich auf einen Dienst, der im Windows system ausgeführt wird, und auf die \_ WMI-Einstellungen, die verwendet werden können.
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
ms.openlocfilehash: f46a9d5fd7c3f0baace1f763b9912f49fbcf318ffd07fa7cbf3138d04d8621f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922540"
---
# <a name="win32_wmielementsetting-class"></a>Win32 \_ WMIElementSetting-Klasse

Die **WMI-Zuordnungsklasse \_ Win32 WMIElementSetting** bezieht sich auf einen Dienst, der im Windows-System ausgeführt wird, und auf die WMI-Einstellungen, die verwendet werden können. [](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

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

Die **Win32 \_ WMIElementSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ WMIElementSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32-Dienst \_**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Service")
</dt> </dl>

Verweis auf die -Instanz, die den Windows mithilfe von WMI-Eigenschaften darstellt oder darauf hinweist.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ WMISetting**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ WMISetting")
</dt> </dl>

Verweis auf die -Instanz, die die WMI-Einstellungen darstellt, die für den Windows sind.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ WMIElementSetting-Klasse** wird von [**CIM \_ ElementSetting abgeleitet.**](cim-elementsetting.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-ElementSetting**](cim-elementsetting.md)
</dt> <dt>

[WMI-Dienstverwaltungsklassen](./wmi-service-management-classes.md)
</dt> </dl>

 

 
