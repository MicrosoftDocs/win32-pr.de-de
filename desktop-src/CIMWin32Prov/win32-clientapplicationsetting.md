---
description: Die \_ WMI-Klasse Win32 clientapplicationsetting Association verknüpft eine ausführbare Datei und eine Component Object Model (com)-Anwendung, die die com-Konfigurationsoptionen für die ausführbare Datei enthält.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Win32_ClientApplicationSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958519"
---
# <a name="win32_clientapplicationsetting-class"></a>Win32 \_ clientapplicationsetting-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ clientapplicationsetting** Association verknüpft eine ausführbare Datei und eine Component Object Model (com)-Anwendung, die die com-Konfigurationsoptionen für die ausführbare Datei enthält.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a>Member

Die **Win32- \_ clientapplicationsetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ clientapplicationsetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Anwendung**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ dcomapplication**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ dcomapplication")
</dt> </dl>

Verweis auf die-Instanz, die die COM-Anwendung darstellt, die Konfigurationsoptionen der ausführbaren Datei enthält.

</dd> <dt>

**Client**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ DataFile**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")
</dt> </dl>

Verweis auf die-Instanz, die die ausführbare Datei darstellt, die com-Einstellungen verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**Win32 \_ "Clientapplicationsetting** " unterstützt keine Enumeration.

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

 

