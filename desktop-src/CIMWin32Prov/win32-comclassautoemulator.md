---
description: Die WMI-Klasse für die Win32 ComClassAutoEmulator-Zuordnung bezieht sich auf eine Component Object Model-Klasse (COM) und eine andere \_ COM-Klasse, die automatisch emuliert wird.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Win32_ComClassAutoEmulator-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba849eed744ff342cfde10d0f31072d4e898cf52cf4e6966760f780236c56df4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986380"
---
# <a name="win32_comclassautoemulator-class"></a>Win32 \_ ComClassAutoEmulator-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für die **Win32 \_ ComClassAutoEmulator-Zuordnung** bezieht sich auf eine Component Object Model-Klasse (COM) und eine andere COM-Klasse, die automatisch emuliert wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a>Member

Die **Win32 \_ ComClassAutoEmulator-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ ComClassAutoEmulator-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Newversion**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Verweis auf die -Instanz, die die COM-Komponente darstellt, die die zugeordnete COM-Komponente automatisch emulieren kann. Diese Informationen werden über den Registrierungseintrag AutoTreatAs erhalten.

</dd> <dt>

**OldVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ ClassicCOMClass**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")
</dt> </dl>

Verweis auf die -Instanz, die die COM-Komponente darstellt, die automatisch von einer anderen Komponente emuliert wird.

</dd> </dl>

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

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

