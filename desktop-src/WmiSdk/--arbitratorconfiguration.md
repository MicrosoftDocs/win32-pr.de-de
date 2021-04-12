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
# <a name="__arbitratorconfiguration-class"></a><span data-ttu-id="67089-103">\_\_"Arbiatorconfiguration"-Klasse</span><span class="sxs-lookup"><span data-stu-id="67089-103">\_\_ArbitratorConfiguration class</span></span>

<span data-ttu-id="67089-104">Die Klasse " **\_ \_ arbiatorconfiguration** " ist eine Konfigurations Klasse, die die internen Ressourcen einschränkt, die von den WMI-Clients initiierten Vorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67089-104">The **\_\_ArbitratorConfiguration** class is a configuration class that limits the internal resources that are used by operations initiated by WMI clients.</span></span> <span data-ttu-id="67089-105">Dies ist eine Singleton-Klasse, die sich im Stamm \\ Namespace befindet.</span><span class="sxs-lookup"><span data-stu-id="67089-105">This is a singleton class that resides in the \\root namespace.</span></span> <span data-ttu-id="67089-106">Die Klasse wird intern generiert, sodass keine MOF-Datei dafür vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="67089-106">The class is internally generated so there is no MOF file for it.</span></span>

<span data-ttu-id="67089-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="67089-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="67089-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="67089-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67089-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="67089-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="67089-110">Member</span><span class="sxs-lookup"><span data-stu-id="67089-110">Members</span></span>

<span data-ttu-id="67089-111">Die Klasse " **\_ \_ arbiatorconfiguration** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="67089-111">The **\_\_ArbitratorConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="67089-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67089-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67089-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67089-113">Properties</span></span>

<span data-ttu-id="67089-114">Die Klasse " **\_ \_ arbiatorconfiguration** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="67089-114">The **\_\_ArbitratorConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67089-115">**Outstandingtasksperuser**</span><span class="sxs-lookup"><span data-stu-id="67089-115">**OutstandingTasksPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-116">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-118">Unused.</span></span> <span data-ttu-id="67089-119">Anzahl ausstehender Benutzer initiierter Aufgaben zu einem beliebigen Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="67089-119">Number of outstanding user initiated tasks at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-120">**Outstandingtaskstotal**</span><span class="sxs-lookup"><span data-stu-id="67089-120">**OutstandingTasksTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-121">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-123">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-123">Unused.</span></span> <span data-ttu-id="67089-124">Die Gesamtanzahl der ausstehenden Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="67089-124">Total number of outstanding tasks at any time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-125">**Permanentabonneptionsperuser**</span><span class="sxs-lookup"><span data-stu-id="67089-125">**PermanentSubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-126">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-128">Die Anzahl der dauerhaften Abonnements, die für einen bestimmten Benutzer gleichzeitig zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="67089-128">Number of permanent subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-129">**Permanent abonniert**</span><span class="sxs-lookup"><span data-stu-id="67089-129">**PermanentSubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-132">Die Gesamtanzahl der dauerhaften Abonnements, die für alle Benutzer gleichzeitig zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="67089-132">Total number of permanent subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-133">**Pollinginstructionsperuser**</span><span class="sxs-lookup"><span data-stu-id="67089-133">**PollingInstructionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-136">Die Anzahl der Abruf Ereignis Abfragen, die für einen bestimmten Benutzer gleichzeitig zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="67089-136">Number of polling event queries allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-137">**Pollinginstructionstotal**</span><span class="sxs-lookup"><span data-stu-id="67089-137">**PollingInstructionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-140">Die Gesamtanzahl der Abruf Anweisungen, die für alle Benutzer gleichzeitig zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="67089-140">Total number of polling instructions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-141">**Pollingmemoryperuser**</span><span class="sxs-lookup"><span data-stu-id="67089-141">**PollingMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-144">Die Menge der von einem bestimmten Benutzer ausgegebenen Arbeitsspeicher-Abruf Ereignis Abfragen kann zu einem beliebigen Zeitpunkt genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="67089-144">Amount of memory polling event queries, issued by a particular user, can consume at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-145">**Pollingmemorytotal**</span><span class="sxs-lookup"><span data-stu-id="67089-145">**PollingMemoryTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-148">Der Gesamtumfang des Arbeitsspeichers, der durch Abfragen von Ereignis Abfragen für alle Benutzer kombiniert wird, kann zu einem beliebigen Zeitpunkt Verbraucher werden.</span><span class="sxs-lookup"><span data-stu-id="67089-148">Total amount of memory that polling event queries, for all users combined, can consumer at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-149">**Quotaretrycount**</span><span class="sxs-lookup"><span data-stu-id="67089-149">**QuotaRetryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-152">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-152">Unused.</span></span> <span data-ttu-id="67089-153">Anzahl von Kontingent Verstößen, die zulässig sind, bevor ein Task abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="67089-153">Number of quota violations permitted before a task is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="67089-154">**Quotaretrywaitinterval**</span><span class="sxs-lookup"><span data-stu-id="67089-154">**QuotaRetryWaitInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-155">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-157">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-157">Unused.</span></span> <span data-ttu-id="67089-158">Die bei der Aufgabenausführung bei den einzelnen Kontingent Verletzungen eingeführte Verzögerung.</span><span class="sxs-lookup"><span data-stu-id="67089-158">Delay introduced into the task execution on each quota violation.</span></span>

