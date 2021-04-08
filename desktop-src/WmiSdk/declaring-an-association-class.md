---
description: Eine Association-Klasse ist eine besondere Art von Klasse, die eine Beziehung zwischen zwei anderen Klassen definiert.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Deklarieren einer Association-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050268"
---
# <a name="declaring-an-association-class"></a><span data-ttu-id="f6e70-103">Deklarieren einer Association-Klasse</span><span class="sxs-lookup"><span data-stu-id="f6e70-103">Declaring an Association Class</span></span>

<span data-ttu-id="f6e70-104">Eine Association-Klasse ist eine besondere Art von Klasse, die eine Beziehung zwischen zwei anderen Klassen definiert.</span><span class="sxs-lookup"><span data-stu-id="f6e70-104">An association class is a special type of class that defines a relationship between two other classes.</span></span>

<span data-ttu-id="f6e70-105">Im folgenden Verfahren wird beschrieben, wie eine Association-Klasse mithilfe von MOF-Code erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f6e70-105">The following procedure describes how to create an association class using MOF code.</span></span>

<span data-ttu-id="f6e70-106">**So erstellen Sie eine Association-Klasse mithilfe von MOF-Code**</span><span class="sxs-lookup"><span data-stu-id="f6e70-106">**To create an association class using MOF code**</span></span>

1.  <span data-ttu-id="f6e70-107">Weisen Sie der Klasse den **Association** -Qualifizierer zu.</span><span class="sxs-lookup"><span data-stu-id="f6e70-107">Assign the **Association** qualifier to your class.</span></span>

    <span data-ttu-id="f6e70-108">Obwohl es möglich ist, eine Klasse mit Verweisen auf Objekte oder Klassen zu erstellen, wird durch die Verwendung des **Association** -Qualifizierers nicht nur klar, dass es sich bei der Klasse um eine Association-Klasse handelt, sondern es wird als bewährte Vorgehensweise sichergestellt, dass die Klasse vollständig als Zuordnungs Klasse fungiert.</span><span class="sxs-lookup"><span data-stu-id="f6e70-108">Although it is possible to create a class with references to objects or classes, using the **Association** qualifier not only makes it clear that your class is an association class, but, as a best practice, ensures that your class fully functions as an association class.</span></span>

2.  <span data-ttu-id="f6e70-109">Erstellen Sie zwei Verweise innerhalb der-Klasse, die die beiden Objektinstanzen beschreiben, die Sie mit dem **ref** -Typ verknüpfen möchten.</span><span class="sxs-lookup"><span data-stu-id="f6e70-109">Create two references within the class describing the two object instances you wish to associate together using the **ref** type.</span></span>

    <span data-ttu-id="f6e70-110">Die Verweise binden die beiden Objekte in der Zuordnung, indem Sie die Pfade zu den-Objekten enthalten.</span><span class="sxs-lookup"><span data-stu-id="f6e70-110">The references bind the two objects in the association by containing paths to the objects.</span></span> <span data-ttu-id="f6e70-111">Auch wenn dies nicht erforderlich ist, verwenden Sie die Verweis Eigenschaften als Schlüsseleigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6e70-111">Although not required, use the reference properties as key properties as well.</span></span>

    <span data-ttu-id="f6e70-112">Obwohl Sie vollständig qualifizierte Verweise oder Namespace relative Verweise erstellen können, bietet WMI nur eingeschränkte Unterstützung für Namespace übergreifende Verweise.</span><span class="sxs-lookup"><span data-stu-id="f6e70-112">Although you can create fully qualified or namespace-relative references, WMI has only limited support for cross-namespace references.</span></span> <span data-ttu-id="f6e70-113">Insbesondere können nur statisch definierte Objekte über Namespace Grenzen hinweg referenziert werden. dynamisch unterstützte Objekte können nicht aufeinander verweisen.</span><span class="sxs-lookup"><span data-stu-id="f6e70-113">Specifically, only statically defined objects can reference each other across namespace boundaries; dynamically supported objects cannot reference each other.</span></span>

    <span data-ttu-id="f6e70-114">Verwenden Sie ggf. die Qualifizierer **hasclassref** und **classref** in Verbindung mit dem **Objekt** Verweistyp, um auf eine Klasse zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="f6e70-114">If necessary, use the **HasClassRef** and **Classref** qualifiers in conjunction with the **object ref** type to reference a class.</span></span>

    <span data-ttu-id="f6e70-115">WMI unterstützt das **vorhanden sein eines** Verweis Verweises auf eine Instanz, und der andere **Objekt** Verweis verweist auf eine Klasse.</span><span class="sxs-lookup"><span data-stu-id="f6e70-115">WMI supports having one **ref** reference point to an instance, and the other **object** reference point to a class.</span></span> <span data-ttu-id="f6e70-116">In diesem Fall würde ihre Association-Klasse eine Zuordnung beschreiben, die Instanzen an Klassen bindet.</span><span class="sxs-lookup"><span data-stu-id="f6e70-116">In this case, your association class would describe an association that binds instances to classes.</span></span>

    <span data-ttu-id="f6e70-117">Im folgenden Codebeispiel wird die Syntax für die Verwendung von **hasclassref** und **classref** mit einem **Objekttyp** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f6e70-117">The following code example describes the syntax for using **HasClassRef** and **Classref** with an **object** type.</span></span>

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    <span data-ttu-id="f6e70-118">Im vorherigen Beispiel kann der **EP1** -Verweis auf die Klassendefinitionen für die **myEndpoint** -Klasse oder die **othercontainer** -Klasse verweisen.</span><span class="sxs-lookup"><span data-stu-id="f6e70-118">In the previous example, the **ep1** reference can point to the class definitions for either the **MyEndpoint** class or the **OtherContainer** class.</span></span> <span data-ttu-id="f6e70-119">Beachten Sie, dass Sie zwar die Verweis Klasse schwach eingeben müssen, Sie können den **classref** -Qualifizierer selbst jedoch nicht schwach eingeben. Dadurch würde die Effizienz der WMI-Abfrage-Engine erheblich reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="f6e70-119">Note that while you must weakly type the reference class, you cannot weakly type the **Classref** qualifier itself; doing so would severely reduce the efficiency of the WMI query engine.</span></span> <span data-ttu-id="f6e70-120">Schwache Typisierung ist das Erstellen eines Verweises, der beliebige Datentypen enthalten kann, indem das **Object** **-Schlüssel** Wort und der Verweis Datentyp verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f6e70-120">Weak typing is creating a reference that can contain any data type by using the **object** keyword and **ref** data type.</span></span> <span data-ttu-id="f6e70-121">Damit **hasclassref** erfolgreich verwendet werden kann, müssen Sie die relevanten qualifizierervarianten so festlegen, dass Sie an alle Instanzen und Unterklassen weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f6e70-121">To successfully use **HasClassRef**, you must set the relevant qualifier flavors to propagate to all instances and subclasses.</span></span>

