---
title: Binden an Active Directory Domain Services
description: In Active Directory Domain Services wird das Zuordnen eines programmgesteuerten Objekts zu einem bestimmten Active Directory Domain Services Objekt als Bindung bezeichnet.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- Bindung an Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, binden an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958211"
---
# <a name="binding-to-active-directory-domain-services"></a><span data-ttu-id="90f17-105">Binden an Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="90f17-105">Binding to Active Directory Domain Services</span></span>

<span data-ttu-id="90f17-106">In Active Directory Domain Services wird das Zuordnen eines programmgesteuerten Objekts zu einem bestimmten Active Directory Domain Services Objekt als *Bindung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="90f17-106">In Active Directory Domain Services, the act of associating a programmatic object with a specific Active Directory Domain Services object is known as *binding*.</span></span> <span data-ttu-id="90f17-107">Wenn ein Programm gesteuertes Objekt, z. b. ein [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -oder [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) -Objekt, einem bestimmten Verzeichnis Objekt zugeordnet ist, wird das programmgesteuerte Objekt als an das Verzeichnis Objekt *gebundene gebunden* .</span><span class="sxs-lookup"><span data-stu-id="90f17-107">When a programmatic object, such as an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) object, is associated with a specific directory object, the programmatic object is considered to be *bound to* the directory object.</span></span>

## <a name="binding-functions-and-methods"></a><span data-ttu-id="90f17-108">Bindungsfunktionen und-Methoden</span><span class="sxs-lookup"><span data-stu-id="90f17-108">Binding Functions and Methods</span></span>

<span data-ttu-id="90f17-109">Die Methode für die programmgesteuerte Bindung an ein Active Directory Objekt hängt von der verwendeten Programmier Technologie ab.</span><span class="sxs-lookup"><span data-stu-id="90f17-109">The method for programmatically binding to an Active Directory object will depend on the programming technology that is used.</span></span> <span data-ttu-id="90f17-110">Weitere Informationen zum Binden an Objekte in Active Directory Domain Services mit einer bestimmten Programmier Technologie finden Sie in den in der folgenden Tabelle aufgeführten Themen.</span><span class="sxs-lookup"><span data-stu-id="90f17-110">For more information about binding to objects in Active Directory Domain Services with a specific programming technology, see the topics listed in the following table.</span></span>



