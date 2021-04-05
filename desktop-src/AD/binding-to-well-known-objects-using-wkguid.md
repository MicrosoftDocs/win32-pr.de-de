---
title: Binden an Well-Known Objekte mithilfe von wkguid
description: In diesem Thema wird gezeigt, wie mithilfe der wkguid-Bindungs Zeichenfolge an Objekte gebunden wird.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Binden an Well-Known Objekte mithilfe von wkguid AD
- Active Directory mithilfe von, Bindung und Verwendung von wkguid für die Bindung an bekannte Objekte
- bekannte Objekte (AD)
- bekannte Objekte (AD), binden an mithilfe von wkguid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724648"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a><span data-ttu-id="a3b3f-107">Binden an Well-Known Objekte mithilfe von wkguid</span><span class="sxs-lookup"><span data-stu-id="a3b3f-107">Binding to Well-Known Objects Using WKGUID</span></span>

<span data-ttu-id="a3b3f-108">Container können über ein oder mehrere wichtige unter Objekte verfügen, die umbenannt oder verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-108">Containers can have one, or more, important subobjects that can be renamed or moved.</span></span> <span data-ttu-id="a3b3f-109">Es kann schwierig sein, diese unter Objekte zu verfolgen und richtige Bindungs Zeichenfolgen zu erstellen, insbesondere, wenn Sie umbenannt oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-109">It can be difficult to track these subobjects and build correct binding strings for them, especially if they are renamed or moved.</span></span>

<span data-ttu-id="a3b3f-110">Um die Umbenennungs sichere Bindung an diese Objekte innerhalb dieser Container zu unterstützen, Active Directory Domain Services über zwei Attribute verfügen: **wellKnownObjects** und **otherWellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-110">To support rename-safe binding to these objects within these containers, Active Directory Domain Services have two attributes: **wellKnownObjects** and **otherWellKnownObjects**.</span></span> <span data-ttu-id="a3b3f-111">Diese Attribute verfügen über eine Attribut Syntax von adstype \_ DN \_ with \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-111">These attributes have an attribute syntax of ADSTYPE\_DN\_WITH\_BINARY.</span></span> <span data-ttu-id="a3b3f-112">Sie lassen mehrere Werte zu und enthalten die GUID/DN-Tupel bekannter Objekte in den Containern, für die Sie festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-112">They allow multiple values and contain the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="a3b3f-113">Der Active Directory Server verwaltet den Distinguished Name-Teil jedes **wellKnownObjects** -und **otherWellKnownObjects** -Eintrags, sodass er den aktuellen Distinguished Name des Objekts enthält, das beim Erstellen des Eintrags angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-113">The Active Directory server maintains the distinguished name portion of each **wellKnownObjects** and **otherWellKnownObjects** entry so that it contains the current distinguished name of the object specified when the entry was created.</span></span>

<span data-ttu-id="a3b3f-114">Die **otherWellKnownObjects** -Eigenschaft kann für jedes beliebige Objekt festgelegt und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-114">The **otherWellKnownObjects** property can be set and used on any object.</span></span>

<span data-ttu-id="a3b3f-115">Die **wellKnownObjects** -Eigenschaft wird für die Domänen DNS-und Konfigurations Container verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-115">The **wellKnownObjects** property is used on the domainDNS and configuration containers.</span></span> <span data-ttu-id="a3b3f-116">Die **wellKnownObjects** -Eigenschaft ist eine reine System Eigenschaft und kann nur vom Betriebssystem geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-116">The **wellKnownObjects** property is a system-only property and can only be modified by the operating system.</span></span>

<span data-ttu-id="a3b3f-117">Der **domainDns** -Container verfügt über die folgenden bekannten Objekte:</span><span class="sxs-lookup"><span data-stu-id="a3b3f-117">The **domainDNS** container has the following well-known objects:</span></span>

-   <span data-ttu-id="a3b3f-118">Benutzer</span><span class="sxs-lookup"><span data-stu-id="a3b3f-118">Users</span></span>
-   <span data-ttu-id="a3b3f-119">Computer</span><span class="sxs-lookup"><span data-stu-id="a3b3f-119">Computers</span></span>
-   <span data-ttu-id="a3b3f-120">System</span><span class="sxs-lookup"><span data-stu-id="a3b3f-120">System</span></span>
-   <span data-ttu-id="a3b3f-121">Domänencontroller</span><span class="sxs-lookup"><span data-stu-id="a3b3f-121">Domain Controllers</span></span>
-   <span data-ttu-id="a3b3f-122">Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="a3b3f-122">Infrastructure</span></span>
-   <span data-ttu-id="a3b3f-123">Gelöschte Objekte</span><span class="sxs-lookup"><span data-stu-id="a3b3f-123">Deleted Objects</span></span>
-   <span data-ttu-id="a3b3f-124">Verloren und gefunden</span><span class="sxs-lookup"><span data-stu-id="a3b3f-124">Lost and Found</span></span>

