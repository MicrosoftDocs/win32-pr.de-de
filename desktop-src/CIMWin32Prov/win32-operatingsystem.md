---
description: Stellt ein Windows-basiertes Betriebssystem dar, das auf einem Computer installiert ist.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Win32_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214270"
---
# <a name="win32_operatingsystem-class"></a>Win32- \_ OperatingSystem-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) des **Win32- \_ OperatingSystems** stellt ein Windows-basiertes Betriebssystem dar, das auf einem Computer installiert ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a>Member

Die **Win32 \_ OperatingSystem** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ OperatingSystem** -Klasse verfügt über diese Methoden.



| Methode                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reboot**](reboot-method-in-class-win32-operatingsystem.md)                             | Der Computer wird heruntergefahren und dann neu gestartet.<br/>                                                                                                                                                                                                           |
| [**SetDateTime**](setdatetime-method-in-class-win32-operatingsystem.md)                   | Ermöglicht das Festlegen des Datums und der Uhrzeit des Computers.<br/>                                                                                                                                                                                                                |
| [**Abschlusses**](shutdown-method-in-class-win32-operatingsystem.md)                         | Entlädt Programme und DLLs an den Punkt, an dem Sie den Computer sicher ausschalten können.<br/>                                                                                                                                                                           |
| [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)               | Bietet den vollständigen Satz von Optionen für das Herunterfahren, die von den Windows-Betriebssystemen<br/>                                                                                                                                                                           |
| [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | Bietet den gleichen Satz von Optionen für das Herunterfahren, der von der [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) -Methode im **Win32- \_ OperatingSystem** unterstützt wird. Sie können jedoch auch Kommentare, einen Grund für das Herunterfahren oder einen Timeout Wert angeben.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ OperatingSystem** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**BootDevice**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Drive \_ map \_ Info \| btInt13Unit")
</dt> </dl>

Der Name des Laufwerks, von dem aus das Windows-Betriebssystem gestartet wird.

Beispiel: " \\ \\ Device \\ Harddisk0"

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")
</dt> </dl>

Buildnummer eines Betriebssystems. Sie kann für präzisere Versionsinformationen als Produkt Versionsnummern verwendet werden.

Beispiel: "1381"

</dd> <dt>

**BuildType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ \| CurrentType")
</dt> </dl>

Typ des Builds, der für ein Betriebssystem verwendet wird.

Beispiele: "" Retail Build "", "" aktivierter Build ""

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge. Die Zeichenfolge enthält die Betriebssystemversion. Beispiel: "Microsoft Windows 7 Enterprise". Diese Eigenschaft kann lokalisiert werden.

**Windows Vista und Windows 7:** Diese Eigenschaft kann nachfolgende Zeichen enthalten. Beispielsweise kann die Zeichenfolge "Microsoft Windows 7 Enterprise" (nachfolgende Leerzeichen) erforderlich sein, um Informationen mithilfe dieser Eigenschaft abzurufen.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Codesatz**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (6), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**getlocaleingefo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ idefaultansicodepage")
</dt> </dl>

Der Code Page Wert, den ein Betriebssystem verwendet. Eine Codepage enthält eine Zeichentabelle, die von einem Betriebssystem verwendet wird, um Zeichen folgen für verschiedene Sprachen zu übersetzen. Der American National Standards Institute (ANSI) listet Werte auf, die definierte Codepages darstellen. Wenn ein Betriebssystem keine ANSI-Codepage verwendet, wird dieses Element auf 0 (null) festgelegt. Die **Codeset** -Zeichenfolge kann maximal sechs Zeichen verwenden, um den Code Page Wert zu definieren.

Beispiel: "1255"

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**getlocaleingefo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ iCountry")
</dt> </dl>

Code für das Land bzw. die Region, das von einem Betriebssystem verwendet wird. Werte basieren auf den Präfixen für die internationale Telefon Wahl – auch als IBM Land/Region-Codes bezeichnet. Für diese Eigenschaft können maximal sechs Zeichen verwendet werden, um den Code Wert für Land/Region zu definieren.

Beispiel: "1" (USA)

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Computer Systems.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**CSDVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")
</dt> </dl>

**Null**-terminierte Zeichenfolge, die die neueste auf einem Computer installierte Service Pack angibt. Wenn keine Service Pack installiert ist, ist die Zeichenfolge **null**.

Beispiel: "Service Pack 3"

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Name des Bereichs Computer Systems.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")
</dt> </dl>

Die Anzahl in Minuten, für die ein Betriebssystem von der Greenwich Mean Time (GMT) versetzt wird. Die Zahl ist positiv, negativ oder 0 (null).

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Dataexecutionprevention \_ 32bitapplications**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Wenn die Hardware Funktion zur Daten Ausführungs Verhinderung verfügbar ist, gibt diese Eigenschaft an, dass die Funktion für 32-Bit-Anwendungen auf **true** festgelegt ist. Auf 64-Bit-Computern wird das Feature zur Verhinderung der Datenausführung im [Startkonfigurationsdaten-Speicher (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) konfiguriert, und die Eigenschaften im **Win32- \_ OperatingSystem** werden entsprechend festgelegt.

</dd> <dt>

**Dataexecutionprevention \_ verfügbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Die Verhinderung von Datenausführung ist eine Hardware Funktion, um Pufferüberlauf Angriffe zu verhindern, indem Sie die Ausführung von Code auf Datentyp-Speicherseiten beenden. **True** gibt an, dass diese Funktion verfügbar ist. Auf 64-Bit-Computern wird das Feature zur Verhinderung der Datenausführung im BCD-Speicher konfiguriert, und die Eigenschaften im **Win32- \_ OperatingSystem** werden entsprechend festgelegt.

</dd> <dt>

**Dataexecutionprevention- \_ Treiber**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Wenn die Hardware Funktion zur Daten Ausführungs Verhinderung verfügbar ist, gibt diese Eigenschaft an, dass die Funktion für Treiber auf " **true**" festgelegt ist. Auf 64-Bit-Computern wird das Feature zur Verhinderung der Datenausführung im BCD-Speicher konfiguriert, und die Eigenschaften im **Win32- \_ OperatingSystem** werden entsprechend festgelegt.

</dd> <dt>

**Dataexecutionprevention \_ supportpolicy**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Gibt an, welche Einstellung für die Daten Ausführungs Verhinderung (DEP) angewendet wird. Die DEP-Einstellung gibt den Umfang an, in dem DEP auf 32-Bit-Anwendungen im System angewendet wird. DEP wird immer auf den Windows-Kernel angewendet.

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Immer aus** (0)


</dt> <dd>

DEP ist für alle 32-Bit-Anwendungen auf dem Computer deaktiviert, ohne dass Ausnahmen auftreten. Diese Einstellung ist für die Benutzeroberfläche nicht verfügbar.

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)


</dt> <dd>

DEP ist für alle 32-Bit-Anwendungen auf dem Computer aktiviert. Diese Einstellung ist für die Benutzeroberfläche nicht verfügbar.

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt in** (2)


</dt> <dd>

DEP ist für eine begrenzte Anzahl von Binärdateien, den Kernel und alle Windows-basierten Dienste aktiviert. Allerdings ist es für alle 32-Bit-Anwendungen standardmäßig deaktiviert. Ein Benutzer oder Administrator muss explizit entweder die **Always on** oder die **opt** -Einstellung auswählen, bevor DEP auf 32-Bit-Anwendungen angewendet werden kann.

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Ablehnen** (3)


</dt> <dd>

DEP ist für alle 32-Bit-Anwendungen standardmäßig aktiviert. Ein Benutzer oder Administrator kann die Unterstützung für eine 32-Bit-Anwendung explizit entfernen, indem er die Anwendung einer Ausnahmeliste hinzufügt.

</dd> </dl>

</dd> <dt>

**Debuggen**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ Debug")
</dt> </dl>

Das Betriebssystem ist ein aktivierter (Debuggen) Build. Wenn der Wert **true** ist, wird die Debugversion installiert. Aktivierte Builds bieten Fehlerüberprüfung, Argument Überprüfung und systemdebugcode. Zusätzlicher Code in einer überprüften Binärdatei generiert eine Kernel Debugger-Fehlermeldung und unterbricht den Debugger. Dadurch können Sie sofort die Ursache und den Speicherort des Fehlers bestimmen. Aufgrund des zusätzlichen Codes, der ausgeführt wird, kann die Leistung von einem aktivierten Build beeinträchtigt werden.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Beschreibung"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Die Beschreibung des Windows-Betriebssystems. Einige Benutzeroberflächen, z. b. solche, die das Bearbeiten dieser Beschreibung ermöglichen, beschränken die Länge auf 48 Zeichen.

</dd> <dt>

**Distri**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das Betriebssystem auf mehrere Computersystem Knoten verteilt ist. Wenn dies der Fall ist, sollten diese Knoten als Cluster gruppiert werden.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**EncryptionLevel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verschlüsselungs Stufe für sichere Transaktionen: 40-Bit, 128-Bit oder *n*-Bit.

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

**40-Bit** (0)


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

**128-Bit** (1)


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

**n-Bit** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ForegroundApplicationBoost**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ prioritycontrol \| Win32PrioritySeparation")
</dt> </dl>

Der Vordergrund Anwendung wird eine Erhöhung der Priorität eingeräumt. Anwendungs Verstärkung wird implementiert, indem eine Anwendung mehr Ausführungszeit Scheiben (Quantum-Längen) bereitstellt.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (0)


</dt> <dd>

Das System erhöht die Quantum-Länge um 6.

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimal** (1)


</dt> <dd>

Das System erhöht die Quantum-Länge um 12.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)


