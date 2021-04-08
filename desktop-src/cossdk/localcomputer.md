---
description: Enthält ein einzelnes-Objekt, das dem Computer entspricht, auf den Sie zugreifen. Dieses Objekt enthält Einstellungs Informationen auf Computer Ebene.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: LocalComputer-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749000"
---
# <a name="localcomputer-collection"></a><span data-ttu-id="f2c00-104">LocalComputer-Sammlung</span><span class="sxs-lookup"><span data-stu-id="f2c00-104">LocalComputer collection</span></span>

<span data-ttu-id="f2c00-105">Enthält ein einzelnes-Objekt, das dem Computer entspricht, auf den Sie zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f2c00-105">Contains a single object that corresponds to the computer whose catalog you are accessing.</span></span> <span data-ttu-id="f2c00-106">Dieses Objekt enthält Einstellungs Informationen auf Computer Ebene.</span><span class="sxs-lookup"><span data-stu-id="f2c00-106">This object holds computer level settings information.</span></span> <span data-ttu-id="f2c00-107">Wenn Sie die [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) -Methode für ein Objekt aufrufen, das aus der [**comadmincatalog**](comadmincatalog.md) -Klasse erstellt wurde, enthält das-Objekt in der **LocalComputer** -Auflistung Informationen über den Remote Computer, auf den Sie zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f2c00-107">If you call the [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) method on an object created from the [**COMAdminCatalog**](comadmincatalog.md) class, the object in the **LocalComputer** collection contains information about the remote computer whose catalog you are accessing.</span></span>

<span data-ttu-id="f2c00-108">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.</span><span class="sxs-lookup"><span data-stu-id="f2c00-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="f2c00-109">Member</span><span class="sxs-lookup"><span data-stu-id="f2c00-109">Members</span></span>

<span data-ttu-id="f2c00-110">Die **LocalComputer** -Sammlung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="f2c00-110">The **LocalComputer** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="f2c00-111">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="f2c00-111">Related Collections</span></span>

<span data-ttu-id="f2c00-112">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="f2c00-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="f2c00-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f2c00-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="f2c00-114">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="f2c00-114">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="f2c00-115">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="f2c00-115">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="f2c00-116">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="f2c00-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="f2c00-117">**Fasst**</span><span class="sxs-lookup"><span data-stu-id="f2c00-117">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="f2c00-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2c00-118">Properties</span></span>