<span data-ttu-id="a3b3f-125">Der Konfigurations Container verfügt über das bekannte Objekt: Gelöschte Objekte.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-125">The configuration container has the well-known object: Deleted Objects.</span></span>

<span data-ttu-id="a3b3f-126">Diese Objekte befinden sich in jedem **Domänen DNS** -und Konfigurations Container in einem Active Directory-Domäne-Dienst.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-126">These objects are in every **domainDNS** and configuration container in an Active Directory Domain Service.</span></span>

<span data-ttu-id="a3b3f-127">Sie können eine Bindung an ein bekanntes Objekt mithilfe des wkguid-Bindungs Formats herstellen.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-127">You can bind to a well-known object using the WKGUID binding format.</span></span> <span data-ttu-id="a3b3f-128">Die Bindung mit wkguid wird nur in Active Directory Domain Services unterstützt, d. h. im LDAP-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-128">Binding with WKGUID is only supported in Active Directory Domain Services, that is, the LDAP provider.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3b3f-129">Verwenden Sie immer das Bindungs Format wkguid, um eine Bindung an die bekannten Objekte (wie oben) in den Domänen-und Konfigurations Containern herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-129">Always use the WKGUID binding format to bind to the well-known objects, as listed above, in the domain and configuration containers.</span></span> <span data-ttu-id="a3b3f-130">Dadurch wird sichergestellt, dass diese Container auch dann an gebunden werden können, wenn Sie verschoben oder umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-130">This ensures that these containers can be bound to even if they are moved or renamed.</span></span>

 

<span data-ttu-id="a3b3f-131">Das Format der wkguid-Bindungs Zeichenfolge lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a3b3f-131">The WKGUID binding string format is as follows:</span></span>


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



<span data-ttu-id="a3b3f-132">" &lt; Servername &gt; " ist der Name des Verzeichnis Servers.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-132">"&lt;server name&gt;" is the directory server name.</span></span> <span data-ttu-id="a3b3f-133">Der " &lt; Servername &gt; " ist optional.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-133">The "&lt;server name&gt;" is optional.</span></span>

<span data-ttu-id="a3b3f-134">" &lt; XXXXX &gt; " ist die Zeichen folgen Darstellung des hexadezimal Werts der GUID, die das bekannte Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-134">"&lt;XXXXX&gt;" is the string representation of the hexadecimal value of the GUID that represents the well-known object.</span></span> <span data-ttu-id="a3b3f-135">Die GUID-Zeichenfolge wird im Formular "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" angegeben und ist nicht identisch mit der GUID-Zeichenfolge, die von der [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) -Funktion erstellt wird, die das Format "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" annimmt.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-135">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form and is not the same form as the GUID string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, which takes the form "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span></span> <span data-ttu-id="a3b3f-136">Weitere Informationen und ein Codebeispiel, das zeigt, wie eine bindbare Zeichenfolge aus einer GUID erstellt wird, finden Sie unter [Beispielcode zum Erstellen einer typfähigen Zeichen folgen Darstellung einer GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="a3b3f-136">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span>

<span data-ttu-id="a3b3f-137">Um an ein Objekt zu binden, das in **otherWellKnownObjects** in einem Objekt angegeben ist, geben Sie " &lt; XXXXX &gt; " als Bindungs Zeichenfolgen-Form der bekannten Objekt-GUID des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-137">To bind to an object specified in **otherWellKnownObjects** in an object, specify "&lt;XXXXX&gt;" as the bind string form of the well-known object GUID of the object.</span></span> <span data-ttu-id="a3b3f-138">Weitere Informationen finden Sie unter [Lesen der objectGUID eines Objekts und Erstellen einer Zeichen folgen Darstellung der GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span><span class="sxs-lookup"><span data-stu-id="a3b3f-138">For more information, see [Reading an Object's objectGUID and Creating a String Representation of the GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span></span> <span data-ttu-id="a3b3f-139">Weitere Informationen zum Festlegen der **otherWellKnownObjects** -Eigenschaft für Objekte finden Sie unter [Aktivieren der Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span><span class="sxs-lookup"><span data-stu-id="a3b3f-139">For more information about setting the **otherWellKnownObjects** property on objects, see [Enabling Rename-Safe Binding with the otherWellKnownObjects Property](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span></span>