</dt> <dd>

Das System erhöht die Quantum-Länge um 18.

</dd> </dl>

</dd> <dt>

**FreePhysicalMemory**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Anzahl von physischem Speicher (in Kilobytes), der derzeit nicht verwendet wird und verfügbar ist.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Freespaceinpagingfiles**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| System Arbeitsspeicher-Einstellungen \| 001,4 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Kilobyte ")
</dt> </dl>

Die Zahl in Kilobytes, die in den Auslagerungs Dateien des Betriebssystems zugeordnet werden kann, ohne dass andere Seiten ausgetauscht werden müssen.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**FreeVirtualMemory**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Anzahl in Kilobyte des virtuellen Speichers, der derzeit nicht verwendet wird und verfügbar ist.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Date-Objekt wurde installiert. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**LargeSystemCache**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Diese Eigenschaft ist veraltet und wird nicht unterstützt.

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Für Anwendungen optimieren** (0)


</dt> <dd>

Optimieren Sie den Arbeitsspeicher für Anwendungen.

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimieren der System Leistung** (1)


</dt> <dd>

Optimieren Sie den Arbeitsspeicher für die Systemleistung.

</dd> </dl>

</dd> <dt>

**LastBootUpTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit des letzten Neustarts des Betriebssystems.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**LocalDateTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrsystemdate "," MIF. Allgemeine Informationen zu DMTF \| \| 001,6 ")
</dt> </dl>

Betriebssystemversion des lokalen Datums und der Tageszeit.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Gebietsschema**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ iLanguage")
</dt> </dl>

Der vom Betriebssystem verwendete sprach Bezeichner. Eine sprach Kennung ist eine standardmäßige internationale numerische Abkürzung für ein Land/eine Region. Jede Sprache verfügt über eine eindeutige Sprach-ID (langid), einen 16-Bit-Wert, der aus einem primären und einem sekundären sprach Bezeichner besteht.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Der Name des Betriebssystem Herstellers. Bei Windows-basierten Systemen ist dieser Wert "Microsoft Corporation".

</dd> <dt>

