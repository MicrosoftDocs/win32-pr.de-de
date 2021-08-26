---
description: Win32 \_ NetworkLoginProfile&\# 8194; Die WMI-Klasse stellt die Netzwerkanmeldungsinformationen eines bestimmten Benutzers auf einem Computersystem dar, auf dem Windows.
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
ms.openlocfilehash: 4fb71b27093cb1011b9aebaadf0a6760124b64f9e13ae7b5ef46f5ffc478cce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972649"
---
# <a name="win32_networkloginprofile-class"></a>Win32 \_ NetworkLoginProfile-Klasse

Die **WMI-Klasse \_ Win32 NetworkLoginProfile** stellt die Netzwerkanmeldungsinformationen eines bestimmten Benutzers auf einem Computersystem dar, auf dem Windows. [](../wmisdk/retrieving-a-class.md) Dies schließt Kennwortstatus, Zugriffsberechtigungen, Datenträgerkontingente und Anmeldeverzeichnispfade ein, ist aber nicht darauf beschränkt.

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

Die **Win32 \_ NetworkLoginProfile-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ NetworkLoginProfile-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccountExpires**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ acct \_ expires")
</dt> </dl>

Das Konto läuft ab. Dieser Wert wird aus der Anzahl der Sekunden berechnet, die seit dem 1. Januar 1970 um 00:00:00 Verstrichen sind, und wird in diesem Format festgelegt: yyyymmddhhmmss.mmmmmm sutc.

Beispiel: 20521201000230.000000 000

</dd> <dt>

**AuthorizationFlags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ auth \_ flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")
</dt> </dl>

Eine Gruppe von Flags, die die Ressourcen angeben, zu deren Verwendung oder Änderung ein Benutzer berechtigt ist.

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

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsfunktionen \| \| NetUserEnum")
</dt> </dl>

Gibt an, wie oft der Benutzer ein fehlerhaftes Kennwort ein gibt, wenn er sich bei einem Computersystem mit Windows.

Beispiel: 0

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**CodePage**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ code \_ page")
</dt> </dl>

Codepage für die Sprache des Benutzers ihrer Wahl. Eine Codepage ist der verwendete Zeichensatz.

</dd> <dt>

**Comment**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")
</dt> </dl>

Kommentar oder Beschreibung für dieses Anmeldeprofil.

</dd> <dt>

**Countrycode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ country \_ code")
</dt> </dl>

Länder-/Regioncode für die Sprache der Wahl des Benutzers.

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

**Flags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account Disabled", "Home Dir Required", "Lockout", "Password Not Required", "Paswword Can't Change", "Encrypted Test Password Allowed", "Temp Duplicate Account", "Normal Account", "InterDomain Trust Account", "WorkStation Trust Account", "Server Trust Account", "Don't Expire Password", "MNS Logon Account", "Smartcard Required", "Trusted for Delegation", "Not Delegated", "Use DES Key Only", "Don't Require Preauthorization", "Password Expired")
</dt> </dl>

Die eigenschaften, die für dieses Netzwerkprofil verfügbar sind.

Folgende Eigenschaften können festgelegt werden:

<dt>

1 (0x1)
</dt> <dd>

Skript

Ein ausgeführtes Anmeldeskript. Dieser Wert muss für LAN Manager 2.0 festgelegt werden.

</dd> <dt>

2 (0x2)
</dt> <dd>

Konto deaktiviert

Das Konto des Benutzers ist deaktiviert.

</dd> <dt>

8 (0x8)
</dt> <dd>

Startverzeichnis erforderlich

Ein Startverzeichnis ist erforderlich.

</dd> <dt>

16 (0x10)
</dt> <dd>

Sperrung

Das Konto ist derzeit gesperrt. Für [**NetUserSetInfo kann**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo)dieser Wert zum Entsperren eines zuvor gesperrten Kontos aufgehoben werden. Dieser Wert kann nicht zum Sperren eines zuvor entsperrten Kontos verwendet werden.

</dd> <dt>

32 (0x20)
</dt> <dd>

Kennwort nicht erforderlich

Es ist kein Kennwort erforderlich.

</dd> <dt>

64 (0x40)
</dt> <dd>

Kennwort kann nicht geändert werden

Der Benutzer kann das Kennwort nicht ändern.

</dd> <dt>

128 (0x80)
</dt> <dd>

Verschlüsseltes Testkennwort zulässig

</dd> <dt>

