---
description: Stellt ein Windows auf einem Computer installiertes Betriebssystem dar.
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
ms.openlocfilehash: a1df0da4cadf0cd610803b2f456f22049471b28bc5653bc400f4c730cb0c47de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972530"
---
# <a name="win32_operatingsystem-class"></a>Win32 \_ OperatingSystem-Klasse

Die **WMI-Klasse Win32 \_ OperatingSystem** stellt ein Windows auf einem Computer installiertes Betriebssystem dar. [](../wmisdk/retrieving-a-class.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

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

Die **Win32 \_ OperatingSystem-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ OperatingSystem-Klasse** verfügt über diese Methoden.



| Methode                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Neustart**](reboot-method-in-class-win32-operatingsystem.md)                             | Fährt das Computersystem herunter und startet es dann neu.<br/>                                                                                                                                                                                                           |
| [**SetDateTime**](setdatetime-method-in-class-win32-operatingsystem.md)                   | Ermöglicht das Festlegen von Datum und Uhrzeit des Computers.<br/>                                                                                                                                                                                                                |
| [**Herunterfahren**](shutdown-method-in-class-win32-operatingsystem.md)                         | Entlädt Programme und DLLs an den Punkt, an dem der Computer sicher ausgeschaltet werden kann.<br/>                                                                                                                                                                           |
| [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)               | Stellt alle Optionen zum Herunterfahren zur Verfügung, die von Windows unterstützt werden.<br/>                                                                                                                                                                           |
| [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | Stellt die gleichen Optionen zum Herunterfahren zur Verfügung, die von der [**Win32Shutdown-Methode**](win32shutdown-method-in-class-win32-operatingsystem.md) in **Win32 \_ OperatingSystem** unterstützt werden. Sie können aber auch Kommentare, einen Grund für das Herunterfahren oder ein Timeout angeben.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ OperatingSystem-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BootDevice**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| DRIVE MAP INFO \_ \_ \| btInt13Unit")
</dt> </dl>

Name des Laufwerks, von dem Windows Betriebssystem gestartet wird.

Beispiel: \\ \\ "Device \\ Harddisk0"

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Systeminformationen Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")
</dt> </dl>

Buildnummer eines Betriebssystems. Sie kann für genauere Versionsinformationen als Produktversionsversionsnummern verwendet werden.

Beispiel: "1381"

</dd> <dt>

**BuildType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows \\ \\ \\ \\ \\ \\ CurrentVersion \| CurrentType")
</dt> </dl>

Buildtyp, der für ein Betriebssystem verwendet wird.

Beispiele: ""retail build"", ""checked build""

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des -Objekts– eine einzeilenbasierte Zeichenfolge. Die Zeichenfolge enthält die Betriebssystemversion. Beispiel: "Microsoft Windows 7 Enterprise". Diese Eigenschaft kann lokalisiert werden.

**Windows Vista und Windows 7:** Diese Eigenschaft kann nach folgende Zeichen enthalten. Beispielsweise kann die Zeichenfolge "Microsoft Windows 7 Enterprise" (nach dem Leerzeichen eingeschlossen) erforderlich sein, um Informationen mithilfe dieser Eigenschaft abzurufen.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ IDEFAULTANSICODEPAGE")
</dt> </dl>

Codepagewert, den ein Betriebssystem verwendet. Eine Codepage enthält eine Zeichentabelle, die ein Betriebssystem verwendet, um Zeichenfolgen für verschiedene Sprachen zu übersetzen. Im American National Standards Institute (ANSI) werden Werte aufgeführt, die definierte Codepages darstellen. Wenn ein Betriebssystem keine ANSI-Codepage verwendet, wird dieser Member auf 0 (null) festgelegt. Die **CodeSet-Zeichenfolge** kann maximal sechs Zeichen verwenden, um den Codepagewert zu definieren.

Beispiel: "1255"

</dd> <dt>

**Countrycode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ ICOUNTRY")
</dt> </dl>

Code für das Land/die Region, das bzw. die ein Betriebssystem verwendet. Die Werte basieren auf Präfixen für internationale Telefonwahlen, die auch als IBM-Länder-/-Region-Codes bezeichnet werden. Diese Eigenschaft kann maximal sechs Zeichen verwenden, um den Länder-/Regioncodewert zu definieren.

Beispiel: "1" (USA)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**\_ CIM-Schlüssel,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Name der ersten konkreten Klasse, die in der Vererbungskette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird vom [**\_ CIM-Betriebssystem geerbt.**](cim-operatingsystem.md)

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ CIM-Schlüssel,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Name der Erstellungsklasse des Bereichscomputersystems.

Diese Eigenschaft wird vom [**\_ CIM-Betriebssystem geerbt.**](cim-operatingsystem.md)

</dd> <dt>

**CSDVersion**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Systeminformationen Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")
</dt> </dl>

**Mit NULL** beendete Zeichenfolge, die das neueste auf einem Computer installierte Service Pack angibt. Wenn kein Service Pack installiert ist, ist die Zeichenfolge **NULL.**

Beispiel: "Service Pack 3"

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**\_ CIM-Schlüssel,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Name des Bereichscomputersystems.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")
</dt> </dl>

Zahl: In Minuten wird ein Betriebssystem von greenwich mean time (GMT) versetzt. Die Zahl ist positiv, negativ oder null.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**DataExecutionPrevention \_ 32BitApplications**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Wenn das Hardwarefeature zur Verhinderung der Datenausführung verfügbar ist, gibt diese Eigenschaft an, dass das Feature für 32-Bit-Anwendungen verwendet werden kann, wenn **true ist.** Auf 64-Bit-Computern wird das Feature zur Verhinderung der Datenausführung im [Startkonfigurationsdaten(BCD)-Speicher](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) konfiguriert, und die Eigenschaften in **Win32 \_ OperatingSystem** werden entsprechend festgelegt.

</dd> <dt>

**DataExecutionPrekonvention \_ verfügbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Die Verhinderung der Datenausführung ist ein Hardwarefeature, um Pufferüberlaufangriffe zu verhindern, indem die Ausführung von Code auf Datenspeicherseiten beendet wird. True gibt an, dass dieses Feature verfügbar ist. Auf 64-Bit-Computern wird das Feature zur Verhinderung der Datenausführung im BCD-Speicher konfiguriert, und die Eigenschaften in **Win32 \_ OperatingSystem** werden entsprechend festgelegt.

</dd> <dt>

**DataExecutionPrekonvention-Treiber \_**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Wenn das Hardwarefeature zur Verhinderung der Datenausführung verfügbar ist, gibt diese Eigenschaft an, dass das Feature für Treiber funktioniert, wenn **true lautet.** Auf 64-Bit-Computern wird das Feature zur Verhinderung der Datenausführung im BCD-Speicher konfiguriert, und die Eigenschaften in **Win32 \_ OperatingSystem** werden entsprechend festgelegt.

</dd> <dt>

**DataExecutionPrelation \_ SupportPolicy**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Gibt an, welche Dep-Einstellung (Datenausführungsverhinderung) angewendet wird. Die DEP-Einstellung gibt den Umfang an, in dem DEP für 32-Bit-Anwendungen auf dem System gilt. DEP wird immer auf den Windows Kernel angewendet.

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)