**Maxnumofprocesses**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrsystemmaxprocesses ")
</dt> </dl>

Maximale Anzahl von Prozess Kontexten, die vom Betriebssystem unterstützt werden können. Der vom Anbieter festgelegte Standardwert ist 4294967295 (0xFFFFFFFF). Wenn kein festes Maximum vorhanden ist, sollte der Wert 0 (null) sein. Auf Systemen mit einem maximalen Höchstwert kann dieses Objekt bei der Diagnose von Fehlern helfen, die auftreten, wenn der Höchstwert erreicht ist – wenn dies unbekannt ist, geben Sie 4294967295 (0xFFFFFFFF) ein.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**MaxProcessMemorySize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Maximale Anzahl von Arbeitsspeicher in Kilobytes, die einem Prozess zugeordnet werden kann. Bei Betriebssystemen ohne virtuellen Arbeitsspeicher entspricht dieser Wert in der Regel der Gesamtmenge an physischem Arbeitsspeicher abzüglich dem vom BIOS und dem Betriebssystem verwendeten Arbeitsspeicher. Bei einigen Betriebssystemen kann dieser Wert unendlich sein. in diesem Fall sollte 0 (null) eingegeben werden. In anderen Fällen kann dieser Wert eine Konstante sein, z. b. 2G oder 4G.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Muilanguages**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Auf dem Computer installierte Multilingual User Interface Pack (MUI Pack)-Sprachen. Beispiel: "en-US". MUI Pack Sprachen sind Ressourcen Dateien, die in der englischen Version des Betriebssystems installiert werden können. Wenn eine MUI Pack installiert ist, können Sie die Sprache der Benutzeroberfläche in eine von 33 unterstützten Sprachen ändern.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Betriebssystem Instanz innerhalb eines Computer Systems.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**"Numoflicensedusers"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Benutzerlizenzen für das Betriebssystem. Wenn unbegrenzt, geben Sie 0 (null) ein. Wenn unbekannt, geben Sie-1 ein.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Anzahlungsprozesse**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrsystemprocesses ")
</dt> </dl>

Anzahl von Prozess Kontexten, die derzeit auf dem Betriebssystem geladen oder ausgeführt werden.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Numofusers**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrsystemnumusers ")
</dt> </dl>

Anzahl der Benutzersitzungen, für die das Betriebssystem derzeit Zustandsinformationen speichert.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**OperatingSystemSKU**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

SKU-Nummer (Stock Keeping Unit) für das Betriebssystem. Diese Werte sind identisch mit den **Product \_ \** _-Konstanten, die in "Winnt. h" definiert sind und mit der Funktion " [_ *GetProductInfo* *](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) " verwendet werden.

In der folgenden Liste werden mögliche SKU-Werte aufgelistet.

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Produkt \_ Nicht definiert** (0)


</dt> <dd>

Nicht definiert

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Produkt \_ Ultimate** (1)


</dt> <dd>

Ultimate Edition, z. b. Windows Vista Ultimate.

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Produkt \_ Home \_ Basic** (2)


</dt> <dd>

Home Basic Edition

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Produkt \_ Home \_ Premium** (3)


</dt> <dd>

Home Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Produkt \_ Enterprise** (4)


</dt> <dd>

Enterprise

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Produkt \_ Business** (6)


</dt> <dd>

Business Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Produkt \_ Standard \_ Server** (7)


</dt> <dd>

Windows Server Standard Edition (Desktop Darstellung-Installation)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Produkt \_ Datacenter \_ Server** (8)


</dt> <dd>

Windows Server Datacenter Edition (Desktop Darstellung-Installation)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Produkt \_ SmallBusiness \_ Server** (9)


</dt> <dd>

Small Business Server-Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Produkt \_ Enterprise \_ Server** (10)


</dt> <dd>

Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Produkt \_ Starter** (11)


</dt> <dd>

 Starter Edition

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Produkt \_ Datacenter \_ Server \_ Core** (12)


</dt> <dd>

Datacenter Server Core Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Produkt \_ Standard \_ Server \_ Core** (13)


</dt> <dd>

Standard Server Core-Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Produkt \_ Enterprise \_ Server \_ Core** (14)


</dt> <dd>

Enterprise Server Core Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Produkt \_ Webserver \_** (17)


</dt> <dd>

Webserver Edition

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Produkt \_ Home \_ Server** (19)


</dt> <dd>

Home Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Produkt \_ Storage \_ Express \_ Server** (20)


</dt> <dd>

Storage Express Server-Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Produkt \_ Storage \_ Standard \_ Server** (21)


</dt> <dd>

Windows Storage Server Standard Edition (Desktop Darstellung-Installation)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Produkt \_ Speicher \_ \_ Arbeitsgruppenserver** (22)


</dt> <dd>

Windows Storage Server Workgroup Edition (Desktop Darstellung Installation)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Produkt \_ Storage \_ Enterprise \_ Server** (23)


</dt> <dd>

Storage Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Produkt \_ Server \_ für \_ SmallBusiness** (24)


</dt> <dd>

Server für Small Business Edition

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Produkt \_ SmallBusiness \_ Server \_ Premium** (25)


</dt> <dd>

Small Business Server Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Produkt \_ Enterprise \_ N** (27)


</dt> <dd>

Windows Enterprise Edition

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Produkt \_ Ultimate \_ N** (28)


</dt> <dd>

Windows Ultimate-Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Produkt \_ Webserver \_ \_ Core** (29)


</dt> <dd>

Windows Server-Webserver Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Produkt \_ Standard \_ Server \_ V** (36)


</dt> <dd>

Windows Server Standard Edition ohne Hyper-V

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Produkt \_ Datacenter \_ Server \_ V** (37)


</dt> <dd>

Windows Server Datacenter Edition ohne Hyper-V (vollständige Installation)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Produkt \_ Enterprise \_ Server \_ V** (38)


</dt> <dd>

