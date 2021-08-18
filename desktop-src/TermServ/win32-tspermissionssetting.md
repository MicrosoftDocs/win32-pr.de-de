---
title: Win32_TSPermissionsSetting-Klasse
description: Enthält eine Methode zum Hinzufügen neuer Konten zum Terminal und eine Methode zum Wiederherstellen der Standardberechtigungen für ein Terminal.
ms.assetid: ebc6e96a-668e-44aa-b589-c3e476fb3029
ms.tgt_platform: multiple
keywords:
- Win32_TSPermissionsSetting-Remotedesktopdienste
- Win32_TSPermissionsSetting klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting.Caption
- Win32_TSPermissionsSetting.Description
- Win32_TSPermissionsSetting.InstallDate
- Win32_TSPermissionsSetting.Name
- Win32_TSPermissionsSetting.Status
- Win32_TSPermissionsSetting.TerminalName
- Win32_TSPermissionsSetting.DenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.PolicySourceDenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.StringSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a853a2630224b108b9003764dd9529f99234774297fb39b3bfe6342c6ecfb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137673"
---
# <a name="win32_tspermissionssetting-class"></a>Win32 \_ TSPermissionsSetting-Klasse

Die WMI-Klasse **Win32 \_ TSPermissionsSetting** enthält eine Methode zum Hinzufügen neuer Konten zum Terminal und eine Methode zum Wiederherstellen der Standardberechtigungen für ein Terminal.

Die folgende Syntax wird von MOF-Code vereinfacht und enthält alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu Methoden finden Sie in der Tabelle der Methoden weiter unten in diesem Thema.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_TSPERMISSIONSSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSPermissionsSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   DenyAdminPermissionForCustomization;
  uint32   PolicySourceDenyAdminPermissionForCustomization;
  string   StringSecurityDescriptor;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSPermissionsSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TSPermissionsSetting-Klasse** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                                                                                    |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**AddAccount**](win32-tspermissionssetting-addaccount.md)           | Fügt dem Terminal ein Konto mit dem Berechtigungssatz hinzu, der im Wert des *PermissionPreSet-Parameters angegeben* ist.<br/> |
| [**RestoreDefaults**](win32-tspermissionssetting-restoredefaults.md) | Stellt die Standardwerte für den Berechtigungssatz für das Terminal wieder auf.<br/>                                                        |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSPermissionsSetting-Klasse** verfügt über diese Eigenschaften.

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

**DenyAdminPermissionForCustomization**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der lokale Administrator über die Berechtigung zum Anpassen verfügt.

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

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**PolicySourceDenyAdminPermissionForCustomization**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, **ob die MinEncryptionLevel-Eigenschaft** vom Server, der Gruppenrichtlinie oder standardmäßig konfiguriert wird.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie

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

**StringSecurityDescriptor**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sicherheitsdeskriptor, der dem Terminal im binären Bytearrayformat zugeordnet ist.

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Terminals.

Diese Eigenschaft wird von [**Win32 \_ TerminalSetting geerbt.**](win32-terminalsetting.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

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
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> </dl>

 

