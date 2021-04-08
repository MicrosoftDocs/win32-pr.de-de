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
# <a name="__win32provider-class"></a><span data-ttu-id="d42da-104">\_\_Win32Provider-Klasse</span><span class="sxs-lookup"><span data-stu-id="d42da-104">\_\_Win32Provider class</span></span>

<span data-ttu-id="d42da-105">Die **\_ \_ Win32Provider** -System Klasse registriert Informationen über die physische Implementierung eines Anbieters in WMI.</span><span class="sxs-lookup"><span data-stu-id="d42da-105">The **\_\_Win32Provider** system class registers information about the physical implementation of a provider in WMI.</span></span> <span data-ttu-id="d42da-106">Anbieter, die die **hostingmodel** -Eigenschaft nicht festlegen, werden standardmäßig geladen, um Sie in einem Wmiprvse.exe Prozess als **Network servicehostorselfhost** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d42da-106">Providers that do not set the **HostingModel** property are loaded, by default, to run in a Wmiprvse.exe process as **NetworkServiceHostOrSelfHost**.</span></span>

<span data-ttu-id="d42da-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d42da-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d42da-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d42da-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d42da-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d42da-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="d42da-110">Member</span><span class="sxs-lookup"><span data-stu-id="d42da-110">Members</span></span>

<span data-ttu-id="d42da-111">Die **\_ \_ Win32Provider** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d42da-111">The **\_\_Win32Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="d42da-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d42da-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d42da-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d42da-113">Properties</span></span>

<span data-ttu-id="d42da-114">Die **\_ \_ Win32Provider** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d42da-114">The **\_\_Win32Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d42da-115">**Clientloadableclsid**</span><span class="sxs-lookup"><span data-stu-id="d42da-115">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d42da-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-118">Klassen Bezeichner, den WMI verwendet, um zu bestimmen, ob ein Hochleistungs Anbieter in den Client Prozess oder den WMI-Prozess geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d42da-118">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="d42da-119">Wenn sich sowohl der Anbieter als auch der Client auf demselben Computer befinden, lädt WMI den Anbieter Prozess Weise auf den Client, indem er **clientloadableclsid** als Klassen Bezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-119">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="d42da-120">Wenn sich der Anbieter und der Client auf unterschiedlichen Computern befinden, wird der Anbieter von WMI in-Process in den WMI-Prozess geladen.</span><span class="sxs-lookup"><span data-stu-id="d42da-120">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="d42da-121">WMI verwendet auch **clientloadableclsid** , um Aktualisierungs Vorgänge zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d42da-121">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="d42da-122">Weitere Informationen finden Sie unter [Registrieren eines High-Performance Anbieters.](registering-a-high-performance-provider.md)</span><span class="sxs-lookup"><span data-stu-id="d42da-122">For more information, see [Registering a High-Performance Provider.](registering-a-high-performance-provider.md)</span></span>

</dd> <dt>

