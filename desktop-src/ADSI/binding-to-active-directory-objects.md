---
title: Binden an Active Directory Objekte
description: Bevor Sie mit diesem Szenario fortfahren, müssen Sie verstehen, wie ADSI-Objekte in Active Directory benannt werden und wie diese gebunden werden. Beim Binden eines ADSI-Objekts wird das Objekt mit dem Verzeichnisdienst verbunden, und Sie können auf die Methoden des Objekts zugreifen.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036321"
---
# <a name="binding-to-active-directory-objects"></a><span data-ttu-id="16dad-104">Binden an Active Directory Objekte</span><span class="sxs-lookup"><span data-stu-id="16dad-104">Binding to Active Directory Objects</span></span>

<span data-ttu-id="16dad-105">Bevor Sie mit diesem Szenario fortfahren, müssen Sie verstehen, wie ADSI-Objekte in Active Directory benannt werden und wie diese gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="16dad-105">Before you continue with this scenario, you must understand how ADSI objects are named in Active Directory, and how to bind them.</span></span> <span data-ttu-id="16dad-106">Beim Binden eines ADSI-Objekts wird das Objekt mit dem Verzeichnisdienst verbunden, und Sie können auf die Methoden des Objekts zugreifen.</span><span class="sxs-lookup"><span data-stu-id="16dad-106">Binding an ADSI object connects the object with the directory service, and allows you to access the methods of the object.</span></span>

## <a name="adspath"></a><span data-ttu-id="16dad-107">ADsPath</span><span class="sxs-lookup"><span data-stu-id="16dad-107">ADsPath</span></span>

<span data-ttu-id="16dad-108">Ein ADSI-Objekt wird durch die Bindungs Zeichenfolge, die auch als ADsPath bezeichnet wird, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="16dad-108">An ADSI object is uniquely identified by its binding string, which is also referred to as an ADsPath.</span></span> <span data-ttu-id="16dad-109">Ein ADsPath ist eine Kombination aus einem programmatischen Bezeichner (ProgID) des ADSI-Anbieters und dem DN (Distinguished Name) des Objekts.</span><span class="sxs-lookup"><span data-stu-id="16dad-109">An ADsPath is a combination of a programmatic identifier (progID) of the ADSI provider, and the distinguished name (DN) of the object.</span></span>

<span data-ttu-id="16dad-110">Dies ist das Format eines ADsPath:</span><span class="sxs-lookup"><span data-stu-id="16dad-110">Here's the format of an ADsPath:</span></span>

<span data-ttu-id="16dad-111">"ProgID://DN"</span><span class="sxs-lookup"><span data-stu-id="16dad-111">"progID://DN"</span></span>

-   <span data-ttu-id="16dad-112">pogid – der programmatische Bezeichner des ADSI-Anbieters, z. b. LDAP oder Winnt.</span><span class="sxs-lookup"><span data-stu-id="16dad-112">pogID — the programmatic identifier of the ADSI provider, such as LDAP or WinNT.</span></span>

-   <span data-ttu-id="16dad-113">://– trennt die ProgID vom DN.</span><span class="sxs-lookup"><span data-stu-id="16dad-113">:// — separates the progID from the DN.</span></span>

-   <span data-ttu-id="16dad-114">DN – der Distinguished Name des ADSI-Objekts, bei dem es sich um den vollständigen Pfad des Objekts handelt, bei dem der Pfad aus den relativen Distinguished Names (rDNS) besteht.</span><span class="sxs-lookup"><span data-stu-id="16dad-114">DN — the distinguished name of the ADSI object, which is the full path of the object, where the path consists of relative distinguished names (RDNs).</span></span>