Windows Server Enterprise Edition ohne Hyper-V (vollständige Installation)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Produkt \_ Datacenter \_ Server \_ Core \_ V** (39)


</dt> <dd>

Windows Server Datacenter Edition ohne Hyper-V (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Produkt \_ Standard \_ Server \_ Core \_ V** (40)


</dt> <dd>

Windows Server Standard Edition ohne Hyper-V (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Produkt \_ Enterprise \_ Server \_ Core \_ V** (41)


</dt> <dd>

Windows Server Enterprise Edition ohne Hyper-V (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Produkt \_ HyperV** (42)


</dt> <dd>

Microsoft Hyper-V Server

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Produkt \_ Storage \_ Express \_ Server \_ Core** (43)


</dt> <dd>

Storage Server Express Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Produkt \_ Storage \_ Standard \_ Server \_ Core** (44)


</dt> <dd>

Storage Server Standard Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Produkt \_ Speicher \_ \_ Arbeitsgruppenserver \_ Core** (45)


</dt> <dd>

Storage Server Workgroup Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Produkt \_ Storage \_ Enterprise \_ Server \_ Core** (46)


</dt> <dd>

Storage Server Workgroup Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Produkt \_ Professional** (48)


</dt> <dd>

Windows Professional

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Produkt \_ SB- \_ Lösungs \_ Server** (50)


</dt> <dd>

Windows Server Essentials (Desktop Darstellung-Installation)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Produkt \_ SmallBusiness \_ Server \_ Premium \_ Core** (63)


</dt> <dd>

Small Business Server Premium (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Produkt \_ Cluster \_ Server \_ V** (64)


</dt> <dd>

Windows Compute Cluster Server ohne Hyper-V

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Produkt \_ \_Kernarm** (97)


</dt> <dd>

Windows RT

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>**Produkt \_ Core** (101)


</dt> <dd>

Windows-Startseite

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Produkt \_ Professional \_ WMC** (103)


</dt> <dd>

Windows Professional mit Media Center

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Produkt \_ Mobile \_ Kerne** (104)


</dt> <dd>

Windows Mobile

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Produkt \_ Iotuap** (123)


</dt> <dd>

Windows IOT (Internet der Dinge) Core

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Produkt \_ Rechenzentrum \_ Nano \_ Server** (143)


</dt> <dd>

Windows Server Datacenter Edition (Nano Server-Installation)

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Produkt \_ Standard \_ Nano \_ Server** (144)


</dt> <dd>

Windows Server Standard Edition (Nano Server-Installation)

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Produkt \_ Datacenter \_ WS \_ Server \_ Core** (147)


</dt> <dd>

Windows Server Datacenter Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Produkt \_ Standard- \_ WS- \_ Server \_ Core** (148)


</dt> <dd>

Windows Server Standard Edition (Server Core-Installation)

</dd> </dl>

</dd> <dt>

**Organisation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")
</dt> </dl>

Der Name des Unternehmens für den registrierten Benutzer des Betriebssystems.

Beispiel: "Microsoft Corporation"

</dd> <dt>

**OSArchitecture**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Architektur des Betriebssystems im Gegensatz zum Prozessor. Diese Eigenschaft kann lokalisiert werden.

Beispiel: 32-Bit

</dd> <dt>

**OSLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Default \\ \\ Control Panel \\ \\ International \| locale")
</dt> </dl>

Die Sprachversion des installierten Betriebssystems. In der folgenden Liste sind die möglichen Werte aufgeführt. Beispiel: 0x0807 (Deutsch, Schweiz).

<dt>

1 (0x1)
</dt> <dd>

Arabisch

</dd> <dt>

4 (0x4)
</dt> <dd>

Chinesisch (vereinfacht) – China

</dd> <dt>

9 (0x9)
</dt> <dd>

Englisch

</dd> <dt>

1025 (0x401)
</dt> <dd>

Arabisch – Saudi-Arabien

</dd> <dt>

1026 (0x402)
</dt> <dd>

Bulgarisch

</dd> <dt>

1027 (0x403)
</dt> <dd>

Katalanisch

</dd> <dt>

1028 (0x404)
</dt> <dd>

Chinesisch (traditionell) – Taiwan

</dd> <dt>

1029 (0x405)
</dt> <dd>

Tschechisch

</dd> <dt>

1030 (0x406)
</dt> <dd>

Dänisch

</dd> <dt>

1031 (0x407)
</dt> <dd>

Deutsch (Deutschland)

</dd> <dt>

1032 (0x408)
</dt> <dd>

Griechisch

</dd> <dt>

1033 (0x409)
</dt> <dd>

Englisch – USA

</dd> <dt>

1034 (0x40a)
</dt> <dd>

Spanisch – traditionelle Sortierung

</dd> <dt>

1035 (0x40b)
</dt> <dd>

Finnisch

</dd> <dt>

1036 (0x40c)
</dt> <dd>

Französisch (Frankreich)

</dd> <dt>

1037 (0x40d)
</dt> <dd>

Hebräisch

</dd> <dt>

1038 (0x40e)
</dt> <dd>

Ungarisch

</dd> <dt>

1039 (0x40f)
</dt> <dd>

Isländisch

</dd> <dt>

1040 (0x410)
</dt> <dd>

Italienisch (Italien)

</dd> <dt>

1041 (0x411)
</dt> <dd>

Japanisch

</dd> <dt>

1042 (0x412)
</dt> <dd>

Koreanisch

</dd> <dt>

1043 (0x413)
</dt> <dd>

Niederländisch (Niederlande)

</dd> <dt>

1044 (0x414)
</dt> <dd>

Norwegisch – Bokmal

</dd> <dt>

1045 (0x415)
</dt> <dd>

Polnisch

</dd> <dt>

1046 (0x416)
</dt> <dd>

Portugiesisch (Brasilien)

</dd> <dt>

1047 (0x417)
</dt> <dd>

Rhaeto-Romanic

</dd> <dt>

1048 (0x418)
</dt> <dd>

Rumänisch

</dd> <dt>

1049 (0x419)
</dt> <dd>

Russisch

</dd> <dt>

1050 (0x41A)
</dt> <dd>

Kroatisch

</dd> <dt>

1051 (0x41b)
</dt> <dd>

Slowakisch

</dd> <dt>

1052 (0x41c)
</dt> <dd>

Albanisch

</dd> <dt>

1053 (0x41d)
</dt> <dd>

Schwedisch

</dd> <dt>

1054 (0x41e)
</dt> <dd>

Thailändisch

</dd> <dt>

1055 (0x41f)
</dt> <dd>

Türkisch

</dd> <dt>

1056 (0x420)
</dt> <dd>

Urdu

</dd> <dt>

1057 (0x421)
</dt> <dd>

Indonesisch

</dd> <dt>

1058 (0x422)
</dt> <dd>

Ukrainisch

</dd> <dt>

1059 (0x423)
</dt> <dd>

Belarussisch

</dd> <dt>

1060 (0x424)
</dt> <dd>

Slowenisch

</dd> <dt>

1061 (0x425)
</dt> <dd>

Estnisch

</dd> <dt>

1062 (0x426)
</dt> <dd>

Lettisch

</dd> <dt>

1063 (0x427)
</dt> <dd>

Litauisch

</dd> <dt>

1065 (0x429)
</dt> <dd>

Persisch

</dd> <dt>

1066 (0x42a)
</dt> <dd>

Vietnamesisch

</dd> <dt>

1069 (0x42d)
</dt> <dd>

Baskisch (Baskenland)

</dd> <dt>

1070 (0x42e)
</dt> <dd>

Serbisch

</dd> <dt>

1071 (0x42f)
</dt> <dd>

Mazedonisch (Nordmazedonien)

</dd> <dt>

1072 (0x430)
</dt> <dd>

Sutu

</dd> <dt>

1073 (0x431)
</dt> <dd>

Tsonga

</dd> <dt>

1074 (0x432)
</dt> <dd>

Tswana

</dd> <dt>

1076 (0x434)
</dt> <dd>

Xhosa

</dd> <dt>

1077 (0x435)
</dt> <dd>

Zulu

</dd> <dt>

1078 (0x436)
</dt> <dd>

Afrikaans

</dd> <dt>

1080 (0x438)
</dt> <dd>

Faeroese

</dd> <dt>

1081 (0x439)
</dt> <dd>

Hindi

</dd> <dt>

1082 (0x43a)
</dt> <dd>

Maltesisch

</dd> <dt>

1084 (0x43c)
</dt> <dd>

Schottisches Gälisch (Vereinigtes Königreich)

</dd> <dt>

1085 (0x43d)
</dt> <dd>

Jiddisch

</dd> <dt>

1086 (0x43e)
</dt> <dd>

Malaiisch – Malaysia

</dd> <dt>

2049 (0x801)
</dt> <dd>

Arabisch – Irak

</dd> <dt>

2052 (0x804)
</dt> <dd>

Chinesisch (vereinfacht) – Volksrepublik China

</dd> <dt>

2055 (0x807)
</dt> <dd>

Deutsch – Schweiz

</dd> <dt>

2057 (0x809)
</dt> <dd>

Englisch – Vereinigtes Königreich

</dd> <dt>

2058 (0x80a)
</dt> <dd>

Spanisch – Mexiko

</dd> <dt>

2060 (0x80c)
</dt> <dd>

Französisch – Belgien

</dd> <dt>

2064 (0x810)
</dt> <dd>

Italienisch – Schweiz

</dd> <dt>

2067 (0x813)
</dt> <dd>

Niederländisch – Belgien

</dd> <dt>

2068 (0x814)
</dt> <dd>

Norwegisch – Nynorsk

</dd> <dt>

2070 (0x816)
</dt> <dd>

Portugiesisch (Portugal)

</dd> <dt>

2072 (0x818)
</dt> <dd>

Rumänisch – Republik Moldau

</dd> <dt>

2073 (0x819)
</dt> <dd>

Russisch – Republik Moldau

</dd> <dt>

2074 (0x81a)
</dt> <dd>

Serbisch – lateinisch

</dd> <dt>

2077 (0x81d)
</dt> <dd>

Schwedisch – Finnland

</dd> <dt>

3073 (0xc01)
</dt> <dd>

Arabisch – Ägypten

</dd> <dt>

3076 (0xc04)
</dt> <dd>

Chinesisch (traditionell) – Hongkong SAR

</dd> <dt>

3079 (0xc07)
</dt> <dd>

Deutsch – Österreich

</dd> <dt>

3081 (0xc09)
</dt> <dd>

Englisch – Australien

</dd> <dt>

3082 (0xc0a)
</dt> <dd>

Spanisch – internationale Sortierung

</dd> <dt>

3084 (0xc0c)
</dt> <dd>

Französisch – Kanada

</dd> <dt>

3098 (0xc1a)
</dt> <dd>

Serbisch – Kyrillisch

</dd> <dt>

4097 (0x1001)
</dt> <dd>

Arabisch – Libyen

</dd> <dt>

4100 (0x1004)
</dt> <dd>

Chinesisch (vereinfacht) – Singapur

</dd> <dt>

4103 (0x1007)
</dt> <dd>

Deutsch – Luxemburg

</dd> <dt>

4105 (0x1009)
</dt> <dd>

Englisch – Kanada

</dd> <dt>

4106 (0x100a)
</dt> <dd>

Spanisch – Guatemala

</dd> <dt>

4108 (0x100c)
</dt> <dd>

Französisch – Schweiz

</dd> <dt>

5121 (0x1401)
</dt> <dd>

Arabisch – Algerien

</dd> <dt>

5127 (0x1407)
</dt> <dd>

Deutsch – Liechtenstein

</dd> <dt>

5129 (0x1409)
</dt> <dd>

Englisch – Neuseeland

</dd> <dt>

5130 (0x140a)
</dt> <dd>

Spanisch – Costa Rica

</dd> <dt>

5132 (0x140c)
</dt> <dd>

Französisch – Luxemburg

</dd> <dt>

6145 (0x1801)
</dt> <dd>

Arabisch – Marokko

</dd> <dt>

6153 (0x1809)
</dt> <dd>

Englisch – Irland

</dd> <dt>

6154 (0x180a)
</dt> <dd>

Spanisch – Panama

</dd> <dt>

7169 (0x1c01)
</dt> <dd>

Arabisch – Tunesien

</dd> <dt>

7177 (0x109)
</dt> <dd>

Englisch – Südafrika

</dd> <dt>

7178 (0x1c0a)
</dt> <dd>

Spanisch – Dominikanische Republik

</dd> <dt>

8193 (0x2001)
</dt> <dd>

Arabisch – Oman

</dd> <dt>

8201 (0x2009)
</dt> <dd>

Englisch – Jamaika

</dd> <dt>

8202 (0x200a)
</dt> <dd>

Spanisch – Venezuela

</dd> <dt>

9217 (0x2401)
</dt> <dd>

Arabisch – Jemen

</dd> <dt>

9226 (0x240 a)
</dt> <dd>

Spanisch – Kolumbien

</dd> <dt>

10241 (0x2801)
</dt> <dd>

Arabisch – Syrien

</dd> <dt>

10249 (0x2809)
</dt> <dd>

Englisch – Belize

</dd> <dt>

10250 (0x280a)
</dt> <dd>

Spanisch – Peru

</dd> <dt>

11265 (0x2c01)
</dt> <dd>

Arabisch – Jordanien

</dd> <dt>

11273 (0x2c09)
</dt> <dd>

Englisch – Trinidad

</dd> <dt>

11274 (0x2c0a)
</dt> <dd>

Spanisch – Argentinien

</dd> <dt>

12289 (0x3001)
</dt> <dd>

Arabisch – Libanon

</dd> <dt>

12298 (0x300a)
</dt> <dd>

Spanisch – Ecuador

</dd> <dt>

13313 (0x3401)
</dt> <dd>

Arabisch – Kuwait

</dd> <dt>

13322 (0x340a)
</dt> <dd>

Spanisch – Chile

</dd> <dt>

14337 (0x3801)
</dt> <dd>

Arabisch – Vereinigte Arabische Emirate

</dd> <dt>

14346 (0x380a)
</dt> <dd>

Spanisch – Uruguay

</dd> <dt>

15361 (0x3c01)
</dt> <dd>

Arabisch – Bahrain

</dd> <dt>

15370 (0x3c0a)
</dt> <dd>

Spanisch – Paraguay

</dd> <dt>

16385 (0x4001)
</dt> <dd>

Arabisch – Katar

</dd> <dt>

16394 (0x400a)
</dt> <dd>

Spanisch – Bolivien

</dd> <dt>

17418 (0x440 a)
</dt> <dd>

Spanisch – El Salvador

</dd> <dt>

18442 (0x480a)
</dt> <dd>

Spanisch – Honduras

</dd> <dt>

19466 (0x4c0a)
</dt> <dd>

Spanisch – Nicaragua

</dd> <dt>

20490 (0x500a)
</dt> <dd>

Spanisch – Puerto Rico

</dd> </dl>

</dd> <dt>

**OSProductSuite**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ PRODUCTOPTIONS \| ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business (restricted)", "Embedded NT", "Data Center")
</dt> </dl>

Installierte und lizenzierte Systemprodukt Erweiterungen für das Betriebssystem. Der Wert 146 (0x92) für **OSProductSuite** zeigt beispielsweise Enterprise, Terminal Services und das Rechenzentrum (Bits 1, vier und sieben) an. In der folgenden Liste sind die möglichen Werte aufgeführt.

<dt>

1 (0x1)
</dt> <dd>

Microsoft Small Business Server wurde installiert, kann jedoch auf eine andere Version von Windows aktualisiert werden.

</dd> <dt>

2 (0x2)
</dt> <dd>

Windows Server 2008 Enterprise ist installiert.

</dd> <dt>

4 (0x4)
</dt> <dd>

Windows BackOffice-Komponenten werden installiert.

</dd> <dt>

8 (0x8)
</dt> <dd>

Der Kommunikations Server ist installiert.

</dd> <dt>

16 (0x10)
</dt> <dd>

Terminal Dienste sind installiert.

</dd> <dt>

32 (0x20)
</dt> <dd>

Microsoft Small Business Server wird mit der eingeschränkten Client Lizenz installiert.

</dd> <dt>

64 (0x40)
</dt> <dd>

Windows Embedded ist installiert.

</dd> <dt>

128 (0x80)
</dt> <dd>

Eine Datacenter Edition ist installiert.

</dd> <dt>

256 (0x100)
</dt> <dd>

Terminal Dienste sind installiert, es wird jedoch nur eine interaktive Sitzung unterstützt.

</dd> <dt>

512 (0x200)
</dt> <dd>

Windows Home Edition ist installiert.

</dd> <dt>

1024 (0x400)
</dt> <dd>

Die Webserver Edition ist installiert.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Storage Server Edition ist installiert.

</dd> <dt>

16384 (0x4000)
</dt> <dd>

Compute Cluster Edition ist installiert.

</dd> </dl>

</dd> <dt>

**OSType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md)".**OtherTypeDescription**")
</dt> </dl>

Typ des Betriebssystems. In der folgenden Liste sind die möglichen Werte aufgeführt.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span id="MACOS"></span><span id="macos"></span>**MacOS** (2)


</dt> <dd>

Gruppieren

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span id="AIX"></span><span id="aix"></span>**AIX** (9)


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span id="MVS"></span><span id="mvs"></span>**MVS** (10)


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span id="OS400"></span><span id="os400"></span>**OS400** (11)


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span id="WIN95"></span><span id="win95"></span>**Win95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**Win98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**WinCE** (19)


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span id="OSF"></span><span id="osf"></span>**OSF** (22)


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span id="IRIX"></span><span id="irix"></span>**IRIX** (28)


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)


</dt> <dd>

Solaris

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span id="LINUX"></span><span id="linux"></span>**Linux** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span id="OS9"></span><span id="os9"></span>**OS9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span id="QNX"></span><span id="qnx"></span>**QNX** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span id="OS_390"></span><span id="os_390"></span>**Betriebssystem/390** (60)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span id="VSE"></span><span id="vse"></span>**VSE** (61)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span id="TPF"></span><span id="tpf"></span>**TPF** (62)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")
</dt> </dl>

Zusätzliche Beschreibung der aktuellen Betriebssystemversion.

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die physischen Adress Erweiterungen (PE) durch das Betriebssystem aktiviert werden, das auf Intel-Prozessoren ausgeführt wird. Mithilfe von "PE" können Anwendungen mehr als 4 GB physischen Arbeitsspeicher adressieren. Wenn "PE" aktiviert ist, verwendet das Betriebssystem die dreistufige lineare Adressübersetzung anstelle von zwei Ebenen. Durch die Bereitstellung von mehr physischem Arbeitsspeicher für eine Anwendung entfällt die Notwendigkeit, Arbeitsspeicher in der Auslagerungs Datei auszutauschen und die Leistung Verwenden Sie zum Aktivieren von, den Schalter "/PAE-Schalter" in der Boot.ini-Datei. Weitere Informationen zur Funktion für die physische Adress Erweiterung finden Sie unter <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .

</dd> <dt>

**PlusProductID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus! ProductID ")
</dt> </dl>

Wird nicht unterstützt.

</dd> <dt>

**Plusversionnumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus! VersionNumber ")
</dt> </dl>

Wird nicht unterstützt.

</dd> <dt>

**Portableoperatingsystem**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Betriebssystem von einem externen USB-Gerät gestartet wurde. True gibt an, dass das Betriebssystem auf einem unterstützten lokal verbundenen Speichergerät gestartet wird.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 8 und Windows Server 2012 nicht unterstützt.

</dd> <dt>

**Primärer Server/verwaltete Instanz**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Gibt an, ob dies das primäre Betriebssystem ist.

</dd> <dt>

**ProductType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Systeminformationen.

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

**Arbeits Station** (1)


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

**Domänen Controller** (2)


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Server** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Quantum length**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ prioritycontrol \| Win32PrioritySeparation")
</dt> </dl>

Nicht unterstützt

* * Windows Server 2008 und Windows Vista: * *

Die **QuantumLength** -Eigenschaft definiert die Anzahl der Takt Ticks pro Quantum. Ein Quantum ist eine Einheit der Ausführungszeit, die dem Scheduler vor dem Wechsel zu anderen Anwendungen zur Verfügung gestellt werden darf. Wenn ein Thread ein Quantum ausführt, entfernt der Kernel ihn vorzeitig und verschiebt ihn an das Ende einer Warteschlange für Anwendungen mit gleicher Priorität. Die tatsächliche Länge des Quantums eines Threads variiert auf verschiedenen Windows-Plattformen. Nur für Windows NT/Windows 2000.

Mögliche Werte sind.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

**Ein Tick** (1)


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

**Zwei Ticks** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Quantum Type**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht unterstützt

* * Windows Server 2008 und Windows Vista: * *

Die **quantumschlag** -Eigenschaft gibt die Quantums mit fester oder variabler Länge an. Windows ist standardmäßig auf Quanten mit variabler Länge festgelegt, wobei die Vordergrund Anwendung ein längeres Quantum als die Hintergrundanwendungen hat. Windows Server ist standardmäßig auf Quantums mit fester Länge eingestellt. Ein Quantum ist eine Einheit der Ausführungszeit, die dem Scheduler vor dem Wechsel zu einer anderen Anwendung erteilt werden darf. Wenn ein Thread ein Quantum ausführt, entfernt der Kernel ihn vorzeitig und verschiebt ihn an das Ende einer Warteschlange für Anwendungen mit gleicher Priorität. Die tatsächliche Länge des Quantums eines Threads variiert auf verschiedenen Windows-Plattformen.

Mögliche Werte sind.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Korrigiert** (1)


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

**Variable** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**RegisteredUser**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| RegisteredOwner")
</dt> </dl>

Der Name des registrierten Benutzers des Betriebssystems.

Beispiel: "Ben Smith"

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductID")
</dt> </dl>

Serielle Identifikationsnummer des Betriebssystem Produkts.

Beispiel: "10497-OEM-0031416-71674"

</dd> <dt>

**ServicePackMajorVersion**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")
</dt> </dl>

Die Hauptversionsnummer der Service Pack, die auf dem Computersystem installiert ist. Wenn keine Service Pack installiert wurde, ist der Wert 0 (null).

</dd> <dt>

**ServicePackMinorVersion**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")
</dt> </dl>

Die neben Versionsnummer der Service Pack, die auf dem Computersystem installiert ist. Wenn keine Service Pack installiert wurde, ist der Wert 0 (null).

</dd> <dt>

**SizeStoredInPagingFiles**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| System Arbeitsspeicher-Einstellungen \| 001,3 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Kilobyte ")
</dt> </dl>

Gesamtanzahl von Kilobyte, die in den Paging-Dateien des Betriebssystems gespeichert werden können – 0 (null) gibt an, dass keine Auslagerungs Dateien vorhanden sind. Beachten Sie, dass diese Zahl nicht die tatsächliche physische Größe der Auslagerungs Datei auf dem Datenträger darstellt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein intelligent-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber prognostiziert einen Fehler in naher Zukunft). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der Dienststatus gilt für administrative Aufgaben, z. b. die Spiegelung eines Datenträgers, das erneute Laden einer Benutzer Berechtigungs Liste oder andere administrative Aufgaben. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> <dt>

