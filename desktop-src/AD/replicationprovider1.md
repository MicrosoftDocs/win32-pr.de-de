---
title: ReplicationProvider1-Klasse
description: Die Basisklasse für die Anbieterinstanz.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- ReplicationProvider1-Klasse Active Directory
- ReplicationProvider1-Klasse Active Directory , beschrieben
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
ms.openlocfilehash: d3e8ca70d2bb5f37303c20117ddba59db6950d1dda58779179c6ef08c95abc4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025128"
---
# <a name="replicationprovider1-class"></a>ReplicationProvider1-Klasse

Die Basisklasse für die Anbieterinstanz.

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

Die **ReplicationProvider1-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ReplicationProvider1-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Klassenbezeichner, mit dem WMI bestimmt, ob ein Hochleistungsanbieter in den Clientprozess oder den WMI-Prozess geladen werden soll. Wenn sich sowohl der Anbieter als auch der Client auf demselben Computer befinden, lädt WMI den prozessübergreifenden Anbieter mit **clientLoadableCLSID** als Klassenbezeichner auf den Client. Wenn sich der Anbieter und der Client auf verschiedenen Computern befinden, lädt WMI den anbieterin-process in WMI. WMI verwendet auch **ClientLoadableCLSID,** um Aktualisierungsvorgänge zu unterstützen.

Weitere Informationen finden Sie unter [Registrieren eines High-Performance-Anbieters.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**GUID,** die den Klassenbezeichner **(CLSID)** des COM-Anbieterobjekts darstellt. Dieses COM-Objekt muss eine Implementierung der [**IWbemProviderInit-Schnittstelle**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) enthalten.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Concurrency**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Computer an, auf dem der Anbieter gestartet werden soll. Wenn der Anbieter auf dem lokalen Computer ausgeführt wird, ist er **NULL.**

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass diese Instanz aktiviert ist und zum Abschließen von Clientanforderungen verwendet werden kann.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreibung**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")
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

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gruppe von Flags, die Informationen zur Serialisierung bereitstellen. Der Standardwert ist 0 (null).

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


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

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**Windows Server 2003:** Diese Eigenschaft ist deaktiviert.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Der Anbietername.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True gibt an, dass der Anbieter für jedes Gebietsschema initialisiert wird, wenn ein Benutzer mehr als einmal mit unterschiedlichen Gebietsschemas eine Verbindung mit demselben Namespace herstellt. Der Standardwert ist **FALSE**.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter einmal für jeden NTLM-Benutzer (NT LAN Manager) initialisiert wird, der Anforderungen an den Anbieter stellt. **False** (Standard) gibt an, dass der Anbieter einmal für alle Benutzer initialisiert wird.

Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.

</dd> <dt>

**Pure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

True **gibt an,** dass sich der Anbieter bereit erklärt, das Entladen vorzubereiten, indem er [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf allen ausstehenden Schnittstellenpunkten aufruft, wenn WMI die **Release-Methode** seiner primären Schnittstelle aufruft. Anbieter, die Clients von WMI bleiben müssen, nachdem sie nicht als Anbieter funktionieren, sollten **Pure auf** **FALSE festlegen.** Die Standardeinstellung ist **TRUE.** Weitere Informationen finden Sie im Abschnitt "Hinweise" dieses Themas.

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sicherheitsdeskriptor (SD) in der SdDL (Security Descriptor Definition Language), der die Gruppe von Benutzern bestimmt, die [**erfolgreich IWbemDeregistrpledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) für den entkoppelten Anbieter aufrufen können. Weitere Informationen finden Sie im Thema [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) im Abschnitt Sicherheit des Windows SDK. Diese Sicherheitsbeschreibung wird nur für entkoppelte Anbieter verwendet und wirkt sich nicht auf andere Anbieter aus. Weitere Informationen finden Sie unter [Integrieren eines Anbieters in eine Anwendung.](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application)

WMI führt Zugriffsüberprüfungen für entkoppelte Anbieter durch, die die [**Schnittstellen IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) und [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) verwenden. Wenn die Sicherheitsbeschreibung **NULL** ist, können nur Anwendungen oder Dienste, die unter den Konten LocalSystem, NetworkService und LocalService ausgeführt werden, einen entkoppelten Anbieter ausführen.

Die folgende Zeichenfolge zeigt einen entkoppelten Anbieter, der nur von integrierten Administratoren ausgeführt werden soll." O:BAG:BAD:(A;;0 x1;;; BA)"

Weitere Informationen zum Festlegen der **SecurityDescriptor-Eigenschaft** finden Sie unter [Maintaining WMI Security](/windows/desktop/WmiSdk/maintaining-wmi-security).

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

[Datums- und Uhrzeitformat,](/windows/desktop/WmiSdk/date-and-time-format) das angibt, wie lange WMI dem Anbieter erlaubt, im Leerlauf zu bleiben, bevor er entladen wird. In der Regel fordern Anbieter an, dass WMI nicht länger als fünf Minuten wartet.

Für die aktuelle Version von WMI wird der Wert dieser Eigenschaft ignoriert. WMI entlädt den Anbieter basierend auf dem Time out-Wert in einer internen Klasse im \\ Stammnamespace. Es wird empfohlen, dass Anbieter **UnloadTimeout festlegen.** Weitere Informationen finden Sie unter [Entladen eines Anbieters.](/windows/desktop/WmiSdk/unloading-a-provider)

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Version des Anbieters. Die unterstützten Versionen sind 1 und 2. Version 2 verstärkt Gültigkeitsprüfungen für alle zugeordneten Eigenschaftenregistrierungen, insbesondere die [**ImpersonationLevel-Eigenschaft.**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel)

Diese Eigenschaft wird von [**\_ \_ Win32Provider geerbt.**](/windows/desktop/WmiSdk/--win32provider)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Instanz dieser Klasse stellt den WMI-Anbieter für Active Directory-Domäne dar. Folgende Standardwerte werden verwendet:

-   Name = "ReplProv1"
-   ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"
-   HostingModel = "NetworkServiceHost"

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

