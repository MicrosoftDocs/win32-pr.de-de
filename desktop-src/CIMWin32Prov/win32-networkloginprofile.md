---
description: Das Win32- \_ networkloginprofile-&\# 8194; Die WMI-Klasse stellt die Netzwerk Anmelde Informationen eines bestimmten Benutzers auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Win32_NetworkLoginProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b138ce4bc92088896286f4a21a039b068e2206e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343005"
---
# <a name="win32_networkloginprofile-class"></a>Win32 \_ networkloginprofile-Klasse

Die **Win32 \_ networkloginprofile**- [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt die Netzwerk Anmelde Informationen eines bestimmten Benutzers auf einem Computersystem dar, auf dem Windows ausgeführt wird. Dies umfasst u. a. den Kenn Wort Status, Zugriffsrechte, Datenträger Kontingente und Anmelde Verzeichnispfade.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a>Member

Die **Win32 \_ networkloginprofile** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ networkloginprofile** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccountExpires**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Acct \_ läuft ab")
</dt> </dl>

Das Konto läuft ab. Dieser Wert wird anhand der Anzahl der seit 00:00:00, dem 1. Januar 1970 verstrichenen Sekunden berechnet und im folgenden Format festgelegt: YYYYMMDDHHMMSS. mmmmmm sutc.

Beispiel: 20521201000230,000000 000

</dd> <dt>

**Authorizationflags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Authentifizierung \_ Flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")
</dt> </dl>

Ein Satz von Flags, die die Ressourcen angeben, die ein Benutzer für die Verwendung oder Änderung autorisiert ist.

<dt>

1 (0x1)
</dt> <dd>

Drucker

</dd> <dt>

2 (0x2)
</dt> <dd>

Kommunikation

</dd> <dt>

4 (0x4)
</dt> <dd>

Server

</dd> <dt>

8 (0x8)
</dt> <dd>

Konten

</dd> </dl>

</dd> <dt>

**BadPasswordCount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| nettuserenum")
</dt> </dl>

Gibt an, wie oft der Benutzer ein ungültiges Kennwort eingibt, wenn er sich bei einem Computersystem mit Windows anmeldet.

Beispiel: 0

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**CodePage**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ Codepage")
</dt> </dl>

Codepage für die Sprache des Benutzers. Eine Codepage ist der verwendete Zeichensatz.

</dd> <dt>

**Kommentar**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")
</dt> </dl>

Kommentar oder Beschreibung für dieses Anmelde Profil.

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Country \_ Code")
</dt> </dl>

Länder-/Regionscode für die Sprache des Benutzers.

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

**Flags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags"), [**Bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account deaktiviert", "Home dir erforderlich", "Lock out", "password not required", "paswword nicht ändern", "verschlüsseltes Testkennwort zulässig", "temporäres doppeltes Konto", "normales Konto", "Konto für Domänen übergreifende Vertrauensstellung" "," Arbeitsstations-Vertrauensstellungs Konto "," Server Vertrauensstellungs Konto "," Kennwort nicht ablaufen "," MNS-Anmelde Konto "," Smartcard erforderlich "," vertrauenswürdig für Delegierung "," nicht delegiert "," nur den Schlüssel verwenden "," keine vorab Autorisierung erforderlich "," Kennwort abgelaufen ")
</dt> </dl>

Die Eigenschaften, die für dieses Netzwerk Profil verfügbar sind.

Folgende Eigenschaften können festgelegt werden:

<dt>

1 (0x1)
</dt> <dd>

Skript

Ein ausgeführtes Anmelde Skript. Dieser Wert muss für den LAN-Manager 2,0 festgelegt werden.

</dd> <dt>

2 (0x2)
</dt> <dd>

Konto deaktiviert

Das Konto des Benutzers ist deaktiviert.

</dd> <dt>

8 (0x8)
</dt> <dd>

Basisverzeichnis erforderlich

Ein Basisverzeichnis ist erforderlich.

</dd> <dt>

16 (0x10)
</dt> <dd>

Sperrung

Das Konto ist zurzeit gesperrt. Für " [**nettusersetinfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo)" kann dieser Wert gelöscht werden, um ein zuvor gesperrtes Konto zu entsperren. Dieser Wert kann nicht verwendet werden, um ein zuvor entsperrtes Konto zu sperren.

</dd> <dt>

32 (0x20)
</dt> <dd>

Kennwort nicht erforderlich

Es ist kein Kennwort erforderlich.

</dd> <dt>

64 (0x40)
</dt> <dd>

Kenn Wort Änderung nicht möglich

Der Benutzer kann das Kennwort nicht ändern.

</dd> <dt>

128 (0x80)
</dt> <dd>

Verschlüsseltes Testkennwort zulässig

</dd> <dt>

256 (0x100)
</dt> <dd>

Temporäres doppeltes Konto

Ein Konto für Benutzer, deren primäres Konto sich in einer anderen Domäne befindet. Dieses Konto ermöglicht dem Benutzer den Zugriff auf diese Domäne, jedoch nicht auf eine Domäne, die dieser Domäne vertraut. Der Benutzer-Manager verweist auf diesen Kontotyp als lokales Benutzerkonto.

</dd> <dt>

512 (0x200)
</dt> <dd>

Normales Konto

Der Standard Kontotyp, der einen typischen Benutzer darstellt.

</dd> <dt>

2048 (0x800)
</dt> <dd>

Konto für Domänen übergreifende Vertrauensstellung

Eine Zulassungsberechtigung für ein Vertrauensstellungs Konto für eine Domäne, die anderen Domänen vertraut.

</dd> <dt>

4096 (0x1000)
</dt> <dd>

Arbeitsstations-Vertrauens Konto

Ein Computer Konto für eine Windows-Arbeitsstation oder einen Server, das Mitglied dieser Domäne ist.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Server Vertrauensstellungs Konto

Ein Computer Konto für einen Sicherungs Domänen Controller, der Mitglied dieser Domäne ist.

</dd> <dt>

65536 (0x10000)
</dt> <dd>

Kennwort nicht ablaufen

</dd> <dt>

131072 (0x20000)
</dt> <dd>

MNS-Anmelde Konto

MNS-Anmelde Kontotyp (Majority Node Set), der einen MNS-Benutzer darstellt.

</dd> <dt>

262144 (0x40000)
</dt> <dd>

Smartcard erforderlich

</dd> <dt>

524288 (0x80000)
</dt> <dd>

Vertrauenswürdige Delegierung

</dd> <dt>

1048576 (0x100000)
</dt> <dd>

Nicht delegiert

</dd> <dt>

2097152 (0x200.000)
</dt> <dd>

Nur des-Schlüssels verwenden

</dd> <dt>

4194304 (0x400000)
</dt> <dd>

Keine vorab Autorisierung erforderlich

</dd> <dt>

8388608 (0x800000)
</dt> <dd>

Kennwort abgelaufen

Gibt an, dass das Kennwort abgelaufen ist.

</dd> </dl>

Die folgenden Eigenschaften beschreiben den Kontotyp. Es kann nur ein Wert festgelegt werden:

-   \_normales \_ Konto
-   \_Konto für Temp Temp- \_ Duplizierung \_
-   Konto der Vertrauensstellung der \_ \_ Vertrauensstellung \_
-   \_ \_ \_ Konto Vertrauens Konto für den Server
-   Konto für die Vertrauensstellung der \_ Verbindungs Domäne \_ \_

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Full \_ Name")
</dt> </dl>

Der vollständige Name des Benutzers, der zum Netzwerk Anmelde Profil gehört. Diese Zeichenfolge kann leer sein, wenn der Benutzer keinen vollständigen Namen mit einem Benutzernamen zuordnen möchte.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir")
</dt> </dl>

Pfad zum Basisverzeichnis des Benutzers. Diese Zeichenfolge ist möglicherweise leer, wenn der Benutzer kein Basisverzeichnis angeben möchte.

Beispiel: " \\ homedir"

</dd> <dt>

**Homedirectorydrive**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir \_ Drive")
</dt> </dl>

Laufwerk Buchstabe, der dem Basisverzeichnis des Benutzers für die Anmeldung zugewiesen wird.

Beispiel: "C:"

</dd> <dt>

**Lastlogoff**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logoff")
</dt> </dl>

Der Benutzer hat das System zuletzt abgemeldet. Dieser Wert wird anhand der Anzahl der Sekunden berechnet, die seit 00:00:00, dem 1. Januar 1970, verstrichen sind. Der Wert " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " bedeutet, dass die letzte Abmelde Zeit unbekannt ist. Das Format dieses Werts lautet YYYYMMDDHHMMSS. mmmmmm sutc. Informationen zum übersetzen dieser Eigenschaft in die Ortszeit finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](../wmisdk/wmi-tasks--dates-and-times.md).