</dt> <dd>

DEP ist für alle 32-Bit-Anwendungen auf dem Computer ohne Ausnahmen deaktiviert. Diese Einstellung ist für die Benutzeroberfläche nicht verfügbar.

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)


</dt> <dd>

DEP ist für alle 32-Bit-Anwendungen auf dem Computer aktiviert. Diese Einstellung ist für die Benutzeroberfläche nicht verfügbar.

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt-In** (2)


</dt> <dd>

DEP ist für eine begrenzte Anzahl von Binärdateien, den Kernel und alle Windows-basierten Dienste aktiviert. Es ist jedoch standardmäßig für alle 32-Bit-Anwendungen deaktiviert. Ein Benutzer oder Administrator muss explizit entweder den **Always On** oder die Einstellung **Abmelden** auswählen, bevor DEP auf 32-Bit-Anwendungen angewendet werden kann.

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Deaktivieren** (3)


</dt> <dd>

DEP ist standardmäßig für alle 32-Bit-Anwendungen aktiviert. Ein Benutzer oder Administrator kann die Unterstützung für eine 32-Bit-Anwendung explizit entfernen, indem er die Anwendung einer Ausnahmenliste hinzufügt.

</dd> </dl>

</dd> <dt>

**Debuggen**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ DEBUG")
</dt> </dl>

Das Betriebssystem ist ein aktivierter Build (Debugbuild). **True** gibt an, dass die Debugversion installiert ist. Überprüfte Builds bieten Fehlerüberprüfung, Argumentüberprüfung und Systemdebuggingcode. Zusätzlicher Code in einer überprüften Binärdatei generiert eine Kerneldebugger-Fehlermeldung und unterbricht den Debugger. Dies hilft, die Ursache und position des Fehlers sofort zu bestimmen. Die Leistung kann in einem überprüften Build aufgrund des zusätzlichen Ausgeführten Codes beeinträchtigt werden.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Überschreiben**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Beschreibung des Windows Betriebssystems. Einige Benutzeroberflächen, z. B. benutzeroberflächen, die die Bearbeitung dieser Beschreibung ermöglichen, beschränken die Länge auf 48 Zeichen.

</dd> <dt>

**Verteilt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das Betriebssystem auf mehrere Computersystemknoten verteilt ist. Wenn ja, sollten diese Knoten als Cluster gruppiert werden.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**EncryptionLevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verschlüsselungsebene für sichere Transaktionen: 40-Bit, 128-Bit oder *n-Bit.*

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

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

Die Vordergrundanwendung erhält eine höhere Priorität. Die Anwendungsstärkung wird implementiert, indem einer Anwendung mehr Slices für die Ausführungszeit (Quantenlängen) zurZeit gegeben werden.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)


</dt> <dd>

Das System erhöht die Quantenlänge um 6.

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)


</dt> <dd>

Das System erhöht die Quantenlänge um 12.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)


</dt> <dd>

Das System erhöht die Quantenlänge um 18.

</dd> </dl>

</dd> <dt>

**FreePhysicalMemory**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobytes")
</dt> </dl>

Anzahl des derzeit nicht verwendeten und verfügbaren physischen Arbeitsspeichers in Kilobyte.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**FreeSpaceInPagingFiles**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|DMTF-Systemspeicher Einstellungen \| 001.4"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobytes")
</dt> </dl>