</dd> <dt>

<span data-ttu-id="67089-159">**Taskthreadsperuser**</span><span class="sxs-lookup"><span data-stu-id="67089-159">**TaskThreadsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-162">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-162">Unused.</span></span> <span data-ttu-id="67089-163">Die maximal zulässige Anzahl von Taskthreads, die einem bestimmten Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="67089-163">Maximum number of task threads associated with a particular user t any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-164">**Taskthreadstotal**</span><span class="sxs-lookup"><span data-stu-id="67089-164">**TaskThreadsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-167">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-167">Unused.</span></span> <span data-ttu-id="67089-168">Maximale Anzahl von Taskthreads.</span><span class="sxs-lookup"><span data-stu-id="67089-168">Maximum number of task threads.</span></span>

</dd> <dt>

<span data-ttu-id="67089-169">**Temporaryabonnemenamtionsperuser**</span><span class="sxs-lookup"><span data-stu-id="67089-169">**TemporarySubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-172">Die Anzahl temporärer Abonnements, die für einen bestimmten Benutzer gleichzeitig zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="67089-172">Number of temporary subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-173">**Temporaryabonnemenzstotal**</span><span class="sxs-lookup"><span data-stu-id="67089-173">**TemporarySubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-174">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-176">Die Gesamtanzahl der temporären Abonnements, die für alle Benutzer gleichzeitig zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="67089-176">Total number of temporary subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-177">**Totalcachedisk**</span><span class="sxs-lookup"><span data-stu-id="67089-177">**TotalCacheDisk**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-178">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-180">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-180">Unused.</span></span> <span data-ttu-id="67089-181">Gesamter Datenträger Cache, der alle Benutzer gleichzeitig zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67089-181">Total disk cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-182">**Totalcachediskpertask**</span><span class="sxs-lookup"><span data-stu-id="67089-182">**TotalCacheDiskPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-183">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-185">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-185">Unused.</span></span> <span data-ttu-id="67089-186">Der gesamte Datenträger Cache, der einer bestimmten Aufgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67089-186">Total disk cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-187">**Totalcachediskperuser**</span><span class="sxs-lookup"><span data-stu-id="67089-187">**TotalCacheDiskPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-188">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-190">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-190">Unused.</span></span> <span data-ttu-id="67089-191">Der gesamte Datenträger Cache, der einem bestimmten Benutzer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67089-191">Total disk cache associated with a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-192">**Totalcachememory**</span><span class="sxs-lookup"><span data-stu-id="67089-192">**TotalCacheMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-193">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-195">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-195">Unused.</span></span> <span data-ttu-id="67089-196">Insgesamt zugeordneter Arbeitsspeicher Cache für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="67089-196">Total memory cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-197">**Totalcachememorypertask**</span><span class="sxs-lookup"><span data-stu-id="67089-197">**TotalCacheMemoryPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-198">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-200">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-200">Unused.</span></span> <span data-ttu-id="67089-201">Der gesamte Arbeitsspeicher Cache, der einer bestimmten Aufgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67089-201">Total memory cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-202">**Totalcachememoryperuser**</span><span class="sxs-lookup"><span data-stu-id="67089-202">**TotalCacheMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-203">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-205">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-205">Unused.</span></span> <span data-ttu-id="67089-206">Gesamter Arbeitsspeicher Cache, der einem bestimmten Benutzer zu jedem Zeitpunkt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67089-206">Total memory cache associated with a particular user at anyone time.</span></span>

</dd> <dt>

<span data-ttu-id="67089-207">**Totalusers**</span><span class="sxs-lookup"><span data-stu-id="67089-207">**TotalUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67089-208">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67089-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67089-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67089-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67089-210">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67089-210">Unused.</span></span> <span data-ttu-id="67089-211">Maximale Anzahl verbundener Benutzer.</span><span class="sxs-lookup"><span data-stu-id="67089-211">Maximum number of connected users.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67089-212">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67089-212">Remarks</span></span>

<span data-ttu-id="67089-213">Die " **\_ \_ arbiatorconfiguration** " wird von " [**\_ \_ System Class**](--systemclass.md)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="67089-213">**\_\_ArbitratorConfiguration** is inherited from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67089-214">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67089-214">Requirements</span></span>



| <span data-ttu-id="67089-215">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67089-215">Requirement</span></span> | <span data-ttu-id="67089-216">Wert</span><span class="sxs-lookup"><span data-stu-id="67089-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="67089-217">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67089-217">Minimum supported client</span></span><br/> | <span data-ttu-id="67089-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67089-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="67089-219">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67089-219">Minimum supported server</span></span><br/> | <span data-ttu-id="67089-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67089-220">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="67089-221">Namespace</span><span class="sxs-lookup"><span data-stu-id="67089-221">Namespace</span></span><br/>                | <span data-ttu-id="67089-222">Root</span><span class="sxs-lookup"><span data-stu-id="67089-222">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="67089-223">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67089-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67089-224">**\_\_System Class**</span><span class="sxs-lookup"><span data-stu-id="67089-224">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="67089-225">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="67089-225">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

