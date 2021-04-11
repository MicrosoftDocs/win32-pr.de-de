---
description: Eine qualifiziererkonfiguration ist ein Flag, das weitere Informationen zu einem Qualifizierer beschreibt.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Beschreiben eines Qualifizierers mit einer qualifiziererkonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215455"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a><span data-ttu-id="45983-103">Beschreiben eines Qualifizierers mit einer qualifiziererkonfiguration</span><span class="sxs-lookup"><span data-stu-id="45983-103">Describing a Qualifier with a Qualifier Flavor</span></span>

<span data-ttu-id="45983-104">Eine [*qualifiziererkonfiguration*](gloss-q.md) ist ein Flag, das weitere Informationen zu einem Qualifizierer beschreibt.</span><span class="sxs-lookup"><span data-stu-id="45983-104">A [*qualifier flavor*](gloss-q.md) is a flag that describes more information about a qualifier.</span></span> <span data-ttu-id="45983-105">Beispielsweise gibt die eingeschränkte qualifiziererkonfiguration an, dass WMI den zugeordneten Qualifizierer nicht an abgeleitete Klassen oder Instanzen weitergeben soll.</span><span class="sxs-lookup"><span data-stu-id="45983-105">For example, the Restricted qualifier flavor states that WMI should not propagate the associated qualifier to any derived classes or instances.</span></span> <span data-ttu-id="45983-106">Sie können die Varianten entweder mithilfe von MOF-Code oder Programm gesteuert festlegen.</span><span class="sxs-lookup"><span data-stu-id="45983-106">You can set flavors using either MOF code or programmatically.</span></span> <span data-ttu-id="45983-107">Obwohl Sie eine Vielzahl von Effekten mit-Variationen beschreiben können, besteht der Hauptzweck von eingabeflags darin, zu definieren, wie WMI Qualifizierer durch Vererbung propagiert.</span><span class="sxs-lookup"><span data-stu-id="45983-107">While you can describe a variety of effects with flavors, the main purposes of flavor flags is to define how WMI propagates qualifiers through inheritance.</span></span>

<span data-ttu-id="45983-108">WMI definiert mehrere qualifizierervarianten, die Sie an einen beliebigen Qualifizierer anfügen können, unabhängig vom Ursprung des Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="45983-108">WMI defines several qualifier flavors that you can attach to any qualifier, regardless of the origin of the qualifier.</span></span> <span data-ttu-id="45983-109">Einige Varianten sind jedoch nicht für alle Qualifizierertypen geeignet.</span><span class="sxs-lookup"><span data-stu-id="45983-109">However, some flavors are not appropriate for all qualifier types.</span></span> <span data-ttu-id="45983-110">Beispielsweise ist die " **desubclass** "-Konfiguration nur für Qualifizierer geeignet, die für eine Klasse definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="45983-110">The **ToSubClass** flavor, for example, is appropriate only for qualifiers defined for a class.</span></span> <span data-ttu-id="45983-111">Sie können " **desubclass** " nicht an einen Qualifizierer anfügen, um eine Instanz zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="45983-111">You cannot attach **ToSubClass** to a qualifier used to describe an instance.</span></span>

<span data-ttu-id="45983-112">Mithilfe von Varianten können Sie verschiedene Effekte für Qualifizierer beschreiben.</span><span class="sxs-lookup"><span data-stu-id="45983-112">You can use flavors to describe a variety of different effects for qualifiers.</span></span> <span data-ttu-id="45983-113">Beispielsweise kann "Flavor" angeben, ob ein Qualifizierer lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="45983-113">For example, flavor can indicate if a qualifier can be localized.</span></span> <span data-ttu-id="45983-114">Einer der Hauptzwecke der qualifiziererkonfiguration besteht jedoch darin zu beschreiben, ob eine übergeordnete Klasse Qualifizierer an eine Unterklasse oder eine Klasseninstanz übergeben kann.</span><span class="sxs-lookup"><span data-stu-id="45983-114">However, one of the main purposes of a qualifier flavor is to describe whether a parent class can pass qualifiers to a subclass or class instance.</span></span> <span data-ttu-id="45983-115">Mithilfe von Varianten können Sie auch bestimmen, ob eine Klassen Eigenschaft einen Qualifizierer an eine Instanzeigenschaft übergibt.</span><span class="sxs-lookup"><span data-stu-id="45983-115">You can also use flavors to determine if a class property passes a qualifier on to an instance property.</span></span> <span data-ttu-id="45983-116">Verwenden Sie zum Schluss mithilfe von-Varianten, ob eine Unterklasse den ursprünglichen Wert eines geerbten Qualifizierers überschreiben kann.</span><span class="sxs-lookup"><span data-stu-id="45983-116">Finally, use flavors to state whether a subclass can override the original value of an inherited qualifier.</span></span> <span data-ttu-id="45983-117">Qualifizierer, die Sie für eine Klasse oder eine Instanz deklarieren, werden jedoch nicht an die Eigenschaften dieser Klasse oder Instanz weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="45983-117">However, qualifiers that you declare for a class or instance do not propagate to the properties of that class or instance.</span></span> <span data-ttu-id="45983-118">Außerdem sind die Varianten, die Außerkraftsetzungs Berechtigungen einrichten, nur gültig, wenn Sie **auch die "** "-oder " **desubclass** "-Varianten festlegen.</span><span class="sxs-lookup"><span data-stu-id="45983-118">Further, flavors that establish override permissions are valid only if you also set the **ToInstance** or **ToSubClass** flavors.</span></span>

