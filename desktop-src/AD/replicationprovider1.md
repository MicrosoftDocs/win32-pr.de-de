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
# <a name="replicationprovider1-class"></a><span data-ttu-id="b8fa9-105">ReplicationProvider1-Klasse</span><span class="sxs-lookup"><span data-stu-id="b8fa9-105">ReplicationProvider1 class</span></span>

<span data-ttu-id="b8fa9-106">Die Basisklasse für die Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-106">The base class for the provider instance.</span></span>

<span data-ttu-id="b8fa9-107">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8fa9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8fa9-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b8fa9-109">Member</span><span class="sxs-lookup"><span data-stu-id="b8fa9-109">Members</span></span>

<span data-ttu-id="b8fa9-110">Die **ReplicationProvider1** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b8fa9-110">The **ReplicationProvider1** class has these types of members:</span></span>

-   [<span data-ttu-id="b8fa9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b8fa9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8fa9-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b8fa9-112">Properties</span></span>

<span data-ttu-id="b8fa9-113">Die **ReplicationProvider1** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-113">The **ReplicationProvider1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8fa9-114">**Clientloadableclsid**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-114">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-117">Klassen Bezeichner, den WMI verwendet, um zu bestimmen, ob ein Hochleistungs Anbieter in den Client Prozess oder den WMI-Prozess geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-117">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="b8fa9-118">Wenn sich sowohl der Anbieter als auch der Client auf demselben Computer befinden, lädt WMI den Anbieter Prozess Weise auf den Client, indem er **clientloadableclsid** als Klassen Bezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-118">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="b8fa9-119">Wenn sich der Anbieter und der Client auf unterschiedlichen Computern befinden, wird der Anbieter von WMI in-Process in den WMI-Prozess geladen.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-119">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="b8fa9-120">WMI verwendet auch **clientloadableclsid** , um Aktualisierungs Vorgänge zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-120">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="b8fa9-121">Weitere Informationen finden Sie unter [Registrieren eines High-Performance Anbieters.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span><span class="sxs-lookup"><span data-stu-id="b8fa9-121">For more information, see [Registering a High-Performance Provider.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span></span>

<span data-ttu-id="b8fa9-122">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-122">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-123">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-126">**GUID** , die den Klassen Bezeichner (**CLSID**) des COM-Objekts des Anbieters darstellt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="b8fa9-127">Dieses com-Objekt muss eine Implementierung der [**iwbemproviderinit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

<span data-ttu-id="b8fa9-128">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-128">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-129">**Parallelität**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-129">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-130">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-132">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-132">Not used.</span></span>

<span data-ttu-id="b8fa9-133">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-133">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-134">**Defaultmachinename**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-134">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-137">Identifiziert den Computer, auf dem der Anbieter gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-137">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="b8fa9-138">Wenn der Anbieter auf dem lokalen Computer ausgeführt wird, ist er **null**.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-138">If the provider runs on the local computer it is **NULL**.</span></span>

<span data-ttu-id="b8fa9-139">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-139">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-140">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-140">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-141">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-143">**True** gibt an, dass diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-143">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

<span data-ttu-id="b8fa9-144">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-144">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-145">**Hostingmodel**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-145">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8fa9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-148">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("hostingmodel")</span><span class="sxs-lookup"><span data-stu-id="b8fa9-148">Qualifiers: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-149">Enthält das Hostingmodell des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-149">Contains the hosting model of the provider.</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-150">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-150">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-151">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-153">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-153">Reserved.</span></span> <span data-ttu-id="b8fa9-154">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b8fa9-154">The default value is zero (0).</span></span>

<span data-ttu-id="b8fa9-155">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-155">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-156">**Initializationreentrancy**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-156">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-157">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-159">Ein Satz von Flags, die Informationen über die Serialisierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-159">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="b8fa9-160">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b8fa9-160">The default value is zero (0).</span></span>

<span data-ttu-id="b8fa9-161">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-161">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b8fa9-162"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-162"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b8fa9-163">Die gesamte Initialisierung dieses Anbieters muss serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-163">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="b8fa9-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b8fa9-165">Alle Initialisierungen dieses Anbieters im gleichen Namespace müssen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-165">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="b8fa9-166"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-166"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="b8fa9-167">Es ist keine Initialisierungs Serialisierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-167">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8fa9-168">**Initializationtimeoutinterval**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-168">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-169">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-169">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-171">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-171">Not used.</span></span>

<span data-ttu-id="b8fa9-172">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-172">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-173">**Initializeasadminfirst**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-173">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-174">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-176">**Windows Server 2003:** Diese Eigenschaft ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-176">**Windows Server 2003:** This property is disabled.</span></span>

<span data-ttu-id="b8fa9-177">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-177">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-180">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-181">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8fa9-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-182">Der Anbietername.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-182">The provider name.</span></span>

<span data-ttu-id="b8fa9-183">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-183">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-184">**Operationtimeoutinterval**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-184">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-185">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-185">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-186">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-187">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-187">Not used.</span></span>

<span data-ttu-id="b8fa9-188">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-188">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-189">**Perlocaleinitialization**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-189">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-190">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-191">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-192">**True** gibt an, dass der Anbieter für jedes Gebiets Schema initialisiert wird, wenn ein Benutzer mehr als einmal mit einem anderen Gebiets Schema eine Verbindung mit dem gleichen Namespace herstellt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-192">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="b8fa9-193">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-193">The default value is **FALSE**.</span></span>

<span data-ttu-id="b8fa9-194">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-194">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-195">**Peruserinitialization**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-195">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-196">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-197">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-198">**True** gibt an, dass der Anbieter für jeden NTLM-Benutzer (NT LAN Manager), der Anforderungen an den Anbieter sendet, einmal initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-198">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="b8fa9-199">Der Standardwert **false** gibt an, dass der Anbieter für alle Benutzer ein Mal initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-199">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

<span data-ttu-id="b8fa9-200">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-200">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-201">**Pure**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-201">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-202">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-203">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-203">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-204">**True** gibt an, dass der Anbieter die Entlade Vorbereitung durch Aufrufen von [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) an allen ausstehenden Schnittstellen Punkten zustimmt, wenn WMI die **releasemethode** der primären Schnittstelle aufruft.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-204">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="b8fa9-205">Anbieter, die Clients von WMI beibehalten müssen, nachdem Sie nicht als Anbieter fungieren, sollten **Pure** auf **false** festlegen.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-205">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="b8fa9-206">Die Standardeinstellung ist **true**.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-206">The default setting is **TRUE**.</span></span> <span data-ttu-id="b8fa9-207">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-207">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="b8fa9-208">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-208">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-209">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-209">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-212">Security Deskriptor (SD) in der Sicherheits beschreibungsdefinitions-Sprache (Security Deskriptor Definition Language, SDDL), die die Gruppe der Benutzer bestimmt, die [**iwbementkopppledregistrierungs: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) für den entkoppelten Anbieter erfolgreich aufruft.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-212">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="b8fa9-213">Weitere Informationen finden Sie im Thema Security [Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) im Abschnitt Security des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-213">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="b8fa9-214">Diese Sicherheits Beschreibung wird nur für entkoppelte Anbieter verwendet und wirkt sich nicht auf andere Anbieter aus.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-214">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="b8fa9-215">Weitere Informationen finden Sie unter [Einbinden eines Anbieters in eine Anwendung](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span><span class="sxs-lookup"><span data-stu-id="b8fa9-215">For more information, see [Incorporating a Provider in an Application](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span></span>

<span data-ttu-id="b8fa9-216">WMI führt Zugriffs Überprüfungen für entkoppelte Anbieter aus, die die Schnittstellen [**iwbemproviderinit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) und [**iwbemubjectsink**](/windows/desktop/WmiSdk/iwbemobjectsink) verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-216">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) interfaces.</span></span> <span data-ttu-id="b8fa9-217">Wenn die Sicherheits Beschreibung **null** ist, können nur Anwendungen oder Dienste, die unter dem Konto "LocalSystem", "NetworkService" und "LocalService" ausgeführt werden, einen entkoppelten Anbieter ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-217">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="b8fa9-218">Die folgende Zeichenfolge zeigt einen entkoppelten Anbieter, der nur von integrierten Administratoren ausgeführt werden soll. " O:Bag: Bad: (A;; 0 x1;;; BA) "</span><span class="sxs-lookup"><span data-stu-id="b8fa9-218">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="b8fa9-219">Weitere Informationen zum Festlegen der **securityDescriptor** -Eigenschaft finden Sie unter Verwalten der [WMI-Sicherheit](/windows/desktop/WmiSdk/maintaining-wmi-security).</span><span class="sxs-lookup"><span data-stu-id="b8fa9-219">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](/windows/desktop/WmiSdk/maintaining-wmi-security).</span></span>

<span data-ttu-id="b8fa9-220">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-220">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-221">**Supportsexplicitshutdown**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-221">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-222">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-224">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-224">Not used.</span></span>

<span data-ttu-id="b8fa9-225">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-225">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-226">**Supportsextendedstatus**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-226">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-227">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-228">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-229">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-229">Not used.</span></span>

<span data-ttu-id="b8fa9-230">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-230">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-231">**Supportsquotas**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-231">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-232">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-233">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-233">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-234">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-234">Not used.</span></span>

<span data-ttu-id="b8fa9-235">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-235">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-236">**Supportssendstatus**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-236">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-237">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-238">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-238">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-239">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-239">Not used.</span></span>

<span data-ttu-id="b8fa9-240">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-240">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-241">**Supportsshutdown**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-241">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-242">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-243">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-244">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-244">Not used.</span></span>

<span data-ttu-id="b8fa9-245">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-245">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-246">**Supportsdrosselung**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-246">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-247">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-248">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-249">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-249">Not used.</span></span>

<span data-ttu-id="b8fa9-250">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-250">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-251">**Unloadtimeout**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-251">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-252">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-254">[Datums-und Uhrzeit Format](/windows/desktop/WmiSdk/date-and-time-format) , das angibt, wie lange der Anbieter von WMI im Leerlauf bleiben kann, bevor er entladen wird.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-254">[Date and Time Format](/windows/desktop/WmiSdk/date-and-time-format) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="b8fa9-255">In der Regel fordern Anbieter an, dass die WMI-Wartezeit nicht länger als fünf Minuten dauert.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-255">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="b8fa9-256">Für die aktuelle Version von WMI wird der Wert dieser Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-256">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="b8fa9-257">WMI entlädt den Anbieter basierend auf dem Timeout Wert in einer internen Klasse im \\ Root-Namespace.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-257">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="b8fa9-258">Es wird empfohlen, dass Anbieter **unloadtimeout** festlegen.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-258">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="b8fa9-259">Weitere Informationen finden Sie unter [Entladen eines Anbieters](/windows/desktop/WmiSdk/unloading-a-provider).</span><span class="sxs-lookup"><span data-stu-id="b8fa9-259">For more information, see [Unloading a Provider](/windows/desktop/WmiSdk/unloading-a-provider).</span></span>

<span data-ttu-id="b8fa9-260">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-260">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="b8fa9-261">**Version**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-261">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8fa9-262">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8fa9-263">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b8fa9-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8fa9-264">Version des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-264">Version of the provider.</span></span> <span data-ttu-id="b8fa9-265">Die unterstützten Versionen sind 1 und 2.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-265">The supported versions are 1 and 2.</span></span> <span data-ttu-id="b8fa9-266">Version 2 stärkt die Gültigkeits Prüfungen für alle zugehörigen Eigenschaften Registrierungen, insbesondere die Eigenschaft "Identitäts [**ationlevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) ".</span><span class="sxs-lookup"><span data-stu-id="b8fa9-266">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) property.</span></span>

<span data-ttu-id="b8fa9-267">Diese Eigenschaft wird von [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-267">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8fa9-268">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8fa9-268">Remarks</span></span>

<span data-ttu-id="b8fa9-269">Eine Instanz dieser Klasse stellt den WMI-Anbieter für Active Directory-Domäne Services dar.</span><span class="sxs-lookup"><span data-stu-id="b8fa9-269">An instance of this class represents the WMI provider for Active Directory Domain services.</span></span> <span data-ttu-id="b8fa9-270">Folgende Standardwerte werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="b8fa9-270">The defaults are as follows:</span></span>

-   <span data-ttu-id="b8fa9-271">Name = "ReplProv1"</span><span class="sxs-lookup"><span data-stu-id="b8fa9-271">Name = "ReplProv1"</span></span>
-   <span data-ttu-id="b8fa9-272">CLSID = "{29288f 43-39b1-40dB-b41b-ce899450e911}"</span><span class="sxs-lookup"><span data-stu-id="b8fa9-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span></span>
-   <span data-ttu-id="b8fa9-273">Hostingmodel = "networkservicehost"</span><span class="sxs-lookup"><span data-stu-id="b8fa9-273">HostingModel = "NetworkServiceHost"</span></span>

## <a name="requirements"></a><span data-ttu-id="b8fa9-274">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8fa9-274">Requirements</span></span>



| <span data-ttu-id="b8fa9-275">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8fa9-275">Requirement</span></span> | <span data-ttu-id="b8fa9-276">Wert</span><span class="sxs-lookup"><span data-stu-id="b8fa9-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8fa9-277">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8fa9-277">Minimum supported client</span></span><br/> | <span data-ttu-id="b8fa9-278">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b8fa9-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b8fa9-279">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8fa9-279">Minimum supported server</span></span><br/> | <span data-ttu-id="b8fa9-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8fa9-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8fa9-281">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8fa9-281">Namespace</span></span><br/>                | <span data-ttu-id="b8fa9-282">\\Microsoftactivedirectory-Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="b8fa9-282">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="b8fa9-283">MOF</span><span class="sxs-lookup"><span data-stu-id="b8fa9-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8fa9-284"><dt>ReplProv. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b8fa9-284"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8fa9-285">DLL</span><span class="sxs-lookup"><span data-stu-id="b8fa9-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8fa9-286"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8fa9-286"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8fa9-287">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8fa9-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8fa9-288">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="b8fa9-288">**\_\_Win32Provider**</span></span>](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

