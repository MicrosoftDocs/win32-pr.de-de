---
description: Wenn die rollenbasierte Sicherheit verwendet wird, kann das Kontext Objekt für den Sicherheits Rückruf verwendet werden, um auf Sicherheitsinformationen zum aktuellen-Befehl zuzugreifen.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Aufrufen von Kontextinformationen für den Sicherheitskontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214222"
---
# <a name="accessing-security-call-context-information"></a><span data-ttu-id="c29e1-103">Aufrufen von Kontextinformationen für den Sicherheitskontext</span><span class="sxs-lookup"><span data-stu-id="c29e1-103">Accessing Security Call Context Information</span></span>

<span data-ttu-id="c29e1-104">Wenn die rollenbasierte Sicherheit verwendet wird, kann das Kontext Objekt für den Sicherheits Rückruf verwendet werden, um auf Sicherheitsinformationen zum aktuellen-Befehl zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c29e1-104">When role-based security is being used, the security call context object can be used to access security information about the current call.</span></span>

<span data-ttu-id="c29e1-105">Die folgenden Auflistungen von Eigenschaften sind im Kontext Objekt für den Sicherheits Rückruf verfügbar:</span><span class="sxs-lookup"><span data-stu-id="c29e1-105">The following collections of properties are available from the security call context object:</span></span>

