---
description: Die \_ WMI-Klasse "Win32 systemtimezone Association" bezieht sich auf ein Computersystem und eine Zeitzone.
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Win32_SystemTimeZone-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ec294600fdc81f085bf29f5e664bcbec961417c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861156"
---
# <a name="win32_systemtimezone-class"></a>Win32 \_ systemtimezone-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ systemtimezone** Association" bezieht sich auf ein Computersystem und eine Zeitzone.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a>Member

Die **Win32- \_ systemtimezone** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ systemtimezone** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")
</dt> </dl>

Verweis auf die-Instanz, die das Computersystem darstellt, das die Zeitzone des Systems nachverfolgt.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Zeitzone**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ TimeZone")
</dt> </dl>

Verweis auf die-Instanz, die die vom Computersystem nach verfolgten Zeit Zonen Eigenschaften darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ systemtimezone** -Klasse wird von [**Win32 \_ systemsetting**](win32-systemsetting.md)abgeleitet.

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

[**Win32- \_ systemsetting**](win32-systemsetting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