<span data-ttu-id="a3b3f-140">Geben Sie zum Binden an ein in **wellKnownObjects** in domainDNS oder in Konfigurations Containern angegebenes Objekt " &lt; XXXXX &gt; " als eine der folgenden Konstanten an, die in der folgenden Tabelle aufgeführt sind, wie in "NTDSAPI. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-140">To bind to an object specified in **wellKnownObjects** in domainDNS or configuration containers, specify "&lt;XXXXX&gt;" as one of the following constants, listed in the following table, as defined in Ntdsapi.h.</span></span>



| <span data-ttu-id="a3b3f-141">Container</span><span class="sxs-lookup"><span data-stu-id="a3b3f-141">Container</span></span>          | <span data-ttu-id="a3b3f-142">GUID-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a3b3f-142">GUID Identifier</span></span>                         |
|--------------------|-----------------------------------------|
| <span data-ttu-id="a3b3f-143">Benutzer</span><span class="sxs-lookup"><span data-stu-id="a3b3f-143">Users</span></span>              | <span data-ttu-id="a3b3f-144">GUID- \_ Benutzer \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="a3b3f-144">GUID\_USERS\_CONTAINER\_W</span></span>               |
| <span data-ttu-id="a3b3f-145">Computer</span><span class="sxs-lookup"><span data-stu-id="a3b3f-145">Computers</span></span>          | <span data-ttu-id="a3b3f-146">GUID- \_ computrs- \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="a3b3f-146">GUID\_COMPUTRS\_CONTAINER\_W</span></span>            |
| <span data-ttu-id="a3b3f-147">System</span><span class="sxs-lookup"><span data-stu-id="a3b3f-147">System</span></span>             | <span data-ttu-id="a3b3f-148">GUID- \_ Systeme \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="a3b3f-148">GUID\_SYSTEMS\_CONTAINER\_W</span></span>             |
| <span data-ttu-id="a3b3f-149">Domänencontroller</span><span class="sxs-lookup"><span data-stu-id="a3b3f-149">Domain Controllers</span></span> | <span data-ttu-id="a3b3f-150">GUID- \_ Domänen \_ Controller \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="a3b3f-150">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span> |
| <span data-ttu-id="a3b3f-151">Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="a3b3f-151">Infrastructure</span></span>     | <span data-ttu-id="a3b3f-152">GUID- \_ Infrastruktur \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="a3b3f-152">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>      |
| <span data-ttu-id="a3b3f-153">Gelöschte Objekte</span><span class="sxs-lookup"><span data-stu-id="a3b3f-153">Deleted Objects</span></span>    | <span data-ttu-id="a3b3f-154">GUID- \_ Gelöschte \_ Objekte \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="a3b3f-154">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>    |
| <span data-ttu-id="a3b3f-155">Verloren und gefunden</span><span class="sxs-lookup"><span data-stu-id="a3b3f-155">Lost and Found</span></span>     | <span data-ttu-id="a3b3f-156">GUID \_ LostAndFound- \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="a3b3f-156">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>        |



 

<span data-ttu-id="a3b3f-157">Wenn Sie z. b. eine Bindung an den Benutzer Container in einer Domäne herstellen möchten, geben Sie den **GUID- \_ Benutzer \_ Container \_ W** als " &lt; XXXXX &gt; " an.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-157">For example, to bind to the user container in a domain, specify **GUID\_USERS\_CONTAINER\_W** as "&lt;XXXXX&gt;".</span></span>

<span data-ttu-id="a3b3f-158">" &lt; Container DN &gt; " ist der Distinguished Name des Container Objekts, für das dieses Objekt in seiner **wellKnownObjects** -Eigenschaft als Wert dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-158">"&lt;container DN&gt;" is the distinguished name of the container object that has this object represented as a value in its **wellKnownObjects** property.</span></span> <span data-ttu-id="a3b3f-159">Wenn Sie z. b. eine Bindung an den Benutzer Container in einer Domäne herstellen möchten, geben Sie den Distinguished Name der Domäne als " &lt; Container-DN &gt; " an.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-159">For example, to bind to the users container in a domain, specify the domain distinguished name as the "&lt;container DN&gt;".</span></span>

<span data-ttu-id="a3b3f-160">Um z. b. an den Benutzer Container der Domäne fabrikam.com zu binden, verwenden Sie die folgende Bindungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a3b3f-160">For example, to bind to the users container of the domain Fabrikam.com, use the following binding string.</span></span>

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

<span data-ttu-id="a3b3f-161">Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie eine Bindung an eine bekannte GUID finden, finden Sie unter [Beispielcode für die Bindung an bekannte Objekte](example-code-for-binding-to-well-known-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a3b3f-161">For more information and a code example that shows how to bind to a well-known GUID, see [Example Code for Binding to Well Known Objects](example-code-for-binding-to-well-known-objects.md).</span></span>

 

 