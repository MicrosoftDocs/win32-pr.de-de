---
description: Enthält ein-Objekt für jede nicht konfigurierte Komponente in der Anwendungs Auflistung. Nicht konfigurierte Komponenten können die com+-Dienste nicht verwenden. Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, halten Einstellungen auf Komponentenebene.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Legacycomponents-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748176"
---
# <a name="legacycomponents-collection"></a><span data-ttu-id="3e5d8-105">Legacycomponents-Sammlung</span><span class="sxs-lookup"><span data-stu-id="3e5d8-105">LegacyComponents collection</span></span>

<span data-ttu-id="3e5d8-106">Enthält ein-Objekt für jede nicht konfigurierte Komponente in der Anwendungs Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-106">Contains an object for each unconfigured component in the Applications collection.</span></span> <span data-ttu-id="3e5d8-107">Nicht konfigurierte Komponenten können die com+-Dienste nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-107">Unconfigured components cannot make use of COM+ services.</span></span> <span data-ttu-id="3e5d8-108">Die Eigenschaften, die von diesen Objekten verfügbar gemacht werden, halten Einstellungen auf Komponentenebene.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-108">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="3e5d8-109">Diese Auflistung unterstützt die [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts, jedoch nicht die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-109">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="3e5d8-110">Verwenden Sie Methoden für das [**comadmincatalog**](comadmincatalog.md) -Objekt, um Komponenten in einer Anwendung zu installieren oder zu importieren.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-110">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="3e5d8-111">Member</span><span class="sxs-lookup"><span data-stu-id="3e5d8-111">Members</span></span>

<span data-ttu-id="3e5d8-112">Die **legacycomponents** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-112">The **LegacyComponents** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="3e5d8-113">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="3e5d8-113">Related Collections</span></span>

<span data-ttu-id="3e5d8-114">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="3e5d8-114">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="3e5d8-115">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="3e5d8-115">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="3e5d8-116">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="3e5d8-116">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="3e5d8-117">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="3e5d8-117">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="3e5d8-118">Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:</span><span class="sxs-lookup"><span data-stu-id="3e5d8-118">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="3e5d8-119">**Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="3e5d8-119">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="3e5d8-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e5d8-120">Properties</span></span>