256 (0x100)
</dt> <dd>

Temporäres doppeltes Konto

Ein Konto für Benutzer, deren primäres Konto sich in einer anderen Domäne befindet. Dieses Konto bietet Benutzerzugriff auf diese Domäne, aber nicht auf eine Domäne, die dieser Domäne vertraut. Der Benutzer-Manager bezieht sich auf diesen Kontotyp als lokales Benutzerkonto.

</dd> <dt>

512 (0x200)
</dt> <dd>

Normales Konto

Standardkontotyp, der einen typischen Benutzer darstellt.

</dd> <dt>

2048 (0x800)
</dt> <dd>

Domänenübergreifendes Vertrauensstellungskonto

Eine Genehmigung für ein Vertrauenskonto für eine Domäne, die anderen Domänen vertraut.

</dd> <dt>

4096 (0x1000)
</dt> <dd>

Arbeitsstations-Vertrauensstellungskonto

Ein Computerkonto für eine Windows arbeitsstation oder server, die bzw. der Mitglied dieser Domäne ist.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Server-Vertrauensstellungskonto

Ein Computerkonto für einen Sicherungsdomänencontroller, der Mitglied dieser Domäne ist.

</dd> <dt>

65536 (0x10000)
</dt> <dd>

Kennwort nicht ablaufen

</dd> <dt>

131072 (0x20000)
</dt> <dd>

MNS-Anmeldekonto

MNS-Anmeldekontotyp (Majority Node Set), der einen MNS-Benutzer darstellt.

</dd> <dt>

262144 (0x40000)
</dt> <dd>

Smartcard erforderlich

</dd> <dt>

524288 (0x80000)
</dt> <dd>

Vertrauenswürdig für Delegierung

</dd> <dt>

1048576 (0x100000)
</dt> <dd>

Nicht delegiert

</dd> <dt>

2097152 (0x200000)
</dt> <dd>

Nur DES-Schlüssel verwenden

</dd> <dt>

4194304 (0x400000)
</dt> <dd>

Keine Vorautorisierung erforderlich

</dd> <dt>

8388608 (0x800000)
</dt> <dd>

Kennwort abgelaufen

Gibt an, dass das Kennwort abgelaufen ist.

</dd> </dl>

Die folgenden Eigenschaften beschreiben den Kontotyp. Es kann nur ein Wert festgelegt werden:

-   NORMALES \_ \_ UF-KONTO
-   TEMPORÄRES \_ DOPPELTES \_ UF-KONTO \_
-   UF \_ WORKSTATION \_ TRUST \_ ACCOUNT
-   UF \_ SERVER \_ TRUST \_ ACCOUNT
-   UF \_ INTERDOMAIN \_ TRUST \_ ACCOUNT

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ full \_ name")
</dt> </dl>

Vollständiger Name des Benutzers, der zum Netzwerkanmeldungsprofil gehört. Diese Zeichenfolge kann leer sein, wenn der Benutzer sich dafür entscheidet, einem Benutzernamen keinen vollständigen Namen zu zuordnen.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home \_ dir")
</dt> </dl>

Pfad zum Startverzeichnis des Benutzers. Diese Zeichenfolge ist möglicherweise leer, wenn der Benutzer kein Startverzeichnis angibt.

Beispiel: \\ "HOMEDIR"

</dd> <dt>

**HomeDirectoryDrive**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home dir \_ \_ drive")
</dt> </dl>

Laufwerkbuchstaben, der dem Basisverzeichnis des Benutzers für die Anmeldung zugewiesen ist.

Beispiel: "C:"

</dd> <dt>

**LastLogoff**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ last \_ logoff")
</dt> </dl>

Der Benutzer hat sich zuletzt vom System abgemelgt. Dieser Wert wird anhand der Anzahl der Sekunden berechnet, die seit dem 1. Januar 1970 um 00:00:00 Verstrichen sind. Der Wert " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " bedeutet, dass der Zeitpunkt der letzten Abmeldezeit unbekannt ist. Das Format dieses Werts ist yyyymmddhhmmss.mmmmmm sutc. Informationen zum Übersetzen dieser Eigenschaft in Ihre lokale Zeit finden Sie unter [WMI Tasks: Dates and Times ( WMI-Aufgaben: Datumsangaben und Uhrzeiten](../wmisdk/wmi-tasks--dates-and-times.md)).

Beispiel: 19521201000230.000000 000

</dd> <dt>

