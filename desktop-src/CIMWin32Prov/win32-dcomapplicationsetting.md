---
description: Win32 \_ dcomapplicationsetting&\# 8194; Die WMI-Klasse stellt die Einstellungen einer DCOM-Anwendung dar.
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Win32_DCOMApplicationSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343019"
---
# <a name="win32_dcomapplicationsetting-class"></a>Win32 \_ dcomapplicationsetting-Klasse

Die **Win32 \_ dcomapplicationsetting** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Einstellungen einer DCOM-Anwendung dar. Sie enthält DCOM-Konfigurationsoptionen, die mit dem **AppID** -Schlüssel in der Registrierung verknüpft sind. Diese Optionen sind für die Komponenten gültig, die logisch unter der angegebenen Anwendungsklasse gruppiert sind.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a>Member

Die **Win32 \_ dcomapplicationsetting** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ dcomapplicationsetting** -Klasse verfügt über diese Methoden.



| Methode                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getaccesssecuritydescriptor**](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Ruft die Sicherheits Beschreibung ab, die steuert, wer auf eine DCOM-Anwendung zugreifen darf.<br/>                                                                                                                              |
| [**Getconfigurationsecuritydescriptor**](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Ruft die Sicherheits Beschreibung ab, die steuert, wer eine DCOM-Anwendung konfigurieren darf.<br/>                                                                                                                           |
| [**Getlaunchsecuritydescriptor**](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | Ruft die Sicherheits Beschreibung ab, die steuert, wer eine DCOM-Anwendung starten darf.<br/>                                                                                                                              |
| [**Setaccesssecuritydescriptor**](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Aktualisiert den Zugriffs Sicherheits Deskriptor der DCOM-Anwendung mit einer neuen Sicherheits Beschreibung, die durch eine Instanz der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse definiert wird.<br/>        |
| [**Setconfigurationsecuritydescriptor**](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Aktualisiert die Konfigurations Sicherheits Beschreibung der DCOM-Anwendung mit einer neuen Sicherheits Beschreibung, die durch eine Instanz der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse definiert wird.<br/> |
| [**Setlaunchsecuritydescriptor**](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Aktualisiert die Start Sicherheits Beschreibung der DCOM-Anwendung mit einer neuen Sicherheits Beschreibung, die durch eine Instanz der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse definiert wird.<br/>        |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ dcomapplicationsetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ Default \] ")
</dt> </dl>

GUID (Global Unique Identifier) für diese DCOM-Anwendung.

</dd> <dt>

**AuthenticationLevel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")
</dt> </dl>

Mindestens erforderliche Client Authentifizierungs Ebene für diesen com-Server. Wenn der Wert **null** ist, werden die Standardwerte verwendet.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (1)


</dt> <dd>

None (keine Authentifizierung erfolgt)

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Verbinden** (2)


</dt> <dd>

Connect (die Authentifizierung wird nur ausgeführt, wenn der Client eine Beziehung mit der Anwendung herstellt)

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>**Rückruf** (3)


</dt> <dd>

Wird aufgerufen (die Authentifizierung wird nur zu Beginn jedes Aufrufes ausgeführt, wenn die Anwendung die Anforderung empfängt)

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Paket** (4)


</dt> <dd>

Paket (Authentifizierung wird für alle vom Client empfangenen Daten ausgeführt)

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**Packetintegrity** (5)


</dt> <dd>

Packetintegrity (alle Daten, die zwischen dem Client und der Anwendung übertragen werden, werden authentifiziert und überprüft.)

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)


</dt> <dd>

PacketPrivacy (die Eigenschaften der anderen Authentifizierungs Ebenen werden verwendet, und alle Daten werden verschlüsselt.)

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**Customersatz**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ dllersatz \] ")
</dt> </dl>

Der Name des benutzerdefinierten Ersatz Zeichens, in dem die Prozess interne DCOM-Anwendung aktiviert ist. Wenn dieser Wert **null** ist und der **UseSurrogate** -Schlüssel auf **true** festgelegt ist, stellt das System einen Ersatzprozess bereit.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**EnableAtStorageActivation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ activateatstorage \] ")
</dt> </dl>

Die DCOM-Anwendung ruft den gespeicherten Zustand der Anwendung ab oder beginnt mit dem Zustand, in dem die Anwendung zuerst initialisiert wird.

</dd> <dt>

**LocalService**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")
</dt> </dl>

Der Name der Dienste, die von der DCOM-Anwendung bereitgestellt werden.

</dd> <dt>

**RemoteServerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ Remoteservername \] ")
</dt> </dl>

Der Name des Remote Servers, auf dem die Anwendung aktiviert ist.

</dd> <dt>

**RunAsUser**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ runas \] ")
</dt> </dl>

Bestimmtes Benutzerkonto, unter dem die Anwendung bei Aktivierung ausgeführt werden soll.

</dd> <dt>

**Service Parameters**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ Service Parameters \] ")
</dt> </dl>

Befehlszeilenparameter, die an die DCOM-Anwendung übermittelt werden. Dies ist nur gültig, wenn die Anwendung als Windows-basierter Dienst geschrieben wird.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**UseSurrogate**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ dllersatz \] ")
</dt> </dl>

Die DCOM-Anwendung kann als Prozess interner Server aktiviert werden, indem eine ausführbare Datei für Ersatz Zeichen verwendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ dcomapplicationsetting** -Klasse wird von [**Win32 \_ comsetting**](win32-comsetting.md)abgeleitet.

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

[**Win32- \_ comsetting**](win32-comsetting.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI-sicherheitsdeskriptorobjekte](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

