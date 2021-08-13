---
description: Win32 \_ DCOMApplicationSetting&\# 8194; Die WMI-Klasse stellt die Einstellungen einer DCOM-Anwendung dar.
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
ms.openlocfilehash: 3b52ace8ea72d78585ac0df858df1fc807fbc65ca74ace92208d2e9fc5c76861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417731"
---
# <a name="win32_dcomapplicationsetting-class"></a>Win32 \_ DCOMApplicationSetting-Klasse

Die **WMI-Klasse Win32 \_ DCOMApplicationSetting** stellt die Einstellungen einer DCOM-Anwendung dar. [](/windows/desktop/WmiSdk/retrieving-a-class) Sie enthält DCOM-Konfigurationsoptionen, die dem **AppID-Schlüssel** in der Registrierung zugeordnet sind. Diese Optionen sind für die Komponenten gültig, die logisch unter der angegebenen Anwendungsklasse gruppiert sind.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **Win32 \_ DCOMApplicationSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ DCOMApplicationSetting-Klasse** verfügt über diese Methoden.



| Methode                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAccessSecurityDescriptor**](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Ruft den Sicherheitsdeskriptor ab, der steuert, wer auf eine DCOM-Anwendung zugreifen darf.<br/>                                                                                                                              |
| [**GetConfigurationSecurityDescriptor**](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Ruft den Sicherheitsdeskriptor ab, der steuert, wer eine DCOM-Anwendung konfigurieren darf.<br/>                                                                                                                           |
| [**GetLaunchSecurityDescriptor**](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | Ruft den Sicherheitsdeskriptor ab, der steuert, wer eine DCOM-Anwendung starten darf.<br/>                                                                                                                              |
| [**SetAccessSecurityDescriptor**](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Aktualisiert die Zugriffssicherheitsbeschreibung der DCOM-Anwendung mit einem neuen Sicherheitsdeskriptor, der von einer Instanz der [**Win32 \_ SecurityDescriptor-Klasse definiert**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) wird.<br/>        |
| [**SetConfigurationSecurityDescriptor**](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Aktualisiert die Konfigurationssicherheitsbeschreibung der DCOM-Anwendung mit einem neuen Sicherheitsdeskriptor, der von einer Instanz der [**Win32 \_ SecurityDescriptor-Klasse definiert**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) wird.<br/> |
| [**SetLaunchSecurityDescriptor**](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Aktualisiert die Startsicherheitsbeschreibung der DCOM-Anwendung mit einem neuen Sicherheitsdeskriptor, der von einer Instanz der [**Win32 \_ SecurityDescriptor-Klasse definiert**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) wird.<br/>        |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ DCOMApplicationSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} Default \[ \] ")
</dt> </dl>

GuiD (Globally Unique Identifier) für diese DCOM-Anwendung.

</dd> <dt>

**Authenticationlevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")
</dt> </dl>

Minimale Clientauthentifizierungsebene, die für diesen COM-Server erforderlich ist. Bei **NULL** werden die Standardwerte verwendet.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (1)


</dt> <dd>

Keine (keine Authentifizierung erfolgt)

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Verbinden** (2)


</dt> <dd>

Verbinden (die Authentifizierung erfolgt nur, wenn der Client eine Beziehung mit der Anwendung ein richtet)

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>**Aufruf** (3)


</dt> <dd>

Aufruf (die Authentifizierung wird nur zu Beginn jedes Aufrufs ausgeführt, wenn die Anwendung die Anforderung empfängt)

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Paket** (4)


</dt> <dd>

Paket (Authentifizierung wird für alle vom Client empfangenen Daten ausgeführt)

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)


</dt> <dd>

PacketIntegrity (alle zwischen dem Client und der Anwendung übertragenen Daten werden authentifiziert und überprüft)

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)


</dt> <dd>

PacketPrivacy (die Eigenschaften der anderen Authentifizierungsebenen werden verwendet, und alle Daten werden verschlüsselt)

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**CustomSurrogate**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")
</dt> </dl>

Name des benutzerdefinierten Ersatzzeichens, in dem die Prozess-DCOM-Anwendung aktiviert ist. Wenn dieser Wert **NULL ist** und **der UseSurrogate-Schlüssel** **TRUE** ist, stellt das System einen Ersatzprozess zur Anwendung.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**EnableAtStorageActivation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] ")
</dt> </dl>

Die DCOM-Anwendung ruft den gespeicherten Zustand der Anwendung ab oder beginnt mit dem Zustand, in dem die Anwendung zuerst initialisiert wird.

</dd> <dt>

**LocalService**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")
</dt> </dl>

Name für die von der DCOM-Anwendung bereitgestellten Dienste.

</dd> <dt>

**RemoteServerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] ")
</dt> </dl>

Name des Remoteservers, auf dem die Anwendung aktiviert ist.

</dd> <dt>

**RunAsUser**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ RunAs \] ")
</dt> </dl>

Ein bestimmtes Benutzerkonto, unter dem die Anwendung bei der Aktivierung ausgeführt werden soll.

</dd> <dt>

**ServiceParameters**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ServiceParameters \] ")
</dt> </dl>

Befehlszeilenparameter, die an die DCOM-Anwendung übergeben werden. Dies ist nur gültig, wenn die Anwendung als Windows Dienst geschrieben wird.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Bezeichner, durch den das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**UseSurrogate**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")
</dt> </dl>

Die DCOM-Anwendung kann mithilfe einer ausführbaren Ersatzdatei als Out-of-Process-Server aktiviert werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ DCOMApplicationSetting-Klasse** wird von [**Win32 \_ COMSetting**](win32-comsetting.md)abgeleitet.

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

[**Win32 \_ COMSetting**](win32-comsetting.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Berechtigungskonstanten**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI-Sicherheitsbeschreibungsobjekte](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Ändern der Zugriffssicherheit für sicherungsfähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