**LastLogon**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ last \_ logon")
</dt> </dl>

Der Benutzer hat sich zuletzt beim System angemeldet. Dieser Wert wird anhand der Anzahl der Sekunden berechnet, die seit dem 1. Januar 1970 um 00:00:00 Verstrichen sind. Das Format dieses Werts ist yyyymmddhhmmss.mmmmmm sutc. Informationen zum Übersetzen dieser Eigenschaft in Ihre lokale Zeit finden Sie unter [WMI Tasks: Dates and Times ( WMI-Aufgaben: Datumsangaben und Uhrzeiten](../wmisdk/wmi-tasks--dates-and-times.md)).

Beispiel: 19521201000230.000000 000

</dd> <dt>

**LogonHours**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ hours")
</dt> </dl>

Zeiten während der Woche, in denen sich der Benutzer anmelden kann. Jedes Bit stellt eine Zeiteinheit dar, die von der **UnitsPerWeek-Eigenschaft angegeben** wird. Wenn die Zeiteinheit beispielsweise stündlich ist, ist das erste Bit (Bit 0, Wort 0) Sonntag, 0:00 bis 0:59, das zweite Bit (Bit 1, Wort 0) Sonntag, 1:00 bis 1:59 und so weiter. Wenn dieser Member auf **NULL festgelegt ist,** gibt es keine Zeitbeschränkung. Die Zeit ist auf GMT festgelegt und muss für andere Zeitzonen angepasst werden (z. B. GMT minus 8 Stunden für PST).

</dd> <dt>

**LogonServer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ server")
</dt> </dl>

Name des Servers, an den Anmeldeanforderungen gesendet werden. Servernamen sollten zwei schräge Schrägstriche vorangehende werden ( \\ \\ ). Ein Servername mit einem Sternchen ( ) gibt an, dass die Anmeldeanforderung von jedem \\ \\ \* Anmeldeserver verarbeitet werden kann. Eine NULL-Zeichenfolge gibt an, dass Anforderungen an den Domänencontroller gesendet werden.

Beispiel: \\ \\ "MyServer"

</dd> <dt>

**MaximumStorage**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ max \_ storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Maximal verfügbarer Speicherplatz für den Benutzer. Wenn MaximumStorage auf USER MAXSTORAGE UNLIMITED festgelegt ist, kann der Benutzer den verfügbaren \_ \_ Speicherplatz nutzen.

