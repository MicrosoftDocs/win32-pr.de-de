---
title: Win32_TSLogonSetting-Klasse
description: Definiert Konfigurationseinstellungen für die Win32 \_ Terminal-Klasse im Zusammenhang mit der Clientanmeldung.
ms.assetid: a2ccb419-da1a-44d1-8a7a-4d0266fc1be8
ms.tgt_platform: multiple
keywords:
- Win32_TSLogonSetting-Klasse Remotedesktopdienste
- Win32_TSLogonSetting-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting
- Win32_TSLogonSetting.Caption
- Win32_TSLogonSetting.Description
- Win32_TSLogonSetting.InstallDate
- Win32_TSLogonSetting.Name
- Win32_TSLogonSetting.Status
- Win32_TSLogonSetting.TerminalName
- Win32_TSLogonSetting.ClientLogonInfoPolicy
- Win32_TSLogonSetting.Domain
- Win32_TSLogonSetting.Password
- Win32_TSLogonSetting.PolicySourceDomain
- Win32_TSLogonSetting.PolicySourcePromptForPassword
- Win32_TSLogonSetting.PolicySourceUserName
- Win32_TSLogonSetting.PromptForPassword
- Win32_TSLogonSetting.UserName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a9d4fd3b3d8aebf60fae1e4f96590b26639dd380fbdb1de6638908299ff59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058318"
---
# <a name="win32_tslogonsetting-class"></a>Win32 \_ TSLogonSetting-Klasse

Die WMI-Klasse **Win32 \_ TSLogonSetting** definiert Konfigurationseinstellungen für die [**Win32 \_ Terminal-Klasse**](win32-terminal.md) im Zusammenhang mit der Clientanmeldung.

Die folgende Syntax wird aus MOF-Code vereinfacht und enthält alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu Methoden finden Sie in der Tabelle der Methoden weiter unten in diesem Thema.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_TSLOGONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSLogonSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientLogonInfoPolicy;
  string   Domain;
  string   Password;
  uint32   PolicySourceDomain;
  uint32   PolicySourcePromptForPassword;
  uint32   PolicySourceUserName;
  uint32   PromptForPassword;
  string   UserName;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSLogonSetting-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSLogonSetting-Klasse** verfügt über diese Methoden.



| Methode                                                                    | Beschreibung                                                                    |
|:--------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ExplicitLogon**](win32-tslogonsetting-explicitlogon.md)               | Legt die Anmeldeinformationen für Benutzername, Kennwort und Domänenauthentifizierung fest.<br/> |
| [**SetPromptForPassword**](win32-tslogonsetting-setpromptforpassword.md) | Legt die **PromptForPassword-Eigenschaft** fest.<br/>                            |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSLogonSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilige Zeichenfolge) des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ClientLogonInfoPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Richtlinie, die der Server zum Bestimmen der Verbindungseinstellungen verwendet.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (0)


</dt> <dd>

Einzelne Benutzerverbindungseinstellungen sind wirksam.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serverüberschreibung** (1)


</dt> <dd>

Einzelne Benutzerverbindungseinstellungen werden vom Server überschrieben.

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Domain**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anmeldeinformationen für die Domänenanmeldung des Benutzers. Dies ist die Domäne, in der sich der Computer des Benutzers befindet. Diese Eigenschaft darf nicht länger als 17 Zeichen sein.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Kennwort**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anmeldeinformationen für die Kennwortanmeldung des Benutzers. Diese Eigenschaft darf nicht länger als 14 Zeichen sein. Es wird empfohlen, die Sicherheitsstufe auf Paketdatenschutz (wbemAuthenticationLevelPktPrivacy = 6) festzulegen, wenn Sie diese Eigenschaft abfragen. Dies liegt daran, dass das Kennwort ohne diese Sicherheitsstufe nicht verschlüsselt wird. Weitere Informationen zum Festlegen von Sicherheitsstufen finden Sie unter Setting Client Application Process Security (Festlegen der Sicherheit des [Clientanwendungsprozesses)](/windows/desktop/WmiSdk/setting-client-application-process-security) in der WMI SDK-Dokumentation.

</dd> <dt>

**PolicySourceDomain**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **Domäneneigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourcePromptForPassword**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **PromptForPassword-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PolicySourceUserName**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **UserName-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

</dd> <dt>

2
</dt> <dd>

Standard

</dd> </dl>

</dd> <dt>

**PromptForPassword**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Benutzer bei der Anmeldung beim Server immer zur Eingabe eines Kennworts aufgefordert wird.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Der Benutzer wird nicht zur Eingabe eines Kennworts aufgefordert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Der Benutzer wird zur Eingabe eines Kennworts aufgefordert.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, sagt aber einen Fehler in naher Zukunft vorher). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während des Spiegelungsresilverings eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Verwaltungsaufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

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
</dt> </dl>

Der Name des Terminals.

Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anmeldeinformationen für den Benutzernamen des Benutzers. Diese Eigenschaft darf nicht länger als 20 Zeichen sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass winstations, die der Konsolensitzung zugeordnet sind, nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen kann. Wenn dies versucht wird, indem "Console" als Wert der TerminalName-Eigenschaft angegeben wird, geben Methoden dieses Objekts **WBEM \_ E NOT SUPPORTED \_ \_ zurück.** Dieser Fehlercode wird zurückgegeben, wenn eine Fensterstation versucht, Methoden dieses Objekts aufzurufen, um die Sicherheitseigenschaften der Konten LocalSystem, LocalService oder NetworkService hinzuzufügen oder zu ändern.

Um eine Verbindung mit dem \\ \\ CIMV2 \\ TerminalServices-Stammnamespace herzustellen, muss die Authentifizierungsebene Paketdatenschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Bei Visual Basic- und Skriptaufrufen ist dies eine Authentifizierungsebene von **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert 6. Das folgende Beispiel Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_Win32-Terminal**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> </dl>

 