<span data-ttu-id="45983-119">Eine Konfiguration kann Global einem Qualifizierer für eine gesamte MOF-Datei zugewiesen werden. dabei wird die folgende Syntax verwendet, in der Leerraum als Trennzeichen fungiert, wenn mehrere Varianten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="45983-119">A flavor can be globally assigned to a qualifier for an entire MOF file using the following syntax in which white space acts as the delimiter when multiple flavors are specified.</span></span>

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

<span data-ttu-id="45983-120">Globale Varianten gelten für alle nachfolgenden Verwendungen des Qualifizierers in der MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="45983-120">Global flavors apply to all subsequent uses of the qualifier in the MOF file.</span></span> <span data-ttu-id="45983-121">Globale Geschmacks Anweisungen können an einer beliebigen Stelle in der Datei außerhalb eines objektdeklarations Blocks auftreten.</span><span class="sxs-lookup"><span data-stu-id="45983-121">Global flavor statements may occur anywhere in the file outside of an object declaration block.</span></span> <span data-ttu-id="45983-122">Auf Klassen-, Instanz-oder Eigenschafts Ebene neu definierte Varianten überschreiben die globalen Geschmacks Deklarationen für den Gültigkeitsbereich dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="45983-122">Flavors redefined at the class, instance, or property level override the global flavor declarations for the scope of that object.</span></span>

<span data-ttu-id="45983-123">Sie können keine neue Konfiguration definieren.</span><span class="sxs-lookup"><span data-stu-id="45983-123">You cannot define a new flavor.</span></span> <span data-ttu-id="45983-124">Obwohl Sie einen neuen Qualifizierer erstellen können, verwenden Sie nur vorhandene [qualifizierervarianten](qualifier-flavors.md) , um den neuen Qualifizierer zu beschreiben</span><span class="sxs-lookup"><span data-stu-id="45983-124">Although you can create a new qualifier, use only existing [Qualifier Flavors](qualifier-flavors.md) to describe your new qualifier.</span></span>

<span data-ttu-id="45983-125">**So definieren Sie qualifizierervarianten in MOF**</span><span class="sxs-lookup"><span data-stu-id="45983-125">**To define qualifier flavors in MOF**</span></span>

-   <span data-ttu-id="45983-126">Deklarieren Sie die Varianten, die einen angegebenen Qualifizierer nach dem Qualifizierernamen beschreiben, zwischen den Qualifizierern</span><span class="sxs-lookup"><span data-stu-id="45983-126">Declare the flavors that describe a given qualifier after the qualifier name, between the qualifier brackets.</span></span> <span data-ttu-id="45983-127">Verwenden Sie Leerraum als Trennzeichen zwischen mehreren Varianten.</span><span class="sxs-lookup"><span data-stu-id="45983-127">Use white space as the delimiter between multiple flavors.</span></span>

    <span data-ttu-id="45983-128">Das folgende Beispiel zeigt das Muster für das Anfügen von vordefinierten Qualifizierern.</span><span class="sxs-lookup"><span data-stu-id="45983-128">The following example shows the pattern for attaching predefined qualifiers.</span></span>

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

<span data-ttu-id="45983-129">Sie können qualifizierervarianten nur Programm gesteuert in C++ hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="45983-129">You can add qualifier flavors programmatically only in C++.</span></span> <span data-ttu-id="45983-130">Dieser Vorgang ist in der Skript- [API für WMI](scripting-api-for-wmi.md)nicht verfügbar. Sie können jedoch einen neuen Qualifizierer hinzufügen, indem Sie " [**austauschen. hinzufügen**](swbemqualifierset-add.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="45983-130">This operation is not available in the [Scripting API for WMI](scripting-api-for-wmi.md), although you can add a new qualifier by calling [**SWbemQualifierSet.Add**](swbemqualifierset-add.md).</span></span>

<span data-ttu-id="45983-131">**So weisen Sie eine Konfiguration mithilfe von C++ zu**</span><span class="sxs-lookup"><span data-stu-id="45983-131">**To assign a flavor using C++**</span></span>

-   <span data-ttu-id="45983-132">Aufrufen der Methode [**iwbemqualifierset::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) mit dem *lflavor* -Parameter, der auf eine der für die Methode definierten Konstanten festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="45983-132">Call the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method with the *lFlavor* parameter set to one of the constants defined for the method.</span></span>

 

 



