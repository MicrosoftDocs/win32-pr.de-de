---
description: Ermöglicht die Festlegung von Grenzwerten für die Host Prozess Verwendung von Systemressourcen.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: __ProviderHostQuotaConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216323"
---
# <a name="__providerhostquotaconfiguration-class"></a><span data-ttu-id="ab792-103">\_\_Providerhostquotaconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="ab792-103">\_\_ProviderHostQuotaConfiguration class</span></span>

<span data-ttu-id="ab792-104">Die " **\_ \_ providerhostquotaconfiguration** "-System Klasse ist eine Konfigurations Klasse für Host Anbieter Prozesse.</span><span class="sxs-lookup"><span data-stu-id="ab792-104">The **\_\_ProviderHostQuotaConfiguration** system class is a configuration class for host provider processes.</span></span> <span data-ttu-id="ab792-105">Diese Klasse befindet sich im Stamm Namespace und ermöglicht die Festlegung von Grenzwerten für die Host Prozess Verwendung von Systemressourcen.</span><span class="sxs-lookup"><span data-stu-id="ab792-105">This class resides in the root namespace and allows limits to be set on host process usage of system resources.</span></span>

<span data-ttu-id="ab792-106">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ab792-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ab792-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ab792-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab792-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab792-108">Syntax</span></span>

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a><span data-ttu-id="ab792-109">Member</span><span class="sxs-lookup"><span data-stu-id="ab792-109">Members</span></span>

<span data-ttu-id="ab792-110">Die **\_ \_ providerhostquotaconfiguration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ab792-110">The **\_\_ProviderHostQuotaConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="ab792-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab792-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab792-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab792-112">Properties</span></span>

<span data-ttu-id="ab792-113">Die **\_ \_ providerhostquotaconfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab792-113">The **\_\_ProviderHostQuotaConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab792-114">**Lenker Host**</span><span class="sxs-lookup"><span data-stu-id="ab792-114">**HandlesPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab792-115">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab792-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab792-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab792-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab792-117">Die Anzahl der Kernel Objekt Handles, die jeder Host aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="ab792-117">Number of kernel object handles each host can have.</span></span>

</dd> <dt>

<span data-ttu-id="ab792-118">**Memoryallhosts**</span><span class="sxs-lookup"><span data-stu-id="ab792-118">**MemoryAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab792-119">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab792-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab792-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab792-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab792-121">Kombinierte Größe des privaten Speichers in Bytes, der von allen Hosts belegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab792-121">Combined amount of private memory in bytes that can be held by all hosts.</span></span>

<span data-ttu-id="ab792-122">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ab792-122">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ab792-123">**Memoryperhost**</span><span class="sxs-lookup"><span data-stu-id="ab792-123">**MemoryPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab792-124">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab792-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab792-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab792-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab792-126">Die Menge des privaten Speichers, der von jedem Host belegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab792-126">Amount of private memory that can be held by each host.</span></span>

<span data-ttu-id="ab792-127">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ab792-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ab792-128">**Processlimitallhosts**</span><span class="sxs-lookup"><span data-stu-id="ab792-128">**ProcessLimitAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab792-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab792-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab792-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab792-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab792-131">Die Gesamtanzahl von Host Prozessen, die gleichzeitig ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="ab792-131">Total number of host processes that can be executing concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="ab792-132">**Threadsperhost**</span><span class="sxs-lookup"><span data-stu-id="ab792-132">**ThreadsPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab792-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab792-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab792-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab792-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab792-135">Anzahl von Threads, die sich im Besitz eines Hosts befinden.</span><span class="sxs-lookup"><span data-stu-id="ab792-135">Number of threads owned by any one host.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab792-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab792-136">Remarks</span></span>

<span data-ttu-id="ab792-137">Die Eigenschaften, die die Grenzwerte darstellen, können geändert werden, aber da es sich bei der Klasse um einen Singleton handelt, haben alle Anbieter Hosts dieselben Grenzen.</span><span class="sxs-lookup"><span data-stu-id="ab792-137">The properties that represent limits can be changed but because the class is a singleton, all the provider hosts share the same limits.</span></span>

<span data-ttu-id="ab792-138">Die folgenden Parameter werden verwendet, wenn die Grenzwerte für das Auftrags Objekt für das Host Auftrags Objekt konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="ab792-138">The following parameters are used when configuring the job object limits for the host job object:</span></span>

-   <span data-ttu-id="ab792-139">**Memoryallhosts**</span><span class="sxs-lookup"><span data-stu-id="ab792-139">**MemoryAllHosts**</span></span>
-   <span data-ttu-id="ab792-140">**Memoryperhost**</span><span class="sxs-lookup"><span data-stu-id="ab792-140">**MemoryPerHost**</span></span>
-   <span data-ttu-id="ab792-141">**Processlimitallhosts**</span><span class="sxs-lookup"><span data-stu-id="ab792-141">**ProcessLimitAllHosts**</span></span>
-   <span data-ttu-id="ab792-142">**Threadsperhost**</span><span class="sxs-lookup"><span data-stu-id="ab792-142">**ThreadsPerHost**</span></span>

<span data-ttu-id="ab792-143">Der Host Prozess fragt die Verwendung von Handles ab und beendet den Prozess, wenn das " **Lenker Host** "-Kontingent verletzt wird.</span><span class="sxs-lookup"><span data-stu-id="ab792-143">The host process polls handle usage and exits the process if the **HandlesPerHost** quota is violated.</span></span> <span data-ttu-id="ab792-144">Änderungen an diesen Werten treten nach dem Neustart des Computers in Kraft.</span><span class="sxs-lookup"><span data-stu-id="ab792-144">Changes to these values take effect after the computer is restarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab792-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab792-145">Requirements</span></span>



| <span data-ttu-id="ab792-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab792-146">Requirement</span></span> | <span data-ttu-id="ab792-147">Wert</span><span class="sxs-lookup"><span data-stu-id="ab792-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ab792-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab792-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ab792-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab792-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ab792-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab792-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ab792-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab792-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ab792-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab792-152">Namespace</span></span><br/>                | <span data-ttu-id="ab792-153">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="ab792-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ab792-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab792-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab792-155">**\_\_System Class**</span><span class="sxs-lookup"><span data-stu-id="ab792-155">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="ab792-156">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="ab792-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

