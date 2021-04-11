---
description: Die \_ WMI-Klasse der Win32 pagefileelementsetting-Zuordnung verknüpft die anfänglichen Einstellungen einer Auslagerungs Datei und den Zustand dieser Einstellungen während der normalen Verwendung.
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Win32_PageFileElementSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc1087225894cef2895cf41af5e5297769a4041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958539"
---
# <a name="win32_pagefileelementsetting-class"></a>Win32 \_ pagefileelementsetting-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32 \_ pagefileelementsetting** -Zuordnung verknüpft die anfänglichen Einstellungen einer Auslagerungs Datei und den Zustand dieser Einstellungen während der normalen Verwendung.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a>Member

Die **Win32-Klasse \_ pagefileelementsetting** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32-Klasse \_ pagefileelementsetting** verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ PageFileUsage**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileUsage")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften einer Auslagerungs Datei darstellt, während das Win32-System verwendet wird.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ pagefilesetting**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ pagefilesetting")
</dt> </dl>

Verweis auf die-Instanz, die die anfänglichen Einstellungen einer Auslagerungs Datei darstellt, wenn das Win32-System gestartet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32-Klasse \_ pagefileelementsetting** wird von [**CIM \_ Element Setting**](cim-elementsetting.md)abgeleitet.

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

 

 
