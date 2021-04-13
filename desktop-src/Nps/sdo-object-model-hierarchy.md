---
title: Objektmodell Hierarchie
description: Die Objekte im SDO-Objektmodell werden in einer Hierarchie angeordnet. Dies bedeutet, dass Objekte in SDO auf andere Objekte in SDO zugreifen können.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390597"
---
# <a name="object-model-hierarchy"></a><span data-ttu-id="bb8b6-104">Objektmodell Hierarchie</span><span class="sxs-lookup"><span data-stu-id="bb8b6-104">Object Model Hierarchy</span></span>

<span data-ttu-id="bb8b6-105">Die Objekte im SDO-Objektmodell werden in einer Hierarchie angeordnet.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-105">The objects in the SDO object model are arranged in a hierarchy.</span></span> <span data-ttu-id="bb8b6-106">Dies bedeutet, dass Objekte in SDO auf andere Objekte in SDO zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-106">This means objects in SDO provide access to other objects in SDO.</span></span>

<span data-ttu-id="bb8b6-107">-Objekte ermöglichen den Zugriff auf andere-Objekte auf zwei Arten.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-107">Objects provide access to other objects in two ways.</span></span> <span data-ttu-id="bb8b6-108">Eine Möglichkeit besteht darin, dass das-Objekt eine Schnittstelle verfügbar macht, die Methoden zum Abrufen anderer Objekte bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-108">One way is for the object to expose an interface that provides methods to retrieve other objects.</span></span> <span data-ttu-id="bb8b6-109">Ein Beispiel für diesen Ansatz ist das Computer Objekt.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-109">An example of this approach is the Machine object.</span></span> <span data-ttu-id="bb8b6-110">Das Computer Objekt macht die [**isdomachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-110">The Machine object exposes the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) interface.</span></span> <span data-ttu-id="bb8b6-111">Die [**isdomachine:: getservicesdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) -Methode ruft ein Dienst Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-111">The [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) method retrieves a Service object.</span></span> <span data-ttu-id="bb8b6-112">Die [**isdomachine:: getusersdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) -Methode ruft ein Benutzerobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-112">The [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) method retrieves a User Object.</span></span>

![Computer Objekt, das die isdomachine-Schnittstelle](images/sdo01.png)