<span data-ttu-id="d42da-123">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="d42da-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d42da-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-126">**GUID** , die den Klassen Bezeichner (**CLSID**) des COM-Objekts des Anbieters darstellt.</span><span class="sxs-lookup"><span data-stu-id="d42da-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="d42da-127">Dieses com-Objekt muss eine Implementierung der [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="d42da-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-128">**Parallelität**</span><span class="sxs-lookup"><span data-stu-id="d42da-128">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d42da-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-131">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-131">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-132">**Defaultmachinename**</span><span class="sxs-lookup"><span data-stu-id="d42da-132">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d42da-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-135">Identifiziert den Computer, auf dem der Anbieter gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d42da-135">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="d42da-136">Wenn der Anbieter auf dem lokalen Computer ausgeführt wird, ist er **null**.</span><span class="sxs-lookup"><span data-stu-id="d42da-136">If the provider runs on the local computer it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-137">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="d42da-137">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-140">**True** gibt an, dass diese Instanz aktiviert ist und verwendet werden kann, um Client Anforderungen abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d42da-140">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-141">**Hostingmodel**</span><span class="sxs-lookup"><span data-stu-id="d42da-141">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d42da-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-144">Diese Eigenschaft besteht aus Werten aus den Eigenschaften **hostinggroup** und **HostingSpecification** der [**MSFT- \_ Anbieter**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .</span><span class="sxs-lookup"><span data-stu-id="d42da-144">This property is composed of values from the [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** and **HostingSpecification** properties.</span></span> <span data-ttu-id="d42da-145">Der Wert dieser Eigenschaft gibt an, wie WMI den Anbieter und das Sicherheits Konto lädt, unter dem er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d42da-145">The value of this property specifies how WMI loads the provider and the security account it runs under.</span></span> <span data-ttu-id="d42da-146">Weitere Informationen zum Festlegen der **hostingmodel** -Eigenschaft finden Sie unter [Hosting und Sicherheit des Anbieters](provider-hosting-and-security.md) und [Registrieren eines Anbieters](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d42da-146">For more information about setting the **HostingModel** property, see [Provider Hosting and Security](provider-hosting-and-security.md) and [Registering a Provider](registering-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42da-147">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="d42da-147">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-148">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d42da-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-150">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d42da-150">Reserved.</span></span> <span data-ttu-id="d42da-151">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d42da-151">The default value is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="d42da-152">**Initializationreentrancy**</span><span class="sxs-lookup"><span data-stu-id="d42da-152">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d42da-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-155">Ein Satz von Flags, die Informationen über die Serialisierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d42da-155">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="d42da-156">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d42da-156">The default value is zero (0).</span></span>

<dt>

<span data-ttu-id="d42da-157">0</span><span class="sxs-lookup"><span data-stu-id="d42da-157">0</span></span>
</dt> <dd>

<span data-ttu-id="d42da-158">Die gesamte Initialisierung dieses Anbieters muss serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d42da-158">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-159">1</span><span class="sxs-lookup"><span data-stu-id="d42da-159">1</span></span>
</dt> <dd>

<span data-ttu-id="d42da-160">Alle Initialisierungen dieses Anbieters im gleichen Namespace müssen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d42da-160">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-161">2</span><span class="sxs-lookup"><span data-stu-id="d42da-161">2</span></span>
</dt> <dd>

<span data-ttu-id="d42da-162">Es ist keine Initialisierungs Serialisierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d42da-162">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d42da-163">**Initializationtimeoutinterval**</span><span class="sxs-lookup"><span data-stu-id="d42da-163">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-164">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d42da-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-166">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-167">**Initializeasadminfirst**</span><span class="sxs-lookup"><span data-stu-id="d42da-167">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-168">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-170">TBD</span><span class="sxs-lookup"><span data-stu-id="d42da-170">TBD</span></span>

</dd> <dt>

<span data-ttu-id="d42da-171">**Name**</span><span class="sxs-lookup"><span data-stu-id="d42da-171">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d42da-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d42da-174">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d42da-174">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d42da-175">Der Anbietername.</span><span class="sxs-lookup"><span data-stu-id="d42da-175">The provider name.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-176">**Operationtimeoutinterval**</span><span class="sxs-lookup"><span data-stu-id="d42da-176">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-177">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d42da-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-179">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-180">**Perlocaleinitialization**</span><span class="sxs-lookup"><span data-stu-id="d42da-180">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-181">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-182">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-183">**True** gibt an, dass der Anbieter für jedes Gebiets Schema initialisiert wird, wenn ein Benutzer mehr als einmal mit einem anderen Gebiets Schema eine Verbindung mit dem gleichen Namespace herstellt.</span><span class="sxs-lookup"><span data-stu-id="d42da-183">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="d42da-184">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d42da-184">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-185">**Peruserinitialization**</span><span class="sxs-lookup"><span data-stu-id="d42da-185">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-186">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-188">**True** gibt an, dass der Anbieter für jeden NTLM-Benutzer (NT LAN Manager), der Anforderungen an den Anbieter sendet, einmal initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d42da-188">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="d42da-189">Der Standardwert **false** gibt an, dass der Anbieter für alle Benutzer ein Mal initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d42da-189">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-190">**Pure**</span><span class="sxs-lookup"><span data-stu-id="d42da-190">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-191">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-192">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-193">**True** gibt an, dass der Anbieter die Entlade Vorbereitung durch Aufrufen von [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) an allen ausstehenden Schnittstellen Punkten zustimmt, wenn WMI die **releasemethode** der primären Schnittstelle aufruft.</span><span class="sxs-lookup"><span data-stu-id="d42da-193">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="d42da-194">Anbieter, die Clients von WMI beibehalten müssen, nachdem Sie nicht als Anbieter fungieren, sollten **Pure** auf **false** festlegen.</span><span class="sxs-lookup"><span data-stu-id="d42da-194">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="d42da-195">Die Standardeinstellung ist **true**.</span><span class="sxs-lookup"><span data-stu-id="d42da-195">The default setting is **TRUE**.</span></span> <span data-ttu-id="d42da-196">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="d42da-196">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-197">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d42da-197">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d42da-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-199">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-200">Security Deskriptor (SD) in der Sicherheits beschreibungsdefinitions-Sprache (Security Deskriptor Definition Language, SDDL), die die Gruppe der Benutzer bestimmt, die [**iwbementkopppledregistrierungs: Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) für den entkoppelten Anbieter erfolgreich aufruft.</span><span class="sxs-lookup"><span data-stu-id="d42da-200">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="d42da-201">Weitere Informationen finden Sie im Thema Security [Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) im Abschnitt Security des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d42da-201">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="d42da-202">Diese Sicherheits Beschreibung wird nur für entkoppelte Anbieter verwendet und wirkt sich nicht auf andere Anbieter aus.</span><span class="sxs-lookup"><span data-stu-id="d42da-202">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="d42da-203">Weitere Informationen finden Sie unter [Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="d42da-203">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="d42da-204">WMI führt Zugriffs Überprüfungen für entkoppelte Anbieter aus, die die Schnittstellen [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und [**iwbemubjectsink**](iwbemobjectsink.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d42da-204">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](iwbemobjectsink.md) interfaces.</span></span> <span data-ttu-id="d42da-205">Wenn die Sicherheits Beschreibung **null** ist, können nur Anwendungen oder Dienste, die unter dem Konto "LocalSystem", "NetworkService" und "LocalService" ausgeführt werden, einen entkoppelten Anbieter ausführen.</span><span class="sxs-lookup"><span data-stu-id="d42da-205">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="d42da-206">Die folgende Zeichenfolge zeigt einen entkoppelten Anbieter, der nur von integrierten Administratoren ausgeführt werden soll. " O:Bag: Bad: (A;; 0 x1;;; BA) "</span><span class="sxs-lookup"><span data-stu-id="d42da-206">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="d42da-207">Weitere Informationen zum Festlegen der **securityDescriptor** -Eigenschaft finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="d42da-207">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42da-208">**Supportsexplicitshutdown**</span><span class="sxs-lookup"><span data-stu-id="d42da-208">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-209">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-210">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-211">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-212">**Supportsextendedstatus**</span><span class="sxs-lookup"><span data-stu-id="d42da-212">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-213">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-215">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-216">**Supportsquotas**</span><span class="sxs-lookup"><span data-stu-id="d42da-216">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-217">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-218">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-219">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-219">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-220">**Supportssendstatus**</span><span class="sxs-lookup"><span data-stu-id="d42da-220">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-221">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-222">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-223">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-223">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-224">**Supportsshutdown**</span><span class="sxs-lookup"><span data-stu-id="d42da-224">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-225">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-227">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-227">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-228">**Supportsdrosselung**</span><span class="sxs-lookup"><span data-stu-id="d42da-228">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-229">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-229">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-230">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-230">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-231">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-231">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d42da-232">**Unloadtimeout**</span><span class="sxs-lookup"><span data-stu-id="d42da-232">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-233">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d42da-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-234">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-234">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-235">[Datums-und Uhrzeit Format](date-and-time-format.md) , das angibt, wie lange der Anbieter von WMI im Leerlauf bleiben kann, bevor er entladen wird.</span><span class="sxs-lookup"><span data-stu-id="d42da-235">[Date and Time Format](date-and-time-format.md) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="d42da-236">In der Regel fordern Anbieter an, dass die WMI-Wartezeit nicht länger als fünf Minuten dauert.</span><span class="sxs-lookup"><span data-stu-id="d42da-236">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="d42da-237">Für die aktuelle Version von WMI wird der Wert dieser Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d42da-237">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="d42da-238">WMI entlädt den Anbieter basierend auf dem Timeout Wert in einer internen Klasse im \\ Root-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d42da-238">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="d42da-239">Es wird empfohlen, dass Anbieter **unloadtimeout** festlegen.</span><span class="sxs-lookup"><span data-stu-id="d42da-239">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="d42da-240">Weitere Informationen finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d42da-240">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42da-241">**Version**</span><span class="sxs-lookup"><span data-stu-id="d42da-241">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42da-242">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d42da-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42da-243">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d42da-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d42da-244">Version des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="d42da-244">Version of the provider.</span></span> <span data-ttu-id="d42da-245">Die unterstützten Versionen sind 1 und 2.</span><span class="sxs-lookup"><span data-stu-id="d42da-245">The supported versions are 1 and 2.</span></span> <span data-ttu-id="d42da-246">Version 2 stärkt die Gültigkeits Prüfungen für alle zugehörigen Eigenschaften Registrierungen, insbesondere die Eigenschaft "Identitäts [**ationlevel**](swbemsecurity-impersonationlevel.md) ".</span><span class="sxs-lookup"><span data-stu-id="d42da-246">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d42da-247">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d42da-247">Remarks</span></span>

