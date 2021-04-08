---
description: Wie viele andere Techniken in Managed Object Format (MOF) ist das Anwenden eines Qualifizierers auf Ihren Code ein relativ einfacher Vorgang.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Anwenden eines Qualifizierers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760777"
---
# <a name="applying-a-qualifier"></a><span data-ttu-id="4c55a-103">Anwenden eines Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="4c55a-103">Applying a Qualifier</span></span>

<span data-ttu-id="4c55a-104">Wie viele andere Techniken in Managed Object Format (MOF) ist das Anwenden eines Qualifizierers auf Ihren Code ein relativ einfacher Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4c55a-104">Like many other techniques in Managed Object Format (MOF), applying a qualifier to your code is a relatively simple process.</span></span>

<span data-ttu-id="4c55a-105">Die einzigen wirklichen Herausforderungen sind die folgenden Einschränkungen bei den Benennungs Konventionen, die von WMI erzwungen werden:</span><span class="sxs-lookup"><span data-stu-id="4c55a-105">The only real challenges are the following restrictions in naming conventions that WMI enforces:</span></span>

-   <span data-ttu-id="4c55a-106">Ein Qualifizierer kann eine Klasse, eine Instanz, eine Eigenschaft, eine Methode oder einen Methoden Parameter beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4c55a-106">A qualifier can describe a class, instance, property, method, or method parameter.</span></span>
-   <span data-ttu-id="4c55a-107">Qualifizierernamen dürfen weder führende noch nachfolgende Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="4c55a-107">Qualifier names cannot have either leading or trailing underscores.</span></span>
-   <span data-ttu-id="4c55a-108">Ein qualifizierername darf nicht mit einer Ziffer beginnen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-108">A qualifier name cannot begin with a digit.</span></span>
-   <span data-ttu-id="4c55a-109">Ein qualifizierername darf keine Sonderzeichen enthalten, z \* . b. & @!</span><span class="sxs-lookup"><span data-stu-id="4c55a-109">A qualifier name cannot contain special characters such as & \* @ !</span></span><span data-ttu-id="4c55a-110"> ~ \\ /.</span><span class="sxs-lookup"><span data-stu-id="4c55a-110"> ~ \\ /.</span></span>
-   <span data-ttu-id="4c55a-111">Bei allen Qualifizierernamen wird Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="4c55a-111">All qualifier names are case-insensitive.</span></span>
-   <span data-ttu-id="4c55a-112">Sie können die standardmäßigen WMI-Qualifizierer oder-Qualifizierer, die in der DMTF CIM-Spezifikation beschrieben werden</span><span class="sxs-lookup"><span data-stu-id="4c55a-112">You cannot redefine the standard WMI qualifiers or any qualifiers described in the DMTF CIM specification.</span></span>
-   <span data-ttu-id="4c55a-113">Qualifizierertypen werden nicht explizit deklariert.</span><span class="sxs-lookup"><span data-stu-id="4c55a-113">Qualifier types are not explicitly declared.</span></span>

    <span data-ttu-id="4c55a-114">Wenn Sie keinen Qualifizierertyp deklarieren, geht WMI davon aus, dass der Typ boolescher Wert mit dem Wert **true** ist.</span><span class="sxs-lookup"><span data-stu-id="4c55a-114">If you do not declare a qualifier type, WMI assumes the type as Boolean with a value of **TRUE**.</span></span> <span data-ttu-id="4c55a-115">Andernfalls sind WMI-Typen Qualifizierer basierend auf den deklarierten Qualifiziererwerten.</span><span class="sxs-lookup"><span data-stu-id="4c55a-115">Otherwise, WMI types qualifiers based on the qualifier values you declare.</span></span>

-   <span data-ttu-id="4c55a-116">Wenn Sie Ihre eigenen Qualifizierer erstellen, sollten Sie Ihren Schema Namen dem Qualifizierernamen voranstellen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-116">When creating your own qualifiers, you should prefix your schema name to your qualifier name.</span></span>

    <span data-ttu-id="4c55a-117">Der Zweck dieser Regel ist die Vermeidung von Verwechslungen mit neuen Qualifizierern.</span><span class="sxs-lookup"><span data-stu-id="4c55a-117">The purpose of this rule is to avoid confusion with new qualifiers.</span></span>

-   <span data-ttu-id="4c55a-118">Sie können homogene Arrays von Qualifizierern erstellen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-118">You can create homogeneous arrays of qualifiers.</span></span>

    <span data-ttu-id="4c55a-119">Im folgenden Codebeispiel wird gezeigt, wie qualifiziererarrays mit geschweiften Klammern angegeben werden, die die Werte umschließen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-119">The following code example shows how qualifier arrays are specified with curly braces that surround the values.</span></span>

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   <span data-ttu-id="4c55a-120">WMI unterstützt keine Automatisierungs Typen, die nicht in der Referenz aufgeführt sind, wie z \_ . b. VT NULL.</span><span class="sxs-lookup"><span data-stu-id="4c55a-120">WMI does not support automation types not listed in the reference, such as VT\_NULL.</span></span> <span data-ttu-id="4c55a-121">Weitere Informationen finden Sie unter [MOF-Datentypen](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="4c55a-121">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

<span data-ttu-id="4c55a-122">Das folgende Verfahren hilft Ihnen bei der Verwendung von C++, um einer Eigenschaft einen Qualifizierer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-122">The following procedure helps you to use C++ to add a qualifier to a property.</span></span>

<span data-ttu-id="4c55a-123">**So wenden Sie einen Qualifizierer mit C++ an**</span><span class="sxs-lookup"><span data-stu-id="4c55a-123">**To apply a qualifier using C++**</span></span>

-   <span data-ttu-id="4c55a-124">Wenden Sie den Qualifizierer mit einem-Befehl an die [**iwbemqualifierset::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) -Methode an.</span><span class="sxs-lookup"><span data-stu-id="4c55a-124">Apply the qualifier with a call to the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="4c55a-125">Sie können andere Methoden von [**iwbemqualifierset**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) verwenden, um vorhandene Qualifizierer abzurufen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="4c55a-125">You can use other methods of [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) to retrieve or delete existing qualifiers.</span></span>

<span data-ttu-id="4c55a-126">Mithilfe des folgenden Verfahrens können Sie einen Qualifizierer in MOF-Dateien anwenden.</span><span class="sxs-lookup"><span data-stu-id="4c55a-126">The following procedure helps you to apply a qualifier in MOF files.</span></span>

<span data-ttu-id="4c55a-127">**So beschreiben Sie ein Schlüsselwort oder einen Bezeichner mit einem Qualifizierer mit MOF**</span><span class="sxs-lookup"><span data-stu-id="4c55a-127">**To describe a keyword or identifier with a qualifier using MOF**</span></span>

-   <span data-ttu-id="4c55a-128">Platzieren Sie einen Qualifizierer in Klammern, bevor Sie das Schlüsselwort oder den Bezeichner beschreiben</span><span class="sxs-lookup"><span data-stu-id="4c55a-128">Place a qualifier in brackets before the keyword or identifier described by the qualifier.</span></span>

    <span data-ttu-id="4c55a-129">Das folgende Codebeispiel zeigt, wie Qualifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c55a-129">The following code example shows how qualifiers are used.</span></span>

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    <span data-ttu-id="4c55a-130">Im folgenden Beispiel wird die richtige Platzierung von Qualifizierern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4c55a-130">The following example describes the proper placement of qualifiers.</span></span>

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