**Suitemask**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, BackOffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")
</dt> </dl>

Bitflags, die die im System verfügbaren Produkt Suites identifizieren.

Wenn Sie z. b. "Personal" und "BackOffice" angeben möchten, legen Sie **suitemask** auf `4 | 512` oder fest `516` .

<dt>

1
</dt> <dd>

Kleinunternehmen

</dd> <dt>

2
</dt> <dd>

Enterprise

</dd> <dt>

4
</dt> <dd>

Back Office

</dd> <dt>

8
</dt> <dd>

Kommunikation

</dd> <dt>

16
</dt> <dd>

Terminaldienste

</dd> <dt>

32
</dt> <dd>

Kleinunternehmen eingeschränkt

</dd> <dt>

64
</dt> <dd>

Embedded Edition

</dd> <dt>

128
</dt> <dd>

Datacenter Edition

</dd> <dt>

256
</dt> <dd>

Einzelner Benutzer

</dd> <dt>

512
</dt> <dd>

Home Edition

</dd> <dt>

1024
</dt> <dd>

Webserver Edition

</dd> </dl>

</dd> <dt>

**SystemDevice**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Registry functions \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| path \| TargetDevice")
</dt> </dl>

Die physische Datenträger Partition, auf der das Betriebssystem installiert ist.