3.  <span data-ttu-id="f6e70-122">Erstellen Sie ggf. weitere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6e70-122">Create any other properties as necessary.</span></span>

    <span data-ttu-id="f6e70-123">Das folgende Codebeispiel zeigt, dass WMI derzeit keine Zuordnungs Klassen unterstützt, die über weniger oder mehr als zwei Verweis Eigenschaften verfügen.</span><span class="sxs-lookup"><span data-stu-id="f6e70-123">The following code example shows that WMI does not currently support association classes having less or more than two reference properties.</span></span>

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  <span data-ttu-id="f6e70-124">Wenn Sie fertig sind, kompilieren Sie den MOF-Code mit dem MOF-Compiler.</span><span class="sxs-lookup"><span data-stu-id="f6e70-124">When finished, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="f6e70-125">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="f6e70-125">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="f6e70-126">Das Codebeispiel in Schritt 3 definiert die Klasse **myassocclass** Association.</span><span class="sxs-lookup"><span data-stu-id="f6e70-126">The code example in Step 3 defines the **MyAssocClass** association class.</span></span> <span data-ttu-id="f6e70-127">Die **myassocclass** -Klasse definiert eine Beziehung zwischen **ClassX** und **eleganten**.</span><span class="sxs-lookup"><span data-stu-id="f6e70-127">The **MyAssocClass** class defines a relationship between **ClassX** and **ClassY**.</span></span> <span data-ttu-id="f6e70-128">Die Eigenschaften **pathyclassx** und **pathyedle** enthalten Objekt Pfade zu den Instanzen der Klassen, die zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f6e70-128">The **PathToClassX** and **PathToClassY** properties contain object paths to the instances of the classes to be associated.</span></span> <span data-ttu-id="f6e70-129">Das Schlüsselwort " **deinstance** " ist eines von mehreren Standardflags, die von WMI definiert werden, um Informationen zur Verwendung eines Qualifizierers bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f6e70-129">The keyword **ToInstance** is one of several flavor flags that WMI defines to provide information about the use of a qualifier.</span></span> <span data-ttu-id="f6e70-130">Das Schlüsselwort " **deinstance** " gibt an, dass WMI den **Assoziations** Qualifizierer an alle Instanzen der Association-Klasse weitergeben soll.</span><span class="sxs-lookup"><span data-stu-id="f6e70-130">The **ToInstance** keyword indicates that WMI should propagate the **Association** qualifier to all instances of the association class.</span></span> <span data-ttu-id="f6e70-131">Durch die Überprüfung dieses instanzqualifizierers kann die Client Software ermitteln, dass eine Instanz zu einer Zuordnungs Klasse gehört, **ohne die Klassen** Definition abrufen zu müssen, um nach dem Zuordnungs Qualifizierer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f6e70-131">By checking this instance qualifier, the client software can determine that an instance belongs to an association class, without having to retrieve the class definition to look for the **Association** qualifier.</span></span> <span data-ttu-id="f6e70-132">Weitere Informationen finden Sie unter [beschreiben eines Qualifizierers mit einer qualifiziererkonfiguration](describing-a-qualifier-with-a-qualifier-flavor.md) und [verweisen](references.md).</span><span class="sxs-lookup"><span data-stu-id="f6e70-132">For more information, see [Describing a Qualifier With a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md) and [References](references.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6e70-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6e70-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6e70-134">Entwerfen von Managed Object Format-Klassen (MOF)</span><span class="sxs-lookup"><span data-stu-id="f6e70-134">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