Beispiel: 10000000

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| \| [**USER INFO \_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Name")
</dt> </dl>

Benutzerkonto auf einer bestimmten Domäne oder einem bestimmten Computer. Die Anzahl der Zeichen im Namen darf den Wert von UNLEN nicht überschreiten.

Beispiel: "somedomain \\ johndoe"

</dd> <dt>

**NumberOfLogons**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num \_ logons")
</dt> </dl>

Anzahl der erfolgreichen Versuche des Benutzers, sich bei diesem Konto anzumelden. Der Wert 0xFFFFFFFF gibt an, dass der Wert unbekannt ist. Diese Eigenschaft wird auf jedem Sicherungsdomänencontroller (BDC) in der Domäne separat verwaltet. Um einen genauen Wert zu erhalten, sollte nur der größte Wert von allen BDCs verwendet werden.

Beispiel: 4

</dd> <dt>

**Parameter**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms")
</dt> </dl>

Speicherplatz, der für die Verwendung durch Anwendungen vorgesehen ist. Diese Zeichenfolge kann NULL sein oder eine beliebige Anzahl von Zeichen vor dem abschließenden NULL-Zeichen enthalten. Microsoft-Produkte verwenden dieses Mitglied, um Benutzerkonfigurationsinformationen zu speichern. Ändern Sie diese Informationen nicht, da dieser Wert für eine Anwendung spezifisch ist.

</dd> <dt>

**PasswordAge**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ age")
</dt> </dl>

Die Zeitspanne, für die ein Kennwort in Kraft war. Dieser Wert wird anhand der Anzahl von Sekunden gemessen, die seit der letzten Änderung des Kennworts verstrichen sind.

Beispiel: 00001201000230.0000000 000

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| \| [**USER \_ MODALS INFO \_ \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ max \_ passwd \_ age")
</dt> </dl>

Datum und Uhrzeit des Ablaufs des Kennworts. Der Wert wird in folgendem Format festgelegt: yyyymmddhhmmss.mmmmmm sutc

Beispiel: 19521201000230.0000000 000

</dd> <dt>

**PrimaryGroupId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ primäre \_ \_ Gruppen-ID")
</dt> </dl>

Relativer Bezeichner (RID) der primären globalen Gruppe für diesen Benutzer. Der Bezeichner überprüft die primäre Gruppe, zu der das Profil des Benutzers gehört.

</dd> <dt>

**Berechtigungen**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv")
</dt> </dl>

Berechtigungsstufe, die der **usri3-Namenseigenschaft \_** zugewiesen ist.

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

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3-Profil") \_
</dt> </dl>

Pfad zum Profil des Benutzers. Dieser Wert kann eine NULL-Zeichenfolge, ein lokaler absoluter Pfad oder ein UNC-Pfad sein. Ein Benutzerprofil enthält Einstellungen, die für jeden Benutzer angepasst werden können, z. B. die Desktopfarben.

Beispiel: "C: \\ Windows"

</dd> <dt>

**ScriptPath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3-Skriptpfad") \_ \_
</dt> </dl>

Verzeichnispfad zum Anmeldeskript des Benutzers. Ein Anmeldeskript führt jedes Mal, wenn sich ein Benutzer bei einem System anmeldet, automatisch eine Reihe von Befehlen aus.

Beispiel: "C: \\ win \\ profiles \\ ThomasSteven"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichner, durch den das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**UnitsPerWeek**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Einheiten pro \_ \_ Woche")
</dt> </dl>

Anzahl der Zeiteinheiten, in die die Woche unterteilt ist. Sie wird mit der **LogonHours-Eigenschaft** verwendet, um den Benutzerzugriff auf den Computer zu beschränken.

Beispiel: 168 (Stunden pro Woche)

</dd> <dt>

**UserComment**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ comment")
</dt> </dl>

Benutzerdefinierter Kommentar oder Beschreibung für dieses Profil.

</dd> <dt>

**UserId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ user \_ id")
</dt> </dl>

RID des Benutzers. Der Bezeichner überprüft, ob der Benutzer vorhanden ist und für diese Domäne eindeutig ist.

</dd> <dt>

**UserType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Netzwerkverwaltungsstrukturen \| USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3-Flags") \_
</dt> </dl>

Typ des Kontos, für das der Benutzer über Berechtigungen verfügt.

Die Werte sind:

-   "Normales Konto"
-   "Doppeltes Konto"
-   "Arbeitsstations-Vertrauenskonto"
-   "Server trust account" (Serververtrauenskonto)
-   "Interdomain Trust Account" (Domänenübergreifendes Vertrauensstellungskonto)
-   "Unbekannt"

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

**Normales Konto** ("normales Konto")


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

**Doppeltes Konto** ("Doppeltes Konto")


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

**Arbeitsstations-Vertrauensstellungskonto** ("Arbeitsstations-Vertrauensstellungskonto")


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

**Server-Vertrauensstellungskonto** ("Server-Vertrauensstellungskonto")


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

**Domänenübergreifendes Vertrauensstellungskonto** ("Domänenübergreifendes Vertrauensstellungskonto")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> </dl>

</dd> <dt>

**Workstations**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USER INFO \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ workstations")
</dt> </dl>

Namen von Arbeitsstationen, von denen sich der Benutzer anmelden kann. Es können bis zu acht Arbeitsstationen angegeben werden. die Namen müssen durch Kommas (,) getrennt werden. Eine NULL-Zeichenfolge gibt keine Einschränkungen an. Um Anmeldungen von allen Arbeitsstationen für dieses Konto zu deaktivieren, legen Sie UF \_ ACCOUNTDISABLE in der **Flags-Eigenschaft** dieser Klasse fest.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ NetworkLoginProfile-Klasse** wird von [**der \_ CIM-Einstellung abgeleitet.**](cim-setting.md)

Der aufrufende Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über SE **\_ RESTORE \_ NAME-Berechtigung** verfügen. Weitere Informationen finden Sie unter [Ausführen von privilegierten Vorgängen.](../wmisdk/executing-privileged-operations.md)

## <a name="examples"></a>Beispiele

Im [PowerShell-Beispiel Netzwerkanmeldungsprofile](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) auflisten werden Netzwerkanmeldungsinformationen für alle Benutzer eines Computers zurückgegeben.

Im folgenden VBScript-Beispiel werden Netzwerkanmeldungsinformationen zurückgegeben.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
