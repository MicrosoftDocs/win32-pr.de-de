---
title: Binden an den globalen Katalog
description: Der globale Katalog ist ein Namespace, der Verzeichnis Daten für alle Domänen in einer Gesamtstruktur enthält.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Binden an den globalen Katalog AD
- globaler Katalog AD, Bindung an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038801"
---
# <a name="binding-to-the-global-catalog"></a><span data-ttu-id="4c35f-105">Binden an den globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="4c35f-105">Binding to the Global Catalog</span></span>

<span data-ttu-id="4c35f-106">Der globale Katalog ist ein Namespace, der Verzeichnis Daten für alle Domänen in einer Gesamtstruktur enthält.</span><span class="sxs-lookup"><span data-stu-id="4c35f-106">The Global Catalog is a namespace that contains directory data for all domains in a forest.</span></span> <span data-ttu-id="4c35f-107">Der globale Katalog enthält ein partielles Replikat jedes Domänen Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="4c35f-107">The Global Catalog contains a partial replica of every domain directory.</span></span> <span data-ttu-id="4c35f-108">Sie enthält einen Eintrag für jedes Objekt in der Enterprise-Gesamtstruktur, enthält jedoch nicht alle Eigenschaften der einzelnen Objekte.</span><span class="sxs-lookup"><span data-stu-id="4c35f-108">It contains an entry for every object in the enterprise forest, but does not contain all the properties of each object.</span></span> <span data-ttu-id="4c35f-109">Stattdessen enthält Sie nur die Eigenschaften, die für die Einbindung in den globalen Katalog angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4c35f-109">Instead, it contains only the properties specified for inclusion in the Global Catalog.</span></span>

<span data-ttu-id="4c35f-110">Der globale Katalog wird auf bestimmten Servern im gesamten Unternehmen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4c35f-110">The Global Catalog is stored on specific servers throughout the enterprise.</span></span> <span data-ttu-id="4c35f-111">Nur Domänen Controller können als globale Katalogserver fungieren.</span><span class="sxs-lookup"><span data-stu-id="4c35f-111">Only domain controllers can serve as Global Catalog servers.</span></span> <span data-ttu-id="4c35f-112">Administratoren geben mithilfe der Active Directory Standorte und Dienste-Manager an, ob ein bestimmter Domänen Controller einen globalen Katalog enthält.</span><span class="sxs-lookup"><span data-stu-id="4c35f-112">Administrators indicate whether a given domain controller holds a Global Catalog by using the Active Directory Sites and Services Manager.</span></span>

<span data-ttu-id="4c35f-113">Verwenden Sie zum Binden an den globalen Katalog mit ADSI den "GC:"-Moniker.</span><span class="sxs-lookup"><span data-stu-id="4c35f-113">To bind to the Global Catalog with ADSI, use the "GC:" moniker.</span></span>

<span data-ttu-id="4c35f-114">Es gibt zwei Möglichkeiten, eine Bindung zum globalen Katalog herzustellen, um eine Suche in einer Gesamtstruktur durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="4c35f-114">There are two ways to bind to the Global Catalog to perform a search in a forest:</span></span>

-   <span data-ttu-id="4c35f-115">Binden Sie an das Stamm Objekt des Unternehmens, um alle Domänen in der Gesamtstruktur zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="4c35f-115">Bind to the enterprise root object to search across all domains in the forest.</span></span>
-   <span data-ttu-id="4c35f-116">Binden an ein bestimmtes Objekt, um das Objekt und seine untergeordneten Elemente zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="4c35f-116">Bind to a specific object to search that object and its children.</span></span> <span data-ttu-id="4c35f-117">Wenn Sie z. b. eine Bindung an eine Domäne herstellen, die in einer Domänen Struktur in der Gesamtstruktur über zwei Domänen verfügt, können Sie diese drei Domänen durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="4c35f-117">For example, if you bind to a domain that has two domains beneath it in a domain tree in the forest, you can search across those three domains.</span></span> <span data-ttu-id="4c35f-118">Beachten Sie, dass der Distinguished Name für das Objekt, an das die Bindung erfolgen soll, identisch mit dem Distinguished Name ist, der zum Binden an den "LDAP:"-Namespace verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c35f-118">Be aware that the distinguished name for the object to bind to is exactly the same as the distinguished name used to bind to the "LDAP:" namespace.</span></span> <span data-ttu-id="4c35f-119">Beachten Sie, dass "LDAP:" ein vollständiges Replikat einer einzelnen Domäne ist und dass "GC:" ein partielles Replikat aller Domänen in der Gesamtstruktur ist.</span><span class="sxs-lookup"><span data-stu-id="4c35f-119">Recall that "LDAP:" is a full replica of a single domain and that "GC:" is a partial replica of all domains in the forest.</span></span>

