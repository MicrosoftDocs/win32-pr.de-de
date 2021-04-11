---
description: Enthält ein-Objekt für jede com+-Anwendung, die auf dem lokalen Computer installiert ist. Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, enthalten alle Einstellungen auf Anwendungsebene.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Applications-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127172"
---
# <a name="applications-collection"></a><span data-ttu-id="34e90-104">Applications-Sammlung</span><span class="sxs-lookup"><span data-stu-id="34e90-104">Applications collection</span></span>

<span data-ttu-id="34e90-105">Enthält ein-Objekt für jede com+-Anwendung, die auf dem lokalen Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-105">Contains an object for each COM+ application installed on the local computer.</span></span> <span data-ttu-id="34e90-106">Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, enthalten alle Einstellungen auf Anwendungsebene.</span><span class="sxs-lookup"><span data-stu-id="34e90-106">The properties exposed by these objects hold all settings made at the application level.</span></span>

<span data-ttu-id="34e90-107">Mithilfe der Auflistung verknüpfter [**Komponenten**](components.md) legen Sie Eigenschaften für Komponenten innerhalb einer Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="34e90-107">You set properties for components within an application by using the related [**Components**](components.md) collection.</span></span> <span data-ttu-id="34e90-108">Sie weisen einer Anwendung Rollen mithilfe der Auflistung verwandte [**Rollen**](roles.md) zu.</span><span class="sxs-lookup"><span data-stu-id="34e90-108">You assign roles to an application by using the related [**Roles**](roles.md) collection.</span></span>

<span data-ttu-id="34e90-109">Verwenden Sie Methoden für das [**comadmincatalog**](comadmincatalog.md) -Objekt, um Komponenten in einer Anwendung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="34e90-109">To install components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="34e90-110">Wenn Sie eine Anwendung aus einer Datei installieren oder eine Anwendung Herunterfahren oder exportieren möchten, verwenden Sie auch Methoden für das **comadmincatalog** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="34e90-110">To install an application from a file or to shut down or export an application, also use methods on the **COMAdminCatalog** object.</span></span> <span data-ttu-id="34e90-111">Andernfalls können Sie der **Anwendungs** Auflistung ein Objekt hinzufügen, um eine neue Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34e90-111">Otherwise, to create a new application, you can add an object to the **Applications** collection.</span></span>

<span data-ttu-id="34e90-112">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="34e90-112">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="34e90-113">Member</span><span class="sxs-lookup"><span data-stu-id="34e90-113">Members</span></span>

<span data-ttu-id="34e90-114">Die **Anwendungs** Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="34e90-114">The **Applications** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="34e90-115">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="34e90-115">Related Collections</span></span>

<span data-ttu-id="34e90-116">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="34e90-116">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="34e90-117">**ApplicationInstance**</span><span class="sxs-lookup"><span data-stu-id="34e90-117">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="34e90-118">**Komponenten**</span><span class="sxs-lookup"><span data-stu-id="34e90-118">**Components**</span></span>](components.md)
-   [<span data-ttu-id="34e90-119">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="34e90-119">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="34e90-120">**Legacycomponents**</span><span class="sxs-lookup"><span data-stu-id="34e90-120">**LegacyComponents**</span></span>](legacycomponents.md)
-   [<span data-ttu-id="34e90-121">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="34e90-121">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="34e90-122">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="34e90-122">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="34e90-123">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="34e90-123">**Roles**</span></span>](roles.md)

<span data-ttu-id="34e90-124">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="34e90-124">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="34e90-125">**Partitionen**</span><span class="sxs-lookup"><span data-stu-id="34e90-125">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="34e90-126">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="34e90-126">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="34e90-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34e90-127">Properties</span></span>

