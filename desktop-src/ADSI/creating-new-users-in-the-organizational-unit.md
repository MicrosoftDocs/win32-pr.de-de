---
title: Erstellen neuer Benutzer in der Organisationseinheit
description: Terry Adams wurde bei der Fabrikam Sales-Organisation eingestellt. Sein direkter Bericht ist Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Erstellen neuer Benutzer in der Organisationseinheit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470805"
---
# <a name="creating-new-users-in-the-organizational-unit"></a><span data-ttu-id="bca0e-105">Erstellen neuer Benutzer in der Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="bca0e-105">Creating New Users in the Organizational Unit</span></span>

<span data-ttu-id="bca0e-106">Terry Adams wurde bei der Fabrikam Sales-Organisation eingestellt.</span><span class="sxs-lookup"><span data-stu-id="bca0e-106">Terry Adams was hired into the Fabrikam Sales organization.</span></span> <span data-ttu-id="bca0e-107">Sein direkter Bericht ist Patrick Hines.</span><span class="sxs-lookup"><span data-stu-id="bca0e-107">His direct report is Patrick Hines.</span></span>

<span data-ttu-id="bca0e-108">Wie im folgenden Codebeispiel gezeigt, erstellt Joe andreshak, der Unternehmens Administrator, ein neues Konto für ihn.</span><span class="sxs-lookup"><span data-stu-id="bca0e-108">As shown in the following code example, Joe Andreshak, the enterprise administrator, will create a new account for him.</span></span>


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



<span data-ttu-id="bca0e-109">Wenn Sie einen neuen Benutzer erstellen, müssen Sie einen **sAMAccountName** angeben.</span><span class="sxs-lookup"><span data-stu-id="bca0e-109">When creating a new user, you must specify a **sAMAccountName**.</span></span> <span data-ttu-id="bca0e-110">Dies ist ein obligatorisches Attribut für die User-Klasse.</span><span class="sxs-lookup"><span data-stu-id="bca0e-110">This is a mandatory attribute for the user class.</span></span> <span data-ttu-id="bca0e-111">Bevor eine Instanz eines Objekts erstellt werden kann, müssen alle obligatorischen Attribute festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bca0e-111">Before an instance of an object can be created, all mandatory attributes must be set.</span></span> <span data-ttu-id="bca0e-112">Der **sAMAccountName** wird automatisch generiert, wenn ein neuer Benutzer nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bca0e-112">The **sAMAccountName** will automatically be generated if one is not specified for a new user.</span></span>

<span data-ttu-id="bca0e-113">Beim Erstellen eines neuen Benutzers müssen alle erforderlichen Attribute im lokalen Cache festgelegt werden, bevor die [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bca0e-113">When creating a new user, all of the required attributes must be set in the local cache before the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

<span data-ttu-id="bca0e-114">Joe kann als Administrator das Kennwort von Terry mithilfe der [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) -Methode zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bca0e-114">Joe, as an administrator, can assign Terry's password using the [**IADsUser.SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="bca0e-115">Die **IADsUser. SetPassword** -Methode funktioniert erst, wenn die [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="bca0e-115">The **IADsUser.SetPassword** method will not work until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method has been called.</span></span>

<span data-ttu-id="bca0e-116">Anschließend aktiviert Joe das Benutzerkonto, indem die [**IADsUser. accountdeaktiviert**](iadsuser-property-methods.md) -Eigenschaft auf **false** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bca0e-116">Then, Joe enables the user account by setting the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property to **FALSE**.</span></span>

<span data-ttu-id="bca0e-117">Im folgenden Codebeispiel wird gezeigt, wie Oliver als Manager für Patrick festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bca0e-117">The following code example shows how to set Terry as Patrick's manager.</span></span>


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



<span data-ttu-id="bca0e-118">Sie Fragen sich vielleicht, was passiert, wenn Terry seinen Namen ändert, zu einer anderen Organisation wechselt oder das Unternehmen verlässt.</span><span class="sxs-lookup"><span data-stu-id="bca0e-118">You may wonder what happens if Terry changes his name, moves to a different organization, or leaves the company.</span></span> <span data-ttu-id="bca0e-119">Wer verwaltet diesen Manager-Direct Report Link?</span><span class="sxs-lookup"><span data-stu-id="bca0e-119">Who maintains this manager-direct report link?</span></span> <span data-ttu-id="bca0e-120">Weitere Informationen und die Lösung für dieses Problem finden Sie unter [Neuorganisation](reorganization.md).</span><span class="sxs-lookup"><span data-stu-id="bca0e-120">For more information, and the solution to this problem, see [Reorganization](reorganization.md).</span></span> <span data-ttu-id="bca0e-121">Da das Active Directory Schema erweiterbar ist, können Sie die Objekte modellieren, um ähnliche Manager-direkte Berichts Stil Beziehungen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="bca0e-121">Because the Active Directory schema is extensible, you can model your objects to include similar manager-direct report style relationships.</span></span>

<span data-ttu-id="bca0e-122">Bevor Sie mit der nächsten Aufgabe fortfahren, sehen Sie sich ein Codebeispiel an, das zeigt, wie Joe die direkten Berichte von Oliver anzeigen würde.</span><span class="sxs-lookup"><span data-stu-id="bca0e-122">Before going on to the next task, look at a code example that shows how Joe would view Terry's direct reports.</span></span>


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



<span data-ttu-id="bca0e-123">In diesem Codebeispiel wird Patrick als direkter Bericht von Oliver angezeigt, auch wenn das **DirectReports** -Attribut nie geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="bca0e-123">In this code example, Patrick will display as Terry's direct report, even though the **directReports** attribute was never modified.</span></span> <span data-ttu-id="bca0e-124">Active Directory führt dies automatisch aus.</span><span class="sxs-lookup"><span data-stu-id="bca0e-124">Active Directory does this automatically.</span></span>

<span data-ttu-id="bca0e-125">In der Verzeichnis Welt kann ein Attribut einen einzelnen oder mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bca0e-125">In the directory world, an attribute can have single or multiple values.</span></span> <span data-ttu-id="bca0e-126">Da **DirectReports** über mehrere Werte verfügen, können Sie diese Informationen überprüfen, indem Sie sich das Schema ansehen. es ist einfacher, die [**IADs. Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode zu verwenden, die ein Array von Werten zurückgibt, unabhängig davon, ob ein oder mehrere Werte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bca0e-126">Because **directReports** has multiple values, you can get this information by looking at the schema, it is easier to use the [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, which returns an array of values regardless of whether single or multiple values are returned.</span></span>

<span data-ttu-id="bca0e-127">Mit dem Snap-in "Active Directory-Benutzer und-Computer" können Sie direktberichte und Manager Beziehungen auf der Eigenschaften Seite des Benutzers anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bca0e-127">The Active Directory Users and Computers snap-in lets you view direct reports and manager relationships on the user's property page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bca0e-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bca0e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bca0e-129">Hinzufügen von Benutzern zu einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="bca0e-129">Adding Users to a Group</span></span>](adding-users-to-a-group.md)
</dt> </dl>

 

 