<span data-ttu-id="4c35f-120">Ebenso wie der "LDAP:"-Moniker können Sie eine Server lose Bindung oder eine Bindung an einen bestimmten globalen Katalogserver verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c35f-120">As with the "LDAP:" moniker, you can use serverless binding or bind to a specific Global Catalog server.</span></span> <span data-ttu-id="4c35f-121">Wenn Sie in der aktuellen Gesamtstruktur suchen, verwenden Sie die Server lose Bindung.</span><span class="sxs-lookup"><span data-stu-id="4c35f-121">If searching in the current forest, use serverless binding.</span></span> <span data-ttu-id="4c35f-122">Wenn Sie jedoch in einer anderen Gesamtstruktur suchen, geben Sie entweder einen Domänen Namen oder einen globalen Katalogserver an, an den die Bindung erfolgen soll, wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c35f-122">However, if searching in another forest, specify either a domain name or a Global Catalog server to bind to, such as shown in the following examples.</span></span>

<span data-ttu-id="4c35f-123">Binden mithilfe des Domänen Namens:</span><span class="sxs-lookup"><span data-stu-id="4c35f-123">Bind using the domain name:</span></span>

``` syntax
GC://fabrikam.com
```

<span data-ttu-id="4c35f-124">Binden mit dem Servernamen:</span><span class="sxs-lookup"><span data-stu-id="4c35f-124">Bind using the server name:</span></span>

``` syntax
GC://servername
```

<span data-ttu-id="4c35f-125">Sie können auch eine Bindung an ein bestimmtes Objekt innerhalb des globalen Katalogs herstellen.</span><span class="sxs-lookup"><span data-stu-id="4c35f-125">You can also bind to a specific object within the Global Catalog.</span></span> <span data-ttu-id="4c35f-126">Verwenden Sie das folgende Format, um eine Bindung zum Sales-Objekt in der Fabrikam-Domäne herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4c35f-126">To bind to the sales object in the fabrikam domain, use the following format.</span></span>

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="4c35f-127">Oder verwenden Sie das folgende Format, um eine Bindung an das Sales-Objekt auf dem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4c35f-127">Or, to bind to the sales object on the server, use the following format.</span></span>

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="4c35f-128">**So durchsuchen Sie die gesamte Gesamtstruktur**</span><span class="sxs-lookup"><span data-stu-id="4c35f-128">**To search the entire forest**</span></span>

1.  <span data-ttu-id="4c35f-129">Binden Sie an den Stamm des globalen Katalog-Namespace.</span><span class="sxs-lookup"><span data-stu-id="4c35f-129">Bind to the root of the Global Catalog namespace.</span></span>
2.  <span data-ttu-id="4c35f-130">Listet den globalen Katalog Container auf.</span><span class="sxs-lookup"><span data-stu-id="4c35f-130">Enumerate the Global Catalog container.</span></span> <span data-ttu-id="4c35f-131">Der Container für den globalen Katalog enthält ein einzelnes-Objekt, das Sie zum Durchsuchen der gesamten Gesamtstruktur verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4c35f-131">The Global Catalog container contains a single object that you can use to search the entire forest.</span></span>
3.  <span data-ttu-id="4c35f-132">Verwenden Sie das-Objekt im Container, um die Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4c35f-132">Use the object in the container to perform the search.</span></span> <span data-ttu-id="4c35f-133">In C/C++ wird [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aufgerufen, um einen [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) -Zeiger auf das Objekt zu erhalten, sodass Sie die **IDirectorySearch** -Schnittstelle zum Durchführen der Suche verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4c35f-133">In C/C++, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer on the object so that you can use the **IDirectorySearch** interface to perform the search.</span></span> <span data-ttu-id="4c35f-134">Verwenden Sie in Visual Basic das Objekt, das von der-Enumeration in der ADO-Abfrage zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4c35f-134">In Visual Basic, use the object returned from the enumeration in your ADO query.</span></span>

<span data-ttu-id="4c35f-135">Um die globalen Katalogserver an einem Standort aufzulisten, führen Sie eine LDAP-Unterstruktur Suche von "CN = <yoursite> , CN = Sites <DN of the configurationNamingContext> " mithilfe der folgenden Filter Zeichenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="4c35f-135">To enumerate the Global Catalog servers in a site, perform an LDAP subtree search of "cn=<yoursite>,cn=sites,<DN of the configurationNamingContext>", using the following filter string.</span></span>

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