<span data-ttu-id="34e90-128">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="34e90-128">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="34e90-129">3gigsupportenabled</span><span class="sxs-lookup"><span data-stu-id="34e90-129">3GigSupportEnabled</span></span>](#3gigsupportenabled)
-   [<span data-ttu-id="34e90-130">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="34e90-130">AccessChecksLevel</span></span>](#accesscheckslevel)
-   [<span data-ttu-id="34e90-131">Aktivierung</span><span class="sxs-lookup"><span data-stu-id="34e90-131">Activation</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="34e90-132">Applicationaccesschecksenabled</span><span class="sxs-lookup"><span data-stu-id="34e90-132">ApplicationAccessChecksEnabled</span></span>](#applicationaccesschecksenabled)
-   [<span data-ttu-id="34e90-133">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="34e90-133">ApplicationDirectory</span></span>](#applicationdirectory)
-   [<span data-ttu-id="34e90-134">Applicationproxy</span><span class="sxs-lookup"><span data-stu-id="34e90-134">ApplicationProxy</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="34e90-135">Applicationproxyservername</span><span class="sxs-lookup"><span data-stu-id="34e90-135">ApplicationProxyServerName</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="34e90-136">Apppartitionid</span><span class="sxs-lookup"><span data-stu-id="34e90-136">AppPartitionID</span></span>](#apppartitionid)
-   [<span data-ttu-id="34e90-137">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="34e90-137">Authentication</span></span>](#authenticationcapability)
-   [<span data-ttu-id="34e90-138">Authenticationcapability</span><span class="sxs-lookup"><span data-stu-id="34e90-138">AuthenticationCapability</span></span>](#authenticationcapability)
-   [<span data-ttu-id="34e90-139">Austauschbar</span><span class="sxs-lookup"><span data-stu-id="34e90-139">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="34e90-140">CommandLine</span><span class="sxs-lookup"><span data-stu-id="34e90-140">CommandLine</span></span>](#commandline)
-   [<span data-ttu-id="34e90-141">Concurrentapps</span><span class="sxs-lookup"><span data-stu-id="34e90-141">ConcurrentApps</span></span>](#concurrentapps)
-   [<span data-ttu-id="34e90-142">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="34e90-142">CreatedBy</span></span>](#createdby)
-   [<span data-ttu-id="34e90-143">Crmenabled</span><span class="sxs-lookup"><span data-stu-id="34e90-143">CRMEnabled</span></span>](#crmenabled)
-   [<span data-ttu-id="34e90-144">Crmlogfile</span><span class="sxs-lookup"><span data-stu-id="34e90-144">CRMLogFile</span></span>](#crmlogfile)
-   [<span data-ttu-id="34e90-145">Gelöscht werden</span><span class="sxs-lookup"><span data-stu-id="34e90-145">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="34e90-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34e90-146">Description</span></span>](#description)
-   [<span data-ttu-id="34e90-147">Dumpfähig</span><span class="sxs-lookup"><span data-stu-id="34e90-147">DumpEnabled</span></span>](#dumpenabled)
-   [<span data-ttu-id="34e90-148">Dumponexception</span><span class="sxs-lookup"><span data-stu-id="34e90-148">DumpOnException</span></span>](#dumponexception)
-   [<span data-ttu-id="34e90-149">Dumponfailfast</span><span class="sxs-lookup"><span data-stu-id="34e90-149">DumpOnFailfast</span></span>](#dumponfailfast)
-   [<span data-ttu-id="34e90-150">DumpPath</span><span class="sxs-lookup"><span data-stu-id="34e90-150">DumpPath</span></span>](#dumppath)
-   [<span data-ttu-id="34e90-151">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="34e90-151">EventsEnabled</span></span>](#eventsenabled)
-   [<span data-ttu-id="34e90-152">ID</span><span class="sxs-lookup"><span data-stu-id="34e90-152">ID</span></span>](#applications-collection)
-   [<span data-ttu-id="34e90-153">Identität</span><span class="sxs-lookup"><span data-stu-id="34e90-153">Identity</span></span>](#identity)
-   [<span data-ttu-id="34e90-154">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="34e90-154">ImpersonationLevel</span></span>](#impersonationlevel)
-   [<span data-ttu-id="34e90-155">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="34e90-155">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="34e90-156">IsSystem</span><span class="sxs-lookup"><span data-stu-id="34e90-156">IsSystem</span></span>](#issystem)
-   [<span data-ttu-id="34e90-157">Maxdumpcount</span><span class="sxs-lookup"><span data-stu-id="34e90-157">MaxDumpCount</span></span>](#maxdumpcount)
-   [<span data-ttu-id="34e90-158">Name</span><span class="sxs-lookup"><span data-stu-id="34e90-158">Name</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="34e90-159">Kennwort</span><span class="sxs-lookup"><span data-stu-id="34e90-159">Password</span></span>](#password)
-   [<span data-ttu-id="34e90-160">Qcauthentikatemsgs</span><span class="sxs-lookup"><span data-stu-id="34e90-160">QCAuthenticateMsgs</span></span>](#qcauthenticatemsgs)
-   [<span data-ttu-id="34e90-161">QcListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="34e90-161">QCListenerMaxThreads</span></span>](#qclistenermaxthreads)
-   [<span data-ttu-id="34e90-162">Queuelisteneraktivierte</span><span class="sxs-lookup"><span data-stu-id="34e90-162">QueueListenerEnabled</span></span>](#queuelistenerenabled)
-   [<span data-ttu-id="34e90-163">Queuingenabled</span><span class="sxs-lookup"><span data-stu-id="34e90-163">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="34e90-164">Recycleactivationlimit</span><span class="sxs-lookup"><span data-stu-id="34e90-164">RecycleActivationLimit</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="34e90-165">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="34e90-165">RecycleCallLimit</span></span>](#recyclecalllimit)
-   [<span data-ttu-id="34e90-166">Recycleexpirationtimeout</span><span class="sxs-lookup"><span data-stu-id="34e90-166">RecycleExpirationTimeout</span></span>](#recycleexpirationtimeout)
-   [<span data-ttu-id="34e90-167">Recyclelifetimelimit</span><span class="sxs-lookup"><span data-stu-id="34e90-167">RecycleLifetimeLimit</span></span>](#recyclelifetimelimit)
-   [<span data-ttu-id="34e90-168">Recyclememorylimit</span><span class="sxs-lookup"><span data-stu-id="34e90-168">RecycleMemoryLimit</span></span>](#recyclememorylimit)
-   [<span data-ttu-id="34e90-169">Replizierbare</span><span class="sxs-lookup"><span data-stu-id="34e90-169">Replicable</span></span>](#replicable)
-   [<span data-ttu-id="34e90-170">Runforever</span><span class="sxs-lookup"><span data-stu-id="34e90-170">RunForever</span></span>](#runforever)
-   [<span data-ttu-id="34e90-171">Service Name</span><span class="sxs-lookup"><span data-stu-id="34e90-171">ServiceName</span></span>](#servicename)
-   [<span data-ttu-id="34e90-172">Shutdownafter</span><span class="sxs-lookup"><span data-stu-id="34e90-172">ShutdownAfter</span></span>](#shutdownafter)
-   [<span data-ttu-id="34e90-173">Soapaktivierte</span><span class="sxs-lookup"><span data-stu-id="34e90-173">SoapActivated</span></span>](#soapactivated)
-   [<span data-ttu-id="34e90-174">Soapbaseurl</span><span class="sxs-lookup"><span data-stu-id="34e90-174">SoapBaseUrl</span></span>](#soapbaseurl)
-   [<span data-ttu-id="34e90-175">Soapmailto</span><span class="sxs-lookup"><span data-stu-id="34e90-175">SoapMailTo</span></span>](#soapmailto)
-   [<span data-ttu-id="34e90-176">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="34e90-176">SoapVRoot</span></span>](#soapvroot)
-   [<span data-ttu-id="34e90-177">Srpabled</span><span class="sxs-lookup"><span data-stu-id="34e90-177">SRPEnabled</span></span>](#srpenabled)
-   [<span data-ttu-id="34e90-178">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="34e90-178">SRPTrustLevel</span></span>](#srptrustlevel)

### <a name="3gigsupportenabled"></a><span data-ttu-id="34e90-179">3gigsupportenabled</span><span class="sxs-lookup"><span data-stu-id="34e90-179">3GigSupportEnabled</span></span>



| <span data-ttu-id="34e90-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-180">Entry</span></span> | <span data-ttu-id="34e90-181">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-181">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-182">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-182">Description</span></span>    | <span data-ttu-id="34e90-183">Gibt an, ob die Anwendung im Prozess 3 GB Arbeitsspeicher verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="34e90-183">Indicates whether the application can use 3 GB of memory in its process.</span></span> <span data-ttu-id="34e90-184">Wenn diese Option nicht aktiviert ist, kann die Anwendung nur 2 GB Arbeitsspeicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="34e90-184">If this is not enabled, the application can use only 2 GB of memory.</span></span> |
| <span data-ttu-id="34e90-185">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-185">Access</span></span>         | <span data-ttu-id="34e90-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-186">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="34e90-187">type</span><span class="sxs-lookup"><span data-stu-id="34e90-187">Type</span></span>           | <span data-ttu-id="34e90-188">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-188">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="34e90-189">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-189">Default</span></span>        | <span data-ttu-id="34e90-190">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-190">False</span></span>                                                                                                                                         |
| <span data-ttu-id="34e90-191">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-191">Minimum system</span></span> | <span data-ttu-id="34e90-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-192">Windows 2000</span></span>                                                                                                                                  |



 

### <a name="accesscheckslevel"></a><span data-ttu-id="34e90-193">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="34e90-193">AccessChecksLevel</span></span>



| <span data-ttu-id="34e90-194">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-194">Entry</span></span> | <span data-ttu-id="34e90-195">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-195">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-196">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-196">Description</span></span>    | <span data-ttu-id="34e90-197">Gibt an, ob Zugriffs Überprüfungen nur auf der Prozessebene oder auf Prozess-und Komponentenebene durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-197">Indicates whether access checks are performed at only the process level or at both the process and component level.</span></span> <span data-ttu-id="34e90-198">Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="34e90-198">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="34e90-199">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-199">Access</span></span>         | <span data-ttu-id="34e90-200">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-200">ReadWrite</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="34e90-201">type</span><span class="sxs-lookup"><span data-stu-id="34e90-201">Type</span></span>           | <span data-ttu-id="34e90-202">Lange mögliche Werte: comadminaccesschecksapplicationlevel (0) comadminaccesschecksapplicationcomponentlevel (1)</span><span class="sxs-lookup"><span data-stu-id="34e90-202">Long Possible values: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                |
| <span data-ttu-id="34e90-203">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-203">Default</span></span>        | <span data-ttu-id="34e90-204">Comadminaccesschecksapplicationcomponentlevel (1)</span><span class="sxs-lookup"><span data-stu-id="34e90-204">COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                                                                               |
| <span data-ttu-id="34e90-205">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-205">Minimum system</span></span> | <span data-ttu-id="34e90-206">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-206">Windows 2000</span></span>                                                                                                                                                                                                    |



 

### <a name="activation"></a><span data-ttu-id="34e90-207">Aktivierung</span><span class="sxs-lookup"><span data-stu-id="34e90-207">Activation</span></span>



| <span data-ttu-id="34e90-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-208">Entry</span></span> | <span data-ttu-id="34e90-209">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-209">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-210">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-210">Description</span></span>    | <span data-ttu-id="34e90-211">Lokale Aktivierung gibt an, dass Objekte innerhalb der Anwendung innerhalb eines dedizierten lokalen Server Prozesses (Serveranwendung) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-211">Local activation indicates that objects within the application run within a dedicated local server process (server application).</span></span> <span data-ttu-id="34e90-212">Die Prozess interne Aktivierung gibt an, dass Objekte im Prozess des Erstellers (Bibliotheks Anwendung) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-212">In-process activation indicates that objects run in their creator's process (library application).</span></span> |
| <span data-ttu-id="34e90-213">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-213">Access</span></span>         | <span data-ttu-id="34e90-214">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-214">ReadWrite</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="34e90-215">type</span><span class="sxs-lookup"><span data-stu-id="34e90-215">Type</span></span>           | <span data-ttu-id="34e90-216">Lange mögliche Werte: comadminactivationinproc (0) comadminactivationlocal (1)</span><span class="sxs-lookup"><span data-stu-id="34e90-216">Long Possible values:COMAdminActivationInproc (0)COMAdminActivationLocal (1)</span></span>                                                                                                                                                        |
| <span data-ttu-id="34e90-217">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-217">Default</span></span>        | <span data-ttu-id="34e90-218">Comadminactivationlocal (1)</span><span class="sxs-lookup"><span data-stu-id="34e90-218">COMAdminActivationLocal (1)</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="34e90-219">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-219">Minimum system</span></span> | <span data-ttu-id="34e90-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-220">Windows 2000</span></span>                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a><span data-ttu-id="34e90-221">Applicationaccesschecksenabled</span><span class="sxs-lookup"><span data-stu-id="34e90-221">ApplicationAccessChecksEnabled</span></span>



| <span data-ttu-id="34e90-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-222">Entry</span></span> | <span data-ttu-id="34e90-223">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-223">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-224">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-224">Description</span></span>    | <span data-ttu-id="34e90-225">Gibt an, ob Zugriffs Überprüfungen für die Anwendung ausgeführt werden, wenn Clients Aufrufe an die Anwendung durchführen.</span><span class="sxs-lookup"><span data-stu-id="34e90-225">Indicates whether access checks are performed for the application when clients make calls into it.</span></span> |
| <span data-ttu-id="34e90-226">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-226">Access</span></span>         | <span data-ttu-id="34e90-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-227">ReadWrite</span></span>                                                                                          |
| <span data-ttu-id="34e90-228">type</span><span class="sxs-lookup"><span data-stu-id="34e90-228">Type</span></span>           | <span data-ttu-id="34e90-229">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-229">Bool</span></span>                                                                                               |
| <span data-ttu-id="34e90-230">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-230">Default</span></span>        | <span data-ttu-id="34e90-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="34e90-231">True</span></span>                                                                                               |
| <span data-ttu-id="34e90-232">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-232">Minimum system</span></span> | <span data-ttu-id="34e90-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-233">Windows 2000</span></span>                                                                                       |



 

### <a name="applicationdirectory"></a><span data-ttu-id="34e90-234">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="34e90-234">ApplicationDirectory</span></span>



| <span data-ttu-id="34e90-235">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-235">Entry</span></span> | <span data-ttu-id="34e90-236">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-236">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-237">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-237">Description</span></span>    | <span data-ttu-id="34e90-238">Der vollständige Pfad zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="34e90-238">The full path to the application.</span></span> <span data-ttu-id="34e90-239">Diese Informationen sind erforderlich, wenn Sie parallele Assemblys (SxS) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="34e90-239">This information is needed when you configure Side-by-Side (SxS) assemblies.</span></span> <span data-ttu-id="34e90-240">Parallele Assemblys (SxS) ermöglichen ASP-Anwendungen, anzugeben, welche Version einer SxS-unterstützten System-DLL verwendet werden soll, z. b. msvcrt, MSXML, COMCTL, gdiplus usw.</span><span class="sxs-lookup"><span data-stu-id="34e90-240">Side-by-side (SxS) assemblies allow ASP applications to specify which version of an SxS-supported system DLL to use, such as MSVCRT, MSXML, COMCTL, GDIPLUS, and so on.</span></span> <span data-ttu-id="34e90-241">Wenn Ihre ASP-Anwendung z. b. msvcrt Version 2,0 verwendet, können Sie sicherstellen, dass Ihre Anwendung weiterhin msvcrt Version 2,0 verwendet, auch nachdem Service Packs auf den Server angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="34e90-241">For example, if your ASP application relies on MSVCRT version 2.0, you can ensure that your application still uses MSVCRT version 2.0 even after service packs are applied to the server.</span></span> <span data-ttu-id="34e90-242">Jede neue Version von msvcrt ist weiterhin auf dem Computer installiert, Version 2,0 bleibt jedoch erhalten und wird von Ihrer Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="34e90-242">Any new version of MSVCRT is still installed on the computer, but version 2.0 remains and is used by your application.</span></span> <span data-ttu-id="34e90-243">SxS-unterstützte DLLs werden in% windir% \\ WinSxS gespeichert.</span><span class="sxs-lookup"><span data-stu-id="34e90-243">SxS-supported DLLs are stored in %WINDIR%\\WinSxS.</span></span> |
| <span data-ttu-id="34e90-244">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-244">Access</span></span>         | <span data-ttu-id="34e90-245">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-245">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="34e90-246">type</span><span class="sxs-lookup"><span data-stu-id="34e90-246">Type</span></span>           | <span data-ttu-id="34e90-247">String</span><span class="sxs-lookup"><span data-stu-id="34e90-247">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="34e90-248">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-248">Default</span></span>        | <span data-ttu-id="34e90-249">""</span><span class="sxs-lookup"><span data-stu-id="34e90-249">""</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="34e90-250">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-250">Minimum system</span></span> | <span data-ttu-id="34e90-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-251">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="34e90-252">Nur eine Version einer System-DLL kann in einem Anwendungs Pool verwendet werden, auch wenn diese Funktion auf Anwendungsebene konfigurierbar ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-252">Only one version of a system DLL can be used in any application pool, even though this feature is configurable at the application level.</span></span> <span data-ttu-id="34e90-253">Wenn z. b. Application App1 msvcrt verwendet, Version 2,5 und Application App2 msvcrt, Version 2,4, verwendet wird, sollten App1 und App2 nicht im selben Anwendungs Pool sein.</span><span class="sxs-lookup"><span data-stu-id="34e90-253">For example, if application App1 uses MSVCRT, version 2.5 and application App2 uses MSVCRT, version 2.4, then App1 and App2 should not be in the same application pool.</span></span> <span data-ttu-id="34e90-254">Wenn dies der Fall ist, wird die Version von msvcrt der Anwendung, die zuerst geladen wird, geladen, und die andere Anwendung wird gezwungen, Sie zu verwenden, bis die Anwendungen entladen werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-254">If they are, the application that is loaded first has its version of MSVCRT loaded, and the other application is forced to use it until the applications are unloaded.</span></span>

 

<span data-ttu-id="34e90-255">Weitere Informationen finden Sie unter "parallele Assemblys" in [Änderungen in den COM+-Diensten in IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="34e90-255">For more information, see "Side-by-Side Assemblies" in [Changes in COM+ Services in IIS 6.0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span></span>

### <a name="applicationproxy"></a><span data-ttu-id="34e90-256">Applicationproxy</span><span class="sxs-lookup"><span data-stu-id="34e90-256">ApplicationProxy</span></span>



| <span data-ttu-id="34e90-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-257">Entry</span></span> | <span data-ttu-id="34e90-258">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-258">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="34e90-259">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-259">Description</span></span>    | <span data-ttu-id="34e90-260">Gibt an, ob die Anwendung ein Anwendungs Proxy ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-260">Indicates whether the application is an application proxy.</span></span> |
| <span data-ttu-id="34e90-261">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-261">Access</span></span>         | <span data-ttu-id="34e90-262">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="34e90-262">ReadOnly</span></span>                                                   |
| <span data-ttu-id="34e90-263">type</span><span class="sxs-lookup"><span data-stu-id="34e90-263">Type</span></span>           | <span data-ttu-id="34e90-264">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-264">Bool</span></span>                                                       |
| <span data-ttu-id="34e90-265">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-265">Default</span></span>        | <span data-ttu-id="34e90-266">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-266">False</span></span>                                                      |
| <span data-ttu-id="34e90-267">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-267">Minimum system</span></span> | <span data-ttu-id="34e90-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-268">Windows 2000</span></span>                                               |



 

### <a name="applicationproxyservername"></a><span data-ttu-id="34e90-269">Applicationproxyservername</span><span class="sxs-lookup"><span data-stu-id="34e90-269">ApplicationProxyServerName</span></span>



| <span data-ttu-id="34e90-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-270">Entry</span></span> | <span data-ttu-id="34e90-271">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-271">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-272">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-272">Description</span></span>    | <span data-ttu-id="34e90-273">Ein Remote Servername, der beim Exportieren des Anwendungs Proxys verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-273">A remote server name used when exporting the application proxy.</span></span> <span data-ttu-id="34e90-274">Dabei handelt es sich um den Servernamen, auf den der Anwendungs Proxy verweist, wenn er auf einem Client Computer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-274">It is this server name that the application proxy points to when it is installed on a client computer.</span></span> |
| <span data-ttu-id="34e90-275">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-275">Access</span></span>         | <span data-ttu-id="34e90-276">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-276">ReadWrite</span></span>                                                                                                                                                              |
| <span data-ttu-id="34e90-277">type</span><span class="sxs-lookup"><span data-stu-id="34e90-277">Type</span></span>           | <span data-ttu-id="34e90-278">String</span><span class="sxs-lookup"><span data-stu-id="34e90-278">String</span></span>                                                                                                                                                                 |
| <span data-ttu-id="34e90-279">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-279">Default</span></span>        | <span data-ttu-id="34e90-280">""</span><span class="sxs-lookup"><span data-stu-id="34e90-280">""</span></span>                                                                                                                                                                     |
| <span data-ttu-id="34e90-281">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-281">Minimum system</span></span> | <span data-ttu-id="34e90-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-282">Windows 2000</span></span>                                                                                                                                                           |



 

### <a name="apppartitionid"></a><span data-ttu-id="34e90-283">Apppartitionid</span><span class="sxs-lookup"><span data-stu-id="34e90-283">AppPartitionID</span></span>



| <span data-ttu-id="34e90-284">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-284">Entry</span></span> | <span data-ttu-id="34e90-285">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-285">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="34e90-286">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-286">Description</span></span>    | <span data-ttu-id="34e90-287">Eine GUID, die die ID der Anwendungs Partition darstellt.</span><span class="sxs-lookup"><span data-stu-id="34e90-287">A GUID representing the application partition ID.</span></span> |
| <span data-ttu-id="34e90-288">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-288">Access</span></span>         | <span data-ttu-id="34e90-289">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="34e90-289">ReadOnly</span></span>                                          |
| <span data-ttu-id="34e90-290">type</span><span class="sxs-lookup"><span data-stu-id="34e90-290">Type</span></span>           | <span data-ttu-id="34e90-291">String</span><span class="sxs-lookup"><span data-stu-id="34e90-291">String</span></span>                                            |
| <span data-ttu-id="34e90-292">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-292">Default</span></span>        | <Generated>                                 |
| <span data-ttu-id="34e90-293">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-293">Minimum system</span></span> | <span data-ttu-id="34e90-294">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34e90-294">Windows Server 2003</span></span>                               |



 

### <a name="authentication"></a><span data-ttu-id="34e90-295">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="34e90-295">Authentication</span></span>



| <span data-ttu-id="34e90-296">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-296">Entry</span></span> | <span data-ttu-id="34e90-297">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-297">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-298">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-298">Description</span></span>    | <span data-ttu-id="34e90-299">Legt die Authentifizierungs Ebene für Aufrufe fest, wobei die Werte den RPC-Authentifizierungs Einstellungen (Remote Procedure Calls) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="34e90-299">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="34e90-300">Wenn comadminauthenticationdefault ausgewählt wird, wird die Einstellung in der DefaultAuthenticationLevel-Eigenschaft in der [**LocalComputer**](localcomputer.md) -Sammlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="34e90-300">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="34e90-301">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-301">Access</span></span>         | <span data-ttu-id="34e90-302">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-302">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="34e90-303">type</span><span class="sxs-lookup"><span data-stu-id="34e90-303">Type</span></span>           | <span data-ttu-id="34e90-304">Lange mögliche Werte: comadminauthenticationdefault (0) comadminauthenticationnone (1) comadminauthenticationconnect (2) comadminauthentication-Aufruf (3) comadminauthenticationpacket (4) comadminauthenticationintegrity (5) comadminauthenticationprivacy (6)</span><span class="sxs-lookup"><span data-stu-id="34e90-304">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="34e90-305">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-305">Default</span></span>        | <span data-ttu-id="34e90-306">Comadminauthenticationpacket (4)</span><span class="sxs-lookup"><span data-stu-id="34e90-306">COMAdminAuthenticationPacket (4)</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="34e90-307">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-307">Minimum system</span></span> | <span data-ttu-id="34e90-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-308">Windows 2000</span></span>                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> <span data-ttu-id="34e90-309">Für Bibliotheksanwendungen (in-Process) sind nur die folgenden gültigen Einstellungen für comadminauthenticationdefault und comadminauthenticationnone zulässig.</span><span class="sxs-lookup"><span data-stu-id="34e90-309">For library (in-process) applications, the only valid settings here are COMAdminAuthenticationDefault and COMAdminAuthenticationNone .</span></span> <span data-ttu-id="34e90-310">Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="34e90-310">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="authenticationcapability"></a><span data-ttu-id="34e90-311">Authenticationcapability</span><span class="sxs-lookup"><span data-stu-id="34e90-311">AuthenticationCapability</span></span>



| <span data-ttu-id="34e90-312">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-312">Entry</span></span> | <span data-ttu-id="34e90-313">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-313">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-314">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-314">Description</span></span>    | <span data-ttu-id="34e90-315">Bestimmt, welche Identität bei Aufrufen von Aufrufen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-315">Determines what identity is presented when calls are impersonated.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="34e90-316">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-316">Access</span></span>         | <span data-ttu-id="34e90-317">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-317">ReadWrite</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="34e90-318">type</span><span class="sxs-lookup"><span data-stu-id="34e90-318">Type</span></span>           | <span data-ttu-id="34e90-319">Lange mögliche Werte: comadminauthenticationcapabilitiesnone (0x0) comadminauthenticationcapabilitiessecurereferen(0x2) comadminauthenticationcapabilitiesstaticcloaking (0x20) comadminauthenticationcapabilitiesdynamiccloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="34e90-319">Long Possible values:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span> |
| <span data-ttu-id="34e90-320">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-320">Default</span></span>        | <span data-ttu-id="34e90-321">Comadminauthenticationcapabilitiesdynamiccloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="34e90-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span>                                                                                                                                                                                |
| <span data-ttu-id="34e90-322">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-322">Minimum system</span></span> | <span data-ttu-id="34e90-323">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-323">Windows 2000</span></span>                                                                                                                                                                                                                            |



 

### <a name="changeable"></a><span data-ttu-id="34e90-324">Austauschbar</span><span class="sxs-lookup"><span data-stu-id="34e90-324">Changeable</span></span>



| <span data-ttu-id="34e90-325">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-325">Entry</span></span> | <span data-ttu-id="34e90-326">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-326">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-327">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-327">Description</span></span>    | <span data-ttu-id="34e90-328">Bestimmt, ob Änderungen an den Anwendungseinstellungen oder den zugehörigen Komponenten entweder Programm gesteuert oder über das Verwaltungs Tool "Komponenten Dienste" zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="34e90-328">Determines whether changes to the application settings or those of its components are allowed, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="34e90-329">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-329">Access</span></span>         | <span data-ttu-id="34e90-330">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-330">ReadWrite</span></span>                                                                                                                                                                     |
| <span data-ttu-id="34e90-331">type</span><span class="sxs-lookup"><span data-stu-id="34e90-331">Type</span></span>           | <span data-ttu-id="34e90-332">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-332">Bool</span></span>                                                                                                                                                                          |
| <span data-ttu-id="34e90-333">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-333">Default</span></span>        | <span data-ttu-id="34e90-334">Richtig</span><span class="sxs-lookup"><span data-stu-id="34e90-334">True</span></span>                                                                                                                                                                          |
| <span data-ttu-id="34e90-335">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-335">Minimum system</span></span> | <span data-ttu-id="34e90-336">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-336">Windows 2000</span></span>                                                                                                                                                                  |



 

### <a name="commandline"></a><span data-ttu-id="34e90-337">CommandLine</span><span class="sxs-lookup"><span data-stu-id="34e90-337">CommandLine</span></span>



| <span data-ttu-id="34e90-338">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-338">Entry</span></span> | <span data-ttu-id="34e90-339">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-339">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-340">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-340">Description</span></span>    | <span data-ttu-id="34e90-341">Eine Befehlszeilen Zeichenfolge für die Verwendung beim Debuggen.</span><span class="sxs-lookup"><span data-stu-id="34e90-341">A command-line string for use in debugging.</span></span> <span data-ttu-id="34e90-342">Die Anwendung kann in einem Debugger mit der angegebenen Befehlszeile gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-342">The application can be launched in a debugger with the specified command line.</span></span> |
| <span data-ttu-id="34e90-343">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-343">Access</span></span>         | <span data-ttu-id="34e90-344">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-344">ReadWrite</span></span>                                                                                                                  |
| <span data-ttu-id="34e90-345">type</span><span class="sxs-lookup"><span data-stu-id="34e90-345">Type</span></span>           | <span data-ttu-id="34e90-346">String</span><span class="sxs-lookup"><span data-stu-id="34e90-346">String</span></span>                                                                                                                     |
| <span data-ttu-id="34e90-347">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-347">Default</span></span>        | <span data-ttu-id="34e90-348">""</span><span class="sxs-lookup"><span data-stu-id="34e90-348">""</span></span>                                                                                                                         |
| <span data-ttu-id="34e90-349">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-349">Minimum system</span></span> | <span data-ttu-id="34e90-350">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-350">Windows 2000</span></span>                                                                                                               |



 

### <a name="concurrentapps"></a><span data-ttu-id="34e90-351">Concurrentapps</span><span class="sxs-lookup"><span data-stu-id="34e90-351">ConcurrentApps</span></span>



| <span data-ttu-id="34e90-352">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-352">Entry</span></span> | <span data-ttu-id="34e90-353">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-353">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-354">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-354">Description</span></span>    | <span data-ttu-id="34e90-355">Gibt die maximale Anzahl von Pool fähigen Anwendungen an, die gleichzeitig ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="34e90-355">Specifies the maximum number of poolable applications that can run concurrently.</span></span> |
| <span data-ttu-id="34e90-356">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-356">Access</span></span>         | <span data-ttu-id="34e90-357">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-357">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="34e90-358">type</span><span class="sxs-lookup"><span data-stu-id="34e90-358">Type</span></span>           | <span data-ttu-id="34e90-359">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="34e90-359">Long (1-1048576)</span></span>                                                                 |
| <span data-ttu-id="34e90-360">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-360">Default</span></span>        | <span data-ttu-id="34e90-361">1</span><span class="sxs-lookup"><span data-stu-id="34e90-361">1</span></span>                                                                                |
| <span data-ttu-id="34e90-362">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-362">Minimum system</span></span> | <span data-ttu-id="34e90-363">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-363">Windows XP</span></span>                                                                       |



 

### <a name="createdby"></a><span data-ttu-id="34e90-364">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="34e90-364">CreatedBy</span></span>



| <span data-ttu-id="34e90-365">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-365">Entry</span></span> | <span data-ttu-id="34e90-366">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-366">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="34e90-367">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-367">Description</span></span>    | <span data-ttu-id="34e90-368">Informations Zeichenfolge, die beschreibt, wer die Anwendung erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="34e90-368">Informational string to describe who created the application.</span></span> |
| <span data-ttu-id="34e90-369">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-369">Access</span></span>         | <span data-ttu-id="34e90-370">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-370">ReadWrite</span></span>                                                     |
| <span data-ttu-id="34e90-371">type</span><span class="sxs-lookup"><span data-stu-id="34e90-371">Type</span></span>           | <span data-ttu-id="34e90-372">String</span><span class="sxs-lookup"><span data-stu-id="34e90-372">String</span></span>                                                        |
| <span data-ttu-id="34e90-373">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-373">Default</span></span>        | <span data-ttu-id="34e90-374">""</span><span class="sxs-lookup"><span data-stu-id="34e90-374">""</span></span>                                                            |
| <span data-ttu-id="34e90-375">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-375">Minimum system</span></span> | <span data-ttu-id="34e90-376">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-376">Windows 2000</span></span>                                                  |



 

### <a name="crmenabled"></a><span data-ttu-id="34e90-377">Crmenabled</span><span class="sxs-lookup"><span data-stu-id="34e90-377">CRMEnabled</span></span>



| <span data-ttu-id="34e90-378">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-378">Entry</span></span> | <span data-ttu-id="34e90-379">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-379">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="34e90-380">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-380">Description</span></span>    | <span data-ttu-id="34e90-381">Bestimmt, ob das kompensierende Ressourcen-Manager aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-381">Determines whether the Compensating Resource Manager is enabled.</span></span> |
| <span data-ttu-id="34e90-382">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-382">Access</span></span>         | <span data-ttu-id="34e90-383">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-383">ReadWrite</span></span>                                                        |
| <span data-ttu-id="34e90-384">type</span><span class="sxs-lookup"><span data-stu-id="34e90-384">Type</span></span>           | <span data-ttu-id="34e90-385">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-385">Bool</span></span>                                                             |
| <span data-ttu-id="34e90-386">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-386">Default</span></span>        | <span data-ttu-id="34e90-387">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-387">False</span></span>                                                            |
| <span data-ttu-id="34e90-388">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-388">Minimum system</span></span> | <span data-ttu-id="34e90-389">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-389">Windows 2000</span></span>                                                     |



 

### <a name="crmlogfile"></a><span data-ttu-id="34e90-390">Crmlogfile</span><span class="sxs-lookup"><span data-stu-id="34e90-390">CRMLogFile</span></span>



| <span data-ttu-id="34e90-391">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-391">Entry</span></span> | <span data-ttu-id="34e90-392">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-392">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-393">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-393">Description</span></span>    | <span data-ttu-id="34e90-394">Name und Pfad der Datei, in der das Protokoll für den kompensierenden Ressourcen-Manager (CRM) aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-394">Name and path of file for keeping the log for the compensating resource manager (CRM).</span></span> |
| <span data-ttu-id="34e90-395">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-395">Access</span></span>         | <span data-ttu-id="34e90-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-396">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="34e90-397">type</span><span class="sxs-lookup"><span data-stu-id="34e90-397">Type</span></span>           | <span data-ttu-id="34e90-398">String</span><span class="sxs-lookup"><span data-stu-id="34e90-398">String</span></span>                                                                                 |
| <span data-ttu-id="34e90-399">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-399">Default</span></span>        | <span data-ttu-id="34e90-400">""</span><span class="sxs-lookup"><span data-stu-id="34e90-400">""</span></span>                                                                                     |
| <span data-ttu-id="34e90-401">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-401">Minimum system</span></span> | <span data-ttu-id="34e90-402">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-402">Windows 2000</span></span>                                                                           |



 

### <a name="deleteable"></a><span data-ttu-id="34e90-403">Gelöscht werden</span><span class="sxs-lookup"><span data-stu-id="34e90-403">Deleteable</span></span>



| <span data-ttu-id="34e90-404">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-404">Entry</span></span> | <span data-ttu-id="34e90-405">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-405">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-406">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-406">Description</span></span>    | <span data-ttu-id="34e90-407">Legt fest, ob die Anwendung entweder Programm gesteuert oder über das Verwaltungs Tool Komponenten Dienste gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="34e90-407">Sets whether the application can be deleted, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="34e90-408">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-408">Access</span></span>         | <span data-ttu-id="34e90-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-409">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="34e90-410">type</span><span class="sxs-lookup"><span data-stu-id="34e90-410">Type</span></span>           | <span data-ttu-id="34e90-411">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-411">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="34e90-412">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-412">Default</span></span>        | <span data-ttu-id="34e90-413">Richtig</span><span class="sxs-lookup"><span data-stu-id="34e90-413">True</span></span>                                                                                                                        |
| <span data-ttu-id="34e90-414">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-414">Minimum system</span></span> | <span data-ttu-id="34e90-415">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-415">Windows 2000</span></span>                                                                                                                |



 

### <a name="description"></a><span data-ttu-id="34e90-416">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-416">Description</span></span>



| <span data-ttu-id="34e90-417">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-417">Entry</span></span> | <span data-ttu-id="34e90-418">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-418">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="34e90-419">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-419">Description</span></span>    | <span data-ttu-id="34e90-420">Beschreibt die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="34e90-420">Describes the application.</span></span> |
| <span data-ttu-id="34e90-421">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-421">Access</span></span>         | <span data-ttu-id="34e90-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-422">ReadWrite</span></span>                  |
| <span data-ttu-id="34e90-423">type</span><span class="sxs-lookup"><span data-stu-id="34e90-423">Type</span></span>           | <span data-ttu-id="34e90-424">String</span><span class="sxs-lookup"><span data-stu-id="34e90-424">String</span></span>                     |
| <span data-ttu-id="34e90-425">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-425">Default</span></span>        | <span data-ttu-id="34e90-426">""</span><span class="sxs-lookup"><span data-stu-id="34e90-426">""</span></span>                         |
| <span data-ttu-id="34e90-427">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-427">Minimum system</span></span> | <span data-ttu-id="34e90-428">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-428">Windows 2000</span></span>               |



 

### <a name="dumpenabled"></a><span data-ttu-id="34e90-429">Dumpfähig</span><span class="sxs-lookup"><span data-stu-id="34e90-429">DumpEnabled</span></span>



| <span data-ttu-id="34e90-430">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-430">Entry</span></span> | <span data-ttu-id="34e90-431">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-431">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-432">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-432">Description</span></span>    | <span data-ttu-id="34e90-433">Ermöglicht das Sichern des Status einer COM+-Anwendung zum Zeitpunkt des Fehlers in einem bestimmten Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="34e90-433">Enables the dump of the state of a COM+ application at the time of failure to a designated directory.</span></span> |
| <span data-ttu-id="34e90-434">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-434">Access</span></span>         | <span data-ttu-id="34e90-435">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-435">ReadWrite</span></span>                                                                                             |
| <span data-ttu-id="34e90-436">type</span><span class="sxs-lookup"><span data-stu-id="34e90-436">Type</span></span>           | <span data-ttu-id="34e90-437">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-437">Bool</span></span>                                                                                                  |
| <span data-ttu-id="34e90-438">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-438">Default</span></span>        | <span data-ttu-id="34e90-439">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-439">False</span></span>                                                                                                 |
| <span data-ttu-id="34e90-440">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-440">Minimum system</span></span> | <span data-ttu-id="34e90-441">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-441">Windows XP</span></span>                                                                                            |



 

> [!Note]  
> <span data-ttu-id="34e90-442">Ab Windows Server 2003 verfügen nur Administratoren über Lese Zugriffsberechtigungen für die com+-Dumpdateien.</span><span class="sxs-lookup"><span data-stu-id="34e90-442">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="dumponexception"></a><span data-ttu-id="34e90-443">Dumponexception</span><span class="sxs-lookup"><span data-stu-id="34e90-443">DumpOnException</span></span>



| <span data-ttu-id="34e90-444">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-444">Entry</span></span> | <span data-ttu-id="34e90-445">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-445">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-446">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-446">Description</span></span>    | <span data-ttu-id="34e90-447">Ermöglicht das Sichern des Status einer COM+-Anwendung, wenn die Anwendung eine nicht behandelte Ausnahme verursacht und von der com+-Laufzeit beendet wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-447">Enables the dump of the state of a COM+ application when the application causes an unhandled exception and is terminated by the COM+ runtime.</span></span> |
| <span data-ttu-id="34e90-448">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-448">Access</span></span>         | <span data-ttu-id="34e90-449">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-449">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="34e90-450">type</span><span class="sxs-lookup"><span data-stu-id="34e90-450">Type</span></span>           | <span data-ttu-id="34e90-451">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-451">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="34e90-452">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-452">Default</span></span>        | <span data-ttu-id="34e90-453">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-453">False</span></span>                                                                                                                                         |
| <span data-ttu-id="34e90-454">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-454">Minimum system</span></span> | <span data-ttu-id="34e90-455">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-455">Windows XP</span></span>                                                                                                                                    |



 

### <a name="dumponfailfast"></a><span data-ttu-id="34e90-456">Dumponfailfast</span><span class="sxs-lookup"><span data-stu-id="34e90-456">DumpOnFailfast</span></span>



| <span data-ttu-id="34e90-457">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-457">Entry</span></span> | <span data-ttu-id="34e90-458">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-458">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-459">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-459">Description</span></span>    | <span data-ttu-id="34e90-460">Ermöglicht das Sichern des Zustands einer COM+-Anwendung, wenn die Anwendung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="34e90-460">Enables the dump of the state of a COM+ application when the application fails.</span></span> |
| <span data-ttu-id="34e90-461">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-461">Access</span></span>         | <span data-ttu-id="34e90-462">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-462">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="34e90-463">type</span><span class="sxs-lookup"><span data-stu-id="34e90-463">Type</span></span>           | <span data-ttu-id="34e90-464">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-464">Bool</span></span>                                                                            |
| <span data-ttu-id="34e90-465">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-465">Default</span></span>        | <span data-ttu-id="34e90-466">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-466">False</span></span>                                                                           |
| <span data-ttu-id="34e90-467">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-467">Minimum system</span></span> | <span data-ttu-id="34e90-468">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-468">Windows XP</span></span>                                                                      |



 

### <a name="dumppath"></a><span data-ttu-id="34e90-469">DumpPath</span><span class="sxs-lookup"><span data-stu-id="34e90-469">DumpPath</span></span>



| <span data-ttu-id="34e90-470">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-470">Entry</span></span> | <span data-ttu-id="34e90-471">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-471">Value</span></span> |
|----------------|--------------------------------------------------------------|
| <span data-ttu-id="34e90-472">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-472">Description</span></span>    | <span data-ttu-id="34e90-473">Der Pfad des Verzeichnisses, in dem die Dumpdateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-473">The path of the directory in which the dump files are saved.</span></span> |
| <span data-ttu-id="34e90-474">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-474">Access</span></span>         | <span data-ttu-id="34e90-475">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-475">ReadWrite</span></span>                                                    |
| <span data-ttu-id="34e90-476">type</span><span class="sxs-lookup"><span data-stu-id="34e90-476">Type</span></span>           | <span data-ttu-id="34e90-477">String</span><span class="sxs-lookup"><span data-stu-id="34e90-477">String</span></span>                                                       |
| <span data-ttu-id="34e90-478">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-478">Default</span></span>        | <span data-ttu-id="34e90-479">"% SystemRoot% \\ system32 \\ com \\ DMP"</span><span class="sxs-lookup"><span data-stu-id="34e90-479">"%systemroot%\\system32\\com\\dmp"</span></span>                           |
| <span data-ttu-id="34e90-480">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-480">Minimum system</span></span> | <span data-ttu-id="34e90-481">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-481">Windows XP</span></span>                                                   |



 

> [!Note]  
> <span data-ttu-id="34e90-482">Ab Windows Server 2003 verfügen nur Administratoren über Lese Zugriffsberechtigungen für die com+-Dumpdateien.</span><span class="sxs-lookup"><span data-stu-id="34e90-482">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="eventsenabled"></a><span data-ttu-id="34e90-483">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="34e90-483">EventsEnabled</span></span>



| <span data-ttu-id="34e90-484">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-484">Entry</span></span> | <span data-ttu-id="34e90-485">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-485">Value</span></span> |
|----------------|-----------------------------------------------------------|
| <span data-ttu-id="34e90-486">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-486">Description</span></span>    | <span data-ttu-id="34e90-487">Gibt an, ob Ereignisse für die Anwendung aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="34e90-487">Indicates whether events are enabled for the application.</span></span> |
| <span data-ttu-id="34e90-488">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-488">Access</span></span>         | <span data-ttu-id="34e90-489">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-489">ReadWrite</span></span>                                                 |
| <span data-ttu-id="34e90-490">type</span><span class="sxs-lookup"><span data-stu-id="34e90-490">Type</span></span>           | <span data-ttu-id="34e90-491">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-491">Bool</span></span>                                                      |
| <span data-ttu-id="34e90-492">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-492">Default</span></span>        | <span data-ttu-id="34e90-493">Richtig</span><span class="sxs-lookup"><span data-stu-id="34e90-493">True</span></span>                                                      |
| <span data-ttu-id="34e90-494">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-494">Minimum system</span></span> | <span data-ttu-id="34e90-495">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-495">Windows 2000</span></span>                                              |



 

### <a name="id"></a><span data-ttu-id="34e90-496">id</span><span class="sxs-lookup"><span data-stu-id="34e90-496">ID</span></span>



| <span data-ttu-id="34e90-497">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-497">Entry</span></span> | <span data-ttu-id="34e90-498">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-498">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-499">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-499">Description</span></span>    | <span data-ttu-id="34e90-500">Eine GUID, die die Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="34e90-500">A GUID representing the application.</span></span> <span data-ttu-id="34e90-501">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-501">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="34e90-502">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-502">Access</span></span>         | <span data-ttu-id="34e90-503">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="34e90-503">WriteOnce</span></span>                                                                                                                                                            |
| <span data-ttu-id="34e90-504">type</span><span class="sxs-lookup"><span data-stu-id="34e90-504">Type</span></span>           | <span data-ttu-id="34e90-505">String</span><span class="sxs-lookup"><span data-stu-id="34e90-505">String</span></span>                                                                                                                                                               |
| <span data-ttu-id="34e90-506">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-506">Default</span></span>        | <Generated>                                                                                                                                                    |
| <span data-ttu-id="34e90-507">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-507">Minimum system</span></span> | <span data-ttu-id="34e90-508">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-508">Windows 2000</span></span>                                                                                                                                                         |



 

### <a name="identity"></a><span data-ttu-id="34e90-509">Identity</span><span class="sxs-lookup"><span data-stu-id="34e90-509">Identity</span></span>



| <span data-ttu-id="34e90-510">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-510">Entry</span></span> | <span data-ttu-id="34e90-511">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-511">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-512">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-512">Description</span></span>    | <span data-ttu-id="34e90-513">Legt die Server Prozess Identität für die Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="34e90-513">Sets the server process identity for the application.</span></span> <span data-ttu-id="34e90-514">Geben Sie ein gültiges Benutzerkonto oder einen interaktiven Benutzer an, damit die Anwendung die Identität des aktuell angemeldeten Benutzers annimmt.</span><span class="sxs-lookup"><span data-stu-id="34e90-514">Specify a valid user account or "Interactive User" to have the application assume the identity of the current logged-on user.</span></span> <span data-ttu-id="34e90-515">Sie können auch die Zeichen folgen "NT Authority \\ LocalService", "NT Authority \\ Network Service" und "NT Authority \\ System" angeben.</span><span class="sxs-lookup"><span data-stu-id="34e90-515">You can also specify the strings "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system".</span></span> <span data-ttu-id="34e90-516">Das Standard Kennwort für diese drei Konten ist "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="34e90-516">The default password for these three accounts is "" (empty string).</span></span> |
| <span data-ttu-id="34e90-517">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-517">Access</span></span>         |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="34e90-518">type</span><span class="sxs-lookup"><span data-stu-id="34e90-518">Type</span></span>           |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="34e90-519">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-519">Default</span></span>        |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="34e90-520">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-520">Minimum system</span></span> | <span data-ttu-id="34e90-521">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-521">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="34e90-522">Die Identity-Eigenschaft ist nicht für Bibliotheksanwendungen aktiviert, die im Client Prozess ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-522">The Identity property is not enabled for library applications, which run in the client process.</span></span>

<span data-ttu-id="34e90-523">Die Password-Eigenschaft sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-523">The Password property should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="34e90-524">Wenn das Kennwort und die Identität nicht synchron sind, kann die Anwendung erst gestartet werden, wenn Sie von einem Administrator zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-524">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="impersonationlevel"></a><span data-ttu-id="34e90-525">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="34e90-525">ImpersonationLevel</span></span>



| <span data-ttu-id="34e90-526">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-526">Entry</span></span> | <span data-ttu-id="34e90-527">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-527">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-528">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-528">Description</span></span>    | <span data-ttu-id="34e90-529">Legt die Identitätswechsel Ebene fest, die für Aufrufe an andere Anwendungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-529">Sets impersonation level used for calls made to other applications.</span></span>                                                                                           |
| <span data-ttu-id="34e90-530">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-530">Access</span></span>         | <span data-ttu-id="34e90-531">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-531">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="34e90-532">type</span><span class="sxs-lookup"><span data-stu-id="34e90-532">Type</span></span>           | <span data-ttu-id="34e90-533">Lange mögliche Werte: comadminimpersonationanonymous (1) comadminimpersonationidentifiout (2) comadminimpersonationidentität (3) comadminimpersonationdelegat (4)</span><span class="sxs-lookup"><span data-stu-id="34e90-533">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="34e90-534">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-534">Default</span></span>        | <span data-ttu-id="34e90-535">Comadminimpersonationimitation (3)</span><span class="sxs-lookup"><span data-stu-id="34e90-535">COMAdminImpersonationImpersonate (3)</span></span>                                                                                                                          |
| <span data-ttu-id="34e90-536">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-536">Minimum system</span></span> | <span data-ttu-id="34e90-537">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-537">Windows 2000</span></span>                                                                                                                                                  |



 

### <a name="isenabled"></a><span data-ttu-id="34e90-538">isEnabled</span><span class="sxs-lookup"><span data-stu-id="34e90-538">IsEnabled</span></span>



| <span data-ttu-id="34e90-539">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-539">Entry</span></span> | <span data-ttu-id="34e90-540">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-540">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-541">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-541">Description</span></span>    | <span data-ttu-id="34e90-542">Wenn die COM+-Anwendung oder-Komponente deaktiviert ist, ist isaktivierter Wert false.</span><span class="sxs-lookup"><span data-stu-id="34e90-542">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="34e90-543">Wenn die COM+-Anwendung oder-Komponente aktiviert ist, ist isaktivierte "true".</span><span class="sxs-lookup"><span data-stu-id="34e90-543">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="34e90-544">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-544">Access</span></span>         | <span data-ttu-id="34e90-545">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-545">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="34e90-546">type</span><span class="sxs-lookup"><span data-stu-id="34e90-546">Type</span></span>           | <span data-ttu-id="34e90-547">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-547">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="34e90-548">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-548">Default</span></span>        | <span data-ttu-id="34e90-549">Richtig</span><span class="sxs-lookup"><span data-stu-id="34e90-549">True</span></span>                                                                                                                                      |
| <span data-ttu-id="34e90-550">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-550">Minimum system</span></span> | <span data-ttu-id="34e90-551">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-551">Windows XP</span></span>                                                                                                                                |



 

### <a name="issystem"></a><span data-ttu-id="34e90-552">IsSystem</span><span class="sxs-lookup"><span data-stu-id="34e90-552">IsSystem</span></span>



| <span data-ttu-id="34e90-553">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-553">Entry</span></span> | <span data-ttu-id="34e90-554">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-554">Value</span></span> |
|----------------|--------------------------------------|
| <span data-ttu-id="34e90-555">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-555">Description</span></span>    | <span data-ttu-id="34e90-556">Identifiziert com+-Systemanwendungen.</span><span class="sxs-lookup"><span data-stu-id="34e90-556">Identifies COM+ system applications.</span></span> |
| <span data-ttu-id="34e90-557">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-557">Access</span></span>         | <span data-ttu-id="34e90-558">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="34e90-558">ReadOnly</span></span>                             |
| <span data-ttu-id="34e90-559">type</span><span class="sxs-lookup"><span data-stu-id="34e90-559">Type</span></span>           | <span data-ttu-id="34e90-560">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-560">Bool</span></span>                                 |
| <span data-ttu-id="34e90-561">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-561">Default</span></span>        | <span data-ttu-id="34e90-562">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-562">False</span></span>                                |
| <span data-ttu-id="34e90-563">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-563">Minimum system</span></span> | <span data-ttu-id="34e90-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-564">Windows 2000</span></span>                         |



 

### <a name="maxdumpcount"></a><span data-ttu-id="34e90-565">Maxdumpcount</span><span class="sxs-lookup"><span data-stu-id="34e90-565">MaxDumpCount</span></span>



| <span data-ttu-id="34e90-566">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-566">Entry</span></span> | <span data-ttu-id="34e90-567">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-567">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-568">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-568">Description</span></span>    | <span data-ttu-id="34e90-569">Gibt die maximale Anzahl der Dateien an, die vor dem Überschreiben generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="34e90-569">Indicates the maximum number of files to be generated before overwriting occurs.</span></span> |
| <span data-ttu-id="34e90-570">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-570">Access</span></span>         | <span data-ttu-id="34e90-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-571">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="34e90-572">type</span><span class="sxs-lookup"><span data-stu-id="34e90-572">Type</span></span>           | <span data-ttu-id="34e90-573">Long (1-200)</span><span class="sxs-lookup"><span data-stu-id="34e90-573">Long (1-200)</span></span>                                                                     |
| <span data-ttu-id="34e90-574">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-574">Default</span></span>        | <span data-ttu-id="34e90-575">5</span><span class="sxs-lookup"><span data-stu-id="34e90-575">5</span></span>                                                                                |
| <span data-ttu-id="34e90-576">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-576">Minimum system</span></span> | <span data-ttu-id="34e90-577">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-577">Windows XP</span></span>                                                                       |



 

### <a name="name"></a><span data-ttu-id="34e90-578">Name</span><span class="sxs-lookup"><span data-stu-id="34e90-578">Name</span></span>



| <span data-ttu-id="34e90-579">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-579">Entry</span></span> | <span data-ttu-id="34e90-580">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-580">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-581">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-581">Description</span></span>    | <span data-ttu-id="34e90-582">Der Namen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="34e90-582">The name of the application.</span></span> <span data-ttu-id="34e90-583">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-583">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="34e90-584">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-584">Access</span></span>         | <span data-ttu-id="34e90-585">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-585">ReadWrite</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="34e90-586">type</span><span class="sxs-lookup"><span data-stu-id="34e90-586">Type</span></span>           | <span data-ttu-id="34e90-587">String</span><span class="sxs-lookup"><span data-stu-id="34e90-587">String</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="34e90-588">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-588">Default</span></span>        | <span data-ttu-id="34e90-589">"Neue Anwendung"</span><span class="sxs-lookup"><span data-stu-id="34e90-589">"New Application"</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="34e90-590">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-590">Minimum system</span></span> | <span data-ttu-id="34e90-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-591">Windows 2000</span></span>                                                                                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="34e90-592">Eindeutige Namen sollten für Anwendungen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-592">Unique names should be chosen for applications.</span></span> <span data-ttu-id="34e90-593">Wenn mehrere Anwendungen mit demselben Namen erstellt werden, kann das verweisen auf die Anwendungen nach Name beeinträchtigt werden, was zu unvorhersehbarem Verhalten führt.</span><span class="sxs-lookup"><span data-stu-id="34e90-593">If multiple applications are created with the same name, it can interfere with referencing the applications by name, resulting in unpredictable behavior.</span></span>

 

### <a name="password"></a><span data-ttu-id="34e90-594">Kennwort</span><span class="sxs-lookup"><span data-stu-id="34e90-594">Password</span></span>



| <span data-ttu-id="34e90-595">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-595">Entry</span></span> | <span data-ttu-id="34e90-596">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-596">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="34e90-597">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-597">Description</span></span>    | <span data-ttu-id="34e90-598">Legt das Kennwort fest, das vom Server Prozess verwendet wird, um sich unter der Identität anzumelden.</span><span class="sxs-lookup"><span data-stu-id="34e90-598">Sets the password used by the server process to log on under the identity.</span></span> |
| <span data-ttu-id="34e90-599">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-599">Access</span></span>         | <span data-ttu-id="34e90-600">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="34e90-600">WriteOnly</span></span>                                                                  |
| <span data-ttu-id="34e90-601">type</span><span class="sxs-lookup"><span data-stu-id="34e90-601">Type</span></span>           | <span data-ttu-id="34e90-602">String</span><span class="sxs-lookup"><span data-stu-id="34e90-602">String</span></span>                                                                     |
| <span data-ttu-id="34e90-603">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-603">Default</span></span>        | <span data-ttu-id="34e90-604">""</span><span class="sxs-lookup"><span data-stu-id="34e90-604">""</span></span>                                                                         |
| <span data-ttu-id="34e90-605">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-605">Minimum system</span></span> | <span data-ttu-id="34e90-606">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-606">Windows 2000</span></span>                                                               |



 

<span data-ttu-id="34e90-607">Das Kennwort sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-607">Password should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="34e90-608">Wenn das Kennwort und die Identität nicht synchron sind, kann die Anwendung erst gestartet werden, wenn Sie von einem Administrator zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-608">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="qcauthenticatemsgs"></a><span data-ttu-id="34e90-609">Qcauthentikatemsgs</span><span class="sxs-lookup"><span data-stu-id="34e90-609">QCAuthenticateMsgs</span></span>



| <span data-ttu-id="34e90-610">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-610">Entry</span></span> | <span data-ttu-id="34e90-611">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-611">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-612">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-612">Description</span></span>    | <span data-ttu-id="34e90-613">Gibt an, unter welchen Umständen Anforderungen in der Warteschlange an eine Anwendung authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-613">Indicates under what circumstances queued requests to an application are authenticated.</span></span>                                                 |
| <span data-ttu-id="34e90-614">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-614">Access</span></span>         | <span data-ttu-id="34e90-615">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-615">ReadWrite</span></span>                                                                                                                               |
| <span data-ttu-id="34e90-616">type</span><span class="sxs-lookup"><span data-stu-id="34e90-616">Type</span></span>           | <span data-ttu-id="34e90-617">Lange mögliche Werte: comadminqcmessageauthenticatesecureapps (0) comadminqcmessageauthenticateoff (1) comadminqcmessageauthenticateon (2)</span><span class="sxs-lookup"><span data-stu-id="34e90-617">Long Possible values:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2)</span></span> |
| <span data-ttu-id="34e90-618">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-618">Default</span></span>        | <span data-ttu-id="34e90-619">Comadminqcmessageauthentipeesecureapps (0)</span><span class="sxs-lookup"><span data-stu-id="34e90-619">COMAdminQCMessageAuthenticateSecureApps (0)</span></span>                                                                                             |
| <span data-ttu-id="34e90-620">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-620">Minimum system</span></span> | <span data-ttu-id="34e90-621">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-621">Windows XP</span></span>                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a><span data-ttu-id="34e90-622">QcListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="34e90-622">QCListenerMaxThreads</span></span>



| <span data-ttu-id="34e90-623">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-623">Entry</span></span> | <span data-ttu-id="34e90-624">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-624">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-625">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-625">Description</span></span>    | <span data-ttu-id="34e90-626">Gibt die maximale Anzahl gleichzeitiger Listenerthreads an.</span><span class="sxs-lookup"><span data-stu-id="34e90-626">Indicates the maximum number of concurrent listener threads.</span></span> <span data-ttu-id="34e90-627">Der gültige Bereich für diese Eigenschaft ist 0 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="34e90-627">The valid range for this property is 0 to 1000.</span></span> <span data-ttu-id="34e90-628">Bei einer neu erstellten Anwendung wird die Einstellung von dem Algorithmus abgeleitet, der derzeit zum Bestimmen der Standard Anzahl von Listenerthreads verwendet wird: das 16-fache der Anzahl der CPUs auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="34e90-628">For a newly created application, the setting is derived from the algorithm currently used for determining the default number of listener threads: 16 times the number of CPUs in the server.</span></span> |
| <span data-ttu-id="34e90-629">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-629">Access</span></span>         | <span data-ttu-id="34e90-630">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-630">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="34e90-631">type</span><span class="sxs-lookup"><span data-stu-id="34e90-631">Type</span></span>           | <span data-ttu-id="34e90-632">Long (0-1000)</span><span class="sxs-lookup"><span data-stu-id="34e90-632">Long (0-1000)</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="34e90-633">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-633">Default</span></span>        | <span data-ttu-id="34e90-634">0</span><span class="sxs-lookup"><span data-stu-id="34e90-634">0</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="34e90-635">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-635">Minimum system</span></span> | <span data-ttu-id="34e90-636">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-636">Windows XP</span></span>                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="34e90-637">Diese Eigenschaft ist auch mit Lese-/Schreibzugriff auf der Registerkarte **Warteschlange** des Verwaltungs Programms Komponenten Dienste verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34e90-637">This property is also available with read/write capability from the **Queuing** tab of the Component Services administrative tool.</span></span>

 

### <a name="queuelistenerenabled"></a><span data-ttu-id="34e90-638">Queuelisteneraktivierte</span><span class="sxs-lookup"><span data-stu-id="34e90-638">QueueListenerEnabled</span></span>



| <span data-ttu-id="34e90-639">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-639">Entry</span></span> | <span data-ttu-id="34e90-640">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-640">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-641">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-641">Description</span></span>    | <span data-ttu-id="34e90-642">Gibt an, ob der in der Warteschlange befindliche Komponenten Listener für die Anwendung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-642">Indicates whether the queued components listener is enabled for the application.</span></span> <span data-ttu-id="34e90-643">Wenn diese Option aktiviert ist, wird der Listener beim Starten der Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="34e90-643">If enabled, the listener is launched when the application starts.</span></span> <span data-ttu-id="34e90-644">Diese Eigenschaft wird nur wirksam, wenn queuingenabled auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-644">This property takes effect only if QueuingEnabled is set to True.</span></span> |
| <span data-ttu-id="34e90-645">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-645">Access</span></span>         | <span data-ttu-id="34e90-646">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-646">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="34e90-647">type</span><span class="sxs-lookup"><span data-stu-id="34e90-647">Type</span></span>           | <span data-ttu-id="34e90-648">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-648">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="34e90-649">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-649">Default</span></span>        | <span data-ttu-id="34e90-650">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-650">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="34e90-651">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-651">Minimum system</span></span> | <span data-ttu-id="34e90-652">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-652">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a><span data-ttu-id="34e90-653">Queuingenabled</span><span class="sxs-lookup"><span data-stu-id="34e90-653">QueuingEnabled</span></span>



| <span data-ttu-id="34e90-654">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-654">Entry</span></span> | <span data-ttu-id="34e90-655">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-655">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-656">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-656">Description</span></span>    | <span data-ttu-id="34e90-657">Gibt an, ob der com+-Dienst in der Warteschlange für die Anwendung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-657">Indicates whether the COM+ Queued Components service is enabled for the application.</span></span> |
| <span data-ttu-id="34e90-658">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-658">Access</span></span>         | <span data-ttu-id="34e90-659">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-659">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="34e90-660">type</span><span class="sxs-lookup"><span data-stu-id="34e90-660">Type</span></span>           | <span data-ttu-id="34e90-661">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-661">Bool</span></span>                                                                                 |
| <span data-ttu-id="34e90-662">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-662">Default</span></span>        | <span data-ttu-id="34e90-663">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-663">False</span></span>                                                                                |
| <span data-ttu-id="34e90-664">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-664">Minimum system</span></span> | <span data-ttu-id="34e90-665">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-665">Windows 2000</span></span>                                                                         |



 

### <a name="recycleactivationlimit"></a><span data-ttu-id="34e90-666">Recycleactivationlimit</span><span class="sxs-lookup"><span data-stu-id="34e90-666">RecycleActivationLimit</span></span>



| <span data-ttu-id="34e90-667">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-667">Entry</span></span> | <span data-ttu-id="34e90-668">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-668">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-669">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-669">Description</span></span>    | <span data-ttu-id="34e90-670">Gibt die maximale Anzahl von Aktivierungen von konfigurierten Objekten in der Anwendung an, die vor der Wiederverwendung des Prozesses akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="34e90-670">Indicates the maximum number of activations of configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="34e90-671">Die Standard Anzahl von Aktivierungen ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="34e90-671">The default number of activations is 0.</span></span> |
| <span data-ttu-id="34e90-672">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-672">Access</span></span>         | <span data-ttu-id="34e90-673">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-673">ReadWrite</span></span>                                                                                                                                                            |
| <span data-ttu-id="34e90-674">type</span><span class="sxs-lookup"><span data-stu-id="34e90-674">Type</span></span>           | <span data-ttu-id="34e90-675">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="34e90-675">Long (0-1048576)</span></span>                                                                                                                                                     |
| <span data-ttu-id="34e90-676">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-676">Default</span></span>        | <span data-ttu-id="34e90-677">0</span><span class="sxs-lookup"><span data-stu-id="34e90-677">0</span></span>                                                                                                                                                                    |
| <span data-ttu-id="34e90-678">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-678">Minimum system</span></span> | <span data-ttu-id="34e90-679">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-679">Windows XP</span></span>                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a><span data-ttu-id="34e90-680">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="34e90-680">RecycleCallLimit</span></span>



| <span data-ttu-id="34e90-681">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-681">Entry</span></span> | <span data-ttu-id="34e90-682">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-682">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-683">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-683">Description</span></span>    | <span data-ttu-id="34e90-684">Gibt die maximale Anzahl von Aufrufen an, mit der konfigurierte Objekte in der Anwendung akzeptiert werden können, bevor der Prozess wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-684">Indicates the maximum number of calls to allow configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="34e90-685">Die Standard Anzahl von Aufrufen ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="34e90-685">The default number of calls is 0.</span></span> |
| <span data-ttu-id="34e90-686">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-686">Access</span></span>         | <span data-ttu-id="34e90-687">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-687">ReadWrite</span></span>                                                                                                                                                      |
| <span data-ttu-id="34e90-688">type</span><span class="sxs-lookup"><span data-stu-id="34e90-688">Type</span></span>           | <span data-ttu-id="34e90-689">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="34e90-689">Long (0-1048576)</span></span>                                                                                                                                               |
| <span data-ttu-id="34e90-690">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-690">Default</span></span>        | <span data-ttu-id="34e90-691">0</span><span class="sxs-lookup"><span data-stu-id="34e90-691">0</span></span>                                                                                                                                                              |
| <span data-ttu-id="34e90-692">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-692">Minimum system</span></span> | <span data-ttu-id="34e90-693">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-693">Windows XP</span></span>                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a><span data-ttu-id="34e90-694">Recycleexpirationtimeout</span><span class="sxs-lookup"><span data-stu-id="34e90-694">RecycleExpirationTimeout</span></span>



| <span data-ttu-id="34e90-695">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-695">Entry</span></span> | <span data-ttu-id="34e90-696">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-696">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-697">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-697">Description</span></span>    | <span data-ttu-id="34e90-698">Gibt die Zeitspanne (in Minuten) an, mit der ein wieder Verwender Prozess vor dem Herunterfahren ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="34e90-698">Indicates the amount of time (in minutes) to allow a recycled process to run before shutting it down.</span></span> <span data-ttu-id="34e90-699">Der Countdown beginnt sofort, nachdem der Prozess wieder verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="34e90-699">The countdown begins immediately after the process is recycled.</span></span> <span data-ttu-id="34e90-700">Der maximale Ablauf Timeout beträgt 1440 Minuten (24 Stunden), und der Standardwert beträgt 15 Minuten.</span><span class="sxs-lookup"><span data-stu-id="34e90-700">The maximum expiration time-out is 1440 minutes (24 hours), and the default is 15 minutes.</span></span> |
| <span data-ttu-id="34e90-701">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-701">Access</span></span>         | <span data-ttu-id="34e90-702">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-702">ReadWrite</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="34e90-703">type</span><span class="sxs-lookup"><span data-stu-id="34e90-703">Type</span></span>           | <span data-ttu-id="34e90-704">Long (1-1440)</span><span class="sxs-lookup"><span data-stu-id="34e90-704">Long (1-1440)</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="34e90-705">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-705">Default</span></span>        | <span data-ttu-id="34e90-706">15</span><span class="sxs-lookup"><span data-stu-id="34e90-706">15</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="34e90-707">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-707">Minimum system</span></span> | <span data-ttu-id="34e90-708">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-708">Windows XP</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a><span data-ttu-id="34e90-709">Recyclelifetimelimit</span><span class="sxs-lookup"><span data-stu-id="34e90-709">RecycleLifetimeLimit</span></span>



| <span data-ttu-id="34e90-710">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-710">Entry</span></span> | <span data-ttu-id="34e90-711">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-711">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-712">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-712">Description</span></span>    | <span data-ttu-id="34e90-713">Gibt die maximale Anzahl von Minuten an, die ein Prozess vor der Wiederverwendung ausgeführt werden darf.</span><span class="sxs-lookup"><span data-stu-id="34e90-713">Indicates the maximum number of minutes to allow a process to run before recycling it.</span></span> <span data-ttu-id="34e90-714">Die maximale Lebensdauer Beschränkung beträgt 30240 Minuten (21 Tage), und der Standardwert beträgt 0 Minuten.</span><span class="sxs-lookup"><span data-stu-id="34e90-714">The maximum lifetime limit is 30240 minutes (21 days), and the default is 0 minutes.</span></span> |
| <span data-ttu-id="34e90-715">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-715">Access</span></span>         | <span data-ttu-id="34e90-716">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-716">ReadWrite</span></span>                                                                                                                                                                   |
| <span data-ttu-id="34e90-717">type</span><span class="sxs-lookup"><span data-stu-id="34e90-717">Type</span></span>           | <span data-ttu-id="34e90-718">Long (0-30240)</span><span class="sxs-lookup"><span data-stu-id="34e90-718">Long (0-30240)</span></span>                                                                                                                                                              |
| <span data-ttu-id="34e90-719">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-719">Default</span></span>        | <span data-ttu-id="34e90-720">0</span><span class="sxs-lookup"><span data-stu-id="34e90-720">0</span></span>                                                                                                                                                                           |
| <span data-ttu-id="34e90-721">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-721">Minimum system</span></span> | <span data-ttu-id="34e90-722">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-722">Windows XP</span></span>                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a><span data-ttu-id="34e90-723">Recyclememorylimit</span><span class="sxs-lookup"><span data-stu-id="34e90-723">RecycleMemoryLimit</span></span>



| <span data-ttu-id="34e90-724">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-724">Entry</span></span> | <span data-ttu-id="34e90-725">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-725">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-726">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-726">Description</span></span>    | <span data-ttu-id="34e90-727">Gibt die maximale Menge an Arbeitsspeicher Auslastung (in Kilobytes) an, die ein Prozess vor der Wiederverwendung zulässt.</span><span class="sxs-lookup"><span data-stu-id="34e90-727">Indicates the maximum amount of memory usage (in kilobytes) allowed a process before it's recycled.</span></span> <span data-ttu-id="34e90-728">Wenn die Prozess Speicherauslastung für einen Zeitraum von mehr als einer Minute die angegebene Anzahl überschreitet, wird der Prozess wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="34e90-728">If the process memory usage exceeds the specified number for a period longer than one minute, the process is recycled.</span></span> <span data-ttu-id="34e90-729">Der Standardwert für die Speicherauslastung beträgt 0 KB.</span><span class="sxs-lookup"><span data-stu-id="34e90-729">The default amount of memory usage is 0 KB.</span></span> |
| <span data-ttu-id="34e90-730">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-730">Access</span></span>         | <span data-ttu-id="34e90-731">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-731">ReadWrite</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="34e90-732">type</span><span class="sxs-lookup"><span data-stu-id="34e90-732">Type</span></span>           | <span data-ttu-id="34e90-733">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="34e90-733">Long (0-1048576)</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="34e90-734">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-734">Default</span></span>        | <span data-ttu-id="34e90-735">0</span><span class="sxs-lookup"><span data-stu-id="34e90-735">0</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="34e90-736">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-736">Minimum system</span></span> | <span data-ttu-id="34e90-737">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-737">Windows XP</span></span>                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a><span data-ttu-id="34e90-738">Replizierbare</span><span class="sxs-lookup"><span data-stu-id="34e90-738">Replicable</span></span>



| <span data-ttu-id="34e90-739">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-739">Entry</span></span> | <span data-ttu-id="34e90-740">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-740">Value</span></span> |
|----------------|------------------------------------------------------|
| <span data-ttu-id="34e90-741">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-741">Description</span></span>    | <span data-ttu-id="34e90-742">Gibt an, ob die Anwendung repliziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="34e90-742">Indicates whether the application can be replicated.</span></span> |
| <span data-ttu-id="34e90-743">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-743">Access</span></span>         | <span data-ttu-id="34e90-744">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-744">ReadWrite</span></span>                                            |
| <span data-ttu-id="34e90-745">type</span><span class="sxs-lookup"><span data-stu-id="34e90-745">Type</span></span>           | <span data-ttu-id="34e90-746">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-746">Bool</span></span>                                                 |
| <span data-ttu-id="34e90-747">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-747">Default</span></span>        | <span data-ttu-id="34e90-748">Richtig</span><span class="sxs-lookup"><span data-stu-id="34e90-748">True</span></span>                                                 |
| <span data-ttu-id="34e90-749">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-749">Minimum system</span></span> | <span data-ttu-id="34e90-750">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-750">Windows XP</span></span>                                           |



 

### <a name="runforever"></a><span data-ttu-id="34e90-751">Runforever</span><span class="sxs-lookup"><span data-stu-id="34e90-751">RunForever</span></span>



| <span data-ttu-id="34e90-752">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-752">Entry</span></span> | <span data-ttu-id="34e90-753">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-753">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-754">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-754">Description</span></span>    | <span data-ttu-id="34e90-755">Ermöglicht, dass ein Server Prozess fortgesetzt wird, wenn sich eine Anwendung im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="34e90-755">Enables a server process to continue if an application is idle.</span></span> <span data-ttu-id="34e90-756">Wenn dieser Wert auf true festgelegt ist, wird der Server Prozess nicht heruntergefahren, wenn er im Leerlauf ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-756">If set to True, the server process does not shut down when left idle.</span></span> <span data-ttu-id="34e90-757">Wenn der Wert auf false festgelegt ist, wird der Prozess gemäß dem Wert heruntergefahren, der von der Eigenschaft shutdownafter festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="34e90-757">If set to False, the process shuts down according to the value set by the ShutdownAfter property.</span></span> <span data-ttu-id="34e90-758">Runforever ist für Anwendungen (in-Process) nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="34e90-758">RunForever is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="34e90-759">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-759">Access</span></span>         | <span data-ttu-id="34e90-760">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-760">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="34e90-761">type</span><span class="sxs-lookup"><span data-stu-id="34e90-761">Type</span></span>           | <span data-ttu-id="34e90-762">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-762">Bool</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="34e90-763">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-763">Default</span></span>        | <span data-ttu-id="34e90-764">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-764">False</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="34e90-765">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-765">Minimum system</span></span> | <span data-ttu-id="34e90-766">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-766">Windows 2000</span></span>                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a><span data-ttu-id="34e90-767">Dienstname</span><span class="sxs-lookup"><span data-stu-id="34e90-767">ServiceName</span></span>



| <span data-ttu-id="34e90-768">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-768">Entry</span></span> | <span data-ttu-id="34e90-769">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-769">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-770">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-770">Description</span></span>    | <span data-ttu-id="34e90-771">Der Dienst Name, der der Anwendung entspricht, die zum Ausführen als Dienst Anwendung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-771">The service name corresponding to the application configured to run as a service application.</span></span> <span data-ttu-id="34e90-772">Wenn dieser Wert **null** ist, ist die Anwendung nicht für die Verwendung als Dienst konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="34e90-772">If this value is **NULL**, the application is not configured to run as a service.</span></span> <span data-ttu-id="34e90-773">Andernfalls können die Konfigurationsinformationen für den Dienst mithilfe des Dienst namens gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-773">Otherwise, the configuration information for the service can be found by using the service name.</span></span> |
| <span data-ttu-id="34e90-774">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-774">Access</span></span>         | <span data-ttu-id="34e90-775">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="34e90-775">ReadOnly</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="34e90-776">type</span><span class="sxs-lookup"><span data-stu-id="34e90-776">Type</span></span>           | <span data-ttu-id="34e90-777">String</span><span class="sxs-lookup"><span data-stu-id="34e90-777">String</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="34e90-778">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-778">Default</span></span>        | <span data-ttu-id="34e90-779">""</span><span class="sxs-lookup"><span data-stu-id="34e90-779">""</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="34e90-780">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-780">Minimum system</span></span> | <span data-ttu-id="34e90-781">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-781">Windows XP</span></span>                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a><span data-ttu-id="34e90-782">Shutdownafter</span><span class="sxs-lookup"><span data-stu-id="34e90-782">ShutdownAfter</span></span>



| <span data-ttu-id="34e90-783">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-783">Entry</span></span> | <span data-ttu-id="34e90-784">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-784">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-785">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-785">Description</span></span>    | <span data-ttu-id="34e90-786">Legt die Verzögerung fest, bevor ein Server Prozess heruntergefahren wird, nachdem er in den Leerlauf wechselt.</span><span class="sxs-lookup"><span data-stu-id="34e90-786">Sets the delay before shutting down a server process after it becomes idle.</span></span> <span data-ttu-id="34e90-787">Die Wartezeit für das Herunterfahren liegt zwischen 0 und 1440 Minuten (24 Stunden).</span><span class="sxs-lookup"><span data-stu-id="34e90-787">Shutdown latency ranges from 0 to 1440 minutes (24 hours).</span></span> <span data-ttu-id="34e90-788">Wenn runforever auf true festgelegt ist, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="34e90-788">If RunForever is set to True, this property is ignored.</span></span> <span data-ttu-id="34e90-789">Shutdownafter ist nicht für die Bibliothek (in-Process)-Anwendungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="34e90-789">ShutdownAfter is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="34e90-790">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-790">Access</span></span>         | <span data-ttu-id="34e90-791">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-791">ReadWrite</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="34e90-792">type</span><span class="sxs-lookup"><span data-stu-id="34e90-792">Type</span></span>           | <span data-ttu-id="34e90-793">Long (0-1440)</span><span class="sxs-lookup"><span data-stu-id="34e90-793">Long (0-1440)</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="34e90-794">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-794">Default</span></span>        | <span data-ttu-id="34e90-795">3</span><span class="sxs-lookup"><span data-stu-id="34e90-795">3</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="34e90-796">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-796">Minimum system</span></span> | <span data-ttu-id="34e90-797">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34e90-797">Windows 2000</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a><span data-ttu-id="34e90-798">Soapaktivierte</span><span class="sxs-lookup"><span data-stu-id="34e90-798">SoapActivated</span></span>



| <span data-ttu-id="34e90-799">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-799">Entry</span></span> | <span data-ttu-id="34e90-800">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-800">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-801">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-801">Description</span></span>    | <span data-ttu-id="34e90-802">Gibt an, ob diese Anwendung für die Nutzung über das SOAP-Protokoll verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-802">Indicates whether this application is exposed for consumption via the SOAP protocol.</span></span> |
| <span data-ttu-id="34e90-803">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-803">Access</span></span>         | <span data-ttu-id="34e90-804">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-804">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="34e90-805">type</span><span class="sxs-lookup"><span data-stu-id="34e90-805">Type</span></span>           | <span data-ttu-id="34e90-806">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-806">Bool</span></span>                                                                                 |
| <span data-ttu-id="34e90-807">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-807">Default</span></span>        | <span data-ttu-id="34e90-808">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-808">False</span></span>                                                                                |
| <span data-ttu-id="34e90-809">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-809">Minimum system</span></span> | <span data-ttu-id="34e90-810">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34e90-810">Windows Server 2003</span></span>                                                                  |



 

### <a name="soapbaseurl"></a><span data-ttu-id="34e90-811">Soapbaseurl</span><span class="sxs-lookup"><span data-stu-id="34e90-811">SoapBaseUrl</span></span>



| <span data-ttu-id="34e90-812">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-812">Entry</span></span> | <span data-ttu-id="34e90-813">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-813">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-814">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-814">Description</span></span>    | <span data-ttu-id="34e90-815">Der URL-Endpunkt, an dem diese Anwendung über das SOAP-Protokoll verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-815">The URL endpoint at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="34e90-816">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-816">Access</span></span>         | <span data-ttu-id="34e90-817">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-817">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="34e90-818">type</span><span class="sxs-lookup"><span data-stu-id="34e90-818">Type</span></span>           | <span data-ttu-id="34e90-819">String</span><span class="sxs-lookup"><span data-stu-id="34e90-819">String</span></span>                                                                       |
| <span data-ttu-id="34e90-820">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-820">Default</span></span>        | <span data-ttu-id="34e90-821">""</span><span class="sxs-lookup"><span data-stu-id="34e90-821">""</span></span>                                                                           |
| <span data-ttu-id="34e90-822">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-822">Minimum system</span></span> | <span data-ttu-id="34e90-823">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34e90-823">Windows Server 2003</span></span>                                                          |



 

### <a name="soapmailto"></a><span data-ttu-id="34e90-824">Soapmailto</span><span class="sxs-lookup"><span data-stu-id="34e90-824">SoapMailTo</span></span>



| <span data-ttu-id="34e90-825">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-825">Entry</span></span> | <span data-ttu-id="34e90-826">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-826">Value</span></span> |
|----------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-827">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-827">Description</span></span>    | <span data-ttu-id="34e90-828">Die e-Mail-Adresse, an der diese Anwendung über das SOAP-Protokoll verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="34e90-828">The email address at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="34e90-829">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-829">Access</span></span>         | <span data-ttu-id="34e90-830">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-830">ReadWrite</span></span>                                                                     |
| <span data-ttu-id="34e90-831">type</span><span class="sxs-lookup"><span data-stu-id="34e90-831">Type</span></span>           | <span data-ttu-id="34e90-832">String</span><span class="sxs-lookup"><span data-stu-id="34e90-832">String</span></span>                                                                        |
| <span data-ttu-id="34e90-833">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-833">Default</span></span>        | <span data-ttu-id="34e90-834">""</span><span class="sxs-lookup"><span data-stu-id="34e90-834">""</span></span>                                                                            |
| <span data-ttu-id="34e90-835">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-835">Minimum system</span></span> | <span data-ttu-id="34e90-836">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34e90-836">Windows Server 2003</span></span>                                                           |



 

### <a name="soapvroot"></a><span data-ttu-id="34e90-837">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="34e90-837">SoapVRoot</span></span>



| <span data-ttu-id="34e90-838">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-838">Entry</span></span> | <span data-ttu-id="34e90-839">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-839">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-840">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-840">Description</span></span>    | <span data-ttu-id="34e90-841">Das virtuelle IIS-Stammverzeichnis, in dem sich die Zugriffs Skripts befinden, die die Anwendung über das SOAP-Protokoll verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="34e90-841">The IIS virtual root directory in which the access scripts that expose the application via the SOAP protocol reside.</span></span> |
| <span data-ttu-id="34e90-842">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-842">Access</span></span>         | <span data-ttu-id="34e90-843">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-843">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="34e90-844">type</span><span class="sxs-lookup"><span data-stu-id="34e90-844">Type</span></span>           | <span data-ttu-id="34e90-845">String</span><span class="sxs-lookup"><span data-stu-id="34e90-845">String</span></span>                                                                                                               |
| <span data-ttu-id="34e90-846">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-846">Default</span></span>        | <span data-ttu-id="34e90-847">""</span><span class="sxs-lookup"><span data-stu-id="34e90-847">""</span></span>                                                                                                                   |
| <span data-ttu-id="34e90-848">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-848">Minimum system</span></span> | <span data-ttu-id="34e90-849">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34e90-849">Windows Server 2003</span></span>                                                                                                  |



 

### <a name="srpenabled"></a><span data-ttu-id="34e90-850">Srpabled</span><span class="sxs-lookup"><span data-stu-id="34e90-850">SRPEnabled</span></span>



| <span data-ttu-id="34e90-851">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-851">Entry</span></span> | <span data-ttu-id="34e90-852">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-852">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-853">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-853">Description</span></span>    | <span data-ttu-id="34e90-854">Bestimmt die Software Einschränkungs Richtlinie (Software Einschränkungs Richtlinie, SRP) für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="34e90-854">Determines the software restriction policy (SRP) for the application.</span></span> <span data-ttu-id="34e90-855">Wenn diese Eigenschaft auf true festgelegt ist, wird die SRPTrustLevel-Eigenschaft für die Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="34e90-855">If set to True, the SRPTrustLevel property for the application is used.</span></span> <span data-ttu-id="34e90-856">Wenn false festgelegt ist, werden die Richtlinien für Software Einschränkung aus den lokalen Sicherheitseinstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="34e90-856">If set to False, the software restriction policies from the local security settings are used.</span></span> <span data-ttu-id="34e90-857">Die lokalen Sicherheitseinstellungen werden über das Snap-in "lokale Sicherheitsrichtlinie" der Microsoft Management Console gesteuert.</span><span class="sxs-lookup"><span data-stu-id="34e90-857">The local security settings are controlled through the Local Security Policy snap-in of the Microsoft Management Console.</span></span> |
| <span data-ttu-id="34e90-858">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-858">Access</span></span>         | <span data-ttu-id="34e90-859">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-859">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="34e90-860">type</span><span class="sxs-lookup"><span data-stu-id="34e90-860">Type</span></span>           | <span data-ttu-id="34e90-861">Bool</span><span class="sxs-lookup"><span data-stu-id="34e90-861">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="34e90-862">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-862">Default</span></span>        | <span data-ttu-id="34e90-863">Falsch</span><span class="sxs-lookup"><span data-stu-id="34e90-863">False</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="34e90-864">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-864">Minimum system</span></span> | <span data-ttu-id="34e90-865">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-865">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a><span data-ttu-id="34e90-866">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="34e90-866">SRPTrustLevel</span></span>



| <span data-ttu-id="34e90-867">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34e90-867">Entry</span></span> | <span data-ttu-id="34e90-868">Wert</span><span class="sxs-lookup"><span data-stu-id="34e90-868">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e90-869">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34e90-869">Description</span></span>    | <span data-ttu-id="34e90-870">Gibt die Richtlinie für die Software Einschränkungs Richtlinie (SRP) der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="34e90-870">Indicates the software restriction policy (SRP) trust level of the application.</span></span> <span data-ttu-id="34e90-871">Diese Eigenschaft wird nur verwendet, wenn die srpabled-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="34e90-871">This property is used only if the SRPEnabled property is set to True.</span></span> <span data-ttu-id="34e90-872">Die SRP-Vertrauens Ebene bezieht sich auf die Vertrauens Ebene, die Sie einer Anwendung bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="34e90-872">The SRP trust level refers to the level of trust that you are willing to give to an application.</span></span> <span data-ttu-id="34e90-873">Eine uneingeschränkte SRP-Vertrauens Ebene entspricht dem \_ fulllytrusted-Enumerationswert der sichereren levelid \_ , während eine unzulässige SRP-Vertrauens Ebene dem sichereren \_ levelid-Enumerationswert entspricht \_ .</span><span class="sxs-lookup"><span data-stu-id="34e90-873">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="34e90-874">Die Enumeration für die Vertrauens Ebenen ist in winsafer. h definiert.</span><span class="sxs-lookup"><span data-stu-id="34e90-874">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="34e90-875">Access</span><span class="sxs-lookup"><span data-stu-id="34e90-875">Access</span></span>         | <span data-ttu-id="34e90-876">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34e90-876">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="34e90-877">type</span><span class="sxs-lookup"><span data-stu-id="34e90-877">Type</span></span>           | <span data-ttu-id="34e90-878">Lange mögliche Werte: sicherere \_ levelid nicht \_ zulässig (0x0) sicherere \_ levelid \_ fullytrusted (0x40000)</span><span class="sxs-lookup"><span data-stu-id="34e90-878">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="34e90-879">Standard</span><span class="sxs-lookup"><span data-stu-id="34e90-879">Default</span></span>        | <span data-ttu-id="34e90-880">Sicherere \_ levelid \_ fullytrusted (0x40000)</span><span class="sxs-lookup"><span data-stu-id="34e90-880">SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="34e90-881">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="34e90-881">Minimum system</span></span> | <span data-ttu-id="34e90-882">Windows XP</span><span class="sxs-lookup"><span data-stu-id="34e90-882">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

<span data-ttu-id="34e90-883">Einer Anwendung, die Sie mit uneingeschränktem Zugriff als vertrauenswürdig einstufen möchten, sollte die strengste Sicherheit angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="34e90-883">An application that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="34e90-884">Anwendungen, die uneingeschränkt sind, können nur unbeschränkte Komponenten laden, während unzulässige Anwendungen nicht ausgeführt werden dürfen und somit keine Komponenten laden können.</span><span class="sxs-lookup"><span data-stu-id="34e90-884">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

## <a name="see-also"></a><span data-ttu-id="34e90-885">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34e90-885">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e90-886">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="34e90-886">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