Anzahl in Kilobyte, die den Auslagerungsdateien des Betriebssystems zugeordnet werden kann, ohne dass andere Seiten ausgetauscht werden.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**FreeVirtualMemory**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobytes")
</dt> </dl>

Anzahl des derzeit nicht verwendeten und verfügbaren virtuellen Arbeitsspeichers in Kilobyte.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Installationsdatum")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**LargeSystemCache**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Diese Eigenschaft ist veraltet und wird nicht unterstützt.

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimieren für Anwendungen** (0)


</dt> <dd>

Optimieren des Arbeitsspeichers für Anwendungen.

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimieren der Systemleistung** (1)


</dt> <dd>

Optimieren sie den Arbeitsspeicher für die Systemleistung.

</dd> </dl>

</dd> <dt>

**LastBootUpTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit des letzten Neustarts des Betriebssystems.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**LocalDateTime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemDate", "MIF. \|DMTF General Information \| 001.6")
</dt> </dl>

Betriebssystemversion des lokalen Datums und der Uhrzeit.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Gebietsschema**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ ILANGUAGE")
</dt> </dl>

Der vom Betriebssystem verwendete Sprachbezeichner. Ein Sprachbezeichner ist eine standardmäßige internationale numerische Abkürzung für ein Land/eine Region. Jede Sprache verfügt über einen eindeutigen Sprachbezeichner (LANGID), einen 16-Bit-Wert, der aus einem primären Sprachbezeichner und einem sekundären Sprachbezeichner besteht.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Name des Betriebssystemherstellers. Bei Windows-basierten Systemen ist dieser Wert "Microsoft Corporation".

</dd> <dt>

**MaxNumberOfProcesses**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemMaxProcesses")
</dt> </dl>

Maximale Anzahl von Prozesskontexten, die das Betriebssystem unterstützen kann. Der vom Anbieter festgelegte Standardwert ist 4294967295 (0xFFFFFFFF). Wenn kein fester Maximalwert vorhanden ist, sollte der Wert 0 (null) sein. Auf Systemen mit einem festen Höchstwert kann dieses Objekt helfen, Fehler zu diagnostizieren, die auftreten, wenn der Höchstwert erreicht wird. Geben Sie bei Unbekanntem 4294967295 (0xFFFFFFFF) ein.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**MaxProcessMemorySize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobytes")
</dt> </dl>

Maximale Anzahl von Arbeitsspeicher in Kilobytes, die einem Prozess zugeordnet werden können. Bei Betriebssystemen ohne virtuellen Arbeitsspeicher entspricht dieser Wert in der Regel der Gesamtmenge des physischen Arbeitsspeichers abzüglich des vom BIOS und dem Betriebssystem verwendeten Arbeitsspeichers. Bei einigen Betriebssystemen kann dieser Wert unendlich sein. In diesem Fall sollte 0 (null) eingegeben werden. In anderen Fällen kann dieser Wert eine Konstante sein, z. B. 2G oder 4G.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**UALanguages**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

mehrsprachige Benutzeroberfläche Packsprachen (MUI Pack ), die auf dem Computer installiert sind. Beispiel: "en-us". MUI Pack Sprachen sind Ressourcendateien, die unter der englischen Version des Betriebssystems installiert werden können. Wenn ein MUI Pack installiert ist, können Sie die Sprache der Benutzeroberfläche in eine von 33 unterstützten Sprachen ändern.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Betriebssysteminstanz innerhalb eines Computersystems.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**NumberOfLicensedUsers**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Benutzerlizenzen für das Betriebssystem. Wenn unbegrenzt, geben Sie 0 (null) ein. Falls unbekannt, geben Sie -1 ein.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**NumberOfProcesses**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemProcesses")
</dt> </dl>

Anzahl der Prozesskontexte, die derzeit auf dem Betriebssystem geladen oder ausgeführt werden.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**NumberOfUsers**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemNumUsers")
</dt> </dl>

Anzahl der Benutzersitzungen, für die das Betriebssystem derzeit Zustandsinformationen speichert.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**OperatingSystemSKU**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

SKU-Nummer (Stock Keeping Unit) für das Betriebssystem. Diese Werte sind identisch mit den **PRODUCT \_ \** _-Konstanten, die in WinNT.h definiert sind und mit der [*_GetProductInfo-Funktion verwendet* *](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) werden.

In der folgenden Liste sind mögliche SKU-Werte aufgeführt.

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODUKT \_ UNDEFINED** (0)


</dt> <dd>

Nicht definiert

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODUKT \_ ULTIMATE** (1)


</dt> <dd>

Ultimate Edition, z.B. Windows Vista Ultimate.

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODUKT \_ HOME \_ BASIC** (2)


</dt> <dd>

Home Basic Edition

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODUKT \_ HOME \_ PREMIUM** (3)


</dt> <dd>

Home Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODUKT \_ ENTERPRISE** (4)


</dt> <dd>

Enterprise

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODUKT \_ BUSINESS** (6)


</dt> <dd>

Business Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODUKT \_ STANDARD \_ SERVER** (7)


</dt> <dd>

Windows Server Standard Edition (Installation der Desktoperfahrung)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODUKT \_ DATACENTER \_ SERVER** (8)


</dt> <dd>

Windows Server Datacenter Edition (Installation der Desktoperfahrung)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODUKT \_ SMALLBUSINESS \_ SERVER** (9)


</dt> <dd>