</dd> <dt>

**System Directory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))
</dt> </dl>

System Verzeichnis des Betriebssystems.

Beispiel: "C: \\ Windows \\ system32"

</dd> <dt>

**SystemDrive**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Buchstabe des Laufwerks, auf dem sich das Betriebssystem befindet. Beispiel: "C:"

</dd> <dt>

**Totaltauapspacesize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Gesamter Auslagerungs Bereich in Kilobyte. Dieser Wert kann **null** (nicht angegeben) sein, wenn der Auslagerungs Bereich nicht von den Auslagerungs Dateien unterschieden wird. Allerdings unterscheiden einige Betriebssysteme diese Konzepte. Beispielsweise können in UNIX gesamte Prozesse ausgetauscht werden, wenn die freie Seitenliste sinkt und unter dem angegebenen Betrag liegt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Totalvirtualmemorysize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Die Zahl des virtuellen Arbeitsspeichers in Kilobyte. Dies kann z. b. durch Hinzufügen des Gesamt RAM zur Größe des Auslagerungs Raums berechnet werden, d. h. durch Hinzufügen der Menge an Arbeitsspeicher, die vom Computersystem der Eigenschaft **SizeStoredInPagingFiles** hinzugefügt oder aggregiert wird.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**TotalVisibleMemorySize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")
</dt> </dl>