Beispiel: 19521201000230,000000 000

</dd> <dt>

**LastLogon**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Login")
</dt> </dl>

Der Benutzer hat sich zuletzt am System angemeldet. Dieser Wert wird anhand der Anzahl der Sekunden berechnet, die seit 00:00:00, dem 1. Januar 1970, verstrichen sind. Das Format dieses Werts lautet YYYYMMDDHHMMSS. mmmmmm sutc. Informationen zum übersetzen dieser Eigenschaft in die Ortszeit finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](../wmisdk/wmi-tasks--dates-and-times.md).

Beispiel: 19521201000230,000000 000

</dd> <dt>

**LogonHours**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (147), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Hours")
</dt> </dl>

Die Zeiten in der Woche, an denen sich der Benutzer anmelden kann. Jedes Bit stellt eine Zeiteinheit dar, die durch die **UnitsPerWeek** -Eigenschaft angegeben wird. Wenn beispielsweise die Zeiteinheit stündlich ist, ist das erste Bit (Bit 0, Wort 0) Sonntag, 0:00 bis 0:59, das zweite Bit (Bit 1, Wort 0) ist Sonntag, 1:00 bis 1:59 usw. Wenn dieser Member auf **null** festgelegt ist, gibt es keine Zeitbeschränkung. Die Uhrzeit wird auf GMT festgelegt und muss für andere Zeitzonen angepasst werden (z. b. GMT minus 8 Stunden für PST).