Small Business Server Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODUKT \_ ENTERPRISE \_ SERVER** (10)


</dt> <dd>

Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODUKT \_ STARTER** (11)


</dt> <dd>

 Starter Edition

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODUKT \_ DATACENTER \_ SERVER \_ CORE** (12)


</dt> <dd>

Datacenter Server Core Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODUKT \_ STANDARD \_ SERVER \_ CORE** (13)


</dt> <dd>

Standard Server Core Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODUKT \_ ENTERPRISE \_ SERVER \_ CORE** (14)


</dt> <dd>

Enterprise Server Core Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODUKT \_ WEBSERVER \_** (17)


</dt> <dd>

Web Server Edition

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODUKT \_ HOME \_ SERVER** (19)


</dt> <dd>

Home Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODUKT \_ STORAGE \_ EXPRESS \_ SERVER** (20)


</dt> <dd>

Storage Express Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODUKT \_ STORAGE \_ STANDARD \_ SERVER** (21)


</dt> <dd>

Windows Storage Server Standard Edition (Installation der Desktoperfahrung)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODUKT \_ STORAGE \_ WORKGROUP \_ SERVER** (22)


</dt> <dd>

Windows Storage Server Workgroup Edition (Installation der Desktoperfahrung)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODUKT \_ STORAGE \_ ENTERPRISE \_ SERVER** (23)


</dt> <dd>

Storage Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODUKT \_ SERVER \_ FOR \_ SMALLBUSINESS** (24)


</dt> <dd>

Server For Small Business Edition

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODUKT \_ SMALLBUSINESS \_ SERVER \_ PREMIUM** (25)


</dt> <dd>

Small Business Server Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODUKT \_ ENTERPRISE \_ N** (27)


</dt> <dd>

Windows Enterprise Edition

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODUKT \_ ULTIMATE \_ N** (28)


</dt> <dd>

Windows Ultimate Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODUKT \_ WEB \_ SERVER \_ CORE** (29)


</dt> <dd>

Windows Server Web Server Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODUKT \_ STANDARD \_ SERVER \_ V** (36)


</dt> <dd>

Windows Server Standard Edition ohne Hyper-V

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODUKT \_ DATACENTER \_ SERVER \_ V** (37)


</dt> <dd>

Windows Server Datacenter Edition ohne Hyper-V (vollständige Installation)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODUKT \_ ENTERPRISE \_ SERVER \_ V** (38)


</dt> <dd>

Windows Server Enterprise Edition ohne Hyper-V (vollständige Installation)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODUKT \_ DATACENTER \_ SERVER \_ CORE \_ V** (39)


</dt> <dd>