<span data-ttu-id="16dad-115">Ein RDN ist der Name des Objekts ohne den Pfad und ist von seinen gleich geordneten Objekten eindeutig.</span><span class="sxs-lookup"><span data-stu-id="16dad-115">An RDN is the name of the object without the path, and is unique from its sibling objects.</span></span> <span data-ttu-id="16dad-116">Ein RDN besteht aus einer Attribut-ID und einem Wert, z. b. "DC = Fabrikam", wobei Domänen Controller das Attribut ist und Fabrikam der Wert ist.</span><span class="sxs-lookup"><span data-stu-id="16dad-116">An RDN consists of an attribute ID and value, such as "DC=Fabrikam", where DC is the attribute, and Fabrikam is the value.</span></span> <span data-ttu-id="16dad-117">DC ist eine RDN-Attribut-ID, die für die Domänen Komponente steht.</span><span class="sxs-lookup"><span data-stu-id="16dad-117">DC is an RDN attribute ID that stands for domain component.</span></span>

<span data-ttu-id="16dad-118">Im folgenden finden Sie ein Beispiel für einen ADsPath:</span><span class="sxs-lookup"><span data-stu-id="16dad-118">Here’s an example of an ADsPath:</span></span>

<span data-ttu-id="16dad-119">"LDAP://DC = fabrikam, DC = com"</span><span class="sxs-lookup"><span data-stu-id="16dad-119">"LDAP://DC=Fabrikam,DC=Com"</span></span>

## <a name="binding-the-object"></a><span data-ttu-id="16dad-120">Binden des Objekts</span><span class="sxs-lookup"><span data-stu-id="16dad-120">Binding the object</span></span>

<span data-ttu-id="16dad-121">Im folgenden wird erläutert, wie Sie das Domänen Objekt in diesem Szenario binden können:</span><span class="sxs-lookup"><span data-stu-id="16dad-121">Here's how you can bind the domain object in this scenario:</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



<span data-ttu-id="16dad-122">Wenn Sie dieses Codebeispiel ausführen, verwendet ADSI den DN, um die zu bindenden ADSI-Objekte zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="16dad-122">When you run this code example, ADSI uses the DN to determine the ADSI objects to bind.</span></span> <span data-ttu-id="16dad-123">Nachdem ADSI diese Objekte gebunden hat, können Sie auf die zugehörigen Methoden zugreifen.</span><span class="sxs-lookup"><span data-stu-id="16dad-123">After ADSI binds these objects, you can access their methods.</span></span> <span data-ttu-id="16dad-124">Im vorherigen Codebeispiel wird ein Domänen Objekt an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) und [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)gebunden.</span><span class="sxs-lookup"><span data-stu-id="16dad-124">The previous code example binds a domain object to [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="16dad-125">Sie können jetzt Methoden für diese Schnittstellen verwenden, z. b. [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)und [**muvehere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span><span class="sxs-lookup"><span data-stu-id="16dad-125">You can now use methods on those interfaces such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete), and [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span></span>

<span data-ttu-id="16dad-126">Nachdem Sie ein Domänen Objekt gebunden haben, können Sie einige seiner Attribute ausdrucken:</span><span class="sxs-lookup"><span data-stu-id="16dad-126">After you bind a domain object, you can print some of its attributes:</span></span>


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



<span data-ttu-id="16dad-127">Weitere Informationen zu ADsPath finden Sie unter [Bindungs Zeichenfolge](binding-string.md).</span><span class="sxs-lookup"><span data-stu-id="16dad-127">For more information about ADsPath, see [Binding String](binding-string.md).</span></span> <span data-ttu-id="16dad-128">Weitere Informationen zur Bindung finden Sie unter [binden an ein ADSI-Objekt](binding-to-an-adsi-object.md).</span><span class="sxs-lookup"><span data-stu-id="16dad-128">For more information about binding, see [Binding to an ADSI Object](binding-to-an-adsi-object.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="16dad-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16dad-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16dad-130">Erstellen einer Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="16dad-130">Creating an Organizational Unit</span></span>](creating-an-organizational-unit.md)
</dt> </dl>

 

 