Gesamtmenge des für das Betriebssystem verfügbaren physischen Speichers in Kilobyte. Dieser Wert gibt nicht notwendigerweise die tatsächliche Menge an physischem Speicher an, sondern dem Betriebssystem als verfügbar gemeldet wird.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Version"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")
</dt> </dl>

Versionsnummer des Betriebssystems.

Beispiel: "4,0"

</dd> <dt>

**WindowsDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")
</dt> </dl>

Windows-Verzeichnis des Betriebssystems.

Beispiel: "C: \\ Windows"

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ OperatingSystem** -Klasse wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)abgeleitet.

Jedes Betriebssystem, das auf einem Computer installiert werden kann, auf dem ein Windows-basiertes Betriebssystem ausgeführt werden kann, ist ein Nachfolger oder Mitglied dieser Klasse. **Win32 \_ "OperatingSystem** " ist eine Singleton-Klasse. Um die einzelne Instanz zu erhalten, verwenden Sie "@" für den Schlüssel.

Im Gegensatz zu den meisten anderen WMI-Klassen, die von Mgmtclassgen generiert werden, gibt die **OperatingSystem. kreateinstance**()-Methode ein leeres **OperatingSystem** -Objekt zurück. Wenn Sie also C \# mit Mgmtclassgen verwenden, können Sie den folgenden Code verwenden:


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a>Beispiele