Windows Server Datacenter Edition ohne Hyper-V (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODUKT \_ STANDARD \_ SERVER \_ CORE \_ V** (40)


</dt> <dd>

Windows Server Standard Edition ohne Hyper-V (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODUKT \_ ENTERPRISE \_ SERVER \_ CORE \_ V** (41)


</dt> <dd>

Windows Server Enterprise Edition ohne Hyper-V (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODUKT \_ HYPERV** (42)


</dt> <dd>

Microsoft Hyper-V Server

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODUKT \_ STORAGE \_ EXPRESS \_ SERVER \_ CORE** (43)


</dt> <dd>

Storage Server Express Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODUKT \_ STORAGE \_ STANDARD \_ SERVER \_ CORE** (44)


</dt> <dd>

Storage Server Standard Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODUKT \_ STORAGE \_ WORKGROUP \_ SERVER \_ CORE** (45)


</dt> <dd>

Storage Server Workgroup Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODUKT \_ STORAGE \_ ENTERPRISE \_ SERVER \_ CORE** (46)


</dt> <dd>

Storage Server Workgroup Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODUKT \_ PROFESSIONAL** (48)


</dt> <dd>

Windows Professional

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODUKT \_ SB \_ SOLUTION \_ SERVER** (50)


</dt> <dd>

Windows Server Essentials (Installation der Desktoperfahrung)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODUKT \_ SMALLBUSINESS \_ SERVER \_ PREMIUM \_ CORE** (63)


</dt> <dd>

Small Business Server Premium (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODUKT \_ CLUSTERSERVER \_ \_ V** (64)


</dt> <dd>

Windows Computeclusterserver ohne Hyper-V

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODUKT \_ CORE \_ ARM** (97)


</dt> <dd>

Windows RT

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODUKT \_ CORE** (101)


</dt> <dd>

Windows Startseite

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODUKT \_ PROFESSIONAL \_ WMC** (103)


</dt> <dd>

Windows Professional mit Media Center

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODUKT \_ MOBILE \_ CORE** (104)


</dt> <dd>

Windows Mobile

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODUKT \_ IOTUAP** (123)


</dt> <dd>

Windows IoT Core (Internet der Dinge)

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODUKT \_ DATACENTER \_ NANO \_ SERVER** (143)


</dt> <dd>

Windows Server Datacenter Edition (Nano Server-Installation)

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODUKT \_ STANDARD \_ NANO \_ SERVER** (144)


</dt> <dd>

Windows Server Standard Edition (Nano Server-Installation)

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODUKT \_ DATACENTER \_ WS \_ SERVER \_ CORE** (147)


</dt> <dd>

Windows Server Datacenter Edition (Server Core-Installation)

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODUKT \_ STANDARD \_ WS \_ SERVER \_ CORE** (148)


</dt> <dd>

Windows Server Standard Edition (Server Core-Installation)

</dd> </dl>

</dd> <dt>

**Organisation**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows \\ \\ \\ \\ \\ \\ CurrentVersion \| RegisteredOrganization")
</dt> </dl>

Firmenname für den registrierten Benutzer des Betriebssystems.

Beispiel: "Microsoft Corporation"

</dd> <dt>

**OSArchitecture**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Architektur des Betriebssystems im Gegensatz zum Prozessor. Diese Eigenschaft kann lokalisiert werden.

Beispiel: 32-Bit

</dd> <dt>

**OSLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| DEFAULT Systemsteuerung International \\ \\ \\ \\ \| Locale")
</dt> </dl>

Sprachversion des installierten Betriebssystems. In der folgenden Liste sind die möglichen Werte aufgeführt. Beispiel: 0x0807 (Deutsch, Schweiz).

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

Arabisch – Vereinigtes Königreich

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

1034 (0x40A)
</dt> <dd>

Spanisch – traditionelle Sortierung

</dd> <dt>

1035 (0x40B)
</dt> <dd>

Finnisch

</dd> <dt>

1036 (0x40C)
</dt> <dd>

Französisch (Frankreich)

</dd> <dt>

1037 (0x40D)
</dt> <dd>

Hebräisch

</dd> <dt>

1038 (0x40E)
</dt> <dd>

Ungarisch

</dd> <dt>

1039 (0x40F)
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

1051 (0x41B)
</dt> <dd>

Slowakisch

</dd> <dt>

1052 (0x41C)
</dt> <dd>

Albanisch

</dd> <dt>

1053 (0x41D)
</dt> <dd>

Schwedisch

</dd> <dt>

1054 (0x41E)
</dt> <dd>

Thailändisch

</dd> <dt>

1055 (0x41F)
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

1066 (0x42A)
</dt> <dd>

Vietnamesisch

</dd> <dt>

1069 (0x42D)
</dt> <dd>

Baskisch (Baskenland)

</dd> <dt>

1070 (0x42E)
</dt> <dd>

Serbisch

</dd> <dt>

1071 (0x42F)
</dt> <dd>

Nordmazedisch (Nordmazedonien)

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

1082 (0x43A)
</dt> <dd>

Maltesisch

</dd> <dt>

1084 (0x43C)
</dt> <dd>

Gaelic (Vereinigtes Königreich)

</dd> <dt>

1085 (0x43D)
</dt> <dd>

Jiddisch

</dd> <dt>

1086 (0x43E)
</dt> <dd>

Malaiisch – Australien

</dd> <dt>

2049 (0x801)
</dt> <dd>

Arabisch – Arabisch

</dd> <dt>

2052 (0x804)
</dt> <dd>

Chinesisch (vereinfacht) – PRC

</dd> <dt>

2055 (0x807)
</dt> <dd>

Deutsch – Schweiz

</dd> <dt>

2057 (0x809)
</dt> <dd>

Englisch – Vereinigtes Königreich

</dd> <dt>

2058 (0x80A)
</dt> <dd>

Spanisch – Mexiko

</dd> <dt>

2060 (0x80C)
</dt> <dd>

Französisch – Spanien

</dd> <dt>

2064 (0x810)
</dt> <dd>

Italienisch – Schweiz

</dd> <dt>

2067 (0x813)
</dt> <dd>

Niederländisch – Spanien

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

2017 – 2017

</dd> <dt>

2073 (0x819)
</dt> <dd>

Russisch – Russisch

</dd> <dt>

2074 (0x81A)
</dt> <dd>

Serbisch – Lateinisch

</dd> <dt>

2077 (0x81D)
</dt> <dd>

Schwedisch – Norwegen

</dd> <dt>

3073 (0xC01)
</dt> <dd>

Arabisch – Arabisch

</dd> <dt>

3076 (0xC04)
</dt> <dd>

Chinesisch (traditionell) – Hongkong SAR

</dd> <dt>

3079 (0xC07)
</dt> <dd>

Deutsch – Schweiz

</dd> <dt>

3081 (0xC09)
</dt> <dd>

Englisch – Australien

</dd> <dt>

3082 (0xC0A)
</dt> <dd>

Spanisch – Internationale Sortierung

</dd> <dt>

3084 (0xC0C)
</dt> <dd>

Französisch – Kanada

</dd> <dt>

3098 (0xC1A)
</dt> <dd>

Serbisch – Kyrillisch

</dd> <dt>

4097 (0x1001)
</dt> <dd>

Arabisch – Arabisch

</dd> <dt>

4100 (0x1004)
</dt> <dd>

Chinesisch (vereinfacht) – Singapur

</dd> <dt>

4103 (0x1007)
</dt> <dd>

Deutsch – Niederlande

</dd> <dt>

4105 (0x1009)
</dt> <dd>

Englisch – Kanada

</dd> <dt>

4106 (0x100A)
</dt> <dd>

Spanisch – Italienisch

</dd> <dt>

4108 (0x100C)
</dt> <dd>

Französisch – Schweiz

</dd> <dt>

5121 (0x1401)
</dt> <dd>

Arabisch – Arabisch

</dd> <dt>

5127 (0x1407)
</dt> <dd>

Deutsch – Norwegen

</dd> <dt>

5129 (0x1409)
</dt> <dd>

Englisch – Neuseeland

</dd> <dt>

5130 (0x140A)
</dt> <dd>

Spanisch – Dassser

</dd> <dt>

5132 (0x140C)
</dt> <dd>

Französisch – Frankreich

</dd> <dt>

6145 (0x1801)
</dt> <dd>

Arabisch – Arabisch – Arabisch

</dd> <dt>

6153 (0x1809)
</dt> <dd>

Englisch – Großbritannien

</dd> <dt>

6154 (0x180A)
</dt> <dd>

Spanisch – Wersin

</dd> <dt>

7169 (0x1C01)
</dt> <dd>

Arabisch – Arabisch – Arabisch

</dd> <dt>

7177 (0x1C09)
</dt> <dd>

Englisch – Südafrika

</dd> <dt>

7178 (0x1C0A)
</dt> <dd>

Spanisch – Vereinigte Republik

</dd> <dt>

8193 (0x2001)
</dt> <dd>

Arabisch – Soll

</dd> <dt>

8201 (0x2009)
</dt> <dd>

Englisch – Deutschland

</dd> <dt>

8202 (0x200A)
</dt> <dd>

Spanisch – Spanien

</dd> <dt>

9217 (0x2401)
</dt> <dd>

Arabisch – Arabisch – Arabisch

</dd> <dt>

9226 (0x240A)
</dt> <dd>

Spanisch – Spanien

</dd> <dt>

10241 (0x2801)
</dt> <dd>

Arabisch – Arabisch – Arabisch

</dd> <dt>

10249 (0x2809)
</dt> <dd>

Englisch – Deutschland

</dd> <dt>

10250 (0x280A)
</dt> <dd>

Spanisch – Mexiko

</dd> <dt>

11265 (0x2C01)
</dt> <dd>

Arabisch – Arabische Sprache

</dd> <dt>

11273 (0x2C09)
</dt> <dd>

Englisch – Deutschland

</dd> <dt>

11274 (0x2C0A)
</dt> <dd>

Spanisch – Argentinien

</dd> <dt>

12289 (0x3001)
</dt> <dd>

Arabisch – Arabisch – Arabisch

</dd> <dt>

12298 (0x300A)
</dt> <dd>

Spanisch – Spanien

</dd> <dt>

13313 (0x3401)
</dt> <dd>

Arabisch – Mexiko

</dd> <dt>

13322 (0x340A)
</dt> <dd>

Spanisch – Brasilien

</dd> <dt>

14337 (0x3801)
</dt> <dd>

Arabisch – USA

</dd> <dt>

14346 (0x380A)
</dt> <dd>

Spanisch – Schweiz

</dd> <dt>

15361 (0x3C01)
</dt> <dd>

Arabisch – Soll

</dd> <dt>

15370 (0x3C0A)
</dt> <dd>

Spanisch – Spanien

</dd> <dt>

16385 (0x4001)
</dt> <dd>

Arabisch – Chinesisch

</dd> <dt>

16394 (0x400A)
</dt> <dd>

Spanisch – Spanien

</dd> <dt>

17418 (0x440A)
</dt> <dd>

Spanisch – El— ——

</dd> <dt>

18442 (0x480A)
</dt> <dd>

Spanisch – Spanien

</dd> <dt>

19466 (0x4C0A)
</dt> <dd>

Spanisch – Spanien

</dd> <dt>

20490 (0x500A)
</dt> <dd>

Spanisch – Rico Rico

</dd> </dl>

</dd> <dt>

**OSProductSuite**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ ProductOptions \| ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")
</dt> </dl>

Installierte und lizenzierte Systemprodukterweiterungen zum Betriebssystem. Der Wert 146 (0x92) für **OSProductSuite** gibt z. B. Enterprise, Terminaldienste und Rechenzentrum an (Bits 1, 4 und 7). In der folgenden Liste sind mögliche Werte aufgeführt.

<dt>

1 (0x1)
</dt> <dd>

Microsoft Small Business Server wurde einmal installiert, aber möglicherweise auf eine andere Version von Windows aktualisiert.

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

Communication Server ist installiert.

</dd> <dt>

16 (0x10)
</dt> <dd>

Terminaldienste sind installiert.

</dd> <dt>

32 (0x20)
</dt> <dd>

Microsoft Small Business Server wird mit der restriktiven Clientlizenz installiert.

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

Terminaldienste werden installiert, aber nur eine interaktive Sitzung wird unterstützt.

</dd> <dt>

512 (0x200)
</dt> <dd>

Windows Home Edition ist installiert.

</dd> <dt>

1024 (0x400)
</dt> <dd>

Die Webserver-Edition ist installiert.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Storage Die Server Edition ist installiert.

</dd> <dt>

16384 (0x4000)
</dt> <dd>

Compute Cluster Edition ist installiert.

</dd> </dl>

</dd> <dt>

**OSType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")
</dt> </dl>

Typ des Betriebssystems. In der folgenden Liste sind die möglichen Werte aufgeführt.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span id="MACOS"></span><span id="macos"></span>**MACOS** (2)


</dt> <dd>

Makros

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)


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

<span id="WIN95"></span><span id="win95"></span>**WIN95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**WIN98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**WINCE** (19)


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

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)


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

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span id="LINUX"></span><span id="linux"></span>**LINUX** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span id="VM_ESA"></span><span id="vm_esa"></span>**VM/MARS** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Gnud** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span id="OS9"></span><span id="os9"></span>**OS9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH-Kernel** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span id="QNX"></span><span id="qnx"></span>**QNX** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span id="EPOC"></span><span id="epoc"></span>**ESAC** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)


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

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedizierend** (59)


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)


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

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")
</dt> </dl>

