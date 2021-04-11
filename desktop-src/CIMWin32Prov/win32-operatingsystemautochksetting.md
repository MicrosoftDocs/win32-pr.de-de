---
description: Diese Klasse stellt die Zuordnung zwischen einem Betriebssystem und den AUTOCHK-Einstellungen dar, die auf die Datenträger auf dem Computer angewendet werden. Beachten Sie, dass die Einstellung dem Betriebssystem und nicht dem Computersystem zugeordnet ist, da ein oder mehrere Betriebssysteme auf dem Computer installiert sein können, die jeweils über eigene automatische chk-Einstellungen verfügen.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Win32_OperatingSystemAutochkSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 905ffc92273b46bb36b7b3e2909afea32e6baeff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127465"
---
# <a name="win32_operatingsystemautochksetting-class"></a>Win32 \_ operatingsystemautochksetting-Klasse

Diese Klasse stellt die Zuordnung zwischen einem Betriebssystem und den AUTOCHK-Einstellungen dar, die auf die Datenträger auf dem Computer angewendet werden. Beachten Sie, dass die Einstellung dem Betriebssystem und nicht dem Computersystem zugeordnet ist, da ein oder mehrere Betriebssysteme auf dem Computer installiert sein können, die jeweils über eigene automatische chk-Einstellungen verfügen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a>Member

Die **Win32 \_ operatingsystemautochksetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ operatingsystemautochksetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ OperatingSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

TBD

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ autochksetting**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Setting"), [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

TBD

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Element Setting**](cim-elementsetting.md)
</dt> </dl>

 

 
