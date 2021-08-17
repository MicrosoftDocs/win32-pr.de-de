---
description: Beschreibt die lokale Installation von WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: __CIMOMIdentification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 50d81fb8cfc5580ad0868df307771c493c0919e1bf2ce4de4b67d48db034a0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321110"
---
# <a name="__cimomidentification-class"></a>\_\_CIMOMIdentification-Klasse

Die **\_ \_ CIMOMIdentification-Systemklasse** beschreibt die lokale Installation von WMI. Dies ist eine Singletonklasse. es gibt nur eine -Instanz. Die **\_ \_ CIMOMIdentification-Klasse** ist nur in den **Namespaces Root** und **Root \\ Default** verfügbar. Benutzer fragen die Instanz ab, um Informationen zur WMI-Installation zu erhalten.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a>Member

Die **\_ \_ CIMOMIdentification-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ CIMOMIdentification-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**SetupDateTime**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Installation. Diese Eigenschaft ist leer, nachdem das Betriebssystem zum ersten Mal installiert wurde.

Wenn das WMI-Repository gelöscht und dann erneut erstellt wurde, enthält diese Eigenschaft das Datum und die Uhrzeit der erneuten Erstellung des Repositorys.

</dd> <dt>

**VersionCurrentlyRunning**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Version des eigentlichen Images an, das den WMI-Dienst enthält, der das Common Information Model (CIM)-Repository erstellt hat. Da sich das Repositoryformat zwischen WMI-Versionen ändern kann, ermöglicht diese Eigenschaft zukünftigen WMI-Upgrades zu bestimmen, ob die Datenbank aktualisiert werden muss. Das Format lautet:

"1.00.183.0000"

Dabei ist die erste Ziffer die Hauptversion, die nächsten beiden Ziffern sind Nebenversionen, und die nächsten drei Ziffern sind die Buildnummer. Die übrigen Ziffern werden nicht verwendet.

</dd> <dt>

**VersionUsedToCreateDB**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Version des tatsächlichen Images an, das den WMI-Dienst enthält, der das CIM-Repository erstellt hat. Da sich das Repositoryformat zwischen WMI-Versionen ändern kann, ermöglicht diese Eigenschaft zukünftigen WMI-Upgrades zu bestimmen, ob die Datenbank aktualisiert werden muss. Das Format lautet:

"1.00.183.0000"

Dabei ist die erste Ziffer die Hauptversion, die nächsten beiden Ziffern sind Nebenversionen, und die nächsten drei Ziffern sind die Buildnummer. Die übrigen Ziffern werden nicht verwendet.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Installationsverzeichnis.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ CIMOMIdentification-Klasse** wird von [**\_ \_ SystemClass abgeleitet,**](--systemclass.md)die über keine Eigenschaften verfügt.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird beschrieben, wie Cim-Objektmodellidentifikationsinformationen angezeigt werden. Es wurde aus dem Beispielverzeichnis unter Program \\ \\ Files Microsoft \\ SDKs Windows \\ \\ v7.0 \\ Samples \\ sysmgmt wmi scripting( Sysmgmt \\ wmi \\ scripting) entnommen.


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



Im folgenden Perl-Codebeispiel wird beschrieben, wie Cim-Objektmodellidentifikationsinformationen angezeigt werden. Es wurde aus dem Beispielverzeichnis unter Program \\ \\ Files Microsoft \\ SDKs Windows \\ \\ v7.0 \\ Samples \\ sysmgmt wmi scripting (Sysmgmt \\ wmi-Skripterstellung für Programme microsoft SDKs Windows v7.0-Beispiele) \\ entnommen.


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

