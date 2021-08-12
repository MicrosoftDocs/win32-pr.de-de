---
description: Win32 \_ QuickFixEngineering&\# 8194; Die WMI-Klasse stellt ein kleines systemweites Update dar, das häufig als Quick Fix Engineering-Update (QFE) bezeichnet wird und auf das aktuelle Betriebssystem angewendet wird.
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Win32_QuickFixEngineering-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15110b5801555947eed434b8148aec3cc753f6eec359f32b96cd67a5b2649f31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675012"
---
# <a name="win32_quickfixengineering-class"></a>Win32 \_ QuickFixEngineering-Klasse

Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) **\_ "Win32 QuickFixEngineering"** stellt ein kleines systemweites Update dar, das häufig als Quick Fix Engineering-Update (QFE) bezeichnet wird und auf das aktuelle Betriebssystem angewendet wird. Diese Klasse gibt nur die Updates zurück, die von der komponentenbasierten Wartung (Component Based Servicing, CBS) bereitgestellt werden. Diese Updates sind nicht in der Registrierung aufgeführt. Updates, die vom Microsoft Windows Installer (MSI) oder dem Windows Updatestandort ( ) bereitgestellt werden, werden von [https://update.microsoft.com](https://update.microsoft.com/) **Win32 \_ QuickFixEngineering nicht zurückgegeben.**

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a>Member

Die **Win32 \_ QuickFixEngineering-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ QuickFixEngineering-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Taste,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Lokaler Name des Computersystems. Der Wert für diese Eigenschaft stammt aus der [**CIM \_ ComputerSystem-Klasse.**](cim-computersystem.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Eine Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**FixComments**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Zusätzliche Kommentare, die sich auf das Update beziehen.

</dd> <dt>

**HotFixID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Eindeutiger Bezeichner, der einem bestimmten Update zugeordnet ist.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Installation date")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**InstalledBy**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Person, die das Update installiert hat. Wenn dieser Wert unbekannt ist, ist die Eigenschaft leer.

</dd> <dt>

**InstalledOn**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Datum, an dem das Update installiert wurde. Wenn dieser Wert unbekannt ist, ist die Eigenschaft leer.

> [!Note]  
> Diese Eigenschaft kann unterschiedliche Formate verwenden, je nachdem, wann QuickFix installiert wurde. Die meisten Systeme verwenden ein Standarddatumsformat, z. B. "23-10-2013". Einige Systeme geben jedoch möglicherweise einen hexadezimalen 64-Bit-Wert im Win32 [**FILETIME-Format**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) zurück.

 

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Bezeichnung, unter der das Objekt bekannt ist. Bei Unterklassen kann diese Eigenschaft überschrieben werden, um eine Schlüsseleigenschaft zu sein.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**ServicePackInEffect**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Das Service Pack ist wirksam, als das Update angewendet wurde. Wenn kein Service Pack angewendet wurde, übernimmt die -Eigenschaft den Wert SP0. Wenn nicht bestimmt werden kann, welches Service Pack in Kraft war, ist diese Eigenschaft **NULL.**

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des Objekts angibt. Betriebsstatus und nicht betriebsbereiter Status können definiert werden. Der Betriebsstatus kann "OK", "Heruntergestuft" und "Fehler vor dem Ausfall" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. B. eine SMART-fähige Festplatte).

Nicht betriebsbereite Status können "Error", "Starting", "Stopping" und "Service" sein. "Dienst" kann während der Spiegelung des Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Heruntergestuft** ("Heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Wird** gestartet ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Wird beendet** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Mannslast** ("1000")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorenes Komma** ("Verlorenes Komma")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ QuickFixEngineering-Klasse** wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.

Da Updates an zwei Stellen gespeichert werden, kann eine Enumeration dieser Klasse zu Duplikaten führen.

Eine Hotfixlösung ist ein temporärer Betriebssystempatch, der von der Gruppe schnelle Problembehebung Engineering bei Microsoft erstellt wurde. Wie Service Packs stellen Hotfixes Änderungen dar, die an einer Version von Windows vorgenommen wurden, nachdem das Betriebssystem veröffentlicht wurde.

Im Gegensatz zu Service Packs sind Hotfixes nicht für die Installation auf allen Computern vorgesehen. Stattdessen werden sie entwickelt, um sehr spezifische Probleme zu beheben, häufig für bestimmte Computerkonfigurationen.

Darüber hinaus stellen Hotfixes unabhängige Installationen dar, die nicht von anderen freigegebenen Hotfixes abhängen. Beispielsweise würde eine hypothetische Hotfix 4 nicht die Fehlerbehebungen und Funktionen enthalten, die in den Hotfixes 1, 2 und 3 enthalten sind. In den meisten Fällen ist es auch nicht erforderlich, die Hotfixes 1, 2 und 3 vor der Installation von Hotfix 4 zu installieren. Dies macht die Enumeration einzelner Hotfixes zu einer wichtigen administrativen Aufgabe: Um die genaue Konfiguration eines Computers zu kennen, müssen Sie nicht nur wissen, welche Service Packs installiert wurden, sondern auch, welche einzelnen Hotfixes installiert wurden.

Mit der **Win32 \_ QuickFixEngineering-Klasse** können Sie alle Hotfixes aufzählen, die auf einem Computer installiert wurden.

## <a name="examples"></a>Beispiele

Im PowerShell-Beispiel [Get Installed Programs (Installierte Programme](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) abrufen) wird eine vollständige Liste der installierten Programme zurückgegeben.

Im folgenden VBScript-Beispiel werden die installierten Hotfixes auf einem Computer aufzählt.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[WMI-Aufgaben: Betriebssysteme](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 
