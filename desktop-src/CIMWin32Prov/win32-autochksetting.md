---
description: Die WMI-Klasse Win32 AutochkSetting stellt die Einstellungen für den Vorgang \_ der automatischen Überprüfung eines Datenträgers dar.
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Win32_AutochkSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6cccf1877d8812e1fee4816e80189b8404d4090a1ef15f45e840fdd6e58d8ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020328"
---
# <a name="win32_autochksetting-class"></a>Win32 \_ AutochkSetting-Klasse

Die **WMI-Klasse \_ Win32 AutochkSetting** stellt die Einstellungen für den Vorgang der automatischen Überprüfung eines Datenträgers dar. [](/windows/desktop/WmiSdk/retrieving-a-class)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a>Member

Die **Win32 \_ AutochkSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ AutochkSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Eine ID, die als Teil eines Schlüssels für das aktuelle Objekt verwendet wird.

</dd> <dt>

**UserInputDelay**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control Session Manager \\ \\ \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")
</dt> </dl>

Die Benutzereingabeverzögerung für die automatische Überprüfung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ AutochkSetting-Klasse** wird von der [**\_ CIM-Einstellung abgeleitet.**](cim-setting.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> </dl>

 