<span data-ttu-id="3e5d8-121">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3e5d8-121">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="3e5d8-122">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="3e5d8-122">AccessPermissions</span></span>](#accesspermissions)
-   [<span data-ttu-id="3e5d8-123">Activateatstorage</span><span class="sxs-lookup"><span data-stu-id="3e5d8-123">ActivateAtStorage</span></span>](#activateatstorage)
-   [<span data-ttu-id="3e5d8-124">AppID</span><span class="sxs-lookup"><span data-stu-id="3e5d8-124">AppID</span></span>](#appid)
-   [<span data-ttu-id="3e5d8-125">AppName</span><span class="sxs-lookup"><span data-stu-id="3e5d8-125">AppName</span></span>](#appname)
-   [<span data-ttu-id="3e5d8-126">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="3e5d8-126">AuthenticationLevel</span></span>](#authenticationlevel)
-   [<span data-ttu-id="3e5d8-127">Bitness</span><span class="sxs-lookup"><span data-stu-id="3e5d8-127">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="3e5d8-128">ClassName</span><span class="sxs-lookup"><span data-stu-id="3e5d8-128">ClassName</span></span>](#classname)
-   [<span data-ttu-id="3e5d8-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="3e5d8-129">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="3e5d8-130">Dllersatz</span><span class="sxs-lookup"><span data-stu-id="3e5d8-130">DllSurrogate</span></span>](#dllsurrogate)
-   [<span data-ttu-id="3e5d8-131">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="3e5d8-131">InprocHandler32</span></span>](#inprochandler32)
-   [<span data-ttu-id="3e5d8-132">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="3e5d8-132">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="3e5d8-133">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="3e5d8-133">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="3e5d8-134">Launchberechtigungen</span><span class="sxs-lookup"><span data-stu-id="3e5d8-134">LaunchPermissions</span></span>](#launchpermissions)
-   [<span data-ttu-id="3e5d8-135">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="3e5d8-135">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="3e5d8-136">LocalService</span><span class="sxs-lookup"><span data-stu-id="3e5d8-136">LocalService</span></span>](#localservice)
-   [<span data-ttu-id="3e5d8-137">Kennwort</span><span class="sxs-lookup"><span data-stu-id="3e5d8-137">Password</span></span>](#password)
-   [<span data-ttu-id="3e5d8-138">ProgID</span><span class="sxs-lookup"><span data-stu-id="3e5d8-138">ProgID</span></span>](#progid)
-   [<span data-ttu-id="3e5d8-139">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="3e5d8-139">RemoteServer</span></span>](#remoteserver)
-   [<span data-ttu-id="3e5d8-140">RunAs</span><span class="sxs-lookup"><span data-stu-id="3e5d8-140">RunAs</span></span>](#runas)
-   [<span data-ttu-id="3e5d8-141">Service Parameter</span><span class="sxs-lookup"><span data-stu-id="3e5d8-141">ServiceParameter</span></span>](#serviceparameter)
-   [<span data-ttu-id="3e5d8-142">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="3e5d8-142">SRPTrustLevel</span></span>](#srptrustlevel)
-   [<span data-ttu-id="3e5d8-143">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="3e5d8-143">ThreadingModel</span></span>](#threadingmodel)

### <a name="accesspermissions"></a><span data-ttu-id="3e5d8-144">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="3e5d8-144">AccessPermissions</span></span>



| <span data-ttu-id="3e5d8-145">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-145">Entry</span></span> | <span data-ttu-id="3e5d8-146">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-146">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-147">Description</span></span>    | <span data-ttu-id="3e5d8-148">Gibt die Benutzerkonten an, denen der Zugriff auf die Komponente gestattet oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-148">Specifies the user accounts that are allowed or denied access to the component.</span></span> |
| <span data-ttu-id="3e5d8-149">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-149">Access</span></span>         | <span data-ttu-id="3e5d8-150">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-150">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="3e5d8-151">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-151">Type</span></span>           | <span data-ttu-id="3e5d8-152">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-152">String</span></span>                                                                          |
| <span data-ttu-id="3e5d8-153">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-153">Default</span></span>        | <span data-ttu-id="3e5d8-154">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-154">N/A</span></span>                                                                             |
| <span data-ttu-id="3e5d8-155">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-155">Minimum system</span></span> | <span data-ttu-id="3e5d8-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-156">Windows XP</span></span>                                                                      |



 

### <a name="activateatstorage"></a><span data-ttu-id="3e5d8-157">Activateatstorage</span><span class="sxs-lookup"><span data-stu-id="3e5d8-157">ActivateAtStorage</span></span>



| <span data-ttu-id="3e5d8-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-158">Entry</span></span> | <span data-ttu-id="3e5d8-159">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-159">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-160">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-160">Description</span></span>    | <span data-ttu-id="3e5d8-161">Gibt an, ob der Server auf dem Datenspeicher Computer ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-161">Specifies whether to run the server on the data storage machine.</span></span> |
| <span data-ttu-id="3e5d8-162">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-162">Access</span></span>         | <span data-ttu-id="3e5d8-163">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-163">ReadWrite</span></span>                                                        |
| <span data-ttu-id="3e5d8-164">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-164">Type</span></span>           | <span data-ttu-id="3e5d8-165">Mögliche Zeichen folgen Werte: "N" "Y"</span><span class="sxs-lookup"><span data-stu-id="3e5d8-165">String Possible values:"N""Y"</span></span>                                    |
| <span data-ttu-id="3e5d8-166">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-166">Default</span></span>        | <span data-ttu-id="3e5d8-167">"N"</span><span class="sxs-lookup"><span data-stu-id="3e5d8-167">"N"</span></span>                                                              |
| <span data-ttu-id="3e5d8-168">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-168">Minimum system</span></span> | <span data-ttu-id="3e5d8-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-169">Windows XP</span></span>                                                       |



 

### <a name="appid"></a><span data-ttu-id="3e5d8-170">AppID</span><span class="sxs-lookup"><span data-stu-id="3e5d8-170">AppID</span></span>



| <span data-ttu-id="3e5d8-171">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-171">Entry</span></span> | <span data-ttu-id="3e5d8-172">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-172">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="3e5d8-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-173">Description</span></span>    | <span data-ttu-id="3e5d8-174">Die Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-174">The application ID.</span></span> |
| <span data-ttu-id="3e5d8-175">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-175">Access</span></span>         | <span data-ttu-id="3e5d8-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e5d8-176">ReadOnly</span></span>            |
| <span data-ttu-id="3e5d8-177">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-177">Type</span></span>           | <span data-ttu-id="3e5d8-178">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-178">String</span></span>              |
| <span data-ttu-id="3e5d8-179">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-179">Default</span></span>        | <span data-ttu-id="3e5d8-180">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-180">N/A</span></span>                 |
| <span data-ttu-id="3e5d8-181">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-181">Minimum system</span></span> | <span data-ttu-id="3e5d8-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-182">Windows XP</span></span>          |



 

### <a name="appname"></a><span data-ttu-id="3e5d8-183">AppName</span><span class="sxs-lookup"><span data-stu-id="3e5d8-183">AppName</span></span>



| <span data-ttu-id="3e5d8-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-184">Entry</span></span> | <span data-ttu-id="3e5d8-185">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-185">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="3e5d8-186">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-186">Description</span></span>    | <span data-ttu-id="3e5d8-187">Der Namen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-187">The name of the application.</span></span> |
| <span data-ttu-id="3e5d8-188">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-188">Access</span></span>         | <span data-ttu-id="3e5d8-189">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e5d8-189">ReadOnly</span></span>                     |
| <span data-ttu-id="3e5d8-190">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-190">Type</span></span>           | <span data-ttu-id="3e5d8-191">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-191">String</span></span>                       |
| <span data-ttu-id="3e5d8-192">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-192">Default</span></span>        | <span data-ttu-id="3e5d8-193">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-193">N/A</span></span>                          |
| <span data-ttu-id="3e5d8-194">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-194">Minimum system</span></span> | <span data-ttu-id="3e5d8-195">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-195">Windows XP</span></span>                   |



 

### <a name="authenticationlevel"></a><span data-ttu-id="3e5d8-196">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="3e5d8-196">AuthenticationLevel</span></span>



| <span data-ttu-id="3e5d8-197">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-197">Entry</span></span> | <span data-ttu-id="3e5d8-198">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-198">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-199">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-199">Description</span></span>    | <span data-ttu-id="3e5d8-200">Legt die Authentifizierungs Ebene für Aufrufe fest, wobei die Werte den RPC-Authentifizierungs Einstellungen (Remote Procedure Calls) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-200">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="3e5d8-201">Wenn comadminauthenticationdefault ausgewählt wird, wird die Einstellung in der DefaultAuthenticationLevel-Eigenschaft in der [**LocalComputer**](localcomputer.md) -Sammlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-201">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="3e5d8-202">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-202">Access</span></span>         | <span data-ttu-id="3e5d8-203">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-203">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3e5d8-204">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-204">Type</span></span>           | <span data-ttu-id="3e5d8-205">Lange mögliche Werte: comadminauthenticationdefault (0) comadminauthenticationnone (1) comadminauthenticationconnect (2) comadminauthentication-Aufruf (3) comadminauthenticationpacket (4) comadminauthenticationintegrity (5) comadminauthenticationprivacy (6)</span><span class="sxs-lookup"><span data-stu-id="3e5d8-205">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="3e5d8-206">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-206">Default</span></span>        | <span data-ttu-id="3e5d8-207">Comadminauthenticationdefault (0)</span><span class="sxs-lookup"><span data-stu-id="3e5d8-207">COMAdminAuthenticationDefault (0)</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3e5d8-208">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-208">Minimum system</span></span> | <span data-ttu-id="3e5d8-209">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-209">Windows XP</span></span>                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> <span data-ttu-id="3e5d8-210">Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-210">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="bitness"></a><span data-ttu-id="3e5d8-211">Bitness</span><span class="sxs-lookup"><span data-stu-id="3e5d8-211">Bitness</span></span>



| <span data-ttu-id="3e5d8-212">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-212">Entry</span></span> | <span data-ttu-id="3e5d8-213">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-213">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-214">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-214">Description</span></span>    | <span data-ttu-id="3e5d8-215">Stellt den binären bikretness-Typ der Komponente dar.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-215">Represents the binary bitness type of the component.</span></span> <span data-ttu-id="3e5d8-216">Auf Systemen, die 64-Bit-Windows verwenden, unterscheidet diese Eigenschaft zwischen 64-Bit-Komponenten und 32-Bit-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-216">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="3e5d8-217">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-217">Access</span></span>         | <span data-ttu-id="3e5d8-218">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e5d8-218">ReadOnly</span></span>                                                                                                                                                              |
| <span data-ttu-id="3e5d8-219">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-219">Type</span></span>           | <span data-ttu-id="3e5d8-220">Lange mögliche Werte: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="3e5d8-220">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                         |
| <span data-ttu-id="3e5d8-221">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-221">Default</span></span>        | <span data-ttu-id="3e5d8-222">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-222">N/A</span></span>                                                                                                                                                                   |
| <span data-ttu-id="3e5d8-223">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-223">Minimum system</span></span> | <span data-ttu-id="3e5d8-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-224">Windows XP</span></span>                                                                                                                                                            |



 

### <a name="classname"></a><span data-ttu-id="3e5d8-225">ClassName</span><span class="sxs-lookup"><span data-stu-id="3e5d8-225">ClassName</span></span>



| <span data-ttu-id="3e5d8-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-226">Entry</span></span> | <span data-ttu-id="3e5d8-227">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-227">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="3e5d8-228">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-228">Description</span></span>    | <span data-ttu-id="3e5d8-229">Der Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-229">The name of the class.</span></span> |
| <span data-ttu-id="3e5d8-230">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-230">Access</span></span>         | <span data-ttu-id="3e5d8-231">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e5d8-231">ReadOnly</span></span>               |
| <span data-ttu-id="3e5d8-232">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-232">Type</span></span>           | <span data-ttu-id="3e5d8-233">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-233">String</span></span>                 |
| <span data-ttu-id="3e5d8-234">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-234">Default</span></span>        | <span data-ttu-id="3e5d8-235">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-235">N/A</span></span>                    |
| <span data-ttu-id="3e5d8-236">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-236">Minimum system</span></span> | <span data-ttu-id="3e5d8-237">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-237">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="3e5d8-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="3e5d8-238">CLSID</span></span>



| <span data-ttu-id="3e5d8-239">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-239">Entry</span></span> | <span data-ttu-id="3e5d8-240">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-240">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-241">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-241">Description</span></span>    | <span data-ttu-id="3e5d8-242">Eine GUID für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-242">A GUID for the component.</span></span> <span data-ttu-id="3e5d8-243">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-243">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3e5d8-244">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-244">Access</span></span>         | <span data-ttu-id="3e5d8-245">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e5d8-245">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="3e5d8-246">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-246">Type</span></span>           | <span data-ttu-id="3e5d8-247">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-247">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="3e5d8-248">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-248">Default</span></span>        | <span data-ttu-id="3e5d8-249">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-249">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="3e5d8-250">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-250">Minimum system</span></span> | <span data-ttu-id="3e5d8-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-251">Windows XP</span></span>                                                                                                                                                |



 

### <a name="dllsurrogate"></a><span data-ttu-id="3e5d8-252">Dllersatz</span><span class="sxs-lookup"><span data-stu-id="3e5d8-252">DllSurrogate</span></span>



| <span data-ttu-id="3e5d8-253">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-253">Entry</span></span> | <span data-ttu-id="3e5d8-254">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-254">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="3e5d8-255">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-255">Description</span></span>    | <span data-ttu-id="3e5d8-256">Gibt den vollständigen Pfad zu einer surragate-Serveranwendung an.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-256">Specifies the full path to a surragate server application.</span></span> |
| <span data-ttu-id="3e5d8-257">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-257">Access</span></span>         | <span data-ttu-id="3e5d8-258">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-258">ReadWrite</span></span>                                                  |
| <span data-ttu-id="3e5d8-259">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-259">Type</span></span>           | <span data-ttu-id="3e5d8-260">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-260">String</span></span>                                                     |
| <span data-ttu-id="3e5d8-261">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-261">Default</span></span>        | <span data-ttu-id="3e5d8-262">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-262">N/A</span></span>                                                        |
| <span data-ttu-id="3e5d8-263">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-263">Minimum system</span></span> | <span data-ttu-id="3e5d8-264">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-264">Windows XP</span></span>                                                 |



 

### <a name="inprochandler32"></a><span data-ttu-id="3e5d8-265">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="3e5d8-265">InprocHandler32</span></span>



| <span data-ttu-id="3e5d8-266">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-266">Entry</span></span> | <span data-ttu-id="3e5d8-267">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-267">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-268">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-268">Description</span></span>    | <span data-ttu-id="3e5d8-269">Gibt den vollständigen Pfad zu einer benutzerdefinierten benutzerdefinierten Handler-dll von 32 Bit an.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-269">Specifies the full path to a 32-bit in-process custom handler DLL.</span></span> |
| <span data-ttu-id="3e5d8-270">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-270">Access</span></span>         | <span data-ttu-id="3e5d8-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-271">ReadWrite</span></span>                                                          |
| <span data-ttu-id="3e5d8-272">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-272">Type</span></span>           | <span data-ttu-id="3e5d8-273">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-273">String</span></span>                                                             |
| <span data-ttu-id="3e5d8-274">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-274">Default</span></span>        | <span data-ttu-id="3e5d8-275">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-275">N/A</span></span>                                                                |
| <span data-ttu-id="3e5d8-276">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-276">Minimum system</span></span> | <span data-ttu-id="3e5d8-277">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-277">Windows XP</span></span>                                                         |



 

### <a name="inprocserver32"></a><span data-ttu-id="3e5d8-278">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="3e5d8-278">InprocServer32</span></span>



| <span data-ttu-id="3e5d8-279">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-279">Entry</span></span> | <span data-ttu-id="3e5d8-280">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-280">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="3e5d8-281">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-281">Description</span></span>    | <span data-ttu-id="3e5d8-282">Gibt den vollständigen Pfad zu einer 32-Bit-Prozess internen Server-DLL an.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-282">Specifies the full path to a 32-bit in-process server DLL.</span></span> |
| <span data-ttu-id="3e5d8-283">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-283">Access</span></span>         | <span data-ttu-id="3e5d8-284">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-284">ReadWrite</span></span>                                                  |
| <span data-ttu-id="3e5d8-285">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-285">Type</span></span>           | <span data-ttu-id="3e5d8-286">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-286">String</span></span>                                                     |
| <span data-ttu-id="3e5d8-287">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-287">Default</span></span>        | <span data-ttu-id="3e5d8-288">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-288">N/A</span></span>                                                        |
| <span data-ttu-id="3e5d8-289">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-289">Minimum system</span></span> | <span data-ttu-id="3e5d8-290">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-290">Windows XP</span></span>                                                 |



 

### <a name="isenabled"></a><span data-ttu-id="3e5d8-291">isEnabled</span><span class="sxs-lookup"><span data-stu-id="3e5d8-291">IsEnabled</span></span>



| <span data-ttu-id="3e5d8-292">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-292">Entry</span></span> | <span data-ttu-id="3e5d8-293">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-293">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-294">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-294">Description</span></span>    | <span data-ttu-id="3e5d8-295">Wenn die COM+-Anwendung oder-Komponente deaktiviert ist, ist isaktivierter Wert false.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-295">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="3e5d8-296">Wenn die COM+-Anwendung oder-Komponente aktiviert ist, ist isaktivierte "true".</span><span class="sxs-lookup"><span data-stu-id="3e5d8-296">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="3e5d8-297">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-297">Access</span></span>         | <span data-ttu-id="3e5d8-298">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-298">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="3e5d8-299">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-299">Type</span></span>           | <span data-ttu-id="3e5d8-300">Bool</span><span class="sxs-lookup"><span data-stu-id="3e5d8-300">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="3e5d8-301">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-301">Default</span></span>        | <span data-ttu-id="3e5d8-302">Richtig</span><span class="sxs-lookup"><span data-stu-id="3e5d8-302">True</span></span>                                                                                                                                      |
| <span data-ttu-id="3e5d8-303">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-303">Minimum system</span></span> | <span data-ttu-id="3e5d8-304">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-304">Windows XP</span></span>                                                                                                                                |



 

### <a name="launchpermissions"></a><span data-ttu-id="3e5d8-305">Launchberechtigungen</span><span class="sxs-lookup"><span data-stu-id="3e5d8-305">LaunchPermissions</span></span>



| <span data-ttu-id="3e5d8-306">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-306">Entry</span></span> | <span data-ttu-id="3e5d8-307">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-307">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-308">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-308">Description</span></span>    | <span data-ttu-id="3e5d8-309">Gibt Benutzerkonten an, denen die Berechtigung zum Starten dieser Komponente gestattet oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-309">Specifies user accounts that are allowed or denied permission to start this component.</span></span> |
| <span data-ttu-id="3e5d8-310">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-310">Access</span></span>         | <span data-ttu-id="3e5d8-311">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-311">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="3e5d8-312">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-312">Type</span></span>           | <span data-ttu-id="3e5d8-313">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-313">String</span></span>                                                                                 |
| <span data-ttu-id="3e5d8-314">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-314">Default</span></span>        | <span data-ttu-id="3e5d8-315">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-315">N/A</span></span>                                                                                    |
| <span data-ttu-id="3e5d8-316">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-316">Minimum system</span></span> | <span data-ttu-id="3e5d8-317">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-317">Windows XP</span></span>                                                                             |



 

### <a name="localserver32"></a><span data-ttu-id="3e5d8-318">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="3e5d8-318">LocalServer32</span></span>



| <span data-ttu-id="3e5d8-319">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-319">Entry</span></span> | <span data-ttu-id="3e5d8-320">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-320">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-321">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-321">Description</span></span>    | <span data-ttu-id="3e5d8-322">Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-322">Specifies the full path to a 32-bit local server application.</span></span> <span data-ttu-id="3e5d8-323">Um die Systemsicherheit zu schützen, verwenden Sie Zeichen folgen in Anführungszeichen im Pfad, um anzugeben, wo der ausführbare Dateiname endet und die Argumente beginnen.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-323">To help protect system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="3e5d8-324">Beispiel: " \\ C: \\ Program Files \\ Company Files \\Application.exe\\ " Param1 Param2 ".</span><span class="sxs-lookup"><span data-stu-id="3e5d8-324">For example, "\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2".</span></span> |
| <span data-ttu-id="3e5d8-325">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-325">Access</span></span>         | <span data-ttu-id="3e5d8-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="3e5d8-327">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-327">Type</span></span>           | <span data-ttu-id="3e5d8-328">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-328">String</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3e5d8-329">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-329">Default</span></span>        | <span data-ttu-id="3e5d8-330">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-330">N/A</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3e5d8-331">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-331">Minimum system</span></span> | <span data-ttu-id="3e5d8-332">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-332">Windows XP</span></span>                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a><span data-ttu-id="3e5d8-333">LocalService</span><span class="sxs-lookup"><span data-stu-id="3e5d8-333">LocalService</span></span>



| <span data-ttu-id="3e5d8-334">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-334">Entry</span></span> | <span data-ttu-id="3e5d8-335">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-335">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="3e5d8-336">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-336">Description</span></span>    | <span data-ttu-id="3e5d8-337">Gibt den vollständigen Pfad zur Dienst Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-337">Specifies the full path to the service application.</span></span> |
| <span data-ttu-id="3e5d8-338">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-338">Access</span></span>         | <span data-ttu-id="3e5d8-339">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-339">ReadWrite</span></span>                                           |
| <span data-ttu-id="3e5d8-340">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-340">Type</span></span>           | <span data-ttu-id="3e5d8-341">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-341">String</span></span>                                              |
| <span data-ttu-id="3e5d8-342">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-342">Default</span></span>        | <span data-ttu-id="3e5d8-343">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-343">N/A</span></span>                                                 |
| <span data-ttu-id="3e5d8-344">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-344">Minimum system</span></span> | <span data-ttu-id="3e5d8-345">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-345">Windows XP</span></span>                                          |



 

### <a name="password"></a><span data-ttu-id="3e5d8-346">Kennwort</span><span class="sxs-lookup"><span data-stu-id="3e5d8-346">Password</span></span>



| <span data-ttu-id="3e5d8-347">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-347">Entry</span></span> | <span data-ttu-id="3e5d8-348">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-348">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-349">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-349">Description</span></span>    | <span data-ttu-id="3e5d8-350">Legt das Kennwort fest, das vom Server Prozess zum Anmelden unter der angegebenen runas-Identität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-350">Sets the password used by the server process to log on under the specified RunAs identity.</span></span> <span data-ttu-id="3e5d8-351">Das Kennwort sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die runas-Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-351">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="3e5d8-352">Wenn das Kennwort und die Identität nicht synchron sind, kann die Komponente erst gestartet werden, wenn Sie von einem Administrator zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-352">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="3e5d8-353">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-353">Access</span></span>         | <span data-ttu-id="3e5d8-354">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="3e5d8-354">WriteOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3e5d8-355">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-355">Type</span></span>           | <span data-ttu-id="3e5d8-356">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-356">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3e5d8-357">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-357">Default</span></span>        | <span data-ttu-id="3e5d8-358">NULL</span><span class="sxs-lookup"><span data-stu-id="3e5d8-358">NULL</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3e5d8-359">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-359">Minimum system</span></span> | <span data-ttu-id="3e5d8-360">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-360">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a><span data-ttu-id="3e5d8-361">ProgID</span><span class="sxs-lookup"><span data-stu-id="3e5d8-361">ProgID</span></span>



| <span data-ttu-id="3e5d8-362">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-362">Entry</span></span> | <span data-ttu-id="3e5d8-363">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-363">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-364">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-364">Description</span></span>    | <span data-ttu-id="3e5d8-365">Ein Name, der die Komponente identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-365">A name identifying the component.</span></span> <span data-ttu-id="3e5d8-366">Diese Eigenschaft wird zurückgegeben, wenn die Name-Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-366">This property is returned when the Name property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3e5d8-367">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-367">Access</span></span>         | <span data-ttu-id="3e5d8-368">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e5d8-368">ReadOnly</span></span>                                                                                                                             |
| <span data-ttu-id="3e5d8-369">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-369">Type</span></span>           | <span data-ttu-id="3e5d8-370">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-370">String</span></span>                                                                                                                               |
| <span data-ttu-id="3e5d8-371">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-371">Default</span></span>        | <span data-ttu-id="3e5d8-372">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-372">N/A</span></span>                                                                                                                                  |
| <span data-ttu-id="3e5d8-373">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-373">Minimum system</span></span> | <span data-ttu-id="3e5d8-374">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-374">Windows XP</span></span>                                                                                                                           |



 

### <a name="remoteserver"></a><span data-ttu-id="3e5d8-375">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="3e5d8-375">RemoteServer</span></span>



| <span data-ttu-id="3e5d8-376">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-376">Entry</span></span> | <span data-ttu-id="3e5d8-377">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-377">Value</span></span> |
|----------------|---------------------------------------|
| <span data-ttu-id="3e5d8-378">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-378">Description</span></span>    | <span data-ttu-id="3e5d8-379">Gibt den Remote Server Computer an.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-379">Specifies the remote server computer.</span></span> |
| <span data-ttu-id="3e5d8-380">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-380">Access</span></span>         | <span data-ttu-id="3e5d8-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-381">ReadWrite</span></span>                             |
| <span data-ttu-id="3e5d8-382">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-382">Type</span></span>           | <span data-ttu-id="3e5d8-383">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-383">String</span></span>                                |
| <span data-ttu-id="3e5d8-384">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-384">Default</span></span>        | <span data-ttu-id="3e5d8-385">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-385">N/A</span></span>                                   |
| <span data-ttu-id="3e5d8-386">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-386">Minimum system</span></span> | <span data-ttu-id="3e5d8-387">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-387">Windows XP</span></span>                            |



 

### <a name="runas"></a><span data-ttu-id="3e5d8-388">RunAs</span><span class="sxs-lookup"><span data-stu-id="3e5d8-388">RunAs</span></span>



| <span data-ttu-id="3e5d8-389">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-389">Entry</span></span> | <span data-ttu-id="3e5d8-390">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-391">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-391">Description</span></span>    | <span data-ttu-id="3e5d8-392">Gibt den Benutzer an, unter dessen Identität die Komponente ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-392">Specifies the user under whose identity the component will run.</span></span> <span data-ttu-id="3e5d8-393">Das Kennwort sollte vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)zur gleichen Zeit wie die runas-Identität festgelegt werden, da das Kennwort und die Identität vor dem Speichern überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-393">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="3e5d8-394">Wenn das Kennwort und die Identität nicht synchron sind, kann die Komponente erst gestartet werden, wenn Sie von einem Administrator zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-394">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="3e5d8-395">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-395">Access</span></span>         | <span data-ttu-id="3e5d8-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-396">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3e5d8-397">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-397">Type</span></span>           | <span data-ttu-id="3e5d8-398">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-398">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3e5d8-399">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-399">Default</span></span>        | <span data-ttu-id="3e5d8-400">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-400">N/A</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3e5d8-401">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-401">Minimum system</span></span> | <span data-ttu-id="3e5d8-402">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-402">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a><span data-ttu-id="3e5d8-403">Service Parameter</span><span class="sxs-lookup"><span data-stu-id="3e5d8-403">ServiceParameter</span></span>



| <span data-ttu-id="3e5d8-404">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-404">Entry</span></span> | <span data-ttu-id="3e5d8-405">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-405">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-406">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-406">Description</span></span>    | <span data-ttu-id="3e5d8-407">Gibt die Parameter an, die an die Anwendung bei Aufruf als Dienst Anwendung übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-407">Specifies the parameters passed to the application when invoked as a service application.</span></span> |
| <span data-ttu-id="3e5d8-408">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-408">Access</span></span>         | <span data-ttu-id="3e5d8-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-409">ReadWrite</span></span>                                                                                 |
| <span data-ttu-id="3e5d8-410">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-410">Type</span></span>           | <span data-ttu-id="3e5d8-411">String</span><span class="sxs-lookup"><span data-stu-id="3e5d8-411">String</span></span>                                                                                    |
| <span data-ttu-id="3e5d8-412">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-412">Default</span></span>        | <span data-ttu-id="3e5d8-413">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-413">N/A</span></span>                                                                                       |
| <span data-ttu-id="3e5d8-414">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-414">Minimum system</span></span> | <span data-ttu-id="3e5d8-415">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-415">Windows XP</span></span>                                                                                |



 

### <a name="srptrustlevel"></a><span data-ttu-id="3e5d8-416">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="3e5d8-416">SRPTrustLevel</span></span>



| <span data-ttu-id="3e5d8-417">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-417">Entry</span></span> | <span data-ttu-id="3e5d8-418">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-418">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-419">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-419">Description</span></span>    | <span data-ttu-id="3e5d8-420">Gibt die Richtlinie für die Software Einschränkungs Richtlinie (SRP) der Komponente an.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-420">Indicates the software restriction policy (SRP) trust level of the component.</span></span> <span data-ttu-id="3e5d8-421">Die SRP-Vertrauens Ebene bezieht sich auf die Vertrauens Ebene, die Sie einer Komponente bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-421">The SRP trust level refers to the level of trust that you are willing to give to a component.</span></span> <span data-ttu-id="3e5d8-422">Eine uneingeschränkte SRP-Vertrauens Ebene entspricht dem \_ fulllytrusted-Enumerationswert der sichereren levelid \_ , während eine unzulässige SRP-Vertrauens Ebene dem sichereren \_ levelid-Enumerationswert entspricht \_ .</span><span class="sxs-lookup"><span data-stu-id="3e5d8-422">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="3e5d8-423">Die Enumeration für die Vertrauens Ebenen ist in winsafer. h definiert.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-423">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="3e5d8-424">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-424">Access</span></span>         | <span data-ttu-id="3e5d8-425">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e5d8-425">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3e5d8-426">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-426">Type</span></span>           | <span data-ttu-id="3e5d8-427">Lange mögliche Werte: sicherere \_ levelid nicht \_ zulässig (0x0) sicherere \_ levelid \_ fullytrusted (0x40000)</span><span class="sxs-lookup"><span data-stu-id="3e5d8-427">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3e5d8-428">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-428">Default</span></span>        | <span data-ttu-id="3e5d8-429">sicherere \_ levelid \_ fullytrusted</span><span class="sxs-lookup"><span data-stu-id="3e5d8-429">SAFER\_LEVELID\_FULLYTRUSTED</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3e5d8-430">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-430">Minimum system</span></span> | <span data-ttu-id="3e5d8-431">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-431">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="3e5d8-432">Eine Komponente, der Sie den uneingeschränkten Zugriff als vertrauenswürdig einstufen möchten, sollte mit der strengsten Sicherheit verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-432">A component that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="3e5d8-433">Anwendungen, die uneingeschränkt sind, können nur unbeschränkte Komponenten laden, während unzulässige Anwendungen nicht ausgeführt werden dürfen und somit keine Komponenten laden können.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-433">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

### <a name="threadingmodel"></a><span data-ttu-id="3e5d8-434">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="3e5d8-434">ThreadingModel</span></span>



| <span data-ttu-id="3e5d8-435">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3e5d8-435">Entry</span></span> | <span data-ttu-id="3e5d8-436">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5d8-436">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d8-437">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5d8-437">Description</span></span>    | <span data-ttu-id="3e5d8-438">Bestimmt, wie Instanzen der Komponente Threads zur Methoden Ausführung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-438">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="3e5d8-439">Werte entsprechen com-Threading Modellen.</span><span class="sxs-lookup"><span data-stu-id="3e5d8-439">Values correspond to COM threading models.</span></span>                                                  |
| <span data-ttu-id="3e5d8-440">Access</span><span class="sxs-lookup"><span data-stu-id="3e5d8-440">Access</span></span>         | <span data-ttu-id="3e5d8-441">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e5d8-441">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="3e5d8-442">type</span><span class="sxs-lookup"><span data-stu-id="3e5d8-442">Type</span></span>           | <span data-ttu-id="3e5d8-443">Lange mögliche Werte: comadminthreadingmodelapartment (0) comadminthreadingmodelfree (1) comadminthreadingmodelmain (2) comadminthreadingmodelboth (3) comadminthreadingmodelneutral (4)</span><span class="sxs-lookup"><span data-stu-id="3e5d8-443">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)</span></span> |
| <span data-ttu-id="3e5d8-444">Standard</span><span class="sxs-lookup"><span data-stu-id="3e5d8-444">Default</span></span>        | <span data-ttu-id="3e5d8-445">–</span><span class="sxs-lookup"><span data-stu-id="3e5d8-445">N/A</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="3e5d8-446">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="3e5d8-446">Minimum system</span></span> | <span data-ttu-id="3e5d8-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5d8-447">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="3e5d8-448">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e5d8-448">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e5d8-449">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="3e5d8-449">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
