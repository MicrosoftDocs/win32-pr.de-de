---
description: Stellt eine Umgebungs- oder Systemumgebungseinstellung auf einem Windows Computersystem dar.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Win32_Environment-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d7237d83c298916045b4bd0443eadc3048c94dc7ad028a1bd7bfa993c4ce764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391750"
---
# <a name="win32_environment-class"></a>Win32 \_ Environment-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **"Win32-Umgebung" \_** stellt eine Umgebungs- oder Systemumgebungseinstellung auf einem Windows Computersystem dar. Beim Abfragen dieser Klasse werden Umgebungsvariablen zurückgegeben, die sich in folgendem Beispiel befinden:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Sessionmanager** \\ **Environment**

und

**HKEY \_** \\ **< BENUTZERbenutzerumgebung >** \\ 

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a>Member

Die **Win32 \_ Environment-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ Win32-Umgebungsklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Beschreibung")
</dt> </dl>

Eine Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installationsdatum")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager \\ \\ \\ \\ Environment")
</dt> </dl>

Zeichenfolge, die den Namen einer Windows-basierten Umgebungsvariablen angibt. Durch Angeben des Namens einer variablen , die noch nicht vorhanden ist, erstellt eine Anwendung eine neue Umgebungsvariable.

Beispiel: "Path"

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Zeichenfolge, die den aktuellen Status des Objekts angibt. Der Betriebsstatus und der nicht betriebsbereite Status können definiert werden. Der Betriebsstatus kann "OK", "Heruntergestuft" und "Fehler vor dem Fehler" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. B. ein SMART-fähiges Festplattenlaufwerk).

Nicht betriebsbereite Status können "Error", "Starting", "Stopping" und "Service" sein. "Dienst" kann während der Datenträgerspiegelung, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Administrativen Arbeiten angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

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

**Wird gestartet** ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Beenden** ("Wird beendet")


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

</dd> <dt>

**SystemVariable**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager \\ \\ \\ \\ Environment")
</dt> </dl>

Gibt an, ob die Variable eine Systemvariable ist. Eine Systemvariable wird vom Betriebssystem festgelegt und ist unabhängig von den Einstellungen der Benutzerumgebung.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager \\ \\ \\ \\ Environment")
</dt> </dl>

Name des Besitzers der Umgebungseinstellung. Sie ist <SYSTEM> für Einstellungen, die für das Windows-basierte System spezifisch sind (im Gegensatz zu einem bestimmten Benutzer), und <DEFAULT> für Standardbenutzereinstellungen auf festgelegt.

Beispiel: "JSmith"

</dd> <dt>

**VariableValue**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager \\ \\ \\ \\ Environment")
</dt> </dl>

Platzhaltervariable einer Windows-basierten Umgebungsvariablen. Informationen wie das Dateisystemverzeichnis können sich von Computer zu Computer ändern. Das Betriebssystem ersetzt Platzhalter für diese.

Beispiel: "%SystemRoot%"

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ Win32-Umgebungsklasse** wird von [**CIM \_ SystemResource**](cim-systemresource.md)abgeleitet. Sie können diese Klasse verwenden, um die Pfade von speziellen Ordnern zu suchen, z. B. den Ordner System oder Programme auf einem Remotecomputer. Beispiele: windir, systemroot, programfiles und userprofile. **Win32 \_ Die Umgebung** gibt im Grunde zurück, was in zu finden ist:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Sessionmanager** \\ **Environment**

und

**HKEY \_** \\ **< BENUTZERbenutzerumgebung >** \\ 

Der aufrufende Prozess, der diese Klasse verwendet, muss über die **SE \_ RESTORE \_ NAME-Berechtigung** auf dem Computer verfügen, auf dem sich die Registrierung befindet. Wenn Sie diese Klasse beispielsweise auf dem lokalen Computer aufzählen, muss das Konto, unter dem die Anwendung ausgeführt wird, über diese Berechtigung verfügen. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge.](/windows/desktop/WmiSdk/executing-privileged-operations)

## <a name="examples"></a>Beispiele

Das [Beispiel Zum Auflisten von Umgebungsvariablen](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) auf einem Computer Perl verwendet WMI, um Informationen zu allen Umgebungsvariablen auf einem Computer zurück zu geben.

Im folgenden VBScript-Codebeispiel werden die Umgebungsvariablen auf dem lokalen Computer aufzählt.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



Im folgenden VBScript-Codebeispiel wird eine Umgebungsvariable mit dem Namen BUILD \_ TYPE in eine Werteingabe des Benutzers geändert. Das Skript geht davon aus, dass die BUILD \_ TYPE-Variable bereits vorhanden ist. Wenn es nicht vorhanden ist, wird das Skript beendet. Der Eingabewert wird überprüft: Er muss entweder "Build1", "Build2" oder "Build3" sein, und es wird kein anderer Wert akzeptiert. Die [VBScript-UCase-Funktion](https://msdn.microsoft.com/library/aa902519.aspx) berücksichtigt die Groß-/Kleinschreibung der Eingabe nicht. Wenn es sich bei dem Typ nicht um einen der drei zulässigen Werte handelt, wird das Skript beendet.


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SystemResource**](cim-systemresource.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