Ein VBScript-Beispiel, das Betriebssystem-und Prozessor Daten von [**Win32 \_ Computersystem**](win32-computersystem.md), [**Win32 \_ Processor**](win32-processor.md)und **Win32 \_ OperatingSystem** erhält, finden Sie in den Beispielen für das [**Win32- \_ Prozessor**](win32-processor.md) Thema.

Im Beispiel " [Generieren von Exchange-Umgebungs Berichten mithilfe von PowerShell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell" in der TechNet Gallery wird eine **Win32- \_ OperatingSystem** -Klasse als Teil einer größeren Anwendung verwendet, um Exchange-Umgebungs Berichte zu generieren.

Das Beispiel [Server-Betriebszeit mithilfe von WMI (Server Betriebszeit](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) ) in der TechNet Gallery verwendet die **LastBootUpTime** -Eigenschaft, um zu bestimmen, wie lange der Server aktiv war. Im Beispiel wird auch die Timeout Option verwendet, um sicherzustellen, dass der WMI-Befehl nicht reagiert.

Das VBScript-Codebeispiel für den [WMI-Informations](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) Abruf in der TechNet-Galerie verwendet die **Win32- \_ OperatingSystem** -Klasse, um Betriebssysteminformationen von einer Reihe von Remote Computern abzurufen.

Das folgende Skript ruft die Instanzen des **Win32- \_ OperatingSystems** im Standard \\ Namespace "root CIMv2" ab und zeigt dann Informationen zum Betriebssystem an.


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



Im folgenden PowerShell-Codebeispiel werden alle Betriebsinformationen zum aktuellen Betriebssystem angezeigt.


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
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

[**CIM- \_ OperatingSystem**](cim-operatingsystem.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[WMI-Tasks: Betriebssysteme](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[WMI-Tasks: Computer Hardware](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[WMI-Tasks: Desktop Verwaltung](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