| <span data-ttu-id="90f17-111">Programmier Technologie</span><span class="sxs-lookup"><span data-stu-id="90f17-111">Programming technology</span></span>                                                                       | <span data-ttu-id="90f17-112">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="90f17-112">For more information</span></span>                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="90f17-113">Active Directory Service Interfaces</span><span class="sxs-lookup"><span data-stu-id="90f17-113">Active Directory Service Interfaces</span></span>](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [<span data-ttu-id="90f17-114">Binden an ein ADSI-Objekt</span><span class="sxs-lookup"><span data-stu-id="90f17-114">Binding to an ADSI Object</span></span>](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [<span data-ttu-id="90f17-115">Lightweight Directory Access Protocol</span><span class="sxs-lookup"><span data-stu-id="90f17-115">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [<span data-ttu-id="90f17-116">Einrichten einer LDAP-Sitzung</span><span class="sxs-lookup"><span data-stu-id="90f17-116">Establishing an LDAP Session</span></span>](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [<span data-ttu-id="90f17-117">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="90f17-117">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)                 | <span data-ttu-id="90f17-118">[Binden an Verzeichnisobjekte](/previous-versions/ms180840(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="90f17-118">[Binding to Directory Objects](/previous-versions/ms180840(v=vs.90))</span></span> |



 

## <a name="binding-strings"></a><span data-ttu-id="90f17-119">Binden von Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="90f17-119">Binding Strings</span></span>

<span data-ttu-id="90f17-120">Alle Bindungsfunktionen und-Methoden erfordern eine Bindungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="90f17-120">All bind functions and methods require a binding string.</span></span> <span data-ttu-id="90f17-121">Die Form der Bindungs Zeichenfolge hängt vom Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="90f17-121">The form of the binding string depends on the provider.</span></span> <span data-ttu-id="90f17-122">Active Directory Domain Services werden von den beiden Anbietern LDAP und WinNT unterstützt.</span><span class="sxs-lookup"><span data-stu-id="90f17-122">Active Directory Domain Services are supported by two providers, LDAP and WinNT.</span></span>

<span data-ttu-id="90f17-123">Ab Windows 2000 wird der LDAP-Anbieter für den Zugriff auf Active Directory Domain Services verwendet.</span><span class="sxs-lookup"><span data-stu-id="90f17-123">Beginning with Windows 2000, the LDAP provider is used to access Active Directory Domain Services.</span></span> <span data-ttu-id="90f17-124">Die LDAP-Bindungs Zeichenfolge kann eine der folgenden Formen annehmen:</span><span class="sxs-lookup"><span data-stu-id="90f17-124">The LDAP binding string can take one of the following forms:</span></span>

-   <span data-ttu-id="90f17-125">"LDAP:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="90f17-125">"LDAP://<host name>/<object name>"</span></span>
-   <span data-ttu-id="90f17-126">"GC:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="90f17-126">"GC://<host name>/<object name>"</span></span>

<span data-ttu-id="90f17-127">In den obigen Beispielen gibt "LDAP:" den LDAP-Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="90f17-127">In the examples above, "LDAP:" specifies the LDAP provider.</span></span> <span data-ttu-id="90f17-128">"GC:" verwendet den LDAP-Anbieter, um eine Bindung mit dem globalen Katalog Dienst herzustellen, um schnelle Abfragen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="90f17-128">"GC:" uses the LDAP provider to bind to the Global Catalog service to execute fast queries.</span></span>

<span data-ttu-id="90f17-129">" &lt; Hostname &gt; " gibt den Server an, an den die Bindung erfolgen soll, und ist optional.</span><span class="sxs-lookup"><span data-stu-id="90f17-129">"&lt;host name&gt;" specifies the server to bind to and is optional.</span></span> <span data-ttu-id="90f17-130">Geben Sie nach Möglichkeit keinen Server an.</span><span class="sxs-lookup"><span data-stu-id="90f17-130">If possible, do not specify a server.</span></span> <span data-ttu-id="90f17-131">Es ist auch möglich, eine Bindung an ein Objekt in einer anderen Domäne herzustellen.</span><span class="sxs-lookup"><span data-stu-id="90f17-131">It is also possible to bind to an object in a different domain.</span></span> <span data-ttu-id="90f17-132">Übergeben Sie dazu den DNS-Namen (Domain Name System) der Zieldomäne für " &lt; Hostname &gt; ".</span><span class="sxs-lookup"><span data-stu-id="90f17-132">To do this pass the domain naming system (DNS) name of the target domain for "&lt;host name&gt;".</span></span> <span data-ttu-id="90f17-133">Um z. b. an den Benutzer Container in der Domäne2-Domäne von fabrikam.com zu binden, ist die Bindungs Zeichenfolge "LDAP://domain2.fabrikam.com/cn=users,DC=domain2,DC=fabrikam,DC=com".</span><span class="sxs-lookup"><span data-stu-id="90f17-133">For example, to bind to the Users container in the domain2 domain of fabrikam.com, the binding string would be "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span></span>

<span data-ttu-id="90f17-134">" &lt; Object Name &gt; " stellt ein bestimmtes Objekt in Active Directory Domain Services dar.</span><span class="sxs-lookup"><span data-stu-id="90f17-134">"&lt;object name&gt;" represents a specific object in Active Directory Domain Services.</span></span> <span data-ttu-id="90f17-135">Der Objektname kann ein definierter Name oder eine Objekt-GUID sein.</span><span class="sxs-lookup"><span data-stu-id="90f17-135">The object name can be a distinguished name or an object GUID.</span></span>

<span data-ttu-id="90f17-136">Weitere Informationen zu LDAP-Bindungs Zeichenfolgen finden Sie unter [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span><span class="sxs-lookup"><span data-stu-id="90f17-136">For more information about LDAP binding strings, see [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span></span>

<span data-ttu-id="90f17-137">Für Windows NT 4,0 wird der WinNT-Anbieter für den Zugriff auf Verzeichnis Daten wie z. b. Benutzer, Benutzergruppen, Computer, Dienste und andere Netzwerk Objekte in Windows 2000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="90f17-137">For Windows NT 4.0, the WinNT provider is used for access to directory data such as users, user groups, computers, services, and other network objects in the Windows 2000.</span></span> <span data-ttu-id="90f17-138">Der WinNT-Anbieter unter Windows 2000 und spätere Systeme verfügt im Vergleich zum LDAP-Anbieter über eingeschränkte Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="90f17-138">The WinNT provider on Windows 2000 and later systems has limited functionality compared to the LDAP provider.</span></span> <span data-ttu-id="90f17-139">Weitere Informationen zu WinNT-Bindungs Zeichenfolgen finden Sie unter [Winnt ADsPath](/windows/desktop/ADSI/winnt-adspath).</span><span class="sxs-lookup"><span data-stu-id="90f17-139">For more information about WinNT binding strings, see [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span></span>

<span data-ttu-id="90f17-140">Ein ADsPath-Element von "LDAP://" oder "GC://" kann verwendet werden, um eine Bindung zum Stammverzeichnis des Namespaces herzustellen.</span><span class="sxs-lookup"><span data-stu-id="90f17-140">An ADsPath of "LDAP://" or "GC://" can be used to bind to the root of the namespace.</span></span> <span data-ttu-id="90f17-141">Wenn das angegebene Namespace Objekt an den Stamm des Namespaces gebunden ist, enthält es keine Eigenschaften und enthält das Domänen Objekt für LDAP und ein Container Objekt, das ein partielles Replikat aller Domänen in der Gesamtstruktur für GC enthält.</span><span class="sxs-lookup"><span data-stu-id="90f17-141">When bound to the root of the namespace, the supplied namespace object contains no properties and contains the domain object for LDAP and a container object containing a partial replica of all domains in the forest for GC.</span></span>

<span data-ttu-id="90f17-142">Weitere Informationen zum Binden in Active Directory Domain Services finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="90f17-142">For more information about binding in Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="90f17-143">Server lose Bindung und RootDSE</span><span class="sxs-lookup"><span data-stu-id="90f17-143">Serverless Binding and RootDSE</span></span>](serverless-binding-and-rootdse.md)
-   [<span data-ttu-id="90f17-144">Binden an den globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="90f17-144">Binding to the Global Catalog</span></span>](binding-to-the-global-catalog.md)
-   [<span data-ttu-id="90f17-145">Verwenden von objectGUID für die Bindung an ein Objekt</span><span class="sxs-lookup"><span data-stu-id="90f17-145">Using objectGUID to Bind to an Object</span></span>](using-objectguid-to-bind-to-an-object.md)
-   [<span data-ttu-id="90f17-146">Binden an Well-Known Objekte mithilfe von wkguid</span><span class="sxs-lookup"><span data-stu-id="90f17-146">Binding to Well-Known Objects Using WKGUID</span></span>](binding-to-well-known-objects-using-wkguid.md)
-   [<span data-ttu-id="90f17-147">Binden an ein Objekt mithilfe einer sid</span><span class="sxs-lookup"><span data-stu-id="90f17-147">Binding to an Object Using a SID</span></span>](binding-to-an-object-using-a-sid.md)
-   [<span data-ttu-id="90f17-148">Aktivieren der Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="90f17-148">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [<span data-ttu-id="90f17-149">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="90f17-149">Authentication</span></span>](authentication.md)

 

 
