---
description: Registriert Informationen über die physische Implementierung eines Anbieters in WMI. Anbieter, die die hostingmodel-Eigenschaft nicht festlegen, werden standardmäßig geladen, um Sie in einem Wmiprvse.exe Prozess als Network servicehostorselfhost auszuführen.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: __Win32Provider-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960622"
---
# <a name="__win32provider-class"></a>\_\_Win32Provider-Klasse

Die **\_ \_ Win32Provider** -System Klasse registriert Informationen über die physische Implementierung eines Anbieters in WMI. Anbieter, die die **hostingmodel** -Eigenschaft nicht festlegen, werden standardmäßig geladen, um Sie in einem Wmiprvse.exe Prozess als **Network servicehostorselfhost** auszuführen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
};
```

## <a name="members"></a>Member

Die **\_ \_ Win32Provider** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Win32Provider** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Clientloadableclsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Klassen Bezeichner, den WMI verwendet, um zu bestimmen, ob ein Hochleistungs Anbieter in den Client Prozess oder den WMI-Prozess geladen werden soll. Wenn sich sowohl der Anbieter als auch der Client auf demselben Computer befinden, lädt WMI den Anbieter Prozess Weise auf den Client, indem er **clientloadableclsid** als Klassen Bezeichner verwendet. Wenn sich der Anbieter und der Client auf unterschiedlichen Computern befinden, wird der Anbieter von WMI in-Process in den WMI-Prozess geladen. WMI verwendet auch **clientloadableclsid** , um Aktualisierungs Vorgänge zu unterstützen.

Weitere Informationen finden Sie unter [Registrieren eines High-Performance Anbieters.](registering-a-high-performance-provider.md)

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**GUID** , die den Klassen Bezeichner (**CLSID**) des COM-Objekts des Anbieters darstellt. Dieses com-Objekt muss eine Implementierung der [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle enthalten.

</dd> <dt>

**Parallelität**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Defaultmachinename**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Identifiziert den Computer, auf dem der Anbieter gestartet werden soll. Wenn der Anbieter auf dem lokalen Computer ausgeführt wird, ist er **null**.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen.

</dd> <dt>

**Hostingmodel**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Diese Eigenschaft besteht aus Werten aus den Eigenschaften **hostinggroup** und **HostingSpecification** der [**MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) . Der Wert dieser Eigenschaft gibt an, wie WMI den Anbieter und das Sicherheits Konto lädt, unter dem er ausgeführt wird. Weitere Informationen zum Festlegen der **hostingmodel** -Eigenschaft finden Sie unter [Hosting und Sicherheit des Anbieters](provider-hosting-and-security.md) und [Registrieren eines Anbieters](registering-a-provider.md).

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Reserviert. Der Standardwert ist 0 (null).

</dd> <dt>

**Initializationreentrancy**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ein Satz von Flags, die Informationen über die Serialisierung bereitstellen. Der Standardwert ist 0 (null).

<dt>

0
</dt> <dd>

Die gesamte Initialisierung dieses Anbieters muss serialisiert werden.

</dd> <dt>

1
</dt> <dd>

Alle Initialisierungen dieses Anbieters im gleichen Namespace müssen serialisiert werden.

</dd> <dt>

2
</dt> <dd>

Es ist keine Initialisierungs Serialisierung erforderlich.

</dd> </dl>

</dd> <dt>

**Initializationtimeoutinterval**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Initializeasadminfirst**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

TBD

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Der Anbietername.

</dd> <dt>

**Operationtimeoutinterval**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Perlocaleinitialization**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter für jedes Gebiets Schema initialisiert wird, wenn ein Benutzer mehr als einmal mit einem anderen Gebiets Schema eine Verbindung mit dem gleichen Namespace herstellt. Der Standardwert ist **FALSE**.

</dd> <dt>

**Peruserinitialization**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter für jeden NTLM-Benutzer (NT LAN Manager), der Anforderungen an den Anbieter sendet, einmal initialisiert wird. Der Standardwert **false** gibt an, dass der Anbieter für alle Benutzer ein Mal initialisiert wird.

</dd> <dt>

**Pure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter die Entlade Vorbereitung durch Aufrufen von [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) an allen ausstehenden Schnittstellen Punkten zustimmt, wenn WMI die **releasemethode** der primären Schnittstelle aufruft. Anbieter, die Clients von WMI beibehalten müssen, nachdem Sie nicht als Anbieter fungieren, sollten **Pure** auf **false** festlegen. Die Standardeinstellung ist **true**. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Security Deskriptor (SD) in der Sicherheits beschreibungsdefinitions-Sprache (Security Deskriptor Definition Language, SDDL), die die Gruppe der Benutzer bestimmt, die [**iwbementkopppledregistrierungs: Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) für den entkoppelten Anbieter erfolgreich aufruft. Weitere Informationen finden Sie im Thema Security [Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) im Abschnitt Security des Windows SDK. Diese Sicherheits Beschreibung wird nur für entkoppelte Anbieter verwendet und wirkt sich nicht auf andere Anbieter aus. Weitere Informationen finden Sie unter [Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md).

WMI führt Zugriffs Überprüfungen für entkoppelte Anbieter aus, die die Schnittstellen [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und [**iwbemubjectsink**](iwbemobjectsink.md) verwenden. Wenn die Sicherheits Beschreibung **null** ist, können nur Anwendungen oder Dienste, die unter dem Konto "LocalSystem", "NetworkService" und "LocalService" ausgeführt werden, einen entkoppelten Anbieter ausführen.

Die folgende Zeichenfolge zeigt einen entkoppelten Anbieter, der nur von integrierten Administratoren ausgeführt werden soll. " O:Bag: Bad: (A;; 0 x1;;; BA) "

Weitere Informationen zum Festlegen der **securityDescriptor** -Eigenschaft finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

</dd> <dt>

**Supportsexplicitshutdown**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Supportsextendedstatus**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Supportsquotas**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Supportssendstatus**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Supportsshutdown**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Supportsdrosselung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Unloadtimeout**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

[Datums-und Uhrzeit Format](date-and-time-format.md) , das angibt, wie lange der Anbieter von WMI im Leerlauf bleiben kann, bevor er entladen wird. In der Regel fordern Anbieter an, dass die WMI-Wartezeit nicht länger als fünf Minuten dauert.

Für die aktuelle Version von WMI wird der Wert dieser Eigenschaft ignoriert. WMI entlädt den Anbieter basierend auf dem Timeout Wert in einer internen Klasse im \\ Root-Namespace. Es wird empfohlen, dass Anbieter **unloadtimeout** festlegen. Weitere Informationen finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Version des Anbieters. Die unterstützten Versionen sind 1 und 2. Version 2 stärkt die Gültigkeits Prüfungen für alle zugehörigen Eigenschaften Registrierungen, insbesondere die Eigenschaft "Identitäts [**ationlevel**](swbemsecurity-impersonationlevel.md) ".

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ Win32Provider** -Klasse wird vom [**\_ \_ Anbieter**](--provider.md)abgeleitet.

Die meisten Anbieter können die Standardwerte für die **initializationreentrancy** -Eigenschaft akzeptieren. Wenn ein Anbieter jedoch die gleichzeitige Initialisierung für separate Benutzer unterstützen kann, kann diese Eigenschaft auf 1 (eins) festgelegt werden. Wenn eine serialisierte Initialisierung erforderlich ist, bleibt **initializationreentrancy** 0 (null). In beiden Fällen ist " **peruserinitialization** " auf " **true**" festgelegt.

Ein reiner Anbieter oder Anbieter, der die **Pure** -Eigenschaft auf **true** festlegt, ist nur für Dienst Anforderungen von Anwendungen und WMI vorhanden. Die meisten Anbieter sind reine Anbieter. Ein nicht reiner Anbieter ist die Ausnahme. Nicht reine Anbieter wechseln nach dem Abschluss von Wartungsanforderungen zur Rolle des Clients.

Ein Beispiel für einen nicht reinen Anbieter ist ein Push-Anbieter, der mit der Ausgabe von Abfragen beginnt und nach Abschluss der Initialisierung Anforderungen an WMI sendet. Ein pushanbieter hat keine Zuständigkeiten, außer wenn das CIM-Repository mit Daten zum Zeitpunkt der Initialisierung aktualisiert wird. Nach dem Aktualisieren des Repository kann ein pushanbieter darauf warten, entladen zu werden, oder zur Client Rolle wechseln. Der Push-Anbieter, der darauf wartet, entladen zu werden, ist ein reiner Anbieter. Der Push-Anbieter, der an Client Aktivitäten teilnimmt, ist nicht rein.

WMI muss in der Lage sein, reine Anbieter von nicht reinen Anbietern zu unterscheiden, damit ermittelt werden kann, wann das Herunterfahren sicher ist. WMI muss darauf warten, dass alle Vorgänge, die nicht-reine Anbieter einschließen, vollständig beendet werden, bevor er sicher heruntergefahren werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Anbieter**](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Registrieren eines Anbieters](registering-a-provider.md)
</dt> </dl>

 

