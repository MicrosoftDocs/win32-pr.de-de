---
title: ReplicationProvider1-Klasse
description: Die Basisklasse für die Anbieter Instanz.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- ReplicationProvider1-Klasse Active Directory
- ReplicationProvider1-Klasse Active Directory, beschrieben
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040514"
---
# <a name="replicationprovider1-class"></a>ReplicationProvider1-Klasse

Die Basisklasse für die Anbieter Instanz.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
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
  string   HostingModel;
};
```

## <a name="members"></a>Member

Die **ReplicationProvider1** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ReplicationProvider1** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Clientloadableclsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Klassen Bezeichner, den WMI verwendet, um zu bestimmen, ob ein Hochleistungs Anbieter in den Client Prozess oder den WMI-Prozess geladen werden soll. Wenn sich sowohl der Anbieter als auch der Client auf demselben Computer befinden, lädt WMI den Anbieter Prozess Weise auf den Client, indem er **clientloadableclsid** als Klassen Bezeichner verwendet. Wenn sich der Anbieter und der Client auf unterschiedlichen Computern befinden, wird der Anbieter von WMI in-Process in den WMI-Prozess geladen. WMI verwendet auch **clientloadableclsid** , um Aktualisierungs Vorgänge zu unterstützen.

Weitere Informationen finden Sie unter [Registrieren eines High-Performance Anbieters.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**GUID** , die den Klassen Bezeichner (**CLSID**) des COM-Objekts des Anbieters darstellt. Dieses com-Objekt muss eine Implementierung der [**iwbemproviderinit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle enthalten.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Parallelität**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Defaultmachinename**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Identifiziert den Computer, auf dem der Anbieter gestartet werden soll. Wenn der Anbieter auf dem lokalen Computer ausgeführt wird, ist er **null**.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Hostingmodel**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("hostingmodel")
</dt> </dl>

Enthält das Hostingmodell des Anbieters.

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Reserviert. Der Standardwert ist 0 (null).

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Initializationreentrancy**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ein Satz von Flags, die Informationen über die Serialisierung bereitstellen. Der Standardwert ist 0 (null).

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Die gesamte Initialisierung dieses Anbieters muss serialisiert werden.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Alle Initialisierungen dieses Anbieters im gleichen Namespace müssen serialisiert werden.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


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

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Initializeasadminfirst**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**Windows Server 2003:** Diese Eigenschaft ist deaktiviert.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Der Anbietername.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Operationtimeoutinterval**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Perlocaleinitialization**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter für jedes Gebiets Schema initialisiert wird, wenn ein Benutzer mehr als einmal mit einem anderen Gebiets Schema eine Verbindung mit dem gleichen Namespace herstellt. Der Standardwert ist **FALSE**.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Peruserinitialization**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter für jeden NTLM-Benutzer (NT LAN Manager), der Anforderungen an den Anbieter sendet, einmal initialisiert wird. Der Standardwert **false** gibt an, dass der Anbieter für alle Benutzer ein Mal initialisiert wird.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Pure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter die Entlade Vorbereitung durch Aufrufen von [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) an allen ausstehenden Schnittstellen Punkten zustimmt, wenn WMI die **releasemethode** der primären Schnittstelle aufruft. Anbieter, die Clients von WMI beibehalten müssen, nachdem Sie nicht als Anbieter fungieren, sollten **Pure** auf **false** festlegen. Die Standardeinstellung ist **true**. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Security Deskriptor (SD) in der Sicherheits beschreibungsdefinitions-Sprache (Security Deskriptor Definition Language, SDDL), die die Gruppe der Benutzer bestimmt, die [**iwbementkopppledregistrierungs: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) für den entkoppelten Anbieter erfolgreich aufruft. Weitere Informationen finden Sie im Thema Security [Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) im Abschnitt Security des Windows SDK. Diese Sicherheits Beschreibung wird nur für entkoppelte Anbieter verwendet und wirkt sich nicht auf andere Anbieter aus. Weitere Informationen finden Sie unter [Einbinden eines Anbieters in eine Anwendung](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).

WMI führt Zugriffs Überprüfungen für entkoppelte Anbieter aus, die die Schnittstellen [**iwbemproviderinit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) und [**iwbemubjectsink**](/windows/desktop/WmiSdk/iwbemobjectsink) verwenden. Wenn die Sicherheits Beschreibung **null** ist, können nur Anwendungen oder Dienste, die unter dem Konto "LocalSystem", "NetworkService" und "LocalService" ausgeführt werden, einen entkoppelten Anbieter ausführen.

Die folgende Zeichenfolge zeigt einen entkoppelten Anbieter, der nur von integrierten Administratoren ausgeführt werden soll. " O:Bag: Bad: (A;; 0 x1;;; BA) "

Weitere Informationen zum Festlegen der **securityDescriptor** -Eigenschaft finden Sie unter Verwalten der [WMI-Sicherheit](/windows/desktop/WmiSdk/maintaining-wmi-security).

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Supportsexplicitshutdown**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Supportsextendedstatus**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Supportsquotas**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Supportssendstatus**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Supportsshutdown**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Supportsdrosselung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Unloadtimeout**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

[Datums-und Uhrzeit Format](/windows/desktop/WmiSdk/date-and-time-format) , das angibt, wie lange der Anbieter von WMI im Leerlauf bleiben kann, bevor er entladen wird. In der Regel fordern Anbieter an, dass die WMI-Wartezeit nicht länger als fünf Minuten dauert.

Für die aktuelle Version von WMI wird der Wert dieser Eigenschaft ignoriert. WMI entlädt den Anbieter basierend auf dem Timeout Wert in einer internen Klasse im \\ Root-Namespace. Es wird empfohlen, dass Anbieter **unloadtimeout** festlegen. Weitere Informationen finden Sie unter [Entladen eines Anbieters](/windows/desktop/WmiSdk/unloading-a-provider).

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Version des Anbieters. Die unterstützten Versionen sind 1 und 2. Version 2 stärkt die Gültigkeits Prüfungen für alle zugehörigen Eigenschaften Registrierungen, insbesondere die Eigenschaft "Identitäts [**ationlevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) ".

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Instanz dieser Klasse stellt den WMI-Anbieter für Active Directory-Domäne Services dar. Folgende Standardwerte werden verwendet:

-   Name = "ReplProv1"
-   CLSID = "{29288f 43-39b1-40dB-b41b-ce899450e911}"
-   Hostingmodel = "networkservicehost"

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Microsoftactivedirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