<span data-ttu-id="bb8b6-114">Weitere Informationen finden Sie unter Abrufen von [Dienst-und Benutzer-SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span><span class="sxs-lookup"><span data-stu-id="bb8b6-114">For more information, see [Obtaining Service and User SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span></span>

<span data-ttu-id="bb8b6-115">Die zweite Möglichkeit, dass Objekte auf andere Objekte zugreifen, besteht darin, dass eine Objekt Auflistung als Eigenschaft des Objekts dargestellt wird, in dem Sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-115">The second way that objects provide access to other objects is that an object collection is represented as a property of the object that contains it.</span></span> <span data-ttu-id="bb8b6-116">Rufen Sie zum Abrufen einer Objekt Auflistung [**isdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) für die-Eigenschaft eines Objekts auf, das die Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-116">To retrieve an object collection, call [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) on the property of an object that represents the collection.</span></span> <span data-ttu-id="bb8b6-117">Um z. b. die Richtlinien Auflistung abzurufen, rufen Sie **isdo:: GetProperty** in der [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle auf, die vom NPS-Objekt verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-117">For example, to retrieve the Policies collection, call **ISdo::GetProperty** on the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface exposed by the NPS object.</span></span>

> [!Note]  
> <span data-ttu-id="bb8b6-118">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-118">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

![Abrufen der Richtlinien Sammlung](images/sdo02.png)

<span data-ttu-id="bb8b6-120">Beispielcode, der die Richtlinien Auflistung abruft, finden Sie unter [Abrufen einer](/windows/desktop/Nps/sdo-retrieving-a-collection)Auflistung.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-120">For sample code that retrieves the Policies collection, see [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection).</span></span>

<span data-ttu-id="bb8b6-121">Das [**NPS-Server Datenobjekt**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) verfügt über die folgenden Eigenschaften, die Sammlungen darstellen:</span><span class="sxs-lookup"><span data-stu-id="bb8b6-121">The [**NPS Server Data Object**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) has the following properties that represent collections:</span></span>

<dl> <dt>

<span data-ttu-id="bb8b6-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Rechnung</span><span class="sxs-lookup"><span data-stu-id="bb8b6-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditors</span></span>
</dt> <dd>

<span data-ttu-id="bb8b6-123">Der einzige Auditor in der Prüfer Sammlung ist das [**NT-Ereignisprotokoll**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span><span class="sxs-lookup"><span data-stu-id="bb8b6-123">The only auditor in the Auditors collection is the [**NT Event Log**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span></span>

</dd> <dt>

<span data-ttu-id="bb8b6-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policies</span><span class="sxs-lookup"><span data-stu-id="bb8b6-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policies</span></span>
</dt> <dd>

<span data-ttu-id="bb8b6-125">Jedes [**Richtlinien Objekt**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) verfügt über eine-Eigenschaft, die eine Auflistung von Bedingungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-125">Each [**policy object**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) has a property that represents a collection of conditions.</span></span>

</dd> <dt>

<span data-ttu-id="bb8b6-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Liert</span><span class="sxs-lookup"><span data-stu-id="bb8b6-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profiles</span></span>
</dt> <dd>

<span data-ttu-id="bb8b6-127">Jedes [**Profil Objekt**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in den Profil Auflistungen verfügt über eine-Eigenschaft, die eine Attribut Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-127">Each [**profile object**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in the Profiles collections has a property that represents an attributes collection.</span></span> <span data-ttu-id="bb8b6-128">Eine Liste der Attribute, die von SDO unterstützt werden, finden [Sie unter Unterstützte SDO-Attribute](/windows/desktop/Nps/sdo-sdo-supported-attributes) .</span><span class="sxs-lookup"><span data-stu-id="bb8b6-128">See [SDO Supported Attributes](/windows/desktop/Nps/sdo-sdo-supported-attributes) for a list of the attributes supported by SDO.</span></span>

</dd> <dt>

<span data-ttu-id="bb8b6-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protokollen</span><span class="sxs-lookup"><span data-stu-id="bb8b6-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocols</span></span>
</dt> <dd>

<span data-ttu-id="bb8b6-130">Die Protokolle-Auflistung enthält das RADIUS-Protokoll Objekt, das eine Clients-Sammlung enthält, die RADIUS-Clients darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-130">The protocols collection contains the RADIUS protocol object, which contains a clients collection that represents RADIUS clients.</span></span> <span data-ttu-id="bb8b6-131">Siehe [Hinzufügen eines Clients](/windows/desktop/Nps/sdo-adding-a-client) für Beispielcode, der zeigt, wie die Client Auflistung abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-131">See [Adding a Client](/windows/desktop/Nps/sdo-adding-a-client) for sample code that shows how to retrieve the client collection.</span></span>

</dd> <dt>

<span data-ttu-id="bb8b6-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bb8b6-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy Policies</span></span>
</dt> <dd>

<span data-ttu-id="bb8b6-133">Diese Sammlung enthält Netzwerk Zugriffsrichtlinien, die für die Verarbeitung von Verbindungsanforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-133">This collection contains Network Access Policies used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="bb8b6-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy profile</span><span class="sxs-lookup"><span data-stu-id="bb8b6-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy Profiles</span></span>
</dt> <dd>

<span data-ttu-id="bb8b6-135">Diese Sammlung enthält Profile, die für die Verarbeitung von Verbindungsanforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-135">This collection contains profiles used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="bb8b6-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS-Server Gruppen</span><span class="sxs-lookup"><span data-stu-id="bb8b6-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS Server Groups</span></span>
</dt> <dd>

<span data-ttu-id="bb8b6-137">Jede [**RADIUS-Server Gruppe**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in der RADIUS-Server Gruppen Auflistung verfügt über eine-Eigenschaft, die die Sammlung der Server in dieser Server Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-137">Each [**RADIUS server group**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in the RADIUS Server Groups collection has a property that represents the collection of servers in that server group.</span></span>

</dd> <dt>

<span data-ttu-id="bb8b6-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Anforderungs Handler</span><span class="sxs-lookup"><span data-stu-id="bb8b6-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Request Handlers</span></span>
</dt> <dd>

<span data-ttu-id="bb8b6-139">Diese Sammlung enthält die "Microsoft Realm Evaluator"-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-139">This collection contains the "Microsoft Realms Evaluator" collection.</span></span> <span data-ttu-id="bb8b6-140">Die Einstellungen "Microsoft NT Sam-Authentifizierung" und "Microsoft Accounting" sind auch in dieser Sammlung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb8b6-140">The "Microsoft NT SAM Authentication" and "Microsoft Accounting" settings are also available in this collection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="bb8b6-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb8b6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb8b6-142">SDO-Objekte und-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bb8b6-142">SDO Objects and Properties</span></span>](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[<span data-ttu-id="bb8b6-143">Unterstützte SDO-Attribute</span><span class="sxs-lookup"><span data-stu-id="bb8b6-143">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 