-   [<span data-ttu-id="c29e1-106">SecurityCallContext-Auflistung</span><span class="sxs-lookup"><span data-stu-id="c29e1-106">SecurityCallContext Collection</span></span>](#securitycallcontext-collection)
-   [<span data-ttu-id="c29e1-107">SecurityCaller-Sammlung</span><span class="sxs-lookup"><span data-stu-id="c29e1-107">SecurityCallers Collection</span></span>](#securitycallers-collection)
-   [<span data-ttu-id="c29e1-108">SecurityIdentity-Sammlung</span><span class="sxs-lookup"><span data-stu-id="c29e1-108">SecurityIdentity Collection</span></span>](#securityidentity-collection)
-   [<span data-ttu-id="c29e1-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c29e1-109">Related topics</span></span>](#related-topics)

## <a name="securitycallcontext-collection"></a><span data-ttu-id="c29e1-110">SecurityCallContext-Auflistung</span><span class="sxs-lookup"><span data-stu-id="c29e1-110">SecurityCallContext Collection</span></span>



| <span data-ttu-id="c29e1-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c29e1-111">Property</span></span>                          | <span data-ttu-id="c29e1-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c29e1-112">Description</span></span>                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c29e1-113">Numaufrufer</span><span class="sxs-lookup"><span data-stu-id="c29e1-113">NumCallers</span></span><br/>             | <span data-ttu-id="c29e1-114">Die Anzahl der Aufrufer in der Aufruf Kette.</span><span class="sxs-lookup"><span data-stu-id="c29e1-114">The number of callers in the chain of calls.</span></span><br/>                                                                                |
| <span data-ttu-id="c29e1-115">MinAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="c29e1-115">MinAuthenticationLevel</span></span><br/> | <span data-ttu-id="c29e1-116">Die am wenigsten sichere Authentifizierungs Ebene aller Aufrufer in der Kette.</span><span class="sxs-lookup"><span data-stu-id="c29e1-116">The least secure authentication level of all callers in the chain.</span></span><br/>                                                          |
| <span data-ttu-id="c29e1-117">Anrufer</span><span class="sxs-lookup"><span data-stu-id="c29e1-117">Callers</span></span><br/>                | <span data-ttu-id="c29e1-118">Informationen zur Identität von upstreamaufrufern in Form einer [**SecurityCaller**](securitycallers.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c29e1-118">Information about the identity of upstream callers, in the form of a [**SecurityCallers**](securitycallers.md) collection.</span></span><br/> |
| <span data-ttu-id="c29e1-119">DirectCaller</span><span class="sxs-lookup"><span data-stu-id="c29e1-119">DirectCaller</span></span><br/>           | <span data-ttu-id="c29e1-120">Der Aufrufer, der das Objekt direkt aufgerufen hat (ohne dazwischen liegende Aufrufer).</span><span class="sxs-lookup"><span data-stu-id="c29e1-120">The caller that called the object directly (with no intervening callers).</span></span> <br/>                                                  |
| <span data-ttu-id="c29e1-121">OriginalCaller</span><span class="sxs-lookup"><span data-stu-id="c29e1-121">OriginalCaller</span></span><br/>         | <span data-ttu-id="c29e1-122">Der Aufrufer, der die Kette der Aufrufe des-Objekts ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="c29e1-122">The caller that originated the chain of calls to the object.</span></span> <br/>                                                               |



 

<span data-ttu-id="c29e1-123">Um weitere Informationen zur Verwendung dieser Sammlung zu erhalten, sollte Microsoft Visual Basic-Entwicklern die [**SecurityCallContext**](securitycallcontext.md) -Klasse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c29e1-123">For more information about how to use this collection, Microsoft Visual Basic developers should see the [**SecurityCallContext**](securitycallcontext.md) class.</span></span> <span data-ttu-id="c29e1-124">C-und C++-Entwickler sollten auf [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)verweisen.</span><span class="sxs-lookup"><span data-stu-id="c29e1-124">C and C++ developers should refer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="securitycallers-collection"></a><span data-ttu-id="c29e1-125">SecurityCaller-Sammlung</span><span class="sxs-lookup"><span data-stu-id="c29e1-125">SecurityCallers Collection</span></span>

<span data-ttu-id="c29e1-126">Die [**SecurityCaller**](securitycallers.md) -Auflistung stellt Aufrufer dar, die mithilfe eines Indexes zwischen 0 und 1 weniger als numcaller, einschließlich, abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="c29e1-126">The [**SecurityCallers**](securitycallers.md) collection represents callers that can be retrieved by using an index between 0 and 1 less than NumCallers, inclusive.</span></span> <span data-ttu-id="c29e1-127">Jeder Aufrufer wird durch ein [**SecurityIdentity**](securityidentity.md) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c29e1-127">Each caller is represented by a [**SecurityIdentity**](securityidentity.md) object.</span></span>

<span data-ttu-id="c29e1-128">Weitere Informationen zu dieser Sammlung finden Visual Basic Entwicklern die [**SecurityCaller**](securitycallers.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="c29e1-128">For more information about this collection, Visual Basic developers should see the [**SecurityCallers**](securitycallers.md) class.</span></span> <span data-ttu-id="c29e1-129">C-und C++-Entwickler sollten auf [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)verweisen.</span><span class="sxs-lookup"><span data-stu-id="c29e1-129">C and C++ developers should refer to [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="securityidentity-collection"></a><span data-ttu-id="c29e1-130">SecurityIdentity-Sammlung</span><span class="sxs-lookup"><span data-stu-id="c29e1-130">SecurityIdentity Collection</span></span>



| <span data-ttu-id="c29e1-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c29e1-131">Property</span></span>                         | <span data-ttu-id="c29e1-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c29e1-132">Description</span></span>                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c29e1-133">SID</span><span class="sxs-lookup"><span data-stu-id="c29e1-133">SID</span></span><br/>                   | <span data-ttu-id="c29e1-134">Die Sicherheits-ID für den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="c29e1-134">The security identifier for the caller.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="c29e1-135">AccountName</span><span class="sxs-lookup"><span data-stu-id="c29e1-135">AccountName</span></span><br/>           | <span data-ttu-id="c29e1-136">Der Kontoname des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="c29e1-136">The account name of the caller.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="c29e1-137">AuthenticationService</span><span class="sxs-lookup"><span data-stu-id="c29e1-137">AuthenticationService</span></span><br/> | <span data-ttu-id="c29e1-138">Der verwendete Authentifizierungsdienst, z. b. NTLMSSP, Kerberos oder SSL.</span><span class="sxs-lookup"><span data-stu-id="c29e1-138">The authentication service used, such as NTLMSSP, Kerberos, or SSL.</span></span><br/>                                                                                       |
| <span data-ttu-id="c29e1-139">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="c29e1-139">AuthenticationLevel</span></span><br/>   | <span data-ttu-id="c29e1-140">Die verwendete Authentifizierungs Ebene, die die für die Kommunikation mit dem-Objekt verwendete Menge an Schutz darstellt.</span><span class="sxs-lookup"><span data-stu-id="c29e1-140">The authentication level used, which represents the amount of protection used when communicating with the object.</span></span><br/>                                         |
| <span data-ttu-id="c29e1-141">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="c29e1-141">ImpersonationLevel</span></span><br/>    | <span data-ttu-id="c29e1-142">Die vom Client festgelegte Ebene des Identitäts Wechsels, wenn der Identitätswechsel verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c29e1-142">The level of impersonation set by the client, if impersonation was used.</span></span> <span data-ttu-id="c29e1-143">Diese Ebene gibt die Menge an Autorität an, die vom Client an den Server übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c29e1-143">This level indicates the amount of authority given to the server by the client.</span></span> <br/> |



 

<span data-ttu-id="c29e1-144">Weitere Informationen zu dieser Sammlung finden Visual Basic Entwicklern die [**SecurityIdentity**](securityidentity.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="c29e1-144">For more information on this collection, Visual Basic developers should see the [**SecurityIdentity**](securityidentity.md) class.</span></span> <span data-ttu-id="c29e1-145">C-und C++-Entwickler sollten sich auf [**isecurityidentitycoll**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)beziehen.</span><span class="sxs-lookup"><span data-stu-id="c29e1-145">C and C++ developers should refer to [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c29e1-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c29e1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c29e1-147">Überprüfen der Rollen Mitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="c29e1-147">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="c29e1-148">Bestimmen, ob Role-Based Sicherheit aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="c29e1-148">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="c29e1-149">Sicherheit für programmgesteuerte Komponenten</span><span class="sxs-lookup"><span data-stu-id="c29e1-149">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 