Zusätzliche Beschreibung für die aktuelle Betriebssystemversion.

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**PAEEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **Boolean**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die physischen Adresserweiterungen (PAE) durch das Betriebssystem aktiviert werden, das auf Intel-Prozessoren ausgeführt wird. Mit PAE können Anwendungen mehr als 4 GB physischen Arbeitsspeicher adressieren. Wenn PAE aktiviert ist, verwendet das Betriebssystem die lineare Adressübersetzung mit drei Ebenen anstelle der zweistufigen Adressübersetzung. Die Bereitstellung von mehr physischem Arbeitsspeicher für eine Anwendung reduziert die Notwendigkeit, den Arbeitsspeicher in die Seitendatei zu vertauschen, und erhöht die Leistung. Verwenden Sie zum Aktivieren von PAE den Schalter "/PAE" in der datei Boot.ini. Weitere Informationen zum Feature "Erweiterung physischer Adressen" finden Sie unter <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .

</dd> <dt>

**PlusProductID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| Plus! ProductId")
</dt> </dl>

Wird nicht unterstützt.

</dd> <dt>

**PlusVersionNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| Plus! VersionNumber")
</dt> </dl>

Wird nicht unterstützt.

</dd> <dt>

**PortableOperatingSystem**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Betriebssystem von einem externen USB-Gerät gestartet wurde. True gibt an, dass das Betriebssystem erkannt hat, dass es auf einem unterstützten lokal verbundenen Speichergerät gestartet wird.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 8 und Windows Server 2012 nicht unterstützt.