<span data-ttu-id="f2c00-119">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f2c00-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="f2c00-120">Applicationproxyrsn</span><span class="sxs-lookup"><span data-stu-id="f2c00-120">ApplicationProxyRSN</span></span>](#applicationproxyrsn)
-   [<span data-ttu-id="f2c00-121">Cisenabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-121">CISEnabled</span></span>](#cisenabled)
-   [<span data-ttu-id="f2c00-122">Dcomaktiviert</span><span class="sxs-lookup"><span data-stu-id="f2c00-122">DCOMEnabled</span></span>](#dcomenabled)
-   [<span data-ttu-id="f2c00-123">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="f2c00-123">DefaultAuthenticationLevel</span></span>](#defaultauthenticationlevel)
-   [<span data-ttu-id="f2c00-124">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="f2c00-124">DefaultImpersonationLevel</span></span>](#defaultimpersonationlevel)
-   [<span data-ttu-id="f2c00-125">Defaultdeinternetports</span><span class="sxs-lookup"><span data-stu-id="f2c00-125">DefaultToInternetPorts</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="f2c00-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2c00-126">Description</span></span>](#description)
-   [<span data-ttu-id="f2c00-127">Dspartitionlookupabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-127">DSPartitionLookupEnabled</span></span>](#dspartitionlookupenabled)
-   [<span data-ttu-id="f2c00-128">Internetportslisted</span><span class="sxs-lookup"><span data-stu-id="f2c00-128">InternetPortsListed</span></span>](#internetportslisted)
-   [<span data-ttu-id="f2c00-129">Isrouter</span><span class="sxs-lookup"><span data-stu-id="f2c00-129">IsRouter</span></span>](#isrouter)
-   [<span data-ttu-id="f2c00-130">Loadbalancingclsid</span><span class="sxs-lookup"><span data-stu-id="f2c00-130">LoadBalancingCLSID</span></span>](#loadbalancingclsid)
-   [<span data-ttu-id="f2c00-131">Localpartitionlookupabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-131">LocalPartitionLookupEnabled</span></span>](#localpartitionlookupenabled)
-   [<span data-ttu-id="f2c00-132">Name</span><span class="sxs-lookup"><span data-stu-id="f2c00-132">Name</span></span>](#name)
-   [<span data-ttu-id="f2c00-133">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-133">OperatingSystem</span></span>](#operatingsystem)
-   [<span data-ttu-id="f2c00-134">Partitionsenabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-134">PartitionsEnabled</span></span>](#partitionsenabled)
-   [<span data-ttu-id="f2c00-135">Ports</span><span class="sxs-lookup"><span data-stu-id="f2c00-135">Ports</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="f2c00-136">Resourcepoolingenabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-136">ResourcePoolingEnabled</span></span>](#resourcepoolingenabled)
-   [<span data-ttu-id="f2c00-137">Rpcproxyaktivierte</span><span class="sxs-lookup"><span data-stu-id="f2c00-137">RPCProxyEnabled</span></span>](#rpcproxyenabled)
-   [<span data-ttu-id="f2c00-138">Securereferencesaktiviert</span><span class="sxs-lookup"><span data-stu-id="f2c00-138">SecureReferencesEnabled</span></span>](#securereferencesenabled)
-   [<span data-ttu-id="f2c00-139">Securitytrackingenabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-139">SecurityTrackingEnabled</span></span>](#securitytrackingenabled)
-   [<span data-ttu-id="f2c00-140">Srpactivateasactivatorchecks</span><span class="sxs-lookup"><span data-stu-id="f2c00-140">SRPActivateAsActivatorChecks</span></span>](#srpactivateasactivatorchecks)
-   [<span data-ttu-id="f2c00-141">Srprunningobjectchecks</span><span class="sxs-lookup"><span data-stu-id="f2c00-141">SRPRunningObjectChecks</span></span>](#srprunningobjectchecks)
-   [<span data-ttu-id="f2c00-142">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="f2c00-142">TransactionTimeout</span></span>](#transactiontimeout)

### <a name="applicationproxyrsn"></a><span data-ttu-id="f2c00-143">Applicationproxyrsn</span><span class="sxs-lookup"><span data-stu-id="f2c00-143">ApplicationProxyRSN</span></span>



| <span data-ttu-id="f2c00-144">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-144">Entry</span></span> | <span data-ttu-id="f2c00-145">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-145">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="f2c00-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-146">Description</span></span>    | <span data-ttu-id="f2c00-147">Standardmäßig von Anwendungs Proxys verwendeter Remote Servername.</span><span class="sxs-lookup"><span data-stu-id="f2c00-147">Remote server name used by application proxies by default.</span></span> |
| <span data-ttu-id="f2c00-148">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-148">Access</span></span>         | <span data-ttu-id="f2c00-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-149">ReadWrite</span></span>                                                  |
| <span data-ttu-id="f2c00-150">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-150">Type</span></span>           | <span data-ttu-id="f2c00-151">String</span><span class="sxs-lookup"><span data-stu-id="f2c00-151">String</span></span>                                                     |
| <span data-ttu-id="f2c00-152">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-152">Default</span></span>        | <span data-ttu-id="f2c00-153">""</span><span class="sxs-lookup"><span data-stu-id="f2c00-153">""</span></span>                                                         |
| <span data-ttu-id="f2c00-154">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-154">Minimum system</span></span> | <span data-ttu-id="f2c00-155">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-155">Windows 2000</span></span>                                               |



 

### <a name="cisenabled"></a><span data-ttu-id="f2c00-156">Cisenabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-156">CISEnabled</span></span>



| <span data-ttu-id="f2c00-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-157">Entry</span></span> | <span data-ttu-id="f2c00-158">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-158">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="f2c00-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-159">Description</span></span>    | <span data-ttu-id="f2c00-160">Gibt an, ob com-Internet Dienste aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="f2c00-160">Indicates whether COM Internet Services is enabled.</span></span> |
| <span data-ttu-id="f2c00-161">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-161">Access</span></span>         | <span data-ttu-id="f2c00-162">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-162">ReadWrite</span></span>                                           |
| <span data-ttu-id="f2c00-163">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-163">Type</span></span>           | <span data-ttu-id="f2c00-164">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-164">Bool</span></span>                                                |
| <span data-ttu-id="f2c00-165">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-165">Default</span></span>        | <span data-ttu-id="f2c00-166">Falsch</span><span class="sxs-lookup"><span data-stu-id="f2c00-166">False</span></span>                                               |
| <span data-ttu-id="f2c00-167">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-167">Minimum system</span></span> | <span data-ttu-id="f2c00-168">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-168">Windows 2000</span></span>                                        |



 

### <a name="dcomenabled"></a><span data-ttu-id="f2c00-169">Dcomaktiviert</span><span class="sxs-lookup"><span data-stu-id="f2c00-169">DCOMEnabled</span></span>



| <span data-ttu-id="f2c00-170">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-170">Entry</span></span> | <span data-ttu-id="f2c00-171">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-171">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="f2c00-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-172">Description</span></span>    | <span data-ttu-id="f2c00-173">Legen Sie diese Option auf true fest, um DCOM auf dem Computer zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="f2c00-173">Set to True to enable DCOM on the computer.</span></span> |
| <span data-ttu-id="f2c00-174">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-174">Access</span></span>         | <span data-ttu-id="f2c00-175">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-175">ReadWrite</span></span>                                   |
| <span data-ttu-id="f2c00-176">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-176">Type</span></span>           | <span data-ttu-id="f2c00-177">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-177">Bool</span></span>                                        |
| <span data-ttu-id="f2c00-178">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-178">Default</span></span>        | <span data-ttu-id="f2c00-179">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2c00-179">True</span></span>                                        |
| <span data-ttu-id="f2c00-180">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-180">Minimum system</span></span> | <span data-ttu-id="f2c00-181">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-181">Windows 2000</span></span>                                |



 

### <a name="defaultauthenticationlevel"></a><span data-ttu-id="f2c00-182">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="f2c00-182">DefaultAuthenticationLevel</span></span>



| <span data-ttu-id="f2c00-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-183">Entry</span></span> | <span data-ttu-id="f2c00-184">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-184">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-185">Description</span></span>    | <span data-ttu-id="f2c00-186">Authentifizierungs Ebene, die von Anwendungen verwendet wird, deren Authentifizierung auf Standard festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2c00-186">Authentication level used by applications that have Authentication set to Default.</span></span> <span data-ttu-id="f2c00-187">Die Werte entsprechen den Authentifizierungs Einstellungen für Remote Prozedur Aufrufe (RPC).</span><span class="sxs-lookup"><span data-stu-id="f2c00-187">Values correspond to the Remote Procedure Call (RPC) authentication settings.</span></span>                                                                                         |
| <span data-ttu-id="f2c00-188">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-188">Access</span></span>         | <span data-ttu-id="f2c00-189">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-189">ReadWrite</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="f2c00-190">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-190">Type</span></span>           | <span data-ttu-id="f2c00-191">Lange mögliche Werte: comadminauthenticationdefault (0) comadminauthenticationnone (1) comadminauthenticationconnect (2) comadminauthentication-Aufruf (3) comadminauthenticationpacket (4) comadminauthenticationintegrity (5) comadminauthenticationprivacy (6)</span><span class="sxs-lookup"><span data-stu-id="f2c00-191">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span> |
| <span data-ttu-id="f2c00-192">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-192">Default</span></span>        | <span data-ttu-id="f2c00-193">Comadminauthenticationconnect (2)</span><span class="sxs-lookup"><span data-stu-id="f2c00-193">COMAdminAuthenticationConnect (2)</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="f2c00-194">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-194">Minimum system</span></span> | <span data-ttu-id="f2c00-195">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-195">Windows 2000</span></span>                                                                                                                                                                                                                                             |



 

> [!Note]  
> <span data-ttu-id="f2c00-196">Comadminauthenticationdefault wird comadminauthenticationconnect zugeordnet, wenn com [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufruft.</span><span class="sxs-lookup"><span data-stu-id="f2c00-196">COMAdminAuthenticationDefault is mapped to COMAdminAuthenticationConnect when COM calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="f2c00-197">Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2c00-197">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="defaultimpersonationlevel"></a><span data-ttu-id="f2c00-198">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="f2c00-198">DefaultImpersonationLevel</span></span>



| <span data-ttu-id="f2c00-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-199">Entry</span></span> | <span data-ttu-id="f2c00-200">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-200">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-201">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-201">Description</span></span>    | <span data-ttu-id="f2c00-202">Die Identitätswechsel Ebene, um zuzulassen, wenn eine nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f2c00-202">Impersonation level to allow if one is not set.</span></span>                                                                                                               |
| <span data-ttu-id="f2c00-203">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-203">Access</span></span>         | <span data-ttu-id="f2c00-204">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-204">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="f2c00-205">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-205">Type</span></span>           | <span data-ttu-id="f2c00-206">Lange mögliche Werte: comadminimpersonationanonymous (1) comadminimpersonationidentifiout (2) comadminimpersonationidentität (3) comadminimpersonationdelegat (4)</span><span class="sxs-lookup"><span data-stu-id="f2c00-206">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="f2c00-207">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-207">Default</span></span>        | <span data-ttu-id="f2c00-208">Comadminimpersonationidentifi(2)</span><span class="sxs-lookup"><span data-stu-id="f2c00-208">COMAdminImpersonationIdentify (2)</span></span>                                                                                                                             |
| <span data-ttu-id="f2c00-209">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-209">Minimum system</span></span> | <span data-ttu-id="f2c00-210">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-210">Windows 2000</span></span>                                                                                                                                                  |



 

> [!Note]  
> <span data-ttu-id="f2c00-211">Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2c00-211">It is recommended that you use the constants in the enumeration, and not the numeric values.</span></span>

 

### <a name="defaulttointernetports"></a><span data-ttu-id="f2c00-212">Defaultdeinternetports</span><span class="sxs-lookup"><span data-stu-id="f2c00-212">DefaultToInternetPorts</span></span>



| <span data-ttu-id="f2c00-213">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-213">Entry</span></span> | <span data-ttu-id="f2c00-214">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-214">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-215">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-215">Description</span></span>    | <span data-ttu-id="f2c00-216">Bestimmt, ob der Standardtyp des angegebenen Ports Internet (true) oder Intranet (false) sein soll.</span><span class="sxs-lookup"><span data-stu-id="f2c00-216">Determines whether the default type of port provided should be Internet (True) or intranet (False).</span></span> |
| <span data-ttu-id="f2c00-217">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-217">Access</span></span>         | <span data-ttu-id="f2c00-218">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-218">ReadWrite</span></span>                                                                                           |
| <span data-ttu-id="f2c00-219">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-219">Type</span></span>           | <span data-ttu-id="f2c00-220">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-220">Bool</span></span>                                                                                                |
| <span data-ttu-id="f2c00-221">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-221">Default</span></span>        | <span data-ttu-id="f2c00-222">Falsch</span><span class="sxs-lookup"><span data-stu-id="f2c00-222">False</span></span>                                                                                               |
| <span data-ttu-id="f2c00-223">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-223">Minimum system</span></span> | <span data-ttu-id="f2c00-224">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-224">Windows 2000</span></span>                                                                                        |



 

### <a name="description"></a><span data-ttu-id="f2c00-225">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-225">Description</span></span>



| <span data-ttu-id="f2c00-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-226">Entry</span></span> | <span data-ttu-id="f2c00-227">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-227">Value</span></span> |
|----------------|--------------------------------|
| <span data-ttu-id="f2c00-228">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-228">Description</span></span>    | <span data-ttu-id="f2c00-229">Eine Beschreibung des Computers.</span><span class="sxs-lookup"><span data-stu-id="f2c00-229">A description of the computer.</span></span> |
| <span data-ttu-id="f2c00-230">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-230">Access</span></span>         | <span data-ttu-id="f2c00-231">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-231">ReadWrite</span></span>                      |
| <span data-ttu-id="f2c00-232">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-232">Type</span></span>           | <span data-ttu-id="f2c00-233">String</span><span class="sxs-lookup"><span data-stu-id="f2c00-233">String</span></span>                         |
| <span data-ttu-id="f2c00-234">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-234">Default</span></span>        | <span data-ttu-id="f2c00-235">""</span><span class="sxs-lookup"><span data-stu-id="f2c00-235">""</span></span>                             |
| <span data-ttu-id="f2c00-236">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-236">Minimum system</span></span> | <span data-ttu-id="f2c00-237">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-237">Windows 2000</span></span>                   |



 

### <a name="dspartitionlookupenabled"></a><span data-ttu-id="f2c00-238">Dspartitionlookupabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-238">DSPartitionLookupEnabled</span></span>



| <span data-ttu-id="f2c00-239">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-239">Entry</span></span> | <span data-ttu-id="f2c00-240">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-240">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-241">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-241">Description</span></span>    | <span data-ttu-id="f2c00-242">Gibt an, ob der Benutzer der Partitions Zuordnungen in den Domänen Speicher eingecheckt wird.</span><span class="sxs-lookup"><span data-stu-id="f2c00-242">Indicates whether the user of the partition mappings is checked into the domain store.</span></span> |
| <span data-ttu-id="f2c00-243">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-243">Access</span></span>         | <span data-ttu-id="f2c00-244">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-244">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="f2c00-245">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-245">Type</span></span>           | <span data-ttu-id="f2c00-246">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-246">Bool</span></span>                                                                                   |
| <span data-ttu-id="f2c00-247">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-247">Default</span></span>        | <span data-ttu-id="f2c00-248">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2c00-248">True</span></span>                                                                                   |
| <span data-ttu-id="f2c00-249">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-249">Minimum system</span></span> | <span data-ttu-id="f2c00-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2c00-250">Windows Server 2003</span></span>                                                                    |



 

### <a name="internetportslisted"></a><span data-ttu-id="f2c00-251">Internetportslisted</span><span class="sxs-lookup"><span data-stu-id="f2c00-251">InternetPortsListed</span></span>



| <span data-ttu-id="f2c00-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-252">Entry</span></span> | <span data-ttu-id="f2c00-253">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-253">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-254">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-254">Description</span></span>    | <span data-ttu-id="f2c00-255">Bestimmt, ob die in der Eigenschaft Ports aufgelisteten Ports für das Internet (true) oder für das Intranet (false) verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2c00-255">Determines whether the ports listed in the Ports property are to be used for Internet (True) or for intranet (False).</span></span> |
| <span data-ttu-id="f2c00-256">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-256">Access</span></span>         | <span data-ttu-id="f2c00-257">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-257">ReadWrite</span></span>                                                                                                             |
| <span data-ttu-id="f2c00-258">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-258">Type</span></span>           | <span data-ttu-id="f2c00-259">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-259">Bool</span></span>                                                                                                                  |
| <span data-ttu-id="f2c00-260">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-260">Default</span></span>        | <span data-ttu-id="f2c00-261">Falsch</span><span class="sxs-lookup"><span data-stu-id="f2c00-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="f2c00-262">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-262">Minimum system</span></span> | <span data-ttu-id="f2c00-263">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-263">Windows 2000</span></span>                                                                                                          |



 

### <a name="isrouter"></a><span data-ttu-id="f2c00-264">Isrouter</span><span class="sxs-lookup"><span data-stu-id="f2c00-264">IsRouter</span></span>



| <span data-ttu-id="f2c00-265">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-265">Entry</span></span> | <span data-ttu-id="f2c00-266">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-266">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-267">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-267">Description</span></span>    | <span data-ttu-id="f2c00-268">Legen Sie diese Einstellung auf true fest, wenn der Computer ein Router für den CLB-Dienst (Component Load Balancing) ist.</span><span class="sxs-lookup"><span data-stu-id="f2c00-268">Set to True if the computer is a router for the component load balancing (CLB) service.</span></span> <span data-ttu-id="f2c00-269">Diese Eigenschaft kann nur auf "true" festgelegt werden, wenn der Komponenten Lastenausgleich-Dienst derzeit auf dem Computer installiert ist. Andernfalls erfordert IT-Fehler mit COMAdmin \_ E eine \_ \_ andere \_ Plattform.</span><span class="sxs-lookup"><span data-stu-id="f2c00-269">This property can be set to True only if the component load balancing service is currently installed on the computer; otherwise, it errors with COMADMIN\_E\_REQUIRES\_DIFFERENT\_PLATFORM.</span></span> |
| <span data-ttu-id="f2c00-270">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-270">Access</span></span>         | <span data-ttu-id="f2c00-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-271">ReadWrite</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f2c00-272">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-272">Type</span></span>           | <span data-ttu-id="f2c00-273">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-273">Bool</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f2c00-274">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-274">Default</span></span>        | <span data-ttu-id="f2c00-275">Falsch</span><span class="sxs-lookup"><span data-stu-id="f2c00-275">False</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f2c00-276">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-276">Minimum system</span></span> | <span data-ttu-id="f2c00-277">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-277">Windows 2000</span></span>                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="f2c00-278">Wenn diese Eigenschaft auf true festgelegt ist, wird der CLB-Server konfiguriert und beim Start gestartet.</span><span class="sxs-lookup"><span data-stu-id="f2c00-278">If this property is set to True, the CLB server is configured and starts at startup.</span></span> <span data-ttu-id="f2c00-279">Der Server wird der ApplicationCluster-Sammlung hinzugefügt, wenn er nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f2c00-279">The server is added to the ApplicationCluster collection if it is not already present.</span></span>

### <a name="loadbalancingclsid"></a><span data-ttu-id="f2c00-280">Loadbalancingclsid</span><span class="sxs-lookup"><span data-stu-id="f2c00-280">LoadBalancingCLSID</span></span>



| <span data-ttu-id="f2c00-281">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-281">Entry</span></span> | <span data-ttu-id="f2c00-282">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-282">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="f2c00-283">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-283">Description</span></span>    | <span data-ttu-id="f2c00-284">Die CLSID des-Objekts, das ausgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2c00-284">The CLSID of the object to balance.</span></span> |
| <span data-ttu-id="f2c00-285">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-285">Access</span></span>         | <span data-ttu-id="f2c00-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-286">ReadWrite</span></span>                           |
| <span data-ttu-id="f2c00-287">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-287">Type</span></span>           | <span data-ttu-id="f2c00-288">String</span><span class="sxs-lookup"><span data-stu-id="f2c00-288">String</span></span>                              |
| <span data-ttu-id="f2c00-289">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-289">Default</span></span>        | <span data-ttu-id="f2c00-290">NULL</span><span class="sxs-lookup"><span data-stu-id="f2c00-290">NULL</span></span>                                |
| <span data-ttu-id="f2c00-291">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-291">Minimum system</span></span> | <span data-ttu-id="f2c00-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f2c00-292">Windows XP</span></span>                          |



 

### <a name="localpartitionlookupenabled"></a><span data-ttu-id="f2c00-293">Localpartitionlookupabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-293">LocalPartitionLookupEnabled</span></span>



| <span data-ttu-id="f2c00-294">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-294">Entry</span></span> | <span data-ttu-id="f2c00-295">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-295">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-296">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-296">Description</span></span>    | <span data-ttu-id="f2c00-297">Gibt an, ob der Benutzer der Partitions Zuordnungen in den lokalen Speicher eingecheckt wird.</span><span class="sxs-lookup"><span data-stu-id="f2c00-297">Indicates whether the user of the partition mappings is checked into the local store.</span></span> |
| <span data-ttu-id="f2c00-298">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-298">Access</span></span>         | <span data-ttu-id="f2c00-299">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-299">ReadWrite</span></span>                                                                             |
| <span data-ttu-id="f2c00-300">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-300">Type</span></span>           | <span data-ttu-id="f2c00-301">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-301">Bool</span></span>                                                                                  |
| <span data-ttu-id="f2c00-302">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-302">Default</span></span>        | <span data-ttu-id="f2c00-303">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2c00-303">True</span></span>                                                                                  |
| <span data-ttu-id="f2c00-304">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-304">Minimum system</span></span> | <span data-ttu-id="f2c00-305">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2c00-305">Windows Server 2003</span></span>                                                                   |



 

### <a name="name"></a><span data-ttu-id="f2c00-306">Name</span><span class="sxs-lookup"><span data-stu-id="f2c00-306">Name</span></span>



| <span data-ttu-id="f2c00-307">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-307">Entry</span></span> | <span data-ttu-id="f2c00-308">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-308">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-309">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-309">Description</span></span>    | <span data-ttu-id="f2c00-310">Der Name des Computers.</span><span class="sxs-lookup"><span data-stu-id="f2c00-310">The name of the computer.</span></span> <span data-ttu-id="f2c00-311">Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f2c00-311">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f2c00-312">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-312">Access</span></span>         | <span data-ttu-id="f2c00-313">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="f2c00-313">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f2c00-314">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-314">Type</span></span>           | <span data-ttu-id="f2c00-315">String</span><span class="sxs-lookup"><span data-stu-id="f2c00-315">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f2c00-316">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-316">Default</span></span>        | <span data-ttu-id="f2c00-317">"Arbeitsplatz"</span><span class="sxs-lookup"><span data-stu-id="f2c00-317">"My Computer"</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f2c00-318">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-318">Minimum system</span></span> | <span data-ttu-id="f2c00-319">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-319">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a><span data-ttu-id="f2c00-320">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-320">OperatingSystem</span></span>



| <span data-ttu-id="f2c00-321">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-321">Entry</span></span> | <span data-ttu-id="f2c00-322">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-322">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-323">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-323">Description</span></span>    | <span data-ttu-id="f2c00-324">Das auf dem lokalen Computer installierte Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="f2c00-324">The operating system installed on the local computer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f2c00-325">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-325">Access</span></span>         | <span data-ttu-id="f2c00-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f2c00-327">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-327">Type</span></span>           | <span data-ttu-id="f2c00-328">Lange mögliche Werte: comadminosnotinitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) comadminosunknown (6) comadminoswindowsxppersonal (11) comadminoswindowsxpprofessional (12) comadminoswindowsnetstandardserver (13) comadminoswindowsnetenterpriseserver (14) comadminoswindowsnetdatacenterserver (15) comadminoswindowsnetwebserver (16)</span><span class="sxs-lookup"><span data-stu-id="f2c00-328">Long Possible values:COMAdminOSNotInitialized (0)COMAdminOSWindows3\_1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknown (6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16)</span></span> |
| <span data-ttu-id="f2c00-329">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-329">Default</span></span>        | <span data-ttu-id="f2c00-330">Comadminosnotinitialized (0)</span><span class="sxs-lookup"><span data-stu-id="f2c00-330">COMAdminOSNotInitialized (0)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f2c00-331">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-331">Minimum system</span></span> | <span data-ttu-id="f2c00-332">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-332">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a><span data-ttu-id="f2c00-333">Partitionsenabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-333">PartitionsEnabled</span></span>



| <span data-ttu-id="f2c00-334">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-334">Entry</span></span> | <span data-ttu-id="f2c00-335">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-335">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-336">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-336">Description</span></span>    | <span data-ttu-id="f2c00-337">Gibt an, ob COM+-Partitionen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f2c00-337">Indicates whether COM+ partitions can be used on the local computer.</span></span> <span data-ttu-id="f2c00-338">Wenn diese Eigenschaft false ist, führt jeder Versuch, com+-Partitionen zu verwenden, zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2c00-338">If this property is False, any attempt to use COM+ partitions results in an error.</span></span> |
| <span data-ttu-id="f2c00-339">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-339">Access</span></span>         | <span data-ttu-id="f2c00-340">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-340">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="f2c00-341">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-341">Type</span></span>           | <span data-ttu-id="f2c00-342">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-342">Bool</span></span>                                                                                                                                                    |
| <span data-ttu-id="f2c00-343">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-343">Default</span></span>        | <span data-ttu-id="f2c00-344">Falsch</span><span class="sxs-lookup"><span data-stu-id="f2c00-344">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="f2c00-345">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-345">Minimum system</span></span> | <span data-ttu-id="f2c00-346">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2c00-346">Windows Server 2003</span></span>                                                                                                                                     |



 

### <a name="ports"></a><span data-ttu-id="f2c00-347">Ports</span><span class="sxs-lookup"><span data-stu-id="f2c00-347">Ports</span></span>



| <span data-ttu-id="f2c00-348">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-348">Entry</span></span> | <span data-ttu-id="f2c00-349">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-349">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-350">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-350">Description</span></span>    | <span data-ttu-id="f2c00-351">Eine Zeichenfolge, die Ports für die Internet-oder Intranetverwendung beschreibt, abhängig von der internetportslisted-Eigenschaft. Beispiel: "500-599:600-800".</span><span class="sxs-lookup"><span data-stu-id="f2c00-351">A string describing ports that are for either Internet or intranet use, depending on the InternetPortsListed property; for example, "500-599: 600-800".</span></span> |
| <span data-ttu-id="f2c00-352">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-352">Access</span></span>         | <span data-ttu-id="f2c00-353">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-353">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="f2c00-354">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-354">Type</span></span>           | <span data-ttu-id="f2c00-355">String</span><span class="sxs-lookup"><span data-stu-id="f2c00-355">String</span></span>                                                                                                                                                  |
| <span data-ttu-id="f2c00-356">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-356">Default</span></span>        | <span data-ttu-id="f2c00-357">""</span><span class="sxs-lookup"><span data-stu-id="f2c00-357">""</span></span>                                                                                                                                                      |
| <span data-ttu-id="f2c00-358">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-358">Minimum system</span></span> | <span data-ttu-id="f2c00-359">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-359">Windows 2000</span></span>                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a><span data-ttu-id="f2c00-360">Resourcepoolingenabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-360">ResourcePoolingEnabled</span></span>



| <span data-ttu-id="f2c00-361">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-361">Entry</span></span> | <span data-ttu-id="f2c00-362">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-362">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="f2c00-363">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-363">Description</span></span>    | <span data-ttu-id="f2c00-364">Ermöglicht die Verwendung von Ressourcen Spendern.</span><span class="sxs-lookup"><span data-stu-id="f2c00-364">Enables use of resource dispensers.</span></span> |
| <span data-ttu-id="f2c00-365">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-365">Access</span></span>         | <span data-ttu-id="f2c00-366">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-366">ReadWrite</span></span>                           |
| <span data-ttu-id="f2c00-367">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-367">Type</span></span>           | <span data-ttu-id="f2c00-368">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-368">Bool</span></span>                                |
| <span data-ttu-id="f2c00-369">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-369">Default</span></span>        | <span data-ttu-id="f2c00-370">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2c00-370">True</span></span>                                |
| <span data-ttu-id="f2c00-371">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-371">Minimum system</span></span> | <span data-ttu-id="f2c00-372">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-372">Windows 2000</span></span>                        |



 

### <a name="rpcproxyenabled"></a><span data-ttu-id="f2c00-373">Rpcproxyaktivierte</span><span class="sxs-lookup"><span data-stu-id="f2c00-373">RPCProxyEnabled</span></span>



| <span data-ttu-id="f2c00-374">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-374">Entry</span></span> | <span data-ttu-id="f2c00-375">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-375">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-376">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-376">Description</span></span>    | <span data-ttu-id="f2c00-377">Steuert, ob der RPC-IIS-Proxy aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f2c00-377">Controls whether the RPC IIS proxy is enabled.</span></span> <span data-ttu-id="f2c00-378">Der RPC-IIS-Proxy wird zusammen mit IIS verwendet, um Aufrufe an den RPC-Mechanismus von IIS weiterzuleiten. dabei handelt es sich um eines der Kernteile von com-Internet Diensten, die durch Festlegen von cisenabled auf true aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="f2c00-378">The RPC IIS proxy is used in conjunction with IIS to forward calls to the RPC mechanism from IIS and is one of the core pieces of COM Internet Services, which is enabled by setting CISEnabled to True.</span></span> <span data-ttu-id="f2c00-379">Weitere Informationen zu rpcproxyaktiviertem finden Sie unter [http-RPC-Sicherheit](/windows/desktop/Rpc/rpc-over-http-security).</span><span class="sxs-lookup"><span data-stu-id="f2c00-379">For more information on RPCProxyEnabled, see [HTTP RPC Security](/windows/desktop/Rpc/rpc-over-http-security).</span></span> |
| <span data-ttu-id="f2c00-380">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-380">Access</span></span>         | <span data-ttu-id="f2c00-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-381">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f2c00-382">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-382">Type</span></span>           | <span data-ttu-id="f2c00-383">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-383">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f2c00-384">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-384">Default</span></span>        | <span data-ttu-id="f2c00-385">Falsch</span><span class="sxs-lookup"><span data-stu-id="f2c00-385">False</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f2c00-386">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-386">Minimum system</span></span> | <span data-ttu-id="f2c00-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-387">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a><span data-ttu-id="f2c00-388">Securereferencesaktiviert</span><span class="sxs-lookup"><span data-stu-id="f2c00-388">SecureReferencesEnabled</span></span>



| <span data-ttu-id="f2c00-389">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-389">Entry</span></span> | <span data-ttu-id="f2c00-390">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-391">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-391">Description</span></span>    | <span data-ttu-id="f2c00-392">Erzwingt in DCOM-Computern, dass prozessübergreifende Aufrufe von [**IUnknown:: adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -und [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) -Methoden gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="f2c00-392">Enforces in DCOM computers that cross-process calls to [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are secured.</span></span> |
| <span data-ttu-id="f2c00-393">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-393">Access</span></span>         | <span data-ttu-id="f2c00-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-394">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="f2c00-395">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-395">Type</span></span>           | <span data-ttu-id="f2c00-396">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-396">Bool</span></span>                                                                                                                                                                      |
| <span data-ttu-id="f2c00-397">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-397">Default</span></span>        | <span data-ttu-id="f2c00-398">Falsch</span><span class="sxs-lookup"><span data-stu-id="f2c00-398">False</span></span>                                                                                                                                                                     |
| <span data-ttu-id="f2c00-399">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-399">Minimum system</span></span> | <span data-ttu-id="f2c00-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-400">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a><span data-ttu-id="f2c00-401">Securitytrackingenabled</span><span class="sxs-lookup"><span data-stu-id="f2c00-401">SecurityTrackingEnabled</span></span>



| <span data-ttu-id="f2c00-402">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-402">Entry</span></span> | <span data-ttu-id="f2c00-403">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-403">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="f2c00-404">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-404">Description</span></span>    | <span data-ttu-id="f2c00-405">Auf "true" festgelegt, wenn die Sicherheitsüberwachung für Objekte aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f2c00-405">Set to True if security tracking is enabled on objects.</span></span> |
| <span data-ttu-id="f2c00-406">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-406">Access</span></span>         | <span data-ttu-id="f2c00-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-407">ReadWrite</span></span>                                               |
| <span data-ttu-id="f2c00-408">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-408">Type</span></span>           | <span data-ttu-id="f2c00-409">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-409">Bool</span></span>                                                    |
| <span data-ttu-id="f2c00-410">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-410">Default</span></span>        | <span data-ttu-id="f2c00-411">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2c00-411">True</span></span>                                                    |
| <span data-ttu-id="f2c00-412">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-412">Minimum system</span></span> | <span data-ttu-id="f2c00-413">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-413">Windows 2000</span></span>                                            |



 

### <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="f2c00-414">Srpactivateasactivatorchecks</span><span class="sxs-lookup"><span data-stu-id="f2c00-414">SRPActivateAsActivatorChecks</span></span>



| <span data-ttu-id="f2c00-415">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-415">Entry</span></span> | <span data-ttu-id="f2c00-416">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-416">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-417">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-417">Description</span></span>    | <span data-ttu-id="f2c00-418">Bestimmt, wie die Software Einschränkungs Richtlinie (Software Einschränkungs Richtlinie, SRP) Aktivierungs-as-activatorverbindungen behandelt.</span><span class="sxs-lookup"><span data-stu-id="f2c00-418">Determines how the software restriction policy (SRP) handles activate-as-activator connections.</span></span> <span data-ttu-id="f2c00-419">Wenn diese Einstellung auf true festgelegt ist, wird die für das Server Objekt konfigurierte SRP-Vertrauens Ebene mit der SRP-Vertrauens Ebene des Client Objekts verglichen, und die höhere (strengere) Vertrauens Ebene wird zum Ausführen des Server Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2c00-419">If set to True, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and the higher (more stringent) trust level is used to run the server object.</span></span> <span data-ttu-id="f2c00-420">Wenn false festgelegt ist, wird das Server Objekt mit der SRP-Vertrauens Ebene des Client Objekts ausgeführt, unabhängig von der SRP-Vertrauens Ebene, mit der der Server konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f2c00-420">If set to False, the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which the server is configured.</span></span> |
| <span data-ttu-id="f2c00-421">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-421">Access</span></span>         | <span data-ttu-id="f2c00-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-422">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f2c00-423">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-423">Type</span></span>           | <span data-ttu-id="f2c00-424">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-424">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f2c00-425">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-425">Default</span></span>        | <span data-ttu-id="f2c00-426">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2c00-426">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f2c00-427">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-427">Minimum system</span></span> | <span data-ttu-id="f2c00-428">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f2c00-428">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a><span data-ttu-id="f2c00-429">Srprunningobjectchecks</span><span class="sxs-lookup"><span data-stu-id="f2c00-429">SRPRunningObjectChecks</span></span>



| <span data-ttu-id="f2c00-430">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-430">Entry</span></span> | <span data-ttu-id="f2c00-431">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-431">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-432">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-432">Description</span></span>    | <span data-ttu-id="f2c00-433">Bestimmt, wie die Software Einschränkungs Richtlinie (SRP) Verbindungsversuche mit vorhandenen Prozessen behandelt.</span><span class="sxs-lookup"><span data-stu-id="f2c00-433">Determines how the software restriction policy (SRP) handles attempted connections to existing processes.</span></span> <span data-ttu-id="f2c00-434">Wenn der Wert auf false festgelegt ist, werden Verbindungsversuche mit laufenden Objekten nicht auf die entsprechenden SRP-Vertrauens Ebenen geprüft.</span><span class="sxs-lookup"><span data-stu-id="f2c00-434">If set to False, attempts to connect to running objects are not checked for appropriate SRP trust levels.</span></span> <span data-ttu-id="f2c00-435">Wenn der Wert auf true festgelegt ist, muss das laufende Objekt eine gleichmäßige oder höhere (strengere) SRP-Vertrauens Ebene aufweisen als das Client Objekt.</span><span class="sxs-lookup"><span data-stu-id="f2c00-435">If set to True, the running object must have an equal or higher (more stringent) SRP trust level than the client object.</span></span> <span data-ttu-id="f2c00-436">Beispielsweise kann ein Client Objekt mit einer uneingeschränkten SRP-Vertrauens Ebene keine Verbindung mit einem laufenden Objekt mit einer unzulässigen SRP-Vertrauens Ebene herstellen.</span><span class="sxs-lookup"><span data-stu-id="f2c00-436">For example, a client object with an Unrestricted SRP trust level cannot connect to a running object with a Disallowed SRP trust level.</span></span> |
| <span data-ttu-id="f2c00-437">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-437">Access</span></span>         | <span data-ttu-id="f2c00-438">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-438">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f2c00-439">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-439">Type</span></span>           | <span data-ttu-id="f2c00-440">Bool</span><span class="sxs-lookup"><span data-stu-id="f2c00-440">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f2c00-441">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-441">Default</span></span>        | <span data-ttu-id="f2c00-442">Richtig</span><span class="sxs-lookup"><span data-stu-id="f2c00-442">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f2c00-443">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-443">Minimum system</span></span> | <span data-ttu-id="f2c00-444">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f2c00-444">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a><span data-ttu-id="f2c00-445">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="f2c00-445">TransactionTimeout</span></span>



| <span data-ttu-id="f2c00-446">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2c00-446">Entry</span></span> | <span data-ttu-id="f2c00-447">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c00-447">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c00-448">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2c00-448">Description</span></span>    | <span data-ttu-id="f2c00-449">Sollte auf einen ausreichenden Wert in Sekunden festgelegt werden, wenn Sie zahlreiche Vorgänge innerhalb einer Transaktion durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="f2c00-449">Should be set to a sufficient value in seconds if you are doing numerous operations within a transaction.</span></span> <span data-ttu-id="f2c00-450">Der Standard Timeout Zeitraum beträgt 60 Sekunden, und der maximale Timeout Zeitraum beträgt 3600 Sekunden (1 Stunde).</span><span class="sxs-lookup"><span data-stu-id="f2c00-450">The default time-out period is 60 seconds, and the maximum time-out period is 3600 seconds (1 hour).</span></span> <span data-ttu-id="f2c00-451">Wenn Sie diese Eigenschaft auf 0 festlegen, werden Transaktions Timeouts deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f2c00-451">Setting this property to 0 disables transaction time-outs.</span></span> <span data-ttu-id="f2c00-452">Diese Eigenschaft kann von einzelnen Komponenten überschrieben werden, indem die componenttransaktiontimeout-Eigenschaft der [**Components**](components.md) -Auflistung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2c00-452">This property can be overridden by individual components by using the ComponentTransactionTimeout property of the [**Components**](components.md) collection.</span></span> |
| <span data-ttu-id="f2c00-453">Access</span><span class="sxs-lookup"><span data-stu-id="f2c00-453">Access</span></span>         | <span data-ttu-id="f2c00-454">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2c00-454">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f2c00-455">type</span><span class="sxs-lookup"><span data-stu-id="f2c00-455">Type</span></span>           | <span data-ttu-id="f2c00-456">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="f2c00-456">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f2c00-457">Standard</span><span class="sxs-lookup"><span data-stu-id="f2c00-457">Default</span></span>        | <span data-ttu-id="f2c00-458">60</span><span class="sxs-lookup"><span data-stu-id="f2c00-458">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f2c00-459">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="f2c00-459">Minimum system</span></span> | <span data-ttu-id="f2c00-460">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f2c00-460">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a><span data-ttu-id="f2c00-461">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f2c00-461">Example</span></span>

<span data-ttu-id="f2c00-462">Im folgenden Microsoft Visual Basic Beispiel wird veranschaulicht, wie Sie eine Verbindung mit einem Remote Computer herstellen und seine securitytrackingenabled-Eigenschaft mithilfe der **LocalComputer** -Sammlung des Remote Computers erhalten.</span><span class="sxs-lookup"><span data-stu-id="f2c00-462">The following Microsoft Visual Basic example demonstrates how to connect to a remote computer and get its SecurityTrackingEnabled property by using the **LocalComputer** collection of the remote computer.</span></span> <span data-ttu-id="f2c00-463">Um dieses Beispiel zu verwenden, fügen Sie die com+ admin-Typbibliothek als Verweis auf Ihr Visual Basic Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="f2c00-463">To use this example, add the COM+ Admin Type Library as a reference to your Visual Basic project.</span></span>


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



<span data-ttu-id="f2c00-464">Um die Funktion zu verwenden, geben Sie einen Zeichen folgen Wert für den Namen des Remote Computers an.</span><span class="sxs-lookup"><span data-stu-id="f2c00-464">To use the function, provide a string value for the name of the remote computer.</span></span> <span data-ttu-id="f2c00-465">Der folgende Visual Basic Code zeigt, wie Sie eine Verbindung mit dem Computer "Remotecomputername" herstellen.</span><span class="sxs-lookup"><span data-stu-id="f2c00-465">The following Visual Basic code shows how to connect to the computer named "RemoteComputerName".</span></span>


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a><span data-ttu-id="f2c00-466">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2c00-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c00-467">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="f2c00-467">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
