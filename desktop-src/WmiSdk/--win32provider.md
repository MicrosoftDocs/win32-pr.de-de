---
description: Registriert Informationen zur physischen Implementierung eines Anbieters in WMI. Anbieter, die die HostingModel-Eigenschaft nicht festlegen, werden standardmäßig geladen, um in einem Wmiprvse.exe Prozess als NetworkServiceHostOrSelfHost ausgeführt zu werden.
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
ms.openlocfilehash: dd7c848e9c792bcff3c0af58143d404bda744a982daeedbff01895242407a7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857690"
---
# <a name="__win32provider-class"></a>\_\_Win32Provider-Klasse

Die **\_ \_ Win32Provider-Systemklasse** registriert Informationen zur physischen Implementierung eines Anbieters in WMI. Anbieter, die die **HostingModel-Eigenschaft** nicht festlegen, werden standardmäßig geladen, um in einem Wmiprvse.exe Prozess als **NetworkServiceHostOrSelfHost** ausgeführt zu werden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ Win32Provider-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Win32Provider-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Klassenbezeichner, mit dem WMI bestimmt, ob ein Hochleistungsanbieter in den Clientprozess oder den WMI-Prozess geladen werden soll. Wenn sich sowohl der Anbieter als auch der Client auf demselben Computer befinden, lädt WMI den prozessübergreifenden Anbieter mit **clientLoadableCLSID** als Klassenbezeichner auf den Client. Wenn sich der Anbieter und der Client auf verschiedenen Computern befinden, lädt WMI den anbieterin-process in WMI. WMI verwendet auch **ClientLoadableCLSID,** um Aktualisierungsvorgänge zu unterstützen.

Weitere Informationen finden Sie unter [Registrieren eines High-Performance-Anbieters.](registering-a-high-performance-provider.md)

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**GUID,** die den Klassenbezeichner **(CLSID)** des COM-Anbieterobjekts darstellt. Dieses COM-Objekt muss eine Implementierung der [**IWbemProviderInit-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) enthalten.

</dd> <dt>

