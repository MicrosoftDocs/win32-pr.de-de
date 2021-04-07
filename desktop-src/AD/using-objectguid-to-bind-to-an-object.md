---
title: Verwenden von objectGUID für die Bindung an ein Objekt
description: Ein definierter Name eines Objekts ändert sich, wenn das Objekt umbenannt oder verschoben wird. der Distinguished Name ist daher kein zuverlässiger Objekt Bezeichner.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Verwenden von objectGUID für die Bindung an ein Objekt AD
- objectGUID AD
- objectGUID AD, verwenden von zum Binden an ein Objekt
- Active Directory mithilfe von, Bindung und Verwendung von objectGUID für die Bindung an das Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038723"
---
# <a name="using-objectguid-to-bind-to-an-object"></a><span data-ttu-id="e3946-107">Verwenden von objectGUID für die Bindung an ein Objekt</span><span class="sxs-lookup"><span data-stu-id="e3946-107">Using objectGUID to Bind to an Object</span></span>

<span data-ttu-id="e3946-108">Ein definierter Name eines Objekts ändert sich, wenn das Objekt umbenannt oder verschoben wird. der Distinguished Name ist daher kein zuverlässiger Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e3946-108">An object distinguished name changes if the object is renamed or moved, therefore the distinguished name is not a reliable object identifier.</span></span> <span data-ttu-id="e3946-109">In Active Directory Domain Services ändert sich die **objectGUID** -Eigenschaft eines Objekts nie, auch wenn das Objekt umbenannt oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e3946-109">In Active Directory Domain Services, an object's **objectGUID** property never changes, even if the object is renamed or moved.</span></span> <span data-ttu-id="e3946-110">Weitere Informationen zu **objectGUID** und Bezeichnerinformationen finden Sie unter [Objektnamen und-Identitäten](object-names-and-identities.md).</span><span class="sxs-lookup"><span data-stu-id="e3946-110">For more information about **objectGUID** and identifiers, see [Object Names and Identities](object-names-and-identities.md).</span></span>

<span data-ttu-id="e3946-111">Der Active Directory LDAP-Anbieter stellt eine Methode bereit, mit der die Objekt-GUID an ein Objekt gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="e3946-111">The Active Directory LDAP provider provides a method to bind to an object using the object GUID.</span></span> <span data-ttu-id="e3946-112">Das Format der Bindungs Zeichenfolge lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e3946-112">The binding string format is as follows:</span></span>


```C++
LDAP://servername/<GUID=XXXXX>
```



<span data-ttu-id="e3946-113">In diesem Beispiel ist "Servername" der Name des Verzeichnis Servers und "xxxxx" die Zeichen folgen Darstellung des hexadezimal Werts der GUID.</span><span class="sxs-lookup"><span data-stu-id="e3946-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the GUID.</span></span> <span data-ttu-id="e3946-114">Der Servername ist optional.</span><span class="sxs-lookup"><span data-stu-id="e3946-114">The "servername" is optional.</span></span> <span data-ttu-id="e3946-115">Die GUID-Zeichenfolge wird im Formular "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" angegeben.</span><span class="sxs-lookup"><span data-stu-id="e3946-115">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form.</span></span> <span data-ttu-id="e3946-116">Die GUID-Zeichenfolge kann auch das Format "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" aufweisen. Dies ist die gleiche Form wie die Zeichenfolge, die von der [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) -Funktion erstellt wurde, ohne die umgebenden geschweiften Klammern " {} ".</span><span class="sxs-lookup"><span data-stu-id="e3946-116">The GUID string can also take the form "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", which is the same form as the string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, without the surrounding braces "{}".</span></span> <span data-ttu-id="e3946-117">Weitere Informationen und ein Codebeispiel, das zeigt, wie eine bindbare Zeichenfolge aus einer GUID erstellt wird, finden Sie unter [Beispielcode zum Erstellen einer typfähigen Zeichen folgen Darstellung einer GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="e3946-117">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span> <span data-ttu-id="e3946-118">Die [**IADs. GUID**](/windows/desktop/ADSI/iads-property-methods) -Eigenschaft kann verwendet werden, um die richtige Zeichen folgen Form der GUID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3946-118">The [**IADs.GUID**](/windows/desktop/ADSI/iads-property-methods) property can be used to retrieve the proper string form of the GUID.</span></span>

<span data-ttu-id="e3946-119">Bei der Bindung mit der Objekt-GUID werden einige [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Methoden und-Eigenschaften nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3946-119">When binding using the object GUID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="e3946-120">Die folgenden **IADs** -Eigenschaften werden von Objekten, die über die Objekt-GUID abgerufen werden, nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e3946-120">The following **IADs** properties are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="e3946-121">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="e3946-121">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="e3946-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="e3946-122">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="e3946-123">**Parent**</span><span class="sxs-lookup"><span data-stu-id="e3946-123">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="e3946-124">Die folgenden **IADsContainer** -Methoden werden von Objekten, die über die Objekt-GUID abgerufen werden, nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e3946-124">The following **IADsContainer** methods are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="e3946-125">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="e3946-125">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="e3946-126">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="e3946-126">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="e3946-127">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="e3946-127">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="e3946-128">**Copyhere**</span><span class="sxs-lookup"><span data-stu-id="e3946-128">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="e3946-129">**Muvehere**</span><span class="sxs-lookup"><span data-stu-id="e3946-129">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="e3946-130">Wenn Sie diese Methoden und Eigenschaften nach dem Binden an ein Objekt mithilfe der Objekt-GUID verwenden möchten, verwenden Sie die [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) -Methode, um den Distinguished Name des Objekts abzurufen, und verwenden Sie dann den Distinguished Name, um die Bindung an das Objekt wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="e3946-130">To use these methods and properties after binding to an object using the object GUID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="e3946-131">Wenn eine Anwendung Bezeichner oder Verweise auf Objekte speichert oder speichert, die in Active Directory Domain Services gespeichert sind, ist die Objekt-GUID der beste Bezeichner, der aus verschiedenen Gründen verwendet werden kann:</span><span class="sxs-lookup"><span data-stu-id="e3946-131">If an application stores or caches identifiers or references to objects stored in Active Directory Domain Services, the object GUID is the best identifier to use for several reasons:</span></span>

-   <span data-ttu-id="e3946-132">Die **objectGUID** -Eigenschaft von für Objekt ändert sich nie, auch wenn das Objekt umbenannt oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e3946-132">The **objectGUID** property of on object never changes even if the object is renamed or moved.</span></span>
-   <span data-ttu-id="e3946-133">Es ist einfach, mithilfe der Objekt-GUID eine Bindung an das Objekt herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e3946-133">It is easy to bind to the object using the object GUID.</span></span>
-   <span data-ttu-id="e3946-134">Wenn das Objekt umbenannt oder verschoben wird, stellt die **objectGUID** -Eigenschaft einen einzelnen Bezeichner bereit, der verwendet werden kann, um das Objekt schnell zu finden und zu identifizieren, anstatt eine Abfrage zu erstellen, die Bedingungen für alle Eigenschaften hat, die das Objekt identifizieren würden.</span><span class="sxs-lookup"><span data-stu-id="e3946-134">If the object is renamed or moved, the **objectGUID** property provides a single identifier that can be used to quickly find and identify the object rather than having to compose a query that has conditions for all properties that would identify that object.</span></span>

 

 