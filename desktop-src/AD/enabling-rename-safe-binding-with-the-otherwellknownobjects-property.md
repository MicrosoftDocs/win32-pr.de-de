---
title: Aktivieren der Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft
description: Objekte der Container Klasse verfügen über ein OtherWellKnownObjects-Attribut, das Sie verwenden können, um eine GUID mit dem Distinguished Name (DN) eines untergeordneten Objekts im Container zuzuordnen.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- otherWellKnownObjects (Eigenschaft)
- otherWellKnownObjects-Eigenschaft, Verwendung für Umbenennungs sichere Bindung
- Active Directory, verwenden, Bindung, Umbenennungs sichere Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206274"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a><span data-ttu-id="a806d-106">Aktivieren der Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a806d-106">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>

<span data-ttu-id="a806d-107">Objekte der Container Klasse verfügen über ein **otherWellKnownObjects** -Attribut, das Sie verwenden können, um eine GUID mit dem Distinguished Name (DN) eines untergeordneten Objekts im Container zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a806d-107">Objects of the Container class have an **otherWellKnownObjects** attribute that you can use to associate a GUID with the distinguished name (DN) of a child object in the container.</span></span> <span data-ttu-id="a806d-108">Wenn das untergeordnete Objekt verschoben oder umbenannt wird, aktualisiert der Active Directory Server den DN im **otherWellKnownObjects** -Wert für dieses untergeordnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="a806d-108">If the child object is moved or renamed, the Active Directory server updates the DN in the **otherWellKnownObjects** value for that child object.</span></span> <span data-ttu-id="a806d-109">Dies ermöglicht die Verwendung des wkguid-Bindungs Features zum Binden an das untergeordnete Objekt mit der GUID und dem DN des Containers anstelle des DN des untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="a806d-109">This enables use of the WKGUID binding feature to bind to the child object using the GUID and the DN of the container rather than the child object's DN.</span></span>

<span data-ttu-id="a806d-110">Das **otherWellKnownObjects** -Attribut entspricht dem **wellKnownObjects** -Attribut, mit dem Unterschied, dass Anwendungen und Dienste einen **otherWellKnownObjects** -Wert schreiben können, aber nur das System kann **wellKnownObjects** schreiben.</span><span class="sxs-lookup"><span data-stu-id="a806d-110">The **otherWellKnownObjects** attribute is equivalent to the **wellKnownObjects** attribute except that applications and services can write an **otherWellKnownObjects** value, but only the system can write **wellKnownObjects**.</span></span>

<span data-ttu-id="a806d-111">Die Verwendung des **otherWellKnownObjects** -Attributs und der wkguid-Bindung ist in den folgenden Situationen vorteilhaft, in denen eine Umbenennungs sichere Bindung in Bezug auf ein bestimmtes Container Objekt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a806d-111">Using **otherWellKnownObjects** attribute and WKGUID binding is beneficial in the following situations where rename-safe binding is required in relation to a specific container object.</span></span>

<span data-ttu-id="a806d-112">, Wenn ein Container Objekt andere wichtige Objekte enthält, oder, wenn wichtige Objekte umbenannt oder verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="a806d-112">If a container object contains other important objects, or if important objects can be renamed or moved.</span></span>

<span data-ttu-id="a806d-113">, Wenn die wichtigen Objekte für jede Instanz des Container Objekts vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a806d-113">If the important objects exist for each instance of the container object.</span></span> <span data-ttu-id="a806d-114">Beispielsweise verwendet das System das **wellKnownObjects** -Attribut jedes **domainDns** -Objekts, um einen Wert für den Benutzer Container zu speichern, der in jeder Instanz eines **domainDns** -Objekts vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a806d-114">For example, the system uses the **wellKnownObjects** attribute of each **domainDNS** object to store a value for the Users container, which exists in every instance of a **domainDNS** object.</span></span> <span data-ttu-id="a806d-115">Dadurch können Anwendungen auf Umbenennungs sichere Weise eine Bindung an den Benutzer Container herstellen, indem Sie die bekannte GUID und den DN des **domainDns** -Containers angeben.</span><span class="sxs-lookup"><span data-stu-id="a806d-115">This enables applications to bind to the Users container in a rename-safe way by specifying the well-known GUID and the DN of the **domainDNS** container.</span></span> <span data-ttu-id="a806d-116">Anwendungen können das **otherWellKnownObjects** -Attribut eines Containers ähnlich verwenden.</span><span class="sxs-lookup"><span data-stu-id="a806d-116">Applications can use a container's **otherWellKnownObjects** attribute similarly.</span></span>

<span data-ttu-id="a806d-117">Wenn Sie für die wichtigen Objekte eine Umbenennungs sichere Bindung und/oder Suchfunktion benötigen.</span><span class="sxs-lookup"><span data-stu-id="a806d-117">If you require rename-safe binding and/or search capability on the important objects.</span></span>

<span data-ttu-id="a806d-118">**So fügen Sie Umbenennungs sichere Bindungs-und Suchfunktionen hinzu**</span><span class="sxs-lookup"><span data-stu-id="a806d-118">**To add rename-safe binding and search capabilities**</span></span>