</dd> <dt>

**LOGONSERVER**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Server")
</dt> </dl>

Der Name des Servers, an den Anmelde Anforderungen gesendet werden. Server Namen sollten zwei umgekehrte Schrägstriche () vorangestellt werden \\ \\ . Ein Servername mit einem Sternchen ( \\ \\ \* ) gibt an, dass die Anmelde Anforderung von jedem beliebigen Anmelde Server verarbeitet werden kann. Eine NULL-Zeichenfolge gibt an, dass Anforderungen an den Domänen Controller gesendet werden.

Beispiel: " \\ \\ myserver"

</dd> <dt>

**MaximumStorage**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ Storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Maximale Menge an Speicherplatz, die dem Benutzer zur Verfügung steht. Wenn MaximumStorage auf User \_ maxstorage Unlimited festgelegt ist \_ , darf der Benutzer den gesamten verfügbaren Speicherplatz verwenden.

Beispiel: 10 Millionen

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Name")
</dt> </dl>

Benutzerkonto für eine bestimmte Domäne oder einen bestimmten Computer. Die Anzahl der Zeichen im Namen darf den Wert von UNLEN nicht überschreiten.

Beispiel: "somedomäne \\ JohnDoe"

</dd> <dt>

**Anzahloflogone**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ NUM \_ Logons")
</dt> </dl>

Gibt an, wie oft der Benutzer versucht hat, sich bei diesem Konto anzumelden. Der Wert 0xFFFFFFFF gibt an, dass der Wert unbekannt ist. Diese Eigenschaft wird auf jedem Sicherungs Domänen Controller (BDC) in der Domäne separat verwaltet. Um einen exakten Wert zu erhalten, sollte nur der größte Wert aus allen BDCs verwendet werden.

Beispiel: 4

</dd> <dt>

**Parameter**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ para")
</dt> </dl>

Leerraum, der für die Verwendung durch Anwendungen reserviert ist. Diese Zeichenfolge kann NULL sein, oder Sie kann eine beliebige Anzahl von Zeichen vor dem abschließenden NULL-Zeichen enthalten. Microsoft-Produkte verwenden dieses Mitglied zum Speichern von Benutzer Konfigurationsinformationen. Ändern Sie diese Informationen nicht, da dieser Wert für eine Anwendung spezifisch ist.

</dd> <dt>

**PasswordAge**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ Age")
</dt> </dl>

Die Zeitspanne, für die ein Kennwort wirksam ist. Dieser Wert wird von der Anzahl der Sekunden gemessen, die seit der letzten Änderung des Kennworts verstrichen sind.