</dd> <dt>

**Primärer Server/verwaltete Instanz**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Gibt an, ob dies das primäre Betriebssystem ist.

</dd> <dt>

**ProductType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Systeminformationen.

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

**Arbeitsstation** (1)


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

**Domänencontroller** (2)


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Server** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumLength**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

Nicht unterstützt

**Windows Server 2008 und Windows Vista: **

Die **QuantumLength-Eigenschaft** definiert die Anzahl der Takte pro Quanten. Ein Quantum ist eine Einheit der Ausführungszeit, die der Planer einer Anwendung vor dem Wechsel zu anderen Anwendungen erteilen darf. Wenn ein Thread ein Quanten ausführt, wird es vom Kernel vorzeitig beendet und an das Ende einer Warteschlange für Anwendungen mit gleichen Prioritäten verschoben. Die tatsächliche Länge des Quantens eines Threads variiert auf verschiedenen Windows Plattformen. Nur für Windows NT/Windows 2000.

Die möglichen Werte sind.

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

**QuantumType**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht unterstützt

**Windows Server 2008 und Windows Vista: **

Die **QuantumType-Eigenschaft** gibt Quanten mit fester oder variabler Länge an. Windows verwendet standardmäßig Quanten variabler Länge, bei denen die Vordergrundanwendung über ein längeres Quantum als die Hintergrundanwendungen verfügt. Windows Der Server verwendet standardmäßig Quanten mit fester Länge. Ein Quanten ist eine Einheit der Ausführungszeit, die der Planer einer Anwendung vor dem Wechsel zu einer anderen Anwendung erteilen darf. Wenn ein Thread ein Quanten ausführt, wird es vom Kernel vorzeitig beendet und an das Ende einer Warteschlange für Anwendungen mit gleichen Prioritäten verschoben. Die tatsächliche Länge des Quantens eines Threads variiert auf verschiedenen Windows Plattformen.

Die möglichen Werte sind.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Behoben** (1)


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

**Variable** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**RegisteredUser**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| RegisteredOwner")
</dt> </dl>

Name des registrierten Benutzers des Betriebssystems.

Beispiel: "Ben Smith"

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| ProductId")
</dt> </dl>

Seriennummer des Betriebssystemprodukts.

Beispiel: "10497-OEM-0031416-71674"

</dd> <dt>

**ServicePackMajorVersion**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Systeminformationen Strukturen \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")
</dt> </dl>

Hauptversionsnummer des Service Packs, das auf dem Computersystem installiert ist. Wenn kein Service Pack installiert wurde, ist der Wert 0 (null).

</dd> <dt>

**ServicePackMinorVersion**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Systeminformationen Strukturen \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")
</dt> </dl>

Nebenversionsnummer des Service Packs, das auf dem Computersystem installiert ist. Wenn kein Service Pack installiert wurde, ist der Wert 0 (null).

</dd> <dt>

**SizeStoredInPagingFiles**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|DMTF-Systemspeicher Einstellungen \| 001.3"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobytes")
</dt> </dl>

Die Gesamtanzahl der Kilobytes, die in den Auslagerungsdateien des Betriebssystems gespeichert werden können– 0 (null) gibt an, dass keine Auslagerungsdateien vorhanden sind. Beachten Sie, dass diese Zahl nicht die tatsächliche physische Größe der Auslagerungsdatei auf dem Datenträger darstellt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. eine SMART-fähige Festplatte, funktioniert möglicherweise ordnungsgemäß, prognostiziert aber einen Fehler in naher Zukunft). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Der Dienststatus gilt für administrative Arbeit, z. B. spiegelungsbasiertes Resilvering eines Datenträgers, erneutes Laden einer Benutzerberechtigungsliste oder andere administrative Arbeit. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

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

