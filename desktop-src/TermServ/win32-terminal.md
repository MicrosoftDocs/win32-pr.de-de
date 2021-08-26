---
title: Win32_Terminal-Klasse
description: Stellt ein Terminal dar.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Win32_Terminal-Remotedesktopdienste
- Win32_Terminal klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e43f3998e1b8f9e7d252a8a4c949d7d083c763a8759d7c9df6aa60c21618e217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867960"
---
# <a name="win32_terminal-class"></a>Win32 \_ Terminal-Klasse

Die **WMI-Klasse \_ des Win32-Terminals** stellt ein Terminal dar.

Die folgende Syntax wird von MOF-Code vereinfacht und enthält alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu Methoden finden Sie in der Tabelle der Methoden weiter unten in diesem Thema.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a>Member

Die **Win32 \_ Terminal-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ Terminal-Klasse** verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Erstellen**](create-win32-terminal.md) | Erstellt ein Terminal mit Standardeinstellungen, die mithilfe der Eigenschaften und Methoden der [**Win32 \_ TerminalSetting-Klassen angepasst werden**](win32-terminalsetting.md) können.<br/> |
| [**Löschen**](delete-win32-terminal.md) | Löscht das angegebene Terminal.<br/>                                                                                                                                              |
| [**Aktivieren**](win32-terminal-enable.md) | Deaktiviert oder aktiviert das Terminal.<br/>                                                                                                                                            |
| [**Umbenennen**](win32-terminal-rename.md) | Benennt das Terminal um.<br/>                                                                                                                                                        |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ Terminal-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilenbasierte Zeichenfolge) des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**fEnableTerminal**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das angegebene Terminal deaktiviert oder aktiviert ist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Das Terminal ist deaktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Das Terminal ist aktiviert.

</dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Ein fehlender Wert gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**LoggedOnUsers**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der angemeldeten Sitzungen für das Terminal.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene betriebsbereite und nicht betriebsbereite Status definiert werden. Folgende Betriebsstatus sind möglich: "OK", "Heruntergestuft" und "Fehler vor dem Ausfall" (ein Element, z. B. eine SMART-fähige Festplatte, funktioniert möglicherweise ordnungsgemäß, aber es wird in naher Zukunft ein Fehler vorhergesagt). Nicht operative Status sind: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während der Spiegelung eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Fehler")


</dt> <dd></dd> <dt>



 ("Heruntergestuft")


</dt> <dd></dd> <dt>



 ("Unbekannt")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Wird gestartet")


</dt> <dd></dd> <dt>



 ("Wird beendet")


</dt> <dd></dd> <dt>



 ("Dienst")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der eindeutige Name, der die Instanz des Terminals identifiziert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**Win32 \_ Terminal** ist [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) als **Element-Eigenschaft** der [**Win32 \_ TerminalTerminalSetting-Zuordnung**](win32-terminalterminalsetting.md) zugeordnet.

Die folgenden Klassen sind Unterklassen der **Win32 \_ Terminal-Klasse:** [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md), [**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md), [**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32 \_ TSClientSetting**](win32-tsclientsetting.md), [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)und [**Win32 \_ TSAccount**](win32-tsaccount.md).

Beachten Sie, dass Winstations, die der Konsolensitzung zugeordnet sind, nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen können. Wenn versucht wird, dies zu tun, indem "Console" als Wert der **TerminalName-Eigenschaft** angegeben wird, geben Methoden dieses Objekts **WBEM \_ E NOT SUPPORTED \_ \_ zurück.** Dieser Fehlercode wird auch zurückgegeben, wenn eine Fensterstation versucht, Methoden dieses Objekts auf aufruft, um die Sicherheitseigenschaften der Konten LocalSystem, LocalService oder NetworkService hinzuzufügen oder zu ändern.

Um eine Verbindung mit dem \\ \\ CIMV2 TerminalServices-Stammnamespace herzustellen, muss \\ die Authentifizierungsebene den Paketschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Für Visual Basic- und Skriptaufrufe ist dies eine Authentifizierungsebene von **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert 6. Das folgende Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> <dt>

[**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)
</dt> </dl>

 