<span data-ttu-id="4c35f-136">Dieser Filter verwendet das **LDAP \_ \_ -Vergleichs \_ Regel \_ -Bit und** den abgleichsregeloperator (1.2.840.113556.1.4.803), um **NTDSDSA** -Objekte zu suchen, für die das niedrige Bit in der Bitmaske des **options** -Attributs festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4c35f-136">This filter uses the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator (1.2.840.113556.1.4.803) to find **nTDSDSA** objects that have the low-order bit set in the bitmask of the **options** attribute.</span></span> <span data-ttu-id="4c35f-137">Das niedrig wertige Bit, das der in NTDSAPI. h definierten **\_ \_ \_ GC** -Konstante entspricht, identifiziert das **NTDSDSA** -Objekt eines globalen Katalog Servers.</span><span class="sxs-lookup"><span data-stu-id="4c35f-137">The low-order bit, which corresponds to the **NTDSDSA\_OPT\_IS\_GC** constant defined in Ntdsapi.h, identifies the **nTDSDSA** object of a Global Catalog server.</span></span> <span data-ttu-id="4c35f-138">Weitere Informationen zu abgleichsregeln finden Sie unter [Such Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="4c35f-138">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="4c35f-139">Das übergeordnete Element des **NTDSDSA** -Objekts ist das Server Objekt, und die **dNSHostName** -Eigenschaft des Server Objekts ist der DNS-Name des globalen Katalog Servers.</span><span class="sxs-lookup"><span data-stu-id="4c35f-139">The parent of the **nTDSDSA** object is the server object, and the **dNSHostName** property of the server object is the DNS name of the Global Catalog server.</span></span>

<span data-ttu-id="4c35f-140">Sie können keine \# Definieren von Konstanten wie **NTDSDSA \_ opt \_ is \_ GC** und **LDAP \_ Matching \_ rule \_ Bit \_ und** direkt in einer Suchfilter Zeichenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c35f-140">You cannot use \#define constants such as **NTDSDSA\_OPT\_IS\_GC** and **LDAP\_MATCHING\_RULE\_BIT\_AND** directly in a search filter string.</span></span> <span data-ttu-id="4c35f-141">Allerdings können Sie diese Konstanten als Argumente für eine Funktion wie z. [**b. "tauprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) " verwenden, um die Konstanten Werte in eine Filter Zeichenfolge einzufügen.</span><span class="sxs-lookup"><span data-stu-id="4c35f-141">However, you could use these constants as arguments to a function such as [**swprintf\_s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) to insert the constant values into a filter string.</span></span>

<span data-ttu-id="4c35f-142">Der globale Katalog stellt nicht die gesamte Gesamtstruktur Struktur dar.</span><span class="sxs-lookup"><span data-stu-id="4c35f-142">The global catalog does not represent the entire forest tree structure.</span></span> <span data-ttu-id="4c35f-143">Beispielsweise können Sie davon ausgehen, dass im folgenden Codebeispiel alle Domänen in der Gesamtstruktur und alle untergeordneten Objekte der einzelnen Domänen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="4c35f-143">For example, you might expect that the following code example would enumerate all of the domains in the forest and all child objects of each domain.</span></span> <span data-ttu-id="4c35f-144">Tatsächlich werden in Wirklichkeit alle Domänen in der Gesamtstruktur aufgelistet, aber keines der aufgelisteten Domänen Objekte enthält untergeordnete Elemente.</span><span class="sxs-lookup"><span data-stu-id="4c35f-144">In reality, what it actually does is enumerate all of the domains in the forest, but none of the enumerated domain objects contain any children.</span></span> <span data-ttu-id="4c35f-145">Dies ist eine Einschränkung des globalen Katalogs.</span><span class="sxs-lookup"><span data-stu-id="4c35f-145">This is a limitation of the global catalog.</span></span>


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="4c35f-146">Um dies zu korrigieren, ist es erforderlich, eine Bindung an jedes Domänen Objekt herzustellen und dann die untergeordneten Objekte der einzelnen Domänen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="4c35f-146">To correct this, it is necessary to bind to each domain object and then enumerate the child objects of each domain.</span></span> <span data-ttu-id="4c35f-147">Das richtige Verfahren wird im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c35f-147">The proper technique is shown in the following code example.</span></span>


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="4c35f-148">Weitere Informationen und Codebeispiele, die zeigen, wie eine ganze Gesamtstruktur durchsucht wird, finden Sie unter [Beispielcode zum Durchsuchen einer](example-code-for-searching-a-forest.md)Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="4c35f-148">For more information and code examples that show how to search an entire forest, see [Example Code for Searching a Forest](example-code-for-searching-a-forest.md).</span></span>

 

 