**SuiteMask**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")
</dt> </dl>

Bitflags, die die im System verfügbaren Produktsammlungen identifizieren.

Um beispielsweise sowohl Personal als auch BackOffice anzugeben, legen **Sie SuiteMask** auf `4 | 512` oder `516` fest.

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

Backoffice

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

Small Business Restricted

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

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Registry Functions \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| Paths \| TargetDevice")
</dt> </dl>

Physische Datenträgerpartition, auf der das Betriebssystem installiert ist.

</dd> <dt>

**SystemDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Systeminformationen Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))
</dt> </dl>

Systemverzeichnis des Betriebssystems.

Beispiel: "C: \\ WINDOWS \\ SYSTEM32"

</dd> <dt>

**SystemDrive**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Buchstabe des Laufwerks, auf dem sich das Betriebssystem befindet. Beispiel: "C:"

</dd> <dt>

**TotalSwapSpaceSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobytes")
</dt> </dl>

Gesamter Auslagerungsspeicherplatz in Kilobyte. Dieser Wert kann **NULL** (nicht angegeben) sein, wenn der Auslagerungsbereich nicht von Seitendateien unterschieden wird. Einige Betriebssysteme unterscheiden diese Konzepte jedoch. Beispielsweise können in UNIX ganze Prozesse ausgetauscht werden, wenn die Liste der kostenlosen Seiten unter einen angegebenen Wert fällt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**TotalVirtualMemorySize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobytes")
</dt> </dl>

Anzahl des virtuellen Arbeitsspeichers in Kilobyte. Dies kann z. B. berechnet werden, indem die Gesamtgröße des ARBEITSSPEICHERs zum Auslagerungsspeicher hinzugefügt wird, d. h. die Menge des Arbeitsspeichers in der -Eigenschaft **SizeStoredInPagingFiles** hinzugefügt oder vom Computersystem aggregiert wird.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**TotalVisibleMemorySize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobytes")
</dt> </dl>

Gesamtmenge des für das Betriebssystem verfügbaren physischen Arbeitsspeichers in Kilobyte. Dieser Wert gibt nicht unbedingt die tatsächliche Menge an physischem Arbeitsspeicher an, sondern gibt an, was dem Betriebssystem als verfügbar gemeldet wird.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

Diese Eigenschaft wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Systeminformationen Strukturen \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")
</dt> </dl>

Versionsnummer des Betriebssystems.

Beispiel: "4.0"

</dd> <dt>

**WindowsDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Systeminformationen Functions \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")
</dt> </dl>

Windows Verzeichnis des Betriebssystems.

Beispiel: "C: \\ WINDOWS"

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ OperatingSystem-Klasse** wird von [**CIM \_ OperatingSystem**](cim-operatingsystem.md)abgeleitet.

Jedes Betriebssystem, das auf einem Computer installiert werden kann, auf dem ein Windows-basiertes Betriebssystem ausgeführt werden kann, ist ein Nachfolger oder Member dieser Klasse. **Win32 \_ OperatingSystem** ist eine Singletonklasse. Um die einzelne Instanz abzurufen, verwenden Sie "@" für den Schlüssel.

Im Gegensatz zu den meisten anderen WMI-Klassen, die von MgmtClassGen generiert werden, gibt die **OperatingSystem.CreateInstance**()-Methode ein leeres **OperatingSystem-Objekt** zurück. Wenn Sie C \# mit MgmtClassGen verwenden, können Sie daher den folgenden Code verwenden:


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a>Beispiele

Ein VBScript-Beispiel, das Betriebssystem- und Prozessordaten von [**\_ Win32-Computersystem,**](win32-computersystem.md) [**Win32-Prozessor \_**](win32-processor.md)und **Win32-Betriebssystem \_** erhält, finden Sie im [**Thema Win32-Prozessorbeispiele. \_**](win32-processor.md)

Das PowerShell PowerShell-Beispiel [generate Exchange Environment Reports using TechNet](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) Gallery verwendet eine **Win32 \_ OperatingSystem-Klasse** als Teil einer größeren Anwendung, um Exchange-Umgebungsberichte zu generieren.

Im [Beispiel Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) im TechNet Gallery wird die **LastBootupTime-Eigenschaft** verwendet, um zu bestimmen, wie lange der Server aktiv war. Im Beispiel wird auch die Option timeout verwendet, um sicherzustellen, dass der WMI-Aufruf nicht hängt.

Im VBScript-Codebeispiel für [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) im TechNet-Katalog wird die **Win32 \_ OperatingSystem-Klasse** verwendet, um Betriebssysteminformationen von einer Reihe von Remotecomputern abzurufen.

Das folgende Skript ruft die Instanzen von **Win32 \_ OperatingSystem** im Standardnamespace "Root \\ CIMv2" ab und zeigt dann Informationen zum Betriebssystem an.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Betriebssystem**](cim-operatingsystem.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> <dt>

[WMI-Aufgaben: Betriebssysteme](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[WMI-Aufgaben: Computerhardware](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[WMI-Aufgaben: Desktopverwaltung](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
