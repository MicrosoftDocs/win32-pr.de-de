---
description: Schränkt die internen Ressourcen ein, die von Vorgängen verwendet werden, die von WMI-Clients initiiert werden.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: __ArbitratorConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 4344eb368a96d2d47207748cba622d07d11ef78e0a046c6ea169305d9c587957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321120"
---
# <a name="__arbitratorconfiguration-class"></a>\_\_Configuration-Klasse

Die **\_ \_ Klasse "Configuration"** ist eine Konfigurationsklasse, die die internen Ressourcen einschränkt, die von Vorgängen verwendet werden, die von WMI-Clients initiiert werden. Dies ist eine Singletonklasse, die sich im \\ Stammnamespace befindet. Die -Klasse wird intern generiert, sodass keine MOF-Datei dafür vorhanden ist.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a>Member

Die **\_ \_ Klasse "Configuration"** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Klasse "Configuration"** verfügt über diese Eigenschaften.

<dl> <dt>

**OutstandingTasksPerUser**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Anzahl der ausstehenden vom Benutzer initiierten Aufgaben gleichzeitig.

</dd> <dt>

**OutstandingTasksTotal**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Gesamtanzahl der zu einem beliebigen Zeitpunkt ausstehenden Aufgaben.

</dd> <dt>

**PermanentSubscriptionsPerUser**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der permanenten Abonnements, die für einen bestimmten Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**PermanentSubscriptionsTotal**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gesamtanzahl der permanenten Abonnements, die für alle Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**PollingInstructionsPerUser**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Abfragen von Abrufereignissen, die für einen bestimmten Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**PollingInstructionsTotal**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gesamtanzahl von Abrufanweisungen, die für alle Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**PollingMemoryPerUser**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Von einem bestimmten Benutzer ausgegebene Menge an Arbeitsspeicherabfragen für Abrufereignisse kann jederzeit verbraucht werden.

</dd> <dt>

**PollingMemoryTotal**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gesamtmenge des Arbeitsspeichers, der für alle Benutzer, die Ereignisabfragen abruft, für alle Benutzer gleichzeitig consumern kann.

</dd> <dt>

**QuotaRetryCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Anzahl der zulässigen Kontingentverletzungen, bevor ein Task abgebrochen wird.

</dd> <dt>

**QuotaRetryWaitInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Verzögerung, die bei jeder Kontingentverletzung in die Taskausführung eingeführt wurde.

</dd> <dt>

**TaskThreadsPerUser**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Maximale Anzahl von Taskthreads, die einem bestimmten Benutzer nicht einmal zugeordnet sind.

</dd> <dt>

**TaskThreadsTotal**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Maximale Anzahl von Taskthreads.

</dd> <dt>

**TemporarySubscriptionsPerUser**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der temporären Abonnements, die für einen bestimmten Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**TemporarySubscriptionsTotal**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gesamtzahl der temporären Abonnements, die für alle Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**TotalCacheDisk**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Gesamter Datenträgercache, der allen Benutzern gleichzeitig zugeordnet ist.

</dd> <dt>

**TotalCacheDiskPerTask**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Gesamter Datenträgercache, der einer bestimmten Aufgabe gleichzeitig zugeordnet ist.

</dd> <dt>

**TotalCacheDiskPerUser**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Gesamter Datenträgercache, der einem bestimmten Benutzer gleichzeitig zugeordnet ist.

</dd> <dt>

**TotalCacheMemory**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Gesamter Speichercache, der allen Benutzern gleichzeitig zugeordnet ist.

</dd> <dt>

**TotalCacheMemoryPerTask**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Gesamter Arbeitsspeichercache, der einem bestimmten Task gleichzeitig zugeordnet ist.

</dd> <dt>

**TotalCacheMemoryPerUser**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Gesamter Arbeitsspeichercache, der einem bestimmten Benutzer zu einem bestimmten Zeitpunkt zugeordnet ist.

</dd> <dt>

**TotalUsers**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Maximale Anzahl verbundener Benutzer.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**\_ \_ "Configuration"** wird von [**\_ \_ SystemClass geerbt.**](--systemclass.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

