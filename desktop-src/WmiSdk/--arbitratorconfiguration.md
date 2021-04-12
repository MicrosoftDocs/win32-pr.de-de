---
description: Schränkt die internen Ressourcen ein, die von von WMI-Clients initiierten Vorgängen verwendet werden.
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
ms.openlocfilehash: 906164d6d715ed70bccecf61fba767ada622c74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216708"
---
# <a name="__arbitratorconfiguration-class"></a>\_\_"Arbiatorconfiguration"-Klasse

Die Klasse " **\_ \_ arbiatorconfiguration** " ist eine Konfigurations Klasse, die die internen Ressourcen einschränkt, die von den WMI-Clients initiierten Vorgängen verwendet werden. Dies ist eine Singleton-Klasse, die sich im Stamm \\ Namespace befindet. Die Klasse wird intern generiert, sodass keine MOF-Datei dafür vorhanden ist.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die Klasse " **\_ \_ arbiatorconfiguration** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse " **\_ \_ arbiatorconfiguration** " verfügt über diese Eigenschaften.

<dl> <dt>

**Outstandingtasksperuser**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Anzahl ausstehender Benutzer initiierter Aufgaben zu einem beliebigen Zeitpunkt.

</dd> <dt>

**Outstandingtaskstotal**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Die Gesamtanzahl der ausstehenden Aufgaben.

</dd> <dt>

**Permanentabonneptionsperuser**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der dauerhaften Abonnements, die für einen bestimmten Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**Permanent abonniert**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der dauerhaften Abonnements, die für alle Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**Pollinginstructionsperuser**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Abruf Ereignis Abfragen, die für einen bestimmten Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**Pollinginstructionstotal**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der Abruf Anweisungen, die für alle Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**Pollingmemoryperuser**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Menge der von einem bestimmten Benutzer ausgegebenen Arbeitsspeicher-Abruf Ereignis Abfragen kann zu einem beliebigen Zeitpunkt genutzt werden.

</dd> <dt>

**Pollingmemorytotal**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Gesamtumfang des Arbeitsspeichers, der durch Abfragen von Ereignis Abfragen für alle Benutzer kombiniert wird, kann zu einem beliebigen Zeitpunkt Verbraucher werden.

</dd> <dt>

**Quotaretrycount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Anzahl von Kontingent Verstößen, die zulässig sind, bevor ein Task abgebrochen wird.

</dd> <dt>

**Quotaretrywaitinterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Die bei der Aufgabenausführung bei den einzelnen Kontingent Verletzungen eingeführte Verzögerung.

</dd> <dt>

**Taskthreadsperuser**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Die maximal zulässige Anzahl von Taskthreads, die einem bestimmten Benutzer zugeordnet sind.

</dd> <dt>

**Taskthreadstotal**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Maximale Anzahl von Taskthreads.

</dd> <dt>

**Temporaryabonnemenamtionsperuser**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl temporärer Abonnements, die für einen bestimmten Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**Temporaryabonnemenzstotal**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der temporären Abonnements, die für alle Benutzer gleichzeitig zulässig sind.

</dd> <dt>

**Totalcachedisk**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Gesamter Datenträger Cache, der alle Benutzer gleichzeitig zugeordnet ist.

</dd> <dt>

**Totalcachediskpertask**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Der gesamte Datenträger Cache, der einer bestimmten Aufgabe zugeordnet ist.

</dd> <dt>

**Totalcachediskperuser**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Der gesamte Datenträger Cache, der einem bestimmten Benutzer zugeordnet ist.

</dd> <dt>

**Totalcachememory**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Insgesamt zugeordneter Arbeitsspeicher Cache für alle Benutzer.

</dd> <dt>

**Totalcachememorypertask**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Der gesamte Arbeitsspeicher Cache, der einer bestimmten Aufgabe zugeordnet ist.

</dd> <dt>

**Totalcachememoryperuser**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Gesamter Arbeitsspeicher Cache, der einem bestimmten Benutzer zu jedem Zeitpunkt zugeordnet ist.

</dd> <dt>

**Totalusers**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nicht verwendet. Maximale Anzahl verbundener Benutzer.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die " **\_ \_ arbiatorconfiguration** " wird von " [**\_ \_ System Class**](--systemclass.md)" geerbt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_System Class**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

