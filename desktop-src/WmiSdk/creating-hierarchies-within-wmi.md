---
description: Der WMI-Namespace ist ein Programmier Objekt, das den Bereich für eine Gruppe von Klassen und Instanzen definiert. WMI-Anbieter Klassen müssen innerhalb eines Namespace definiert werden.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Erstellen von Hierarchien in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215460"
---
# <a name="creating-hierarchies-within-wmi"></a><span data-ttu-id="79941-104">Erstellen von Hierarchien in WMI</span><span class="sxs-lookup"><span data-stu-id="79941-104">Creating Hierarchies Within WMI</span></span>

<span data-ttu-id="79941-105">Der [*WMI-Namespace*](gloss-n.md) ist ein Programmier Objekt, das den Bereich für eine Gruppe von Klassen und Instanzen definiert.</span><span class="sxs-lookup"><span data-stu-id="79941-105">[*WMI namespace*](gloss-n.md) is a programming object that defines the scope for a set of classes and instances.</span></span> <span data-ttu-id="79941-106">WMI-Anbieter Klassen müssen innerhalb eines Namespace definiert werden.</span><span class="sxs-lookup"><span data-stu-id="79941-106">WMI provider classes must be defined inside a namespace.</span></span>

<span data-ttu-id="79941-107">Namespaces beschreiben verschiedene verwaltete Umgebungen, z. b. die SMS-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="79941-107">Namespaces describe different managed environments, such as the SMS environment.</span></span> <span data-ttu-id="79941-108">Da die Klassen und Instanzen eines Schemas die Komponenten einer verwalteten Umgebung definieren, erfordert jedes neue Schema einen neuen Namespace.</span><span class="sxs-lookup"><span data-stu-id="79941-108">Because the classes and instances of a schema define the components of a managed environment, each new schema requires a new namespace.</span></span> <span data-ttu-id="79941-109">Der root \\ CIMV2-Namespace enthält z. b. die Klassen und Instanzen, die im Win32-Schema definiert sind, sowie die CIM-Klassen (Parent Common Information Model), aus denen das Win32-Schema erbt.</span><span class="sxs-lookup"><span data-stu-id="79941-109">For example, the root\\cimv2 namespace contains the classes and instances defined in the Win32 schema as well as the parent Common Information Model (CIM) classes from which the Win32 schema inherits.</span></span> <span data-ttu-id="79941-110">CIM-Klassen werden von der verteilten Verwaltungs Task Force ([DMTF](https://www.dmtf.org/home)) definiert.</span><span class="sxs-lookup"><span data-stu-id="79941-110">CIM classes are defined by the Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).</span></span>

> [!Note]  
> <span data-ttu-id="79941-111">Um sicherzustellen, dass alle ihre WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wieder hergestellt werden, wenn WMI einen Fehler aufweist und neu gestartet wird, verwenden Sie die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung in der [*MOF-Datei (Managed Object Format)*](gloss-m.md) .</span><span class="sxs-lookup"><span data-stu-id="79941-111">To ensure that all of your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format (MOF)*](gloss-m.md) file.</span></span>

 

<span data-ttu-id="79941-112">WMI definiert einen Namespace als Instanz der [**\_ \_ Namespace**](--namespace.md) -System Klasse oder einer beliebigen Klasse, die vom **\_ \_ Namespace** abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="79941-112">WMI defines a namespace as an instance of the [**\_\_Namespace**](--namespace.md) system class or any class that derives from **\_\_Namespace**.</span></span> <span data-ttu-id="79941-113">Die **\_ \_ Namespace** -System Klasse verfügt über eine einzelne Eigenschaft namens **Name**, die innerhalb des Gültigkeits Bereichs des übergeordneten Namespaces eindeutig sein muss.</span><span class="sxs-lookup"><span data-stu-id="79941-113">The **\_\_Namespace** system class has a single property called **Name**, which must be unique within the scope of the parent namespace.</span></span> <span data-ttu-id="79941-114">Die **Name** -Eigenschaft muss auch eine Zeichenfolge enthalten, die mit einem Buchstaben beginnt.</span><span class="sxs-lookup"><span data-stu-id="79941-114">The **Name** property must also contain a string that begins with a letter.</span></span> <span data-ttu-id="79941-115">Alle anderen Zeichen in der Zeichenfolge können Buchstaben, Ziffern oder Unterstriche sein.</span><span class="sxs-lookup"><span data-stu-id="79941-115">All other characters in the string can be letters, digits, or underscores.</span></span> <span data-ttu-id="79941-116">Bei allen Zeichen wird Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="79941-116">All characters are case-insensitive.</span></span>

<span data-ttu-id="79941-117">Der übergeordnete WMI-Namespace kann nicht nur den eindeutigen Namen für einen untergeordneten Namespace festlegen, sondern auch die statischen Instanzen der Klassen vor versehentlichen Änderungen durch andere Anbieter.</span><span class="sxs-lookup"><span data-stu-id="79941-117">In addition to determining the unique name for a child namespace, the parent WMI namespace can protect the static instances of your classes from accidental modification by other providers.</span></span> <span data-ttu-id="79941-118">Beispielsweise kann es sinnvoll sein, einen neuen Namespace unter einem vorhandenen Namespace für einen anderen Anbieter zu schachteln.</span><span class="sxs-lookup"><span data-stu-id="79941-118">For example, you may find it convenient to nest a new namespace under an existing namespace for another provider.</span></span> <span data-ttu-id="79941-119">Der ursprüngliche Anbieter kann jedoch versuchen, alle Klassen Instanzen so zu aktualisieren, dass Sie mit einem neuen Schema zu vergleichen sind.</span><span class="sxs-lookup"><span data-stu-id="79941-119">However, the original provider may try to update all class instances to match up with a new schema.</span></span> <span data-ttu-id="79941-120">Dabei kann der ursprüngliche Anbieter alle untergeordneten untergeordneten Elemente in einem Namespace löschen.</span><span class="sxs-lookup"><span data-stu-id="79941-120">In doing so, the original provider may delete all sub-children in a namespace.</span></span> <span data-ttu-id="79941-121">Obwohl dies eine geeignete Aktion für den Ziel Namespace sein kann, wirkt sich dies möglicherweise auf nicht verknüpfte Klassen Instanzen in einem untergeordneten Namespace aus (d. h. ihre eigenen Anbieter Klassen).</span><span class="sxs-lookup"><span data-stu-id="79941-121">While this may be an appropriate action for the target namespace, it may affect unrelated class instances in a child namespace (i.e., your own provider classes).</span></span>

<span data-ttu-id="79941-122">Daher empfiehlt es sich im Allgemeinen, Ihren Namespace als separat von Namespaces zu erstellen und zu registrieren, die Sie nicht direkt steuern.</span><span class="sxs-lookup"><span data-stu-id="79941-122">Therefore, it is generally recommended that you create and register your namespace as separate from namespaces that you do not directly control.</span></span> <span data-ttu-id="79941-123">Dies trifft vor allem dann zu, wenn Ihre Klassen nur von allgemeinen CIM-Klassen oder anderen Klassen von Ihrem Unternehmen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="79941-123">This is especially true if your classes derive only from general CIM classes or other classes from your company.</span></span> <span data-ttu-id="79941-124">Der Namespace kann sich unter dem **Stamm Namespace** befinden, z. b. wie folgt:</span><span class="sxs-lookup"><span data-stu-id="79941-124">Your namespace can be under the **Root** namespace, such as the following:</span></span>

<span data-ttu-id="79941-125">**Root/MyCompany/MyProduct**</span><span class="sxs-lookup"><span data-stu-id="79941-125">**Root/myCompany/myProduct**</span></span>

<span data-ttu-id="79941-126">Wenn die neue Klasse dagegen von der Klasse eines anderen Anbieters abgeleitet ist, müssen Sie möglicherweise die Klasse in einem untergeordneten Namespace dieses Anbieters speichern.</span><span class="sxs-lookup"><span data-stu-id="79941-126">In contrast, if your new class derives from the class of another provider, you may need to store your class in a sub-namespace of that provider.</span></span> <span data-ttu-id="79941-127">Beachten Sie, dass dadurch die neue Klasse für das versehentliche Löschen durch den ursprünglichen Anbieter verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="79941-127">Note that this exposes your new class to accidental deletion by the original provider.</span></span>

<span data-ttu-id="79941-128">WMI bietet verschiedene Möglichkeiten zum Erstellen eines Namespace:</span><span class="sxs-lookup"><span data-stu-id="79941-128">WMI provides several different ways to create a namespace:</span></span>

-   [<span data-ttu-id="79941-129">Erstellen eines untergeordneten Namespace mit MOF-Code</span><span class="sxs-lookup"><span data-stu-id="79941-129">Creating a Child Namespace with MOF Code</span></span>](creating-a-child-namespace-with-mof-code.md)
-   [<span data-ttu-id="79941-130">Erstellen eines gleich geordneten Namespace mit MOF-Code</span><span class="sxs-lookup"><span data-stu-id="79941-130">Creating a Sibling Namespace with MOF Code</span></span>](creating-a-sibling-namespace-with-mof-code.md)
-   [<span data-ttu-id="79941-131">Erstellen eines Namespace mit der WMI-API</span><span class="sxs-lookup"><span data-stu-id="79941-131">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a><span data-ttu-id="79941-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79941-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79941-133">Entwerfen von Managed Object Format-Klassen (MOF)</span><span class="sxs-lookup"><span data-stu-id="79941-133">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



