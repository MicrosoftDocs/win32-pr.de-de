---
description: Diese Klasse stellt die Zuordnung zwischen einem Betriebssystem und den Autochk-Einstellungen dar, die für die Datenträger auf dem Computer gelten. Beachten Sie, dass die Einstellung dem Betriebssystem und nicht dem Computersystem zugeordnet ist, da ein oder mehrere Betriebssysteme auf dem Computer installiert sein können, die jeweils über eigene Autochk-Einstellungen installiert sind.
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
ms.openlocfilehash: cfa6e90828935dda8aa163967985813526042b8800f91cb01825fbd158f8a63d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972540"
---
# <a name="win32_operatingsystemautochksetting-class"></a>Win32 \_ OperatingSystemAutochkSetting-Klasse

Diese Klasse stellt die Zuordnung zwischen einem Betriebssystem und den Autochk-Einstellungen dar, die für die Datenträger auf dem Computer gelten. Beachten Sie, dass die Einstellung dem Betriebssystem und nicht dem Computersystem zugeordnet ist, da ein oder mehrere Betriebssysteme auf dem Computer installiert sein können, die jeweils über eigene Autochk-Einstellungen installiert sind.

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

Die **Win32 \_ OperatingSystemAutochkSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ OperatingSystemAutochkSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ OperatingSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("Element"), [**Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

TBD

</dd> <dt>

**Einstellung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ AutochkSetting**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("Einstellung"), [**Schlüssel**](../wmisdk/key-qualifier.md)
</dt> </dl>

TBD

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-ElementSetting**](cim-elementsetting.md)
</dt> </dl>

 

 
