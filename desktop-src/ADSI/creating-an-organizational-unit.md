---
title: Erstellen einer Organisationseinheit
description: Nachdem Sie nun über das Domänen Objekt verfügen, können Sie damit beginnen, Organisationseinheiten zu erstellen.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Erstellen einer Organisationseinheit für ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947351"
---
# <a name="creating-an-organizational-unit"></a><span data-ttu-id="60d80-104">Erstellen einer Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="60d80-104">Creating an Organizational Unit</span></span>

<span data-ttu-id="60d80-105">Nachdem Sie nun über das Domänen Objekt verfügen, können Sie damit beginnen, Organisationseinheiten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60d80-105">Now that you have the domain object, you can start creating organizational units.</span></span> <span data-ttu-id="60d80-106">Fabrikam hat zwei Bereiche: Vertrieb und Produktion.</span><span class="sxs-lookup"><span data-stu-id="60d80-106">Fabrikam has two divisions: Sales and Production.</span></span> <span data-ttu-id="60d80-107">Das Unternehmen plant, zwei Windows 2000-Administratoren zur Verwaltung der einzelnen Abteilungen zu beauftragen.</span><span class="sxs-lookup"><span data-stu-id="60d80-107">The company is planning to hire two Windows 2000 administrators to manage each division.</span></span> <span data-ttu-id="60d80-108">Joe kam, als Unternehmens Administrator, erstellt in der Domäne "Fabrikam" zwei neue Organisationseinheiten.</span><span class="sxs-lookup"><span data-stu-id="60d80-108">Joe Worden, as the enterprise administrator, will create two new organizational units under the Fabrikam domain.</span></span> <span data-ttu-id="60d80-109">Durch das Erstellen einer Organisationseinheit kann Joe mehrere Objekte gruppieren und anderen Personen die Möglichkeit geben, diese Objekte zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="60d80-109">By creating an organizational unit, Joe can group multiple objects together and let someone else manage these objects.</span></span> <span data-ttu-id="60d80-110">Im folgenden Codebeispiel wird die Organisationseinheit "Sales" (OU) erstellt.</span><span class="sxs-lookup"><span data-stu-id="60d80-110">The following code example creates the Sales Organizational Unit (OU).</span></span>


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



<span data-ttu-id="60d80-111">Die [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) -Methode akzeptiert den Klassennamen und den Namen des neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="60d80-111">The [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) method accepts the class name and the name of the new object.</span></span> <span data-ttu-id="60d80-112">An diesem Punkt wird das Objekt nicht an Active Directory committet.</span><span class="sxs-lookup"><span data-stu-id="60d80-112">At this point the object is not committed to Active Directory.</span></span> <span data-ttu-id="60d80-113">Sie verfügen jedoch über einen ADSI/COM-Objekt Verweis auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="60d80-113">You, however, will have an ADSI/COM object reference on the client.</span></span> <span data-ttu-id="60d80-114">Mit diesem ADSI-Objekt können Sie Attribute mithilfe der [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) -Methode festlegen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="60d80-114">With this ADSI object, you can set or modify attributes using the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span> <span data-ttu-id="60d80-115">Die **IADs. Put** -Methode akzeptiert den Attributnamen und den Wert des Attributs.</span><span class="sxs-lookup"><span data-stu-id="60d80-115">The **IADs.Put** method accepts the attribute name and the value of the attribute.</span></span> <span data-ttu-id="60d80-116">Trotzdem wird nichts in das Verzeichnis übertragen. alles wird auf dem Client zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="60d80-116">Still, nothing is committed to the directory; everything is cached at the client.</span></span> <span data-ttu-id="60d80-117">Wenn Sie die [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode aufruft, werden die Änderungen, in diesem Fall die Objekt Erstellung und die Attribut Änderung, in das Verzeichnis übertragen.</span><span class="sxs-lookup"><span data-stu-id="60d80-117">When you call the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method, the changes, in this case, object creation and attribute modification, are committed to the directory.</span></span> <span data-ttu-id="60d80-118">Diese Änderungen werden transaktiv durchgeführt. das bedeutet, dass Sie entweder das neue Objekt mit allen von Ihnen festgelegten Attributen oder überhaupt kein Objekt sehen werden.</span><span class="sxs-lookup"><span data-stu-id="60d80-118">These changes are transacted, meaning that you will see either the new object with all attributes you set, or no object at all.</span></span>

<span data-ttu-id="60d80-119">Sie können auch Organisationseinheiten Schachteln.</span><span class="sxs-lookup"><span data-stu-id="60d80-119">You can also nest organizational units.</span></span> <span data-ttu-id="60d80-120">Im folgenden Codebeispiel wird davon ausgegangen, dass die Vertriebsabteilung in die Regionen "Osten" und "West" aufgeteilt ist.</span><span class="sxs-lookup"><span data-stu-id="60d80-120">The following code example assumes that the Sales division is divided further into the East and West regions.</span></span>


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



<span data-ttu-id="60d80-121">Dies gilt auch für die Region "Europa, Westen".</span><span class="sxs-lookup"><span data-stu-id="60d80-121">This also applies for the West region.</span></span>

<span data-ttu-id="60d80-122">Geben Sie den Distinguished Name an, um direkt an die Region "Osten" in der Vertriebsorganisation zu binden.</span><span class="sxs-lookup"><span data-stu-id="60d80-122">To bind directly to the East region in the Sales organization, specify the distinguished name.</span></span>


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



<span data-ttu-id="60d80-123">Wenn Sie bereits an das übergeordnete Objekt (Sales) gebunden sind, können Sie mit dem relativen Namen des untergeordneten Objekts an das untergeordnete Objekt (Osten) des übergeordneten Objekts binden.</span><span class="sxs-lookup"><span data-stu-id="60d80-123">If you have already bound to the parent object (Sales), you can bind to the child object (East) from the parent object using the relative name of the child object.</span></span>


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



<span data-ttu-id="60d80-124">Um sicherzustellen, dass die Objekte erstellt wurden, verwenden Sie das MMC-Snap-in "Active Directory-Benutzer und-Computer", um die neuen Organisationseinheiten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="60d80-124">To ensure that the objects have been created, use the Active Directory Users and Computers MMC snap-in to view the new organizational units.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60d80-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60d80-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60d80-126">Verschieben vorhandener Benutzer in die Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="60d80-126">Moving Existing Users to the Organizational Unit</span></span>](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