Beispiel: 00001201000230,000000 000

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**Benutzer \_ modals \_ Info \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ Kennwort \_ Age")
</dt> </dl>

Datum und Uhrzeit des Ablaufs des Kennworts. Der Wert wird im folgenden Format festgelegt: YYYYMMDDHHMMSS. mmmmmm sutc

Beispiel: 19521201000230,000000 000

</dd> <dt>

**PrimaryGroupId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Primary \_ Group \_ ID")
</dt> </dl>

Relativer Bezeichner (RID) der primären globalen Gruppe für diesen Benutzer. Der Bezeichner überprüft die primäre Gruppe, zu der das Profil des Benutzers gehört.

</dd> <dt>

**Berechtigungen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ PRIV")
</dt> </dl>

Ebene der Berechtigung, die der **usri3 \_ Name** -Eigenschaft zugewiesen ist.

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

**Gast** (0)


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

**Benutzer** (1)


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

**Administrator** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Profil**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ profile")
</dt> </dl>

Der Pfad zum Profil des Benutzers. Dieser Wert kann eine NULL-Zeichenfolge, ein lokaler absoluter Pfad oder ein UNC-Pfad sein. Ein Benutzerprofil enthält Einstellungen, die für jeden Benutzer anpassbar sind, z. b. die Desktop Farben.

Beispiel: "C: \\ Windows"

</dd> <dt>

**ScriptPath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Script \_ path")
</dt> </dl>

Verzeichnispfad zum Anmelde Skript des Benutzers. Ein Anmelde Skript führt automatisch eine Reihe von Befehlen aus, wenn sich ein Benutzer bei einem System anmeldet.

Beispiel: "C: \\ Win \\ Profiles \\ thomassteven"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**UnitsPerWeek**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Units \_ per \_ Week")
</dt> </dl>

Die Anzahl der Zeiteinheiten, in die die Woche aufgeteilt ist. Sie wird mit der **LogonHours** -Eigenschaft verwendet, um den Benutzer Zugriff auf den Computer einzuschränken.

Beispiel: 168 (Stunden pro Woche)

</dd> <dt>

**UserComment**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ comment")
</dt> </dl>

Benutzerdefinierter Kommentar oder Beschreibung für dieses Profil.

</dd> <dt>

**UserId**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ User \_ ID")
</dt> </dl>

Entfernen Sie den Benutzer. Der Bezeichner überprüft, ob der Benutzer vorhanden und für diese Domäne eindeutig ist.

</dd> <dt>

**UserType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags")
</dt> </dl>

Der Kontotyp, für den der Benutzer über Berechtigungen verfügt.

Die Werte sind:

-   "Normales Konto"
-   "Doppeltes Konto"
-   "Arbeitsstations-Vertrauens Konto"
-   "Server Vertrauensstellungs Konto"
-   "Vertrauenswürdiges Domänen Konto"
-   Unbekannter

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

**Normales Konto** ("normales Konto")


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

**Doppeltes Konto** ("doppeltes Konto")


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

Arbeitsstations **Vertrauens Konto** ("Arbeitsstations-Vertrauensstellungs Konto")


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

**Server Vertrauensstellungs Konto** ("Server Vertrauensstellungs Konto")


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

**Domänen Vertrauensstellungs Konto** ("interdomäne-Vertrauensstellungs Konto")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> </dl>

</dd> <dt>

**Arbeitsstationen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Workstations")
</dt> </dl>

Namen von Arbeitsstationen, von denen der Benutzer sich anmelden kann. Es können bis zu acht Arbeitsstationen angegeben werden. die Namen müssen durch Kommas (,) getrennt werden. Eine NULL-Zeichenfolge weist keine Einschränkungen auf. Um Anmeldungen von allen Arbeitsstationen für dieses Konto zu deaktivieren, legen Sie die Eigenschaft "UF \_ accountdeaktiviert" in der **Flags** -Eigenschaft dieser Klasse fest.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ networkloginprofile** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](../wmisdk/executing-privileged-operations.md).

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel " [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) " gibt Netzwerk Anmelde Informationen für alle Benutzer eines Computers zurück.

Im folgenden VBScript-Beispiel werden Netzwerk Anmelde Informationen zurückgegeben.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



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

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
