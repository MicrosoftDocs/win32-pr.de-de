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
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349939"
---
# <a name="__cimomidentification-class"></a>\_\_Cimumidentificlass

Die " **\_ \_ cimumidentifisystem** "-Klasse beschreibt die lokale Installation von WMI. Dies ist eine Singleton-Klasse. Es gibt nur eine Instanz. Die **\_ \_ cimumidentificlass** ist nur in den **\\ Standard** Namespaces **root** und Root verfügbar. Benutzer Fragen die-Instanz ab, um Informationen zur WMI-Installation zu erhalten.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **\_ \_ cimumidentifizierungsklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ cimumidentificlass** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Setupdatetime**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Installation. Diese Eigenschaft ist leer, nachdem das Betriebssystem zum ersten Mal installiert wurde.

Wenn das WMI-Repository gelöscht und dann erneut erstellt wurde, enthält diese Eigenschaft das Datum und die Uhrzeit der erneuten Erstellung des Repository.

</dd> <dt>

**Versioncurrentlyrunning**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Version des eigentlichen Bilds an, das den WMI-Dienst enthält, der das Common Information Model (CIM)-Repository erstellt hat. Da sich das Repository-Format zwischen den Versionen von WMI ändern kann, ermöglicht diese Eigenschaft zukünftigen WMI-Upgrades, zu bestimmen, ob die Datenbank aktualisiert werden muss. Das Format lautet:

"1.00.183.0000"

Wenn die erste Ziffer die Hauptversion ist, sind die nächsten zwei Ziffern neben Versionen, und die nächsten drei Ziffern sind die Buildnummer. Die verbleibenden Ziffern werden nicht verwendet.

</dd> <dt>

**Versionusedtykreatedb**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Version des eigentlichen Bilds an, das den WMI-Dienst enthält, der das CIM-Repository erstellt hat. Da sich das Repository-Format zwischen den Versionen von WMI ändern kann, ermöglicht diese Eigenschaft zukünftigen WMI-Upgrades, zu bestimmen, ob die Datenbank aktualisiert werden muss. Das Format lautet:

"1.00.183.0000"

Wenn die erste Ziffer die Hauptversion ist, sind die nächsten zwei Ziffern neben Versionen, und die nächsten drei Ziffern sind die Buildnummer. Die verbleibenden Ziffern werden nicht verwendet.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Installationsverzeichnis.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ cimumidentificlass** wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet, die keine Eigenschaften hat.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird beschrieben, wie die Identifikationsinformationen des CIM-Objektmodells angezeigt und aus dem Beispiel Verzeichnis unter \\ \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ sysmgmt \\ WMI \\ Scripting verwendet werden.


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



Im folgenden perl-Codebeispiel wird beschrieben, wie die Identifikationsinformationen des CIM-Objektmodells angezeigt und aus dem Beispiel Verzeichnis unter \\ \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ sysmgmt \\ WMI \\ Scripting verwendet werden.


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_System Class**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