<span data-ttu-id="d42da-248">Die **\_ \_ Win32Provider** -Klasse wird vom [**\_ \_ Anbieter**](--provider.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d42da-248">The **\_\_Win32Provider** class is derived from [**\_\_Provider**](--provider.md).</span></span>

<span data-ttu-id="d42da-249">Die meisten Anbieter können die Standardwerte für die **initializationreentrancy** -Eigenschaft akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="d42da-249">Most providers can accept the default values for the **InitializationReentrancy** property.</span></span> <span data-ttu-id="d42da-250">Wenn ein Anbieter jedoch die gleichzeitige Initialisierung für separate Benutzer unterstützen kann, kann diese Eigenschaft auf 1 (eins) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d42da-250">However, if a provider can support simultaneous initialization for separate users, this property can be set to 1 (one).</span></span> <span data-ttu-id="d42da-251">Wenn eine serialisierte Initialisierung erforderlich ist, bleibt **initializationreentrancy** 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d42da-251">If serialized initialization is necessary, **InitializationReentrancy** remains 0 (zero).</span></span> <span data-ttu-id="d42da-252">In beiden Fällen ist " **peruserinitialization** " auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d42da-252">In both instances, **PerUserInitialization** is set to **TRUE**.</span></span>

<span data-ttu-id="d42da-253">Ein reiner Anbieter oder Anbieter, der die **Pure** -Eigenschaft auf **true** festlegt, ist nur für Dienst Anforderungen von Anwendungen und WMI vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d42da-253">A pure provider or a provider that sets the **Pure** property to **TRUE**, exists only to service requests from applications and WMI.</span></span> <span data-ttu-id="d42da-254">Die meisten Anbieter sind reine Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d42da-254">Most providers are pure providers.</span></span> <span data-ttu-id="d42da-255">Ein nicht reiner Anbieter ist die Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="d42da-255">A nonpure provider is the exception.</span></span> <span data-ttu-id="d42da-256">Nicht reine Anbieter wechseln nach dem Abschluss von Wartungsanforderungen zur Rolle des Clients.</span><span class="sxs-lookup"><span data-stu-id="d42da-256">Nonpure providers transition to the role of client after they complete servicing requests.</span></span>

<span data-ttu-id="d42da-257">Ein Beispiel für einen nicht reinen Anbieter ist ein Push-Anbieter, der mit der Ausgabe von Abfragen beginnt und nach Abschluss der Initialisierung Anforderungen an WMI sendet.</span><span class="sxs-lookup"><span data-stu-id="d42da-257">An example of a nonpure provider is a push provider that starts to issue queries, and makes requests of WMI after it completes initialization.</span></span> <span data-ttu-id="d42da-258">Ein pushanbieter hat keine Zuständigkeiten, außer wenn das CIM-Repository mit Daten zum Zeitpunkt der Initialisierung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d42da-258">A push provider does not have responsibilities except to update the CIM repository with data at initialization time.</span></span> <span data-ttu-id="d42da-259">Nach dem Aktualisieren des Repository kann ein pushanbieter darauf warten, entladen zu werden, oder zur Client Rolle wechseln.</span><span class="sxs-lookup"><span data-stu-id="d42da-259">After updating the repository, a push provider can wait to be unloaded, or transition to the role of client.</span></span> <span data-ttu-id="d42da-260">Der Push-Anbieter, der darauf wartet, entladen zu werden, ist ein reiner Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d42da-260">The push provider that waits to be unloaded is a pure provider.</span></span> <span data-ttu-id="d42da-261">Der Push-Anbieter, der an Client Aktivitäten teilnimmt, ist nicht rein.</span><span class="sxs-lookup"><span data-stu-id="d42da-261">The push provider that participates in client activities is nonpure.</span></span>

<span data-ttu-id="d42da-262">WMI muss in der Lage sein, reine Anbieter von nicht reinen Anbietern zu unterscheiden, damit ermittelt werden kann, wann das Herunterfahren sicher ist.</span><span class="sxs-lookup"><span data-stu-id="d42da-262">WMI must be able to distinguish pure providers from non-pure providers so that it can determine when it is safe to shut down.</span></span> <span data-ttu-id="d42da-263">WMI muss darauf warten, dass alle Vorgänge, die nicht-reine Anbieter einschließen, vollständig beendet werden, bevor er sicher heruntergefahren werden kann.</span><span class="sxs-lookup"><span data-stu-id="d42da-263">WMI must wait for all operations that involve non-pure providers to complete before it can shut down safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="d42da-264">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d42da-264">Requirements</span></span>



| <span data-ttu-id="d42da-265">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d42da-265">Requirement</span></span> | <span data-ttu-id="d42da-266">Wert</span><span class="sxs-lookup"><span data-stu-id="d42da-266">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d42da-267">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d42da-267">Minimum supported client</span></span><br/> | <span data-ttu-id="d42da-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d42da-268">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d42da-269">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d42da-269">Minimum supported server</span></span><br/> | <span data-ttu-id="d42da-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d42da-270">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d42da-271">Namespace</span><span class="sxs-lookup"><span data-stu-id="d42da-271">Namespace</span></span><br/>                | <span data-ttu-id="d42da-272">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="d42da-272">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d42da-273">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d42da-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d42da-274">**\_\_Anbieter**</span><span class="sxs-lookup"><span data-stu-id="d42da-274">**\_\_Provider**</span></span>](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[<span data-ttu-id="d42da-275">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="d42da-275">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d42da-276">Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="d42da-276">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