**Concurrency**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Computer an, auf dem der Anbieter gestartet werden soll. Wenn der Anbieter auf dem lokalen Computer ausgeführt wird, ist er **NULL.**

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass diese Instanz aktiviert ist und zum Abschließen von Clientanforderungen verwendet werden kann.

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Diese Eigenschaft besteht aus Werten aus den Eigenschaften [**MSFT \_ Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** und **HostingSpecification.** Der Wert dieser Eigenschaft gibt an, wie WMI den Anbieter und das Sicherheitskonto lädt, unter dem er ausgeführt wird. Weitere Informationen zum Festlegen der **HostingModel-Eigenschaft** finden Sie unter [Anbieterhosting und Sicherheit](provider-hosting-and-security.md) und [Registrieren eines Anbieters.](registering-a-provider.md)

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Reserviert. Der Standardwert ist 0 (null).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gruppe von Flags, die Informationen zur Serialisierung bereitstellen. Der Standardwert ist 0 (null).

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

Es ist keine Initialisierungsserialisierung erforderlich.

</dd> </dl>

</dd> <dt>

**InitializationTimeoutInterval**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

TBD

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Der Anbietername.

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Anbieter für jedes Gebietsschema initialisiert wird, wenn ein Benutzer mehr als einmal mit unterschiedlichen Gebietsschemas eine Verbindung mit demselben Namespace herstellt. Der Standardwert ist **FALSE**.

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Anbieter einmal für jeden NTLM-Benutzer (NT LAN Manager) initialisiert wird, der Anforderungen an den Anbieter stellt. False  (Standard) gibt an, dass der Anbieter einmal für alle Benutzer initialisiert wird.

</dd> <dt>

**Pure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Anbieter bereit ist, das Entladen vorzubereiten, indem [**er IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für alle ausstehenden Schnittstellenpunkte aufruft, wenn WMI die **Release-Methode** seiner primären Schnittstelle aufruft. Anbieter, die WMI-Clients bleiben müssen, nachdem sie nicht als Anbieter fungieren, sollten **Pure** auf **FALSE** festlegen. Die Standardeinstellung ist **TRUE.** Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sicherheitsdeskriptor (SD) in der Sicherheitsdeskriptordefinitionssprache (Security Descriptor Definition Language, SDDL), die den Satz von Benutzern bestimmt, die [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) für den entkoppelten Anbieter erfolgreich aufrufen können. Weitere Informationen finden Sie im Thema [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) im Abschnitt Sicherheit des Windows SDK. Diese Sicherheitsbeschreibung wird nur für entkoppelte Anbieter verwendet und wirkt sich nicht auf andere Anbieter aus. Weitere Informationen finden Sie unter [Integrieren eines Anbieters in eine Anwendung.](incorporating-a-provider-in-an-application.md)

WMI führt Zugriffsüberprüfungen für entkoppelte Anbieter durch, die die [**Schnittstellen IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und [**IWbemObjectSink**](iwbemobjectsink.md) verwenden. Wenn die Sicherheitsbeschreibung **NULL** ist, können nur Anwendungen oder Dienste, die unter den Konten LocalSystem, NetworkService und LocalService ausgeführt werden, einen entkoppelten Anbieter ausführen.

Die folgende Zeichenfolge zeigt einen entkoppelten Anbieter, der nur von integrierten Administratoren ausgeführt werden soll." O:BAG:BAD:(A;;0 x1;;; BA)"

Weitere Informationen zum Festlegen der **SecurityDescriptor-Eigenschaft** finden Sie unter [Maintaining WMI Security](maintaining-wmi-security.md).

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

[Datums- und Uhrzeitformat,](date-and-time-format.md) das angibt, wie lange WMI dem Anbieter erlaubt, im Leerlauf zu bleiben, bevor er entladen wird. In der Regel fordern Anbieter an, dass WMI nicht länger als fünf Minuten wartet.

Für die aktuelle Version von WMI wird der Wert dieser Eigenschaft ignoriert. WMI entlädt den Anbieter basierend auf dem Time out-Wert in einer internen Klasse im \\ Stammnamespace. Es wird empfohlen, dass Anbieter **UnloadTimeout festlegen.** Weitere Informationen finden Sie unter [Entladen eines Anbieters.](unloading-a-provider.md)

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Version des Anbieters. Die unterstützten Versionen sind 1 und 2. Version 2 verstärkt Gültigkeitsprüfungen für alle zugeordneten Eigenschaftenregistrierungen, insbesondere die [**ImpersonationLevel-Eigenschaft.**](swbemsecurity-impersonationlevel.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ Win32Provider-Klasse** wird vom Anbieter [**\_ \_ abgeleitet.**](--provider.md)

Die meisten Anbieter können die Standardwerte für die **InitializationReentrancy-Eigenschaft** akzeptieren. Wenn ein Anbieter jedoch die gleichzeitige Initialisierung für separate Benutzer unterstützen kann, kann diese Eigenschaft auf 1 (eins) festgelegt werden. Wenn eine serialisierte Initialisierung erforderlich ist, **bleibt InitializationReentrancy** 0 (null). In beiden Instanzen ist **PerUserInitialization** auf **TRUE festgelegt.**

Ein reiner Anbieter oder ein Anbieter, der die **Pure-Eigenschaft** auf **TRUE** legt, ist nur für Dienstanforderungen von Anwendungen und WMI vorhanden. Die meisten Anbieter sind reine Anbieter. Ein Nicht-Pure-Anbieter ist die Ausnahme. Nicht-Anbieter werden in die Rolle des Clients überwechseln, nachdem sie Wartungsanforderungen abgeschlossen haben.

Ein Beispiel für einen nicht zu verwendenden Anbieter ist ein Pushanbieter, der mit der Ausgabe von Abfragen beginnt und WMI-Anforderungen nach Abschluss der Initialisierung stellt. Ein Pushanbieter ist nicht zuständig, außer das CIM-Repository zum Zeitpunkt der Initialisierung mit Daten zu aktualisieren. Nach dem Aktualisieren des Repositorys kann ein Pushanbieter warten, bis er entladen wurde, oder auf die Rolle des Clients umstiegen. Der Pushanbieter, der auf das Entladen wartet, ist ein reiner Anbieter. Der Pushanbieter, der an Clientaktivitäten beteiligt ist, ist nicht von Bezweck.

WMI muss in der Lage sein, reine Anbieter von nicht reinen Anbietern zu unterscheiden, damit sie bestimmen kann, wann das Herunterfahren sicher ist. WMI muss warten, bis alle Vorgänge mit nicht reinen Anbietern abgeschlossen sind, bevor es sicher heruntergefahren werden kann.

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

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[Registrieren eines Anbieters](registering-a-provider.md)
</dt> </dl>

 

