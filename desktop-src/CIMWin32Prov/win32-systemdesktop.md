---
description: Die \_ WMI-Klasse der Win32 Systemdesktop Association bezieht sich auf ein Computersystem und dessen Desktop Konfiguration.
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Win32_SystemDesktop-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e14cab58a445fd645b9d59c1aea713bf6c40ac0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958572"
---
# <a name="win32_systemdesktop-class"></a>Win32 \_ Systemdesktop-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32 \_ Systemdesktop** Association bezieht sich auf ein Computersystem und dessen Desktop Konfiguration.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a>Member

Die **Win32- \_ Systemdesktop-** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ Systemdesktop-** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Computersystem")
</dt> </dl>

Verweis auf die-Instanz, die das Computersystem darstellt, auf dem die Desktop Konfiguration vorhanden ist.

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ -Desktop**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Setting"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")
</dt> </dl>

Verweis auf die-Instanz, die die auf dem Computersystem vorhandene Konfiguration darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ Systemdesktop-** Klasse wird von [**Win32 \_ systemsetting**](win32-systemsetting.md)abgeleitet.

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

 

 
