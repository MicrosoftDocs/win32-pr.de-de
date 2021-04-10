---
description: Die \_ WMI-Klasse "Win32 comclassautoemulator Association" verknüpft eine Component Object Model (com)-Klasse und eine andere com-Klasse, die Sie automatisch emuliert.
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
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127345"
---
# <a name="win32_comclassautoemulator-class"></a>Win32 \_ comclassautoemulator-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ comclassautoemulator** Association" verknüpft eine Component Object Model (com)-Klasse und eine andere com-Klasse, die Sie automatisch emuliert.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **Win32 \_ comclassautoemulator** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ comclassautoemulator** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**NewVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ classiccomclass**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")
</dt> </dl>

Verweis auf die Instanz, die die COM-Komponente darstellt, die die zugeordnete COM-Komponente automatisch emulieren kann. Diese Informationen werden über den Registrierungs Eintrag AutoTreatAs abgerufen.

</dd> <dt>

**OldVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ classiccomclass**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ classiccomclass")
</dt> </dl>

Verweis auf die-Instanz, die die COM-Komponente darstellt, die von einer anderen Komponente automatisch emuliert wird.

</dd> </dl>

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

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