1.  <span data-ttu-id="a806d-119">Fügen Sie der **otherWellKnownObjects** -Eigenschaft des Container Objekts einen Wert hinzu, wenn das wichtige Objekt in diesem Container erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a806d-119">Add a value to the **otherWellKnownObjects** property of the container object when the important object is created within that container.</span></span> <span data-ttu-id="a806d-120">Der Wert enthält die GUID, die das bekannte Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a806d-120">The value contains the GUID that represents the well-known object.</span></span> <span data-ttu-id="a806d-121">Beachten Sie, dass es sich hierbei nicht um die **objectGUID** und den **unterscheidbaren Namen** für dieses Objekt handelt.</span><span class="sxs-lookup"><span data-stu-id="a806d-121">Be aware that this is not the **objectGUID** and the **distinguishedName** for that object.</span></span>
2.  <span data-ttu-id="a806d-122">Verwenden Sie das Bindungs Feature von wkguid, um das wichtige Objekt zu binden oder zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="a806d-122">Use the WKGUID binding feature to bind to or search the important object.</span></span>

<span data-ttu-id="a806d-123">Das **otherWellKnownObjects** -Attribut kann mehrere Werte aufweisen und die GUID/DN-Tupel bekannter Objekte in den Containern enthalten, für die Sie festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="a806d-123">The **otherWellKnownObjects** attribute can have multiple values and contains the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="a806d-124">Das **otherWellKnownObjects** -Attribut verfügt über die DNWithBinary-Syntax, in der die Werte die folgende Form aufweisen:</span><span class="sxs-lookup"><span data-stu-id="a806d-124">The **otherWellKnownObjects** attribute has the DNWithBinary syntax in which values have the following form:</span></span>


```C++
B:<char count>:<well known GUID>:<object DN>
```



<span data-ttu-id="a806d-125">In diesem Beispiel ist " &lt; char Count &gt; " die Anzahl von hexadezimalen Ziffern in " &lt; well known GUID &gt; 32" (Anzahl der hexadezimalen Ziffern in einer GUID) für " **otherWellKnownObjects** " und " **wellKnownObjects**".</span><span class="sxs-lookup"><span data-stu-id="a806d-125">In this example, "&lt;char count&gt;" is the count of hexadecimal digits in "&lt;well known GUID&gt;", which is 32 (number of hex digits in a GUID) for both **otherWellKnownObjects** and **wellKnownObjects**.</span></span> <span data-ttu-id="a806d-126">" &lt; well known GUID &gt; " ist die hexadezimale Ziffern Darstellung der bekannten GUID.</span><span class="sxs-lookup"><span data-stu-id="a806d-126">"&lt;well known GUID&gt;" is the hexadecimal digit representation of the well-known GUID.</span></span> <span data-ttu-id="a806d-127">" &lt; Object DN &gt; " ist der Distinguished Name des Objekts, das durch diesen WKO-Wert dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a806d-127">"&lt;object DN&gt;" is the distinguished name of the object represented by this WKO value.</span></span> <span data-ttu-id="a806d-128">Der Server verwaltet den objectdn-Teil jedes **wellKnownObjects** -und **otherWellKnownObjects** -Werts, sodass er den aktuellen Distinguished Name des Objekts enthält, das ursprünglich beim Erstellen des Werts angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a806d-128">The server maintains the ObjectDN portion of each **wellKnownObjects** and **otherWellKnownObjects** value so that it contains the current distinguished name of the object originally specified when the value was created.</span></span>

<span data-ttu-id="a806d-129">Wenn {df447b5e-aa5b-11d2-8d53-00c04f79ab81} z. b. die bekannte GUID des MyObject-Objekts im Container MyContainer in der Fabrikam.com-Domäne ist, würde der **otherWellKnownObjects** -Wert die bekannte GUID und den DN von MyObject angeben:</span><span class="sxs-lookup"><span data-stu-id="a806d-129">For example, if {df447b5e-aa5b-11d2-8d53-00c04f79ab81} is the well-known GUID of the MyObject object in the MyContainer container in the Fabrikam.com domain, the **otherWellKnownObjects** value would specify the well-known GUID and the DN of MyObject:</span></span>


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



<span data-ttu-id="a806d-130">Um an dieses Objekt zu binden, verwenden Sie die folgende wkguid-Bindungs Zeichenfolge, die die bekannte GUID des Objekts und den DN des Containers angibt:</span><span class="sxs-lookup"><span data-stu-id="a806d-130">To bind to this object, use the following WKGUID binding string that specifies the well-known GUID of the object and the DN of the container:</span></span>


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



<span data-ttu-id="a806d-131">Nachdem Sie an dieses Objekt gebunden haben, können Sie die ADSI-COM-Schnittstellen verwenden, um das Objekt zu suchen, zu lesen, zu ändern oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a806d-131">After binding to this object, you can use the ADSI COM interfaces to search, read, modify, or delete the object.</span></span>

<span data-ttu-id="a806d-132">Weitere Informationen und ein Codebeispiel, das zeigt, wie ein Objekt zum **otherWellKnownObjects** -Attribut hinzugefügt wird, finden Sie unter [Beispielcode zum Erstellen eines Container Objekts](example-code-for-creating-a-container-object.md).</span><span class="sxs-lookup"><span data-stu-id="a806d-132">For more information and a code example that shows how to add an object to the **otherWellKnownObjects** attribute, see [Example Code for Creating a Container Object](example-code-for-creating-a-container-object.md).</span></span>

 

 




