---
description: Enthält ein-Objekt für jede Komponente in der zugehörigen Anwendung.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Components-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524216"
---
# <a name="components-collection"></a><span data-ttu-id="07876-103">Components-Sammlung</span><span class="sxs-lookup"><span data-stu-id="07876-103">Components collection</span></span>

<span data-ttu-id="07876-104">Enthält ein-Objekt für jede Komponente in der zugehörigen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="07876-104">Contains an object for each component in the related application.</span></span> <span data-ttu-id="07876-105">Die **Komponenten** Sammlung bezieht sich immer auf ein Objekt in der [**Anwendungs**](applications.md) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="07876-105">The **Components** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="07876-106">Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, halten Einstellungen auf Komponentenebene.</span><span class="sxs-lookup"><span data-stu-id="07876-106">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="07876-107">Diese Auflistung unterstützt die [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts, jedoch nicht die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -Methode.</span><span class="sxs-lookup"><span data-stu-id="07876-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="07876-108">Verwenden Sie Methoden für das [**comadmincatalog**](comadmincatalog.md) -Objekt, um Komponenten in einer Anwendung zu installieren oder zu importieren.</span><span class="sxs-lookup"><span data-stu-id="07876-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="07876-109">Member</span><span class="sxs-lookup"><span data-stu-id="07876-109">Members</span></span>

<span data-ttu-id="07876-110">Die **Components** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="07876-110">The **Components** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="07876-111">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="07876-111">Related Collections</span></span>

<span data-ttu-id="07876-112">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="07876-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="07876-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="07876-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="07876-114">**Interfakesforcomponent**</span><span class="sxs-lookup"><span data-stu-id="07876-114">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)
-   [<span data-ttu-id="07876-115">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="07876-115">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="07876-116">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="07876-116">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="07876-117">**Rolesforcomponent**</span><span class="sxs-lookup"><span data-stu-id="07876-117">**RolesForComponent**</span></span>](rolesforcomponent.md)
-   [<span data-ttu-id="07876-118">**Abonnement forcomponent**</span><span class="sxs-lookup"><span data-stu-id="07876-118">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

<span data-ttu-id="07876-119">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="07876-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="07876-120">**Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="07876-120">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="07876-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07876-121">Properties</span></span>

<span data-ttu-id="07876-122">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="07876-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="07876-123">"Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="07876-123">AllowInprocSubscribers</span></span>](#allowinprocsubscribers)
-   [<span data-ttu-id="07876-124">ApplicationId</span><span class="sxs-lookup"><span data-stu-id="07876-124">ApplicationID</span></span>](#applicationid)
-   [<span data-ttu-id="07876-125">Bitness</span><span class="sxs-lookup"><span data-stu-id="07876-125">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="07876-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="07876-126">CLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="07876-127">Componentaccesschecksenabled</span><span class="sxs-lookup"><span data-stu-id="07876-127">ComponentAccessChecksEnabled</span></span>](#componentaccesschecksenabled)
-   [<span data-ttu-id="07876-128">Componenttransaktiontimeout</span><span class="sxs-lookup"><span data-stu-id="07876-128">ComponentTransactionTimeout</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="07876-129">Componenttransaktiontimeoutenabled</span><span class="sxs-lookup"><span data-stu-id="07876-129">ComponentTransactionTimeoutEnabled</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="07876-130">Comtiintrinsie</span><span class="sxs-lookup"><span data-stu-id="07876-130">COMTIIntrinsics</span></span>](#comtiintrinsics)
-   [<span data-ttu-id="07876-131">Konstruktionaktiviert</span><span class="sxs-lookup"><span data-stu-id="07876-131">ConstructionEnabled</span></span>](#constructionenabled)
-   [<span data-ttu-id="07876-132">Constructor String</span><span class="sxs-lookup"><span data-stu-id="07876-132">ConstructorString</span></span>](#constructorstring)
-   [<span data-ttu-id="07876-133">"Kreationtimeout"</span><span class="sxs-lookup"><span data-stu-id="07876-133">CreationTimeout</span></span>](#creationtimeout)
-   [<span data-ttu-id="07876-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07876-134">Description</span></span>](#description)
-   [<span data-ttu-id="07876-135">DLL</span><span class="sxs-lookup"><span data-stu-id="07876-135">DLL</span></span>](#dll)
-   [<span data-ttu-id="07876-136">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="07876-136">EventTrackingEnabled</span></span>](#eventtrackingenabled)
-   [<span data-ttu-id="07876-137">exceptionClass</span><span class="sxs-lookup"><span data-stu-id="07876-137">ExceptionClass</span></span>](#exceptionclass)
-   [<span data-ttu-id="07876-138">"Freinparallel"</span><span class="sxs-lookup"><span data-stu-id="07876-138">FireInParallel</span></span>](#fireinparallel)
-   [<span data-ttu-id="07876-139">Iisintrinsics</span><span class="sxs-lookup"><span data-stu-id="07876-139">IISIntrinsics</span></span>](#iisintrinsics)
-   [<span data-ttu-id="07876-140">Initializeserverapplication</span><span class="sxs-lookup"><span data-stu-id="07876-140">InitializeServerApplication</span></span>](#initializeserverapplication)
-   [<span data-ttu-id="07876-141">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="07876-141">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="07876-142">Isiebziger Class</span><span class="sxs-lookup"><span data-stu-id="07876-142">IsEventClass</span></span>](#iseventclass)
-   [<span data-ttu-id="07876-143">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="07876-143">IsInstalled</span></span>](#isinstalled)
-   [<span data-ttu-id="07876-144">Isprivatecomponent</span><span class="sxs-lookup"><span data-stu-id="07876-144">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="07876-145">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="07876-145">JustInTimeActivation</span></span>](#justintimeactivation)
-   [<span data-ttu-id="07876-146">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="07876-146">LoadBalancingSupported</span></span>](#loadbalancingsupported)
-   [<span data-ttu-id="07876-147">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="07876-147">MaxPoolSize</span></span>](#maxpoolsize)
-   [<span data-ttu-id="07876-148">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="07876-148">MinPoolSize</span></span>](#minpoolsize)
-   [<span data-ttu-id="07876-149">Multiinterfacepublisherfilterclsid</span><span class="sxs-lookup"><span data-stu-id="07876-149">MultiInterfacePublisherFilterCLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="07876-150">Mustrauuninclientcontext</span><span class="sxs-lookup"><span data-stu-id="07876-150">MustRunInClientContext</span></span>](#mustruninclientcontext)
-   [<span data-ttu-id="07876-151">Mustranunindefehlercontext</span><span class="sxs-lookup"><span data-stu-id="07876-151">MustRunInDefaultContext</span></span>](#mustrunindefaultcontext)
-   [<span data-ttu-id="07876-152">Objectpoolingenabled</span><span class="sxs-lookup"><span data-stu-id="07876-152">ObjectPoolingEnabled</span></span>](#objectpoolingenabled)
-   [<span data-ttu-id="07876-153">ProgID</span><span class="sxs-lookup"><span data-stu-id="07876-153">ProgID</span></span>](#progid)
-   [<span data-ttu-id="07876-154">PublisherID</span><span class="sxs-lookup"><span data-stu-id="07876-154">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="07876-155">Soapassemblyname</span><span class="sxs-lookup"><span data-stu-id="07876-155">SoapAssemblyName</span></span>](#soapassemblyname)
-   [<span data-ttu-id="07876-156">Soaptyname</span><span class="sxs-lookup"><span data-stu-id="07876-156">SoapTypeName</span></span>](#soaptypename)
-   [<span data-ttu-id="07876-157">Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="07876-157">Synchronization</span></span>](#synchronization)
-   [<span data-ttu-id="07876-158">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="07876-158">ThreadingModel</span></span>](#threadingmodel)
-   [<span data-ttu-id="07876-159">Transaktion</span><span class="sxs-lookup"><span data-stu-id="07876-159">Transaction</span></span>](#componenttransactiontimeout)
-   [<span data-ttu-id="07876-160">Txisolationlevel</span><span class="sxs-lookup"><span data-stu-id="07876-160">TxIsolationLevel</span></span>](#txisolationlevel)
-   [<span data-ttu-id="07876-161">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="07876-161">VersionBuild</span></span>](#versionbuild)
-   [<span data-ttu-id="07876-162">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="07876-162">VersionMajor</span></span>](#versionmajor)
-   [<span data-ttu-id="07876-163">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="07876-163">VersionMinor</span></span>](#versionminor)
-   [<span data-ttu-id="07876-164">Versionsubbuild</span><span class="sxs-lookup"><span data-stu-id="07876-164">VersionSubBuild</span></span>](#versionsubbuild)

### <a name="allowinprocsubscribers"></a><span data-ttu-id="07876-165">"Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="07876-165">AllowInprocSubscribers</span></span>



| <span data-ttu-id="07876-166">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-166">Entry</span></span> | <span data-ttu-id="07876-167">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-167">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="07876-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-168">Description</span></span>    | <span data-ttu-id="07876-169">Aktiviert in Prozess Abonnenten, wenn die Komponente eine Ereignisklasse ist.</span><span class="sxs-lookup"><span data-stu-id="07876-169">Enables in process subscribers if the component is an event class.</span></span> |
| <span data-ttu-id="07876-170">Access</span><span class="sxs-lookup"><span data-stu-id="07876-170">Access</span></span>         | <span data-ttu-id="07876-171">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-171">ReadWrite</span></span>                                                          |
| <span data-ttu-id="07876-172">type</span><span class="sxs-lookup"><span data-stu-id="07876-172">Type</span></span>           | <span data-ttu-id="07876-173">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-173">Bool</span></span>                                                               |
| <span data-ttu-id="07876-174">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-174">Default</span></span>        | <span data-ttu-id="07876-175">Richtig</span><span class="sxs-lookup"><span data-stu-id="07876-175">True</span></span>                                                               |
| <span data-ttu-id="07876-176">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-176">Minimum system</span></span> | <span data-ttu-id="07876-177">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-177">Windows 2000</span></span>                                                       |



 

### <a name="applicationid"></a><span data-ttu-id="07876-178">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="07876-178">ApplicationID</span></span>



| <span data-ttu-id="07876-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-179">Entry</span></span> | <span data-ttu-id="07876-180">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-180">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-181">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-181">Description</span></span>    | <span data-ttu-id="07876-182">Die GUID für die Anwendung, die die Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="07876-182">The GUID for the application containing the component.</span></span> <span data-ttu-id="07876-183">Muss eine gültige Anwendungs-GUID sein, die überprüft wird, bevor [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="07876-183">Must be a valid application's GUID, which is verified before [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) is called.</span></span> <span data-ttu-id="07876-184">Wenn dieser Wert in eine GUID für eine andere Anwendung geändert wird, wechselt die Komponente in diese Anwendung.</span><span class="sxs-lookup"><span data-stu-id="07876-184">If this value is changed to be a GUID for a different application, the component moves to that application.</span></span> |
| <span data-ttu-id="07876-185">Access</span><span class="sxs-lookup"><span data-stu-id="07876-185">Access</span></span>         | <span data-ttu-id="07876-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-186">ReadWrite</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="07876-187">type</span><span class="sxs-lookup"><span data-stu-id="07876-187">Type</span></span>           | <span data-ttu-id="07876-188">String</span><span class="sxs-lookup"><span data-stu-id="07876-188">String</span></span>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="07876-189">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-189">Default</span></span>        | <span data-ttu-id="07876-190">–</span><span class="sxs-lookup"><span data-stu-id="07876-190">N/A</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="07876-191">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-191">Minimum system</span></span> | <span data-ttu-id="07876-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-192">Windows 2000</span></span>                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a><span data-ttu-id="07876-193">Bitness</span><span class="sxs-lookup"><span data-stu-id="07876-193">Bitness</span></span>



| <span data-ttu-id="07876-194">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-194">Entry</span></span> | <span data-ttu-id="07876-195">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-195">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-196">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-196">Description</span></span>    | <span data-ttu-id="07876-197">Stellt den binären bikretivität einer Komponente dar.</span><span class="sxs-lookup"><span data-stu-id="07876-197">Represents the binary bitness type of a component.</span></span> <span data-ttu-id="07876-198">Auf Systemen, die 64-Bit-Windows verwenden, unterscheidet diese Eigenschaft zwischen 64-Bit-Komponenten und 32-Bit-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="07876-198">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="07876-199">Access</span><span class="sxs-lookup"><span data-stu-id="07876-199">Access</span></span>         | <span data-ttu-id="07876-200">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-200">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="07876-201">type</span><span class="sxs-lookup"><span data-stu-id="07876-201">Type</span></span>           | <span data-ttu-id="07876-202">Lange mögliche Werte: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="07876-202">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                       |
| <span data-ttu-id="07876-203">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-203">Default</span></span>        | <span data-ttu-id="07876-204">–</span><span class="sxs-lookup"><span data-stu-id="07876-204">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="07876-205">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-205">Minimum system</span></span> | <span data-ttu-id="07876-206">Windows XP</span><span class="sxs-lookup"><span data-stu-id="07876-206">Windows XP</span></span>                                                                                                                                                          |



 

### <a name="clsid"></a><span data-ttu-id="07876-207">CLSID</span><span class="sxs-lookup"><span data-stu-id="07876-207">CLSID</span></span>



| <span data-ttu-id="07876-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-208">Entry</span></span> | <span data-ttu-id="07876-209">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-209">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-210">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-210">Description</span></span>    | <span data-ttu-id="07876-211">Eine GUID für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="07876-211">A GUID for the component.</span></span> <span data-ttu-id="07876-212">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="07876-212">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="07876-213">Access</span><span class="sxs-lookup"><span data-stu-id="07876-213">Access</span></span>         | <span data-ttu-id="07876-214">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-214">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="07876-215">type</span><span class="sxs-lookup"><span data-stu-id="07876-215">Type</span></span>           | <span data-ttu-id="07876-216">String</span><span class="sxs-lookup"><span data-stu-id="07876-216">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="07876-217">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-217">Default</span></span>        | <span data-ttu-id="07876-218">–</span><span class="sxs-lookup"><span data-stu-id="07876-218">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="07876-219">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-219">Minimum system</span></span> | <span data-ttu-id="07876-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-220">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a><span data-ttu-id="07876-221">Componentaccesschecksenabled</span><span class="sxs-lookup"><span data-stu-id="07876-221">ComponentAccessChecksEnabled</span></span>



| <span data-ttu-id="07876-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-222">Entry</span></span> | <span data-ttu-id="07876-223">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-223">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-224">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-224">Description</span></span>    | <span data-ttu-id="07876-225">Gibt an, ob rollenbasierte Zugriffs Überprüfungen bei Aufrufen der Komponente ausgeführt werden und in Verbindung mit den Eigenschaften AccessChecksLevel und applicationaccesschecksenabled der Anwendung funktionieren.</span><span class="sxs-lookup"><span data-stu-id="07876-225">Indicates whether role-based access checks are performed on calls into the component and works in conjunction with the AccessChecksLevel and ApplicationAccessChecksEnabled properties on the application.</span></span> |
| <span data-ttu-id="07876-226">Access</span><span class="sxs-lookup"><span data-stu-id="07876-226">Access</span></span>         | <span data-ttu-id="07876-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-227">ReadWrite</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="07876-228">type</span><span class="sxs-lookup"><span data-stu-id="07876-228">Type</span></span>           | <span data-ttu-id="07876-229">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-229">Bool</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="07876-230">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-230">Default</span></span>        | <span data-ttu-id="07876-231">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-231">False</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="07876-232">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-232">Minimum system</span></span> | <span data-ttu-id="07876-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-233">Windows 2000</span></span>                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a><span data-ttu-id="07876-234">Componenttransaktiontimeout</span><span class="sxs-lookup"><span data-stu-id="07876-234">ComponentTransactionTimeout</span></span>



| <span data-ttu-id="07876-235">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-235">Entry</span></span> | <span data-ttu-id="07876-236">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-236">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-237">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-237">Description</span></span>    | <span data-ttu-id="07876-238">Gibt bei Verwendung in einer Transaktion den Zeitraum an, in dem diese Komponente zum Timeout der Transaktion veranlasst. Der Standardwert ist 60 Sekunden und darf nicht länger als 3600 Sekunden (1 Stunde) sein.</span><span class="sxs-lookup"><span data-stu-id="07876-238">When used in a transaction, specifies the time period in which this component causes the transaction to time out. The default is 60 seconds and cannot be longer than 3600 seconds (1 hour).</span></span> <span data-ttu-id="07876-239">Der Timeout Wert kann auf 0 festgelegt werden und einen unbegrenzten Transaktions Timeout Zeitraum angeben.</span><span class="sxs-lookup"><span data-stu-id="07876-239">The time-out value can be set to 0, specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="07876-240">Damit diese Eigenschaft verwendet werden kann, muss componenttransaktiontimeoutenabled den Wert "true" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="07876-240">For this property to be used, ComponentTransactionTimeoutEnabled must be True.</span></span> <span data-ttu-id="07876-241">Der Wert dieser Eigenschaft überschreibt den globalen Transaktions Timeout, der durch die transaktiontimeout-Eigenschaft der [**LocalComputer**](localcomputer.md) -Auflistung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07876-241">The value of this property overrides the global transaction time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection.</span></span> |
| <span data-ttu-id="07876-242">Access</span><span class="sxs-lookup"><span data-stu-id="07876-242">Access</span></span>         | <span data-ttu-id="07876-243">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-243">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="07876-244">type</span><span class="sxs-lookup"><span data-stu-id="07876-244">Type</span></span>           | <span data-ttu-id="07876-245">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="07876-245">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="07876-246">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-246">Default</span></span>        | <span data-ttu-id="07876-247">60</span><span class="sxs-lookup"><span data-stu-id="07876-247">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="07876-248">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-248">Minimum system</span></span> | <span data-ttu-id="07876-249">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-249">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a><span data-ttu-id="07876-250">Componenttransaktiontimeoutenabled</span><span class="sxs-lookup"><span data-stu-id="07876-250">ComponentTransactionTimeoutEnabled</span></span>



| <span data-ttu-id="07876-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-251">Entry</span></span> | <span data-ttu-id="07876-252">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-252">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-253">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-253">Description</span></span>    | <span data-ttu-id="07876-254">Gibt an, ob der Transaktions Timeout Zeitraum für diese Komponente aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="07876-254">Specifies whether the transaction time-out period is enabled for this component.</span></span> <span data-ttu-id="07876-255">Standardmäßig ist das Timeout Feature für Transaktionen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="07876-255">By default, the transaction time-out feature is disabled.</span></span> <span data-ttu-id="07876-256">Wenn diese Eigenschaft auf true festgelegt ist, wird das von componenttransaktiontimeout angegebene Timeout verwendet.</span><span class="sxs-lookup"><span data-stu-id="07876-256">When this property is True, the time-out specified by ComponentTransactionTimeout is used.</span></span> <span data-ttu-id="07876-257">Wenn diese Eigenschaft auf false festgelegt ist, wird das von der transaktiontimeout-Eigenschaft der [**LocalComputer**](localcomputer.md) -Auflistung angegebene Timeout verwendet.</span><span class="sxs-lookup"><span data-stu-id="07876-257">When this property is False, the time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="07876-258">Access</span><span class="sxs-lookup"><span data-stu-id="07876-258">Access</span></span>         | <span data-ttu-id="07876-259">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-259">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="07876-260">type</span><span class="sxs-lookup"><span data-stu-id="07876-260">Type</span></span>           | <span data-ttu-id="07876-261">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-261">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="07876-262">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-262">Default</span></span>        | <span data-ttu-id="07876-263">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-263">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="07876-264">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-264">Minimum system</span></span> | <span data-ttu-id="07876-265">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-265">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a><span data-ttu-id="07876-266">Comtiintrinsie</span><span class="sxs-lookup"><span data-stu-id="07876-266">COMTIIntrinsics</span></span>



| <span data-ttu-id="07876-267">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-267">Entry</span></span> | <span data-ttu-id="07876-268">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-268">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-269">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-269">Description</span></span>    | <span data-ttu-id="07876-270">Ermöglicht das Übergeben von Kontexteigenschaften aus dem com Transaction Integrator (COMTI) in den Kontext für diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="07876-270">Enables passing of context properties from the COM Transaction Integrator (COMTI) into the context for this class.</span></span> <span data-ttu-id="07876-271">Die COMTI vereinfacht die Aufgabe zum Umwickeln von Main Frame Transaktionen und Geschäftslogik als COM-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="07876-271">The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.</span></span> |
| <span data-ttu-id="07876-272">Access</span><span class="sxs-lookup"><span data-stu-id="07876-272">Access</span></span>         | <span data-ttu-id="07876-273">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-273">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="07876-274">type</span><span class="sxs-lookup"><span data-stu-id="07876-274">Type</span></span>           | <span data-ttu-id="07876-275">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-275">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="07876-276">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-276">Default</span></span>        | <span data-ttu-id="07876-277">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-277">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="07876-278">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-278">Minimum system</span></span> | <span data-ttu-id="07876-279">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-279">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a><span data-ttu-id="07876-280">Konstruktionaktiviert</span><span class="sxs-lookup"><span data-stu-id="07876-280">ConstructionEnabled</span></span>



| <span data-ttu-id="07876-281">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-281">Entry</span></span> | <span data-ttu-id="07876-282">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-282">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-283">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-283">Description</span></span>    | <span data-ttu-id="07876-284">Bestimmt, ob der konstruktorstring beim Konstruieren an das-Objekt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="07876-284">Determines whether the ConstructorString is passed to the object when it is constructed.</span></span> |
| <span data-ttu-id="07876-285">Access</span><span class="sxs-lookup"><span data-stu-id="07876-285">Access</span></span>         | <span data-ttu-id="07876-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-286">ReadWrite</span></span>                                                                                |
| <span data-ttu-id="07876-287">type</span><span class="sxs-lookup"><span data-stu-id="07876-287">Type</span></span>           | <span data-ttu-id="07876-288">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-288">Bool</span></span>                                                                                     |
| <span data-ttu-id="07876-289">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-289">Default</span></span>        | <span data-ttu-id="07876-290">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-290">False</span></span>                                                                                    |
| <span data-ttu-id="07876-291">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-291">Minimum system</span></span> | <span data-ttu-id="07876-292">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-292">Windows 2000</span></span>                                                                             |



 

### <a name="constructorstring"></a><span data-ttu-id="07876-293">Constructor String</span><span class="sxs-lookup"><span data-stu-id="07876-293">ConstructorString</span></span>



| <span data-ttu-id="07876-294">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-294">Entry</span></span> | <span data-ttu-id="07876-295">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-295">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-296">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-296">Description</span></span>    | <span data-ttu-id="07876-297">Initialisierungs Zeichenfolge für die Komponenten Konstruktion.</span><span class="sxs-lookup"><span data-stu-id="07876-297">Initialization string for component construction.</span></span> <span data-ttu-id="07876-298">Sie können unterschiedliche Objekte aus derselben generischen Komponente erstellen, indem Sie objektkonstruktorzeichenfolgen verwenden.</span><span class="sxs-lookup"><span data-stu-id="07876-298">You can create different objects from the same generic component by using object constructor strings.</span></span> <span data-ttu-id="07876-299">Wenn constructionaktivierte den Wert false hat, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="07876-299">If ConstructionEnabled is False, this property is ignored.</span></span> |
| <span data-ttu-id="07876-300">Access</span><span class="sxs-lookup"><span data-stu-id="07876-300">Access</span></span>         | <span data-ttu-id="07876-301">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-301">ReadWrite</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="07876-302">type</span><span class="sxs-lookup"><span data-stu-id="07876-302">Type</span></span>           | <span data-ttu-id="07876-303">String</span><span class="sxs-lookup"><span data-stu-id="07876-303">String</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="07876-304">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-304">Default</span></span>        | <span data-ttu-id="07876-305">""</span><span class="sxs-lookup"><span data-stu-id="07876-305">""</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="07876-306">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-306">Minimum system</span></span> | <span data-ttu-id="07876-307">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-307">Windows 2000</span></span>                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a><span data-ttu-id="07876-308">"Kreationtimeout"</span><span class="sxs-lookup"><span data-stu-id="07876-308">CreationTimeout</span></span>



| <span data-ttu-id="07876-309">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-309">Entry</span></span> | <span data-ttu-id="07876-310">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-310">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-311">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-311">Description</span></span>    | <span data-ttu-id="07876-312">Wenn das Objekt erstellt wird, wird die Anzahl von Millisekunden vor dem zurückgegebenen Timeout Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="07876-312">When creating the object, number of milliseconds before a time-out error is returned.</span></span> <span data-ttu-id="07876-313">Das maximale Timeout beträgt 2147483647 Millisekunden (ungefähr 25 Tage).</span><span class="sxs-lookup"><span data-stu-id="07876-313">The maximum time-out is 2147483647 milliseconds (about 25 days).</span></span> |
| <span data-ttu-id="07876-314">Access</span><span class="sxs-lookup"><span data-stu-id="07876-314">Access</span></span>         | <span data-ttu-id="07876-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-315">ReadWrite</span></span>                                                                                                                                              |
| <span data-ttu-id="07876-316">type</span><span class="sxs-lookup"><span data-stu-id="07876-316">Type</span></span>           | <span data-ttu-id="07876-317">Long (0-2147483647)</span><span class="sxs-lookup"><span data-stu-id="07876-317">Long (0-2147483647)</span></span>                                                                                                                                    |
| <span data-ttu-id="07876-318">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-318">Default</span></span>        | <span data-ttu-id="07876-319">0</span><span class="sxs-lookup"><span data-stu-id="07876-319">0</span></span>                                                                                                                                                      |
| <span data-ttu-id="07876-320">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-320">Minimum system</span></span> | <span data-ttu-id="07876-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-321">Windows 2000</span></span>                                                                                                                                           |



 

### <a name="description"></a><span data-ttu-id="07876-322">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-322">Description</span></span>



| <span data-ttu-id="07876-323">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-323">Entry</span></span> | <span data-ttu-id="07876-324">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-324">Value</span></span> |
|----------------|--------------------------|
| <span data-ttu-id="07876-325">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-325">Description</span></span>    | <span data-ttu-id="07876-326">Beschreibt die Komponente.</span><span class="sxs-lookup"><span data-stu-id="07876-326">Describes the component.</span></span> |
| <span data-ttu-id="07876-327">Access</span><span class="sxs-lookup"><span data-stu-id="07876-327">Access</span></span>         | <span data-ttu-id="07876-328">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-328">ReadWrite</span></span>                |
| <span data-ttu-id="07876-329">type</span><span class="sxs-lookup"><span data-stu-id="07876-329">Type</span></span>           | <span data-ttu-id="07876-330">String</span><span class="sxs-lookup"><span data-stu-id="07876-330">String</span></span>                   |
| <span data-ttu-id="07876-331">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-331">Default</span></span>        | <span data-ttu-id="07876-332">""</span><span class="sxs-lookup"><span data-stu-id="07876-332">""</span></span>                       |
| <span data-ttu-id="07876-333">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-333">Minimum system</span></span> | <span data-ttu-id="07876-334">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-334">Windows 2000</span></span>             |



 

### <a name="dll"></a><span data-ttu-id="07876-335">DLL</span><span class="sxs-lookup"><span data-stu-id="07876-335">DLL</span></span>



| <span data-ttu-id="07876-336">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-336">Entry</span></span> | <span data-ttu-id="07876-337">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-337">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="07876-338">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-338">Description</span></span>    | <span data-ttu-id="07876-339">Der Name und der Pfad der Datei, die die Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="07876-339">The name and path of the file containing the component.</span></span> |
| <span data-ttu-id="07876-340">Access</span><span class="sxs-lookup"><span data-stu-id="07876-340">Access</span></span>         | <span data-ttu-id="07876-341">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-341">ReadOnly</span></span>                                                |
| <span data-ttu-id="07876-342">type</span><span class="sxs-lookup"><span data-stu-id="07876-342">Type</span></span>           | <span data-ttu-id="07876-343">String</span><span class="sxs-lookup"><span data-stu-id="07876-343">String</span></span>                                                  |
| <span data-ttu-id="07876-344">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-344">Default</span></span>        | <span data-ttu-id="07876-345">–</span><span class="sxs-lookup"><span data-stu-id="07876-345">N/A</span></span>                                                     |
| <span data-ttu-id="07876-346">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-346">Minimum system</span></span> | <span data-ttu-id="07876-347">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-347">Windows 2000</span></span>                                            |



 

### <a name="eventtrackingenabled"></a><span data-ttu-id="07876-348">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="07876-348">EventTrackingEnabled</span></span>



| <span data-ttu-id="07876-349">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-349">Entry</span></span> | <span data-ttu-id="07876-350">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-350">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-351">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-351">Description</span></span>    | <span data-ttu-id="07876-352">Bestimmt, ob Ereignisse nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="07876-352">Determines whether events are tracked.</span></span> <span data-ttu-id="07876-353">Zu den Ereignissen gehören Aktionen wie das Herunterfahren der Anwendung. Objekt Erstellung und-Freigabe; Objekt Verweise, Konsistenz, Aktivierung und decoaktivierung; Methodenaufrufe, Rückgaben und Ausnahmen; Starten der Transaktion, Vorbereitung auf den Commit und Abbrechen; Verbindung, Zuordnung und Wiederverwendung des Ressourcen Verteilers Thread Zuordnung und-Wiederverwendung.</span><span class="sxs-lookup"><span data-stu-id="07876-353">Events include actions such as application shutdown; object creation and release; object references, consistency, activation, and deactivation; method calls, returns, and exceptions; transaction startup, preparing to commit, and abort; resource dispenser connection, allocation, and recycling; thread allocation and recycling.</span></span> |
| <span data-ttu-id="07876-354">Access</span><span class="sxs-lookup"><span data-stu-id="07876-354">Access</span></span>         | <span data-ttu-id="07876-355">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-355">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="07876-356">type</span><span class="sxs-lookup"><span data-stu-id="07876-356">Type</span></span>           | <span data-ttu-id="07876-357">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-357">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="07876-358">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-358">Default</span></span>        | <span data-ttu-id="07876-359">Richtig</span><span class="sxs-lookup"><span data-stu-id="07876-359">True</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="07876-360">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-360">Minimum system</span></span> | <span data-ttu-id="07876-361">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-361">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a><span data-ttu-id="07876-362">exceptionClass</span><span class="sxs-lookup"><span data-stu-id="07876-362">ExceptionClass</span></span>



| <span data-ttu-id="07876-363">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-363">Entry</span></span> | <span data-ttu-id="07876-364">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-364">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-365">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-365">Description</span></span>    | <span data-ttu-id="07876-366">Die CLSID, bei der es sich um eine GUID oder eine Monikerzeichenfolge handeln kann, um ein alternatives Programm während des Vorgangs zu aktivieren, das wiederholt fehlerhafte Komponenten in der Warteschlange verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="07876-366">The CLSID, which can be a GUID or a moniker string, to activate an alternative program during the process of dealing with a repeatedly failing queued components program.</span></span> |
| <span data-ttu-id="07876-367">Access</span><span class="sxs-lookup"><span data-stu-id="07876-367">Access</span></span>         | <span data-ttu-id="07876-368">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-368">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="07876-369">type</span><span class="sxs-lookup"><span data-stu-id="07876-369">Type</span></span>           | <span data-ttu-id="07876-370">String</span><span class="sxs-lookup"><span data-stu-id="07876-370">String</span></span>                                                                                                                                                                    |
| <span data-ttu-id="07876-371">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-371">Default</span></span>        | <span data-ttu-id="07876-372">""</span><span class="sxs-lookup"><span data-stu-id="07876-372">""</span></span>                                                                                                                                                                        |
| <span data-ttu-id="07876-373">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-373">Minimum system</span></span> | <span data-ttu-id="07876-374">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-374">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="fireinparallel"></a><span data-ttu-id="07876-375">"Freinparallel"</span><span class="sxs-lookup"><span data-stu-id="07876-375">FireInParallel</span></span>



| <span data-ttu-id="07876-376">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-376">Entry</span></span> | <span data-ttu-id="07876-377">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-377">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="07876-378">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-378">Description</span></span>    | <span data-ttu-id="07876-379">Ermöglicht das parallele Auslösen von Ereignissen, wenn die Komponente eine Ereignisklasse ist.</span><span class="sxs-lookup"><span data-stu-id="07876-379">Enables events to be fired in parallel if the component is an event class.</span></span> |
| <span data-ttu-id="07876-380">Access</span><span class="sxs-lookup"><span data-stu-id="07876-380">Access</span></span>         | <span data-ttu-id="07876-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-381">ReadWrite</span></span>                                                                  |
| <span data-ttu-id="07876-382">type</span><span class="sxs-lookup"><span data-stu-id="07876-382">Type</span></span>           | <span data-ttu-id="07876-383">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-383">Bool</span></span>                                                                       |
| <span data-ttu-id="07876-384">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-384">Default</span></span>        | <span data-ttu-id="07876-385">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-385">False</span></span>                                                                      |
| <span data-ttu-id="07876-386">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-386">Minimum system</span></span> | <span data-ttu-id="07876-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-387">Windows 2000</span></span>                                                               |



 

### <a name="iisintrinsics"></a><span data-ttu-id="07876-388">Iisintrinsics</span><span class="sxs-lookup"><span data-stu-id="07876-388">IISIntrinsics</span></span>



| <span data-ttu-id="07876-389">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-389">Entry</span></span> | <span data-ttu-id="07876-390">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-391">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-391">Description</span></span>    | <span data-ttu-id="07876-392">Ermöglicht das Übergeben von IIS-Kontexteigenschaften, z. b. eines Anwendungs Sitzungs Objekts oder eines Benutzer Sitzungs Objekts, in den Kontext für diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="07876-392">Enables passing of IIS context properties, such as an application session object or a user session object, into the context for this class.</span></span> |
| <span data-ttu-id="07876-393">Access</span><span class="sxs-lookup"><span data-stu-id="07876-393">Access</span></span>         | <span data-ttu-id="07876-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-394">ReadWrite</span></span>                                                                                                                                   |
| <span data-ttu-id="07876-395">type</span><span class="sxs-lookup"><span data-stu-id="07876-395">Type</span></span>           | <span data-ttu-id="07876-396">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-396">Bool</span></span>                                                                                                                                        |
| <span data-ttu-id="07876-397">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-397">Default</span></span>        | <span data-ttu-id="07876-398">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-398">False</span></span>                                                                                                                                       |
| <span data-ttu-id="07876-399">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-399">Minimum system</span></span> | <span data-ttu-id="07876-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-400">Windows 2000</span></span>                                                                                                                                |



 

### <a name="initializeserverapplication"></a><span data-ttu-id="07876-401">Initializeserverapplication</span><span class="sxs-lookup"><span data-stu-id="07876-401">InitializeServerApplication</span></span>



| <span data-ttu-id="07876-402">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-402">Entry</span></span> | <span data-ttu-id="07876-403">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-403">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="07876-404">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-404">Description</span></span>    | <span data-ttu-id="07876-405">Gibt an, ob die-Komponente verwendet wird, um eine Serveranwendung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="07876-405">Indicates whether the component is used to initialize a server application.</span></span> |
| <span data-ttu-id="07876-406">Access</span><span class="sxs-lookup"><span data-stu-id="07876-406">Access</span></span>         | <span data-ttu-id="07876-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-407">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="07876-408">type</span><span class="sxs-lookup"><span data-stu-id="07876-408">Type</span></span>           | <span data-ttu-id="07876-409">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-409">Bool</span></span>                                                                        |
| <span data-ttu-id="07876-410">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-410">Default</span></span>        | <span data-ttu-id="07876-411">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-411">False</span></span>                                                                       |
| <span data-ttu-id="07876-412">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-412">Minimum system</span></span> | <span data-ttu-id="07876-413">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="07876-413">Windows Server 2003</span></span>                                                         |



 

### <a name="isenabled"></a><span data-ttu-id="07876-414">isEnabled</span><span class="sxs-lookup"><span data-stu-id="07876-414">IsEnabled</span></span>



| <span data-ttu-id="07876-415">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-415">Entry</span></span> | <span data-ttu-id="07876-416">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-416">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-417">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-417">Description</span></span>    | <span data-ttu-id="07876-418">False, wenn die COM+-Anwendung oder-Komponente deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="07876-418">False if the COM+ application or component is disabled.</span></span> <span data-ttu-id="07876-419">Wenn die COM+-Anwendung oder-Komponente aktiviert ist, ist isaktivierte "true".</span><span class="sxs-lookup"><span data-stu-id="07876-419">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="07876-420">Access</span><span class="sxs-lookup"><span data-stu-id="07876-420">Access</span></span>         | <span data-ttu-id="07876-421">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-421">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="07876-422">type</span><span class="sxs-lookup"><span data-stu-id="07876-422">Type</span></span>           | <span data-ttu-id="07876-423">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-423">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="07876-424">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-424">Default</span></span>        | <span data-ttu-id="07876-425">Richtig</span><span class="sxs-lookup"><span data-stu-id="07876-425">True</span></span>                                                                                                                        |
| <span data-ttu-id="07876-426">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-426">Minimum system</span></span> | <span data-ttu-id="07876-427">Windows XP</span><span class="sxs-lookup"><span data-stu-id="07876-427">Windows XP</span></span>                                                                                                                  |



 

### <a name="iseventclass"></a><span data-ttu-id="07876-428">Isiebziger Class</span><span class="sxs-lookup"><span data-stu-id="07876-428">IsEventClass</span></span>



| <span data-ttu-id="07876-429">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-429">Entry</span></span> | <span data-ttu-id="07876-430">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-430">Value</span></span> |
|----------------|----------------------------------------------------|
| <span data-ttu-id="07876-431">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-431">Description</span></span>    | <span data-ttu-id="07876-432">Gibt an, ob die Komponente eine Ereignisklasse ist.</span><span class="sxs-lookup"><span data-stu-id="07876-432">Indicates whether the component is an event class.</span></span> |
| <span data-ttu-id="07876-433">Access</span><span class="sxs-lookup"><span data-stu-id="07876-433">Access</span></span>         | <span data-ttu-id="07876-434">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-434">ReadOnly</span></span>                                           |
| <span data-ttu-id="07876-435">type</span><span class="sxs-lookup"><span data-stu-id="07876-435">Type</span></span>           | <span data-ttu-id="07876-436">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-436">Bool</span></span>                                               |
| <span data-ttu-id="07876-437">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-437">Default</span></span>        | <span data-ttu-id="07876-438">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-438">False</span></span>                                              |
| <span data-ttu-id="07876-439">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-439">Minimum system</span></span> | <span data-ttu-id="07876-440">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-440">Windows 2000</span></span>                                       |



 

### <a name="isinstalled"></a><span data-ttu-id="07876-441">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="07876-441">IsInstalled</span></span>



| <span data-ttu-id="07876-442">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-442">Entry</span></span> | <span data-ttu-id="07876-443">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-443">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="07876-444">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-444">Description</span></span>    | <span data-ttu-id="07876-445">Gibt an, ob die Komponente in einer Anwendung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="07876-445">Indicates whether the component is installed in an application.</span></span> |
| <span data-ttu-id="07876-446">Access</span><span class="sxs-lookup"><span data-stu-id="07876-446">Access</span></span>         | <span data-ttu-id="07876-447">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-447">ReadOnly</span></span>                                                        |
| <span data-ttu-id="07876-448">type</span><span class="sxs-lookup"><span data-stu-id="07876-448">Type</span></span>           | <span data-ttu-id="07876-449">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-449">Bool</span></span>                                                            |
| <span data-ttu-id="07876-450">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-450">Default</span></span>        | <span data-ttu-id="07876-451">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-451">False</span></span>                                                           |
| <span data-ttu-id="07876-452">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-452">Minimum system</span></span> | <span data-ttu-id="07876-453">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="07876-453">Windows Server 2003</span></span>                                             |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="07876-454">Isprivatecomponent</span><span class="sxs-lookup"><span data-stu-id="07876-454">IsPrivateComponent</span></span>



| <span data-ttu-id="07876-455">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-455">Entry</span></span> | <span data-ttu-id="07876-456">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-456">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-457">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-457">Description</span></span>    | <span data-ttu-id="07876-458">Bestimmt, ob eine Serveranwendung eine private Komponente ist.</span><span class="sxs-lookup"><span data-stu-id="07876-458">Determines whether a server application is a private component.</span></span> <span data-ttu-id="07876-459">Eine private Komponente in einer Serveranwendung kann nur innerhalb der Anwendung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="07876-459">A private component in a server application can be activated only from within the application.</span></span> <span data-ttu-id="07876-460">Wenn Sie z. b. [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) für eine private Komponente aufrufen, tritt ein Fehler außerhalb des Prozesses auf, aber der Prozess ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="07876-460">For example, if you call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) on a private component, it fails from out-of-process but succeeds in-process.</span></span> <span data-ttu-id="07876-461">Wenn Sie dagegen **cokreateinstance** für eine öffentliche Komponente aufrufen, ist Sie sowohl in-Process als auch außerhalb des Prozesses erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="07876-461">In contrast, if you call **CoCreateInstance** on a public component, it succeeds both in-process and out-of-process.</span></span> |
| <span data-ttu-id="07876-462">Access</span><span class="sxs-lookup"><span data-stu-id="07876-462">Access</span></span>         | <span data-ttu-id="07876-463">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-463">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="07876-464">type</span><span class="sxs-lookup"><span data-stu-id="07876-464">Type</span></span>           | <span data-ttu-id="07876-465">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-465">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="07876-466">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-466">Default</span></span>        | <span data-ttu-id="07876-467">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-467">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="07876-468">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-468">Minimum system</span></span> | <span data-ttu-id="07876-469">Windows XP</span><span class="sxs-lookup"><span data-stu-id="07876-469">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a><span data-ttu-id="07876-470">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="07876-470">JustInTimeActivation</span></span>



| <span data-ttu-id="07876-471">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-471">Entry</span></span> | <span data-ttu-id="07876-472">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-472">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-473">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-473">Description</span></span>    | <span data-ttu-id="07876-474">Bestimmt, ob die [JIT-Aktivierung](enabling-jit-activation-for-a-component.md) für die Komponente aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="07876-474">Determines whether [JIT activation](enabling-jit-activation-for-a-component.md) is enabled for the component.</span></span> <span data-ttu-id="07876-475">Diese Eigenschaft wird auf true festgelegt, wenn die [Transaktionsunterstützung](setting-the-transaction-attribute.md) auf erforderlich festgelegt ist, New oder supported erfordert.</span><span class="sxs-lookup"><span data-stu-id="07876-475">This property is set to True when [transaction support](setting-the-transaction-attribute.md) is set to Required, Requires New, or Supported.</span></span> <span data-ttu-id="07876-476">Wenn JustInTimeActivation auf true festgelegt ist, muss die [Synchronisierungs Unterstützung](setting-the-synchronization-attribute.md) auf Required (Standardeinstellung) festgelegt oder auf New festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="07876-476">When JustInTimeActivation is set to True, [synchronization support](setting-the-synchronization-attribute.md) must be set to Required (the default) or Requires New.</span></span> |
| <span data-ttu-id="07876-477">Access</span><span class="sxs-lookup"><span data-stu-id="07876-477">Access</span></span>         | <span data-ttu-id="07876-478">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-478">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="07876-479">type</span><span class="sxs-lookup"><span data-stu-id="07876-479">Type</span></span>           | <span data-ttu-id="07876-480">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-480">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="07876-481">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-481">Default</span></span>        | <span data-ttu-id="07876-482">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-482">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="07876-483">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-483">Minimum system</span></span> | <span data-ttu-id="07876-484">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-484">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a><span data-ttu-id="07876-485">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="07876-485">LoadBalancingSupported</span></span>



| <span data-ttu-id="07876-486">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-486">Entry</span></span> | <span data-ttu-id="07876-487">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-487">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-488">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-488">Description</span></span>    | <span data-ttu-id="07876-489">Wenn der Komponenten Lastenausgleich-Dienst auf dem Server installiert und aktiviert ist, bestimmt, ob die Komponente am Lastenausgleich beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="07876-489">If the component load balancing service is installed and enabled on the server, determines whether the component participates in load balancing.</span></span> |
| <span data-ttu-id="07876-490">Access</span><span class="sxs-lookup"><span data-stu-id="07876-490">Access</span></span>         | <span data-ttu-id="07876-491">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-491">ReadWrite</span></span>                                                                                                                                        |
| <span data-ttu-id="07876-492">type</span><span class="sxs-lookup"><span data-stu-id="07876-492">Type</span></span>           | <span data-ttu-id="07876-493">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-493">Bool</span></span>                                                                                                                                             |
| <span data-ttu-id="07876-494">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-494">Default</span></span>        | <span data-ttu-id="07876-495">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-495">False</span></span>                                                                                                                                            |
| <span data-ttu-id="07876-496">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-496">Minimum system</span></span> | <span data-ttu-id="07876-497">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-497">Windows 2000</span></span>                                                                                                                                     |



 

### <a name="maxpoolsize"></a><span data-ttu-id="07876-498">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="07876-498">MaxPoolSize</span></span>



| <span data-ttu-id="07876-499">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-499">Entry</span></span> | <span data-ttu-id="07876-500">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-500">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="07876-501">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-501">Description</span></span>    | <span data-ttu-id="07876-502">Maximale Anzahl von Objekten in einem Pool.</span><span class="sxs-lookup"><span data-stu-id="07876-502">Maximum number of objects pooled.</span></span> |
| <span data-ttu-id="07876-503">Access</span><span class="sxs-lookup"><span data-stu-id="07876-503">Access</span></span>         | <span data-ttu-id="07876-504">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-504">ReadWrite</span></span>                         |
| <span data-ttu-id="07876-505">type</span><span class="sxs-lookup"><span data-stu-id="07876-505">Type</span></span>           | <span data-ttu-id="07876-506">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="07876-506">Long (1-1048576)</span></span>                  |
| <span data-ttu-id="07876-507">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-507">Default</span></span>        | <span data-ttu-id="07876-508">1048576</span><span class="sxs-lookup"><span data-stu-id="07876-508">1048576</span></span>                           |
| <span data-ttu-id="07876-509">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-509">Minimum system</span></span> | <span data-ttu-id="07876-510">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-510">Windows 2000</span></span>                      |



 

### <a name="minpoolsize"></a><span data-ttu-id="07876-511">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="07876-511">MinPoolSize</span></span>



| <span data-ttu-id="07876-512">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-512">Entry</span></span> | <span data-ttu-id="07876-513">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-513">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="07876-514">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-514">Description</span></span>    | <span data-ttu-id="07876-515">Minimale Anzahl von Objekten in einem Pool.</span><span class="sxs-lookup"><span data-stu-id="07876-515">Minimum number of objects pooled.</span></span> |
| <span data-ttu-id="07876-516">Access</span><span class="sxs-lookup"><span data-stu-id="07876-516">Access</span></span>         | <span data-ttu-id="07876-517">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-517">ReadWrite</span></span>                         |
| <span data-ttu-id="07876-518">type</span><span class="sxs-lookup"><span data-stu-id="07876-518">Type</span></span>           | <span data-ttu-id="07876-519">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="07876-519">Long (0-1048576)</span></span>                  |
| <span data-ttu-id="07876-520">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-520">Default</span></span>        | <span data-ttu-id="07876-521">0</span><span class="sxs-lookup"><span data-stu-id="07876-521">0</span></span>                                 |
| <span data-ttu-id="07876-522">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-522">Minimum system</span></span> | <span data-ttu-id="07876-523">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-523">Windows 2000</span></span>                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a><span data-ttu-id="07876-524">Multiinterfacepublisherfilterclsid</span><span class="sxs-lookup"><span data-stu-id="07876-524">MultiInterfacePublisherFilterCLSID</span></span>



| <span data-ttu-id="07876-525">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-525">Entry</span></span> | <span data-ttu-id="07876-526">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-526">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="07876-527">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-527">Description</span></span>    | <span data-ttu-id="07876-528">CLSID für den Herausgeber Filter, der verwendet wird, wenn die Komponente eine Ereignisklasse ist.</span><span class="sxs-lookup"><span data-stu-id="07876-528">CLSID for the publisher filter used if the component is an event class.</span></span> |
| <span data-ttu-id="07876-529">Access</span><span class="sxs-lookup"><span data-stu-id="07876-529">Access</span></span>         | <span data-ttu-id="07876-530">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-530">ReadWrite</span></span>                                                               |
| <span data-ttu-id="07876-531">type</span><span class="sxs-lookup"><span data-stu-id="07876-531">Type</span></span>           | <span data-ttu-id="07876-532">String</span><span class="sxs-lookup"><span data-stu-id="07876-532">String</span></span>                                                                  |
| <span data-ttu-id="07876-533">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-533">Default</span></span>        | <span data-ttu-id="07876-534">–</span><span class="sxs-lookup"><span data-stu-id="07876-534">N/A</span></span>                                                                     |
| <span data-ttu-id="07876-535">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-535">Minimum system</span></span> | <span data-ttu-id="07876-536">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-536">Windows 2000</span></span>                                                            |



 

### <a name="mustruninclientcontext"></a><span data-ttu-id="07876-537">Mustrauuninclientcontext</span><span class="sxs-lookup"><span data-stu-id="07876-537">MustRunInClientContext</span></span>



| <span data-ttu-id="07876-538">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-538">Entry</span></span> | <span data-ttu-id="07876-539">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-539">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-540">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-540">Description</span></span>    | <span data-ttu-id="07876-541">Gibt an, dass die Komponente im Kontext des ursprünglichen Aufrufers aktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="07876-541">Indicates that component must be activated in its original caller's context.</span></span> <span data-ttu-id="07876-542">Andernfalls schlägt die Aktivierung fehl.</span><span class="sxs-lookup"><span data-stu-id="07876-542">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="07876-543">Access</span><span class="sxs-lookup"><span data-stu-id="07876-543">Access</span></span>         | <span data-ttu-id="07876-544">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-544">ReadWrite</span></span>                                                                                                 |
| <span data-ttu-id="07876-545">type</span><span class="sxs-lookup"><span data-stu-id="07876-545">Type</span></span>           | <span data-ttu-id="07876-546">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-546">Bool</span></span>                                                                                                      |
| <span data-ttu-id="07876-547">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-547">Default</span></span>        | <span data-ttu-id="07876-548">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-548">False</span></span>                                                                                                     |
| <span data-ttu-id="07876-549">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-549">Minimum system</span></span> | <span data-ttu-id="07876-550">Windows XP</span><span class="sxs-lookup"><span data-stu-id="07876-550">Windows XP</span></span>                                                                                                |



 

### <a name="mustrunindefaultcontext"></a><span data-ttu-id="07876-551">Mustranunindefehlercontext</span><span class="sxs-lookup"><span data-stu-id="07876-551">MustRunInDefaultContext</span></span>



| <span data-ttu-id="07876-552">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-552">Entry</span></span> | <span data-ttu-id="07876-553">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-553">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-554">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-554">Description</span></span>    | <span data-ttu-id="07876-555">Gibt an, dass die Komponente im Kontext des Standard Aufrufers aktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="07876-555">Indicates that the component must be activated in the default caller's context.</span></span> <span data-ttu-id="07876-556">Andernfalls schlägt die Aktivierung fehl.</span><span class="sxs-lookup"><span data-stu-id="07876-556">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="07876-557">Access</span><span class="sxs-lookup"><span data-stu-id="07876-557">Access</span></span>         | <span data-ttu-id="07876-558">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-558">ReadWrite</span></span>                                                                                                    |
| <span data-ttu-id="07876-559">type</span><span class="sxs-lookup"><span data-stu-id="07876-559">Type</span></span>           | <span data-ttu-id="07876-560">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-560">Bool</span></span>                                                                                                         |
| <span data-ttu-id="07876-561">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-561">Default</span></span>        | <span data-ttu-id="07876-562">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-562">False</span></span>                                                                                                        |
| <span data-ttu-id="07876-563">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-563">Minimum system</span></span> | <span data-ttu-id="07876-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-564">Windows 2000</span></span>                                                                                                 |



 

### <a name="objectpoolingenabled"></a><span data-ttu-id="07876-565">Objectpoolingenabled</span><span class="sxs-lookup"><span data-stu-id="07876-565">ObjectPoolingEnabled</span></span>



| <span data-ttu-id="07876-566">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-566">Entry</span></span> | <span data-ttu-id="07876-567">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-567">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-568">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-568">Description</span></span>    | <span data-ttu-id="07876-569">Bestimmt, ob das [com+-Objekt Pooling](com--object-pooling.md) für die Komponente aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="07876-569">Determines whether [COM+ object pooling](com--object-pooling.md) is enabled for the component.</span></span> |
| <span data-ttu-id="07876-570">Access</span><span class="sxs-lookup"><span data-stu-id="07876-570">Access</span></span>         | <span data-ttu-id="07876-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-571">ReadWrite</span></span>                                                                                       |
| <span data-ttu-id="07876-572">type</span><span class="sxs-lookup"><span data-stu-id="07876-572">Type</span></span>           | <span data-ttu-id="07876-573">Bool</span><span class="sxs-lookup"><span data-stu-id="07876-573">Bool</span></span>                                                                                            |
| <span data-ttu-id="07876-574">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-574">Default</span></span>        | <span data-ttu-id="07876-575">Falsch</span><span class="sxs-lookup"><span data-stu-id="07876-575">False</span></span>                                                                                           |
| <span data-ttu-id="07876-576">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-576">Minimum system</span></span> | <span data-ttu-id="07876-577">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-577">Windows 2000</span></span>                                                                                    |



 

### <a name="progid"></a><span data-ttu-id="07876-578">ProgID</span><span class="sxs-lookup"><span data-stu-id="07876-578">ProgID</span></span>



| <span data-ttu-id="07876-579">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-579">Entry</span></span> | <span data-ttu-id="07876-580">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-580">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-581">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-581">Description</span></span>    | <span data-ttu-id="07876-582">Ein Anzeige Name, der zum Identifizieren der Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07876-582">A friendly name used for identifying the component.</span></span> <span data-ttu-id="07876-583">Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="07876-583">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="07876-584">Access</span><span class="sxs-lookup"><span data-stu-id="07876-584">Access</span></span>         | <span data-ttu-id="07876-585">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-585">ReadOnly</span></span>                                                                                                                                                                              |
| <span data-ttu-id="07876-586">type</span><span class="sxs-lookup"><span data-stu-id="07876-586">Type</span></span>           | <span data-ttu-id="07876-587">String</span><span class="sxs-lookup"><span data-stu-id="07876-587">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="07876-588">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-588">Default</span></span>        | <span data-ttu-id="07876-589">–</span><span class="sxs-lookup"><span data-stu-id="07876-589">N/A</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="07876-590">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-590">Minimum system</span></span> | <span data-ttu-id="07876-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-591">Windows 2000</span></span>                                                                                                                                                                          |



 

### <a name="publisherid"></a><span data-ttu-id="07876-592">PublisherID</span><span class="sxs-lookup"><span data-stu-id="07876-592">PublisherID</span></span>



| <span data-ttu-id="07876-593">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-593">Entry</span></span> | <span data-ttu-id="07876-594">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-594">Value</span></span> |
|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="07876-595">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-595">Description</span></span>    | <span data-ttu-id="07876-596">Der Bezeichner für den Ereignis Herausgeber, wenn die Komponente eine Ereignisklasse ist.</span><span class="sxs-lookup"><span data-stu-id="07876-596">Identifier for the event publisher if the component is an event class.</span></span> |
| <span data-ttu-id="07876-597">Access</span><span class="sxs-lookup"><span data-stu-id="07876-597">Access</span></span>         | <span data-ttu-id="07876-598">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-598">ReadWrite</span></span>                                                              |
| <span data-ttu-id="07876-599">type</span><span class="sxs-lookup"><span data-stu-id="07876-599">Type</span></span>           | <span data-ttu-id="07876-600">String</span><span class="sxs-lookup"><span data-stu-id="07876-600">String</span></span>                                                                 |
| <span data-ttu-id="07876-601">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-601">Default</span></span>        | <span data-ttu-id="07876-602">""</span><span class="sxs-lookup"><span data-stu-id="07876-602">""</span></span>                                                                     |
| <span data-ttu-id="07876-603">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-603">Minimum system</span></span> | <span data-ttu-id="07876-604">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-604">Windows 2000</span></span>                                                           |



 

### <a name="soapassemblyname"></a><span data-ttu-id="07876-605">Soapassemblyname</span><span class="sxs-lookup"><span data-stu-id="07876-605">SoapAssemblyName</span></span>



| <span data-ttu-id="07876-606">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-606">Entry</span></span> | <span data-ttu-id="07876-607">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-607">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-608">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-608">Description</span></span>    | <span data-ttu-id="07876-609">Eine GUID, die die GAC-Assembly identifiziert, die ausgeführt wird, wenn die Komponente als SOAP-Dienst aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="07876-609">A GUID identifying the GAC assembly that is run when the component is invoked as a SOAP service.</span></span> |
| <span data-ttu-id="07876-610">Access</span><span class="sxs-lookup"><span data-stu-id="07876-610">Access</span></span>         | <span data-ttu-id="07876-611">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-611">ReadWrite</span></span>                                                                                        |
| <span data-ttu-id="07876-612">type</span><span class="sxs-lookup"><span data-stu-id="07876-612">Type</span></span>           | <span data-ttu-id="07876-613">String</span><span class="sxs-lookup"><span data-stu-id="07876-613">String</span></span>                                                                                           |
| <span data-ttu-id="07876-614">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-614">Default</span></span>        | <span data-ttu-id="07876-615">NULL</span><span class="sxs-lookup"><span data-stu-id="07876-615">NULL</span></span>                                                                                             |
| <span data-ttu-id="07876-616">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-616">Minimum system</span></span> | <span data-ttu-id="07876-617">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="07876-617">Windows Server 2003</span></span>                                                                              |



 

### <a name="soaptypename"></a><span data-ttu-id="07876-618">Soaptyname</span><span class="sxs-lookup"><span data-stu-id="07876-618">SoapTypeName</span></span>



| <span data-ttu-id="07876-619">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-619">Entry</span></span> | <span data-ttu-id="07876-620">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-620">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="07876-621">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-621">Description</span></span>    | <span data-ttu-id="07876-622">Der verwaltete Typname für eine Komponente, die als SOAP-Dienst aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="07876-622">The managed type name for a component that can be invoked as a SOAP service.</span></span> |
| <span data-ttu-id="07876-623">Access</span><span class="sxs-lookup"><span data-stu-id="07876-623">Access</span></span>         | <span data-ttu-id="07876-624">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-624">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="07876-625">type</span><span class="sxs-lookup"><span data-stu-id="07876-625">Type</span></span>           | <span data-ttu-id="07876-626">String</span><span class="sxs-lookup"><span data-stu-id="07876-626">String</span></span>                                                                       |
| <span data-ttu-id="07876-627">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-627">Default</span></span>        | <span data-ttu-id="07876-628">NULL</span><span class="sxs-lookup"><span data-stu-id="07876-628">NULL</span></span>                                                                         |
| <span data-ttu-id="07876-629">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-629">Minimum system</span></span> | <span data-ttu-id="07876-630">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="07876-630">Windows Server 2003</span></span>                                                          |



 

### <a name="synchronization"></a><span data-ttu-id="07876-631">Synchronization</span><span class="sxs-lookup"><span data-stu-id="07876-631">Synchronization</span></span>



| <span data-ttu-id="07876-632">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-632">Entry</span></span> | <span data-ttu-id="07876-633">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-633">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-634">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-634">Description</span></span>    | <span data-ttu-id="07876-635">Bestimmt die Rückruf [Synchronisierung](setting-the-synchronization-attribute.md) für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="07876-635">Determines call [synchronization](setting-the-synchronization-attribute.md) for the component.</span></span>                                                                                                     |
| <span data-ttu-id="07876-636">Access</span><span class="sxs-lookup"><span data-stu-id="07876-636">Access</span></span>         | <span data-ttu-id="07876-637">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-637">ReadWrite</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="07876-638">type</span><span class="sxs-lookup"><span data-stu-id="07876-638">Type</span></span>           | <span data-ttu-id="07876-639">Lange mögliche Werte: comadminsynchronizationignorierte (0) comadminsynchronizationnone (1) comadminsynchronizationsupported (2) comadminsynchronizationrequired (3) comadminsynchronizationrequirements (4)</span><span class="sxs-lookup"><span data-stu-id="07876-639">Long Possible values:COMAdminSynchronizationIgnored (0)COMAdminSynchronizationNone (1)COMAdminSynchronizationSupported (2)COMAdminSynchronizationRequired (3)COMAdminSynchronizationRequiresNew (4)</span></span> |
| <span data-ttu-id="07876-640">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-640">Default</span></span>        | <span data-ttu-id="07876-641">Comadminsynchronizationignoriignoriert (0)</span><span class="sxs-lookup"><span data-stu-id="07876-641">COMAdminSynchronizationIgnored (0)</span></span>                                                                                                                                                                  |
| <span data-ttu-id="07876-642">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-642">Minimum system</span></span> | <span data-ttu-id="07876-643">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-643">Windows 2000</span></span>                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a><span data-ttu-id="07876-644">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="07876-644">ThreadingModel</span></span>



| <span data-ttu-id="07876-645">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-645">Entry</span></span> | <span data-ttu-id="07876-646">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-646">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-647">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-647">Description</span></span>    | <span data-ttu-id="07876-648">Bestimmt, wie Instanzen der Komponente Threads zur Methoden Ausführung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="07876-648">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="07876-649">Werte entsprechen com-Threading Modellen.</span><span class="sxs-lookup"><span data-stu-id="07876-649">Values correspond to COM threading models.</span></span>                                                                                        |
| <span data-ttu-id="07876-650">Access</span><span class="sxs-lookup"><span data-stu-id="07876-650">Access</span></span>         | <span data-ttu-id="07876-651">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-651">ReadOnly</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="07876-652">type</span><span class="sxs-lookup"><span data-stu-id="07876-652">Type</span></span>           | <span data-ttu-id="07876-653">Lange mögliche Werte: comadminthreadingmodelapartment (0) comadminthreadingmodelfree (1) comadminthreadingmodelmain (2) comadminthreadingmodelboth (3) comadminthreadingmodelneutral (4) comadminthreadingmodelnotangegeben (5)</span><span class="sxs-lookup"><span data-stu-id="07876-653">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)COMAdminThreadingModelNotSpecified (5)</span></span> |
| <span data-ttu-id="07876-654">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-654">Default</span></span>        | <span data-ttu-id="07876-655">–</span><span class="sxs-lookup"><span data-stu-id="07876-655">N/A</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="07876-656">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-656">Minimum system</span></span> | <span data-ttu-id="07876-657">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-657">Windows 2000</span></span>                                                                                                                                                                                                              |



 

### <a name="transaction"></a><span data-ttu-id="07876-658">Transaktion</span><span class="sxs-lookup"><span data-stu-id="07876-658">Transaction</span></span>



| <span data-ttu-id="07876-659">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-659">Entry</span></span> | <span data-ttu-id="07876-660">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-660">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-661">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-661">Description</span></span>    | <span data-ttu-id="07876-662">Bestimmt, wie eine Komponente [Transaktionen](setting-the-transaction-attribute.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="07876-662">Determines how a component supports [transactions](setting-the-transaction-attribute.md).</span></span> <span data-ttu-id="07876-663">Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="07876-663">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="07876-664">Access</span><span class="sxs-lookup"><span data-stu-id="07876-664">Access</span></span>         | <span data-ttu-id="07876-665">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-665">ReadWrite</span></span>                                                                                                                                                                              |
| <span data-ttu-id="07876-666">type</span><span class="sxs-lookup"><span data-stu-id="07876-666">Type</span></span>           | <span data-ttu-id="07876-667">Lange mögliche Werte: comadmintransaktionignorierte (0) comadmintransaktionsnone (1) comadmintransaktionssupported (2) comadmintransaktionrequired (2) comadmintransaktionrequirements (3) comadmintransaktiongsnew (4)</span><span class="sxs-lookup"><span data-stu-id="07876-667">Long Possible values:COMAdminTransactionIgnored (0)COMAdminTransactionNone (1)COMAdminTransactionSupported (2)COMAdminTransactionRequired (3)COMAdminTransactionRequiresNew (4)</span></span>        |
| <span data-ttu-id="07876-668">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-668">Default</span></span>        | <span data-ttu-id="07876-669">Comadmintransaktionnone (1)</span><span class="sxs-lookup"><span data-stu-id="07876-669">COMAdminTransactionNone (1)</span></span>                                                                                                                                                            |
| <span data-ttu-id="07876-670">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-670">Minimum system</span></span> | <span data-ttu-id="07876-671">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-671">Windows 2000</span></span>                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a><span data-ttu-id="07876-672">Txisolationlevel</span><span class="sxs-lookup"><span data-stu-id="07876-672">TxIsolationLevel</span></span>



| <span data-ttu-id="07876-673">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-673">Entry</span></span> | <span data-ttu-id="07876-674">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-674">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-675">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-675">Description</span></span>    | <span data-ttu-id="07876-676">Gibt die Transaktions Isolations Stufen an.</span><span class="sxs-lookup"><span data-stu-id="07876-676">Indicates the transaction isolation levels.</span></span> <span data-ttu-id="07876-677">Es gibt fünf Isolations Stufen: None, Read uncommit, Read Commit, Repeatable Read und serialized.</span><span class="sxs-lookup"><span data-stu-id="07876-677">There are five isolation levels: none, read uncommitted, read committed, repeatable read, and serialized.</span></span> <span data-ttu-id="07876-678">Die Standard Isolationsstufe wird serialisiert.</span><span class="sxs-lookup"><span data-stu-id="07876-678">The default isolation level is serialized.</span></span>                           |
| <span data-ttu-id="07876-679">Access</span><span class="sxs-lookup"><span data-stu-id="07876-679">Access</span></span>         | <span data-ttu-id="07876-680">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07876-680">ReadWrite</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="07876-681">type</span><span class="sxs-lookup"><span data-stu-id="07876-681">Type</span></span>           | <span data-ttu-id="07876-682">Lange mögliche Werte: comadmintxisolationlevelany (0) comadmintxisolationlevelleuncommit (1) comadmintxisolationlevellecommit (2) comadmintxisolationlevelrepeatableread (3) comadmintxisolationlevelserialisierbar (4)</span><span class="sxs-lookup"><span data-stu-id="07876-682">Long Possible values:COMAdminTxIsolationLevelAny (0)COMAdminTxIsolationLevelReadUnCommitted (1)COMAdminTxIsolationLevelReadCommitted (2)COMAdminTxIsolationLevelRepeatableRead (3)COMAdminTxIsolationLevelSerializable (4)</span></span> |
| <span data-ttu-id="07876-683">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-683">Default</span></span>        | <span data-ttu-id="07876-684">Comadmintxisolationlevelserialisierbar (4)</span><span class="sxs-lookup"><span data-stu-id="07876-684">COMAdminTxIsolationLevelSerializable (4)</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="07876-685">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-685">Minimum system</span></span> | <span data-ttu-id="07876-686">Windows XP</span><span class="sxs-lookup"><span data-stu-id="07876-686">Windows XP</span></span>                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a><span data-ttu-id="07876-687">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="07876-687">VersionBuild</span></span>



| <span data-ttu-id="07876-688">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-688">Entry</span></span> | <span data-ttu-id="07876-689">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-689">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="07876-690">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-690">Description</span></span>    | <span data-ttu-id="07876-691">Buildbezeichner der Version.</span><span class="sxs-lookup"><span data-stu-id="07876-691">Version build identifier.</span></span> |
| <span data-ttu-id="07876-692">Access</span><span class="sxs-lookup"><span data-stu-id="07876-692">Access</span></span>         | <span data-ttu-id="07876-693">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-693">ReadOnly</span></span>                  |
| <span data-ttu-id="07876-694">type</span><span class="sxs-lookup"><span data-stu-id="07876-694">Type</span></span>           | <span data-ttu-id="07876-695">String</span><span class="sxs-lookup"><span data-stu-id="07876-695">String</span></span>                    |
| <span data-ttu-id="07876-696">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-696">Default</span></span>        | <span data-ttu-id="07876-697">""</span><span class="sxs-lookup"><span data-stu-id="07876-697">""</span></span>                        |
| <span data-ttu-id="07876-698">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-698">Minimum system</span></span> | <span data-ttu-id="07876-699">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-699">Windows 2000</span></span>              |



 

### <a name="versionmajor"></a><span data-ttu-id="07876-700">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="07876-700">VersionMajor</span></span>



| <span data-ttu-id="07876-701">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-701">Entry</span></span> | <span data-ttu-id="07876-702">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-702">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="07876-703">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-703">Description</span></span>    | <span data-ttu-id="07876-704">Versions Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="07876-704">Version identifier.</span></span> |
| <span data-ttu-id="07876-705">Access</span><span class="sxs-lookup"><span data-stu-id="07876-705">Access</span></span>         | <span data-ttu-id="07876-706">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-706">ReadOnly</span></span>            |
| <span data-ttu-id="07876-707">type</span><span class="sxs-lookup"><span data-stu-id="07876-707">Type</span></span>           | <span data-ttu-id="07876-708">String</span><span class="sxs-lookup"><span data-stu-id="07876-708">String</span></span>              |
| <span data-ttu-id="07876-709">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-709">Default</span></span>        | <span data-ttu-id="07876-710">""</span><span class="sxs-lookup"><span data-stu-id="07876-710">""</span></span>                  |
| <span data-ttu-id="07876-711">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-711">Minimum system</span></span> | <span data-ttu-id="07876-712">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-712">Windows 2000</span></span>        |



 

### <a name="versionminor"></a><span data-ttu-id="07876-713">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="07876-713">VersionMinor</span></span>



| <span data-ttu-id="07876-714">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-714">Entry</span></span> | <span data-ttu-id="07876-715">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-715">Value</span></span> |
|----------------|-------------------------|
| <span data-ttu-id="07876-716">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-716">Description</span></span>    | <span data-ttu-id="07876-717">Versions Unterzeichner.</span><span class="sxs-lookup"><span data-stu-id="07876-717">Version sub-identifier.</span></span> |
| <span data-ttu-id="07876-718">Access</span><span class="sxs-lookup"><span data-stu-id="07876-718">Access</span></span>         | <span data-ttu-id="07876-719">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-719">ReadOnly</span></span>                |
| <span data-ttu-id="07876-720">type</span><span class="sxs-lookup"><span data-stu-id="07876-720">Type</span></span>           | <span data-ttu-id="07876-721">String</span><span class="sxs-lookup"><span data-stu-id="07876-721">String</span></span>                  |
| <span data-ttu-id="07876-722">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-722">Default</span></span>        | <span data-ttu-id="07876-723">""</span><span class="sxs-lookup"><span data-stu-id="07876-723">""</span></span>                      |
| <span data-ttu-id="07876-724">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-724">Minimum system</span></span> | <span data-ttu-id="07876-725">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-725">Windows 2000</span></span>            |



 

### <a name="versionsubbuild"></a><span data-ttu-id="07876-726">Versionsubbuild</span><span class="sxs-lookup"><span data-stu-id="07876-726">VersionSubBuild</span></span>



| <span data-ttu-id="07876-727">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07876-727">Entry</span></span> | <span data-ttu-id="07876-728">Wert</span><span class="sxs-lookup"><span data-stu-id="07876-728">Value</span></span> |
|----------------|-------------------------------|
| <span data-ttu-id="07876-729">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07876-729">Description</span></span>    | <span data-ttu-id="07876-730">Versionssubbuildbezeichner.</span><span class="sxs-lookup"><span data-stu-id="07876-730">Version sub-build identifier.</span></span> |
| <span data-ttu-id="07876-731">Access</span><span class="sxs-lookup"><span data-stu-id="07876-731">Access</span></span>         | <span data-ttu-id="07876-732">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="07876-732">ReadOnly</span></span>                      |
| <span data-ttu-id="07876-733">type</span><span class="sxs-lookup"><span data-stu-id="07876-733">Type</span></span>           | <span data-ttu-id="07876-734">String</span><span class="sxs-lookup"><span data-stu-id="07876-734">String</span></span>                        |
| <span data-ttu-id="07876-735">Standard</span><span class="sxs-lookup"><span data-stu-id="07876-735">Default</span></span>        | <span data-ttu-id="07876-736">""</span><span class="sxs-lookup"><span data-stu-id="07876-736">""</span></span>                            |
| <span data-ttu-id="07876-737">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="07876-737">Minimum system</span></span> | <span data-ttu-id="07876-738">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07876-738">Windows 2000</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="07876-739">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07876-739">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07876-740">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="07876-740">